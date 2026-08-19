# HeatShield: My Literature Review
## Heat-Risk Indicators, Data Sources, and Backend Ingestion Feasibility

## 1. Scope and research question

This review focuses on one question:

How should the Heat Risk Dashboard select heat-risk indicators and data sources that are feasible for backend ingestion, periodic refresh, quality validation, and safe dashboard handoff without claiming weather prediction or clinical diagnosis?

Boundary used in this review:

- In scope: indicator selection, source feasibility, data definitions, update cadence, ingestion design.
- Out of scope: building a new forecasting model, diagnosis or treatment rules, patient-identifiable data.

## 2. Source coverage and current status

This is a Phase 0 scoping review prepared before final per-source evidence extraction is complete.

What is covered now:

- Candidate public weather and heat data APIs
- Candidate climate and historical baseline datasets
- Candidate official alert/threshold references
- Typical backend ingestion constraints for prototype systems

What is not complete yet:

- Final claim-by-claim citations from validated source artifacts
- Jurisdiction-specific legal and licensing confirmation for every source
- Local operational threshold confirmation by responsible authorities

Current traceability status:

- Six per-source summary scaffolds are created and ready for evidence fill-in.
- Each scaffold includes metadata, indicator extraction, ingestion notes, limitations, and follow-up questions.

## 3. Source-to-indicator inventory (prototype-oriented)

| Indicator | Definition and unit | Geographic level | Time horizon | Candidate source types | Typical update frequency | Notes and limitations |
|---|---|---|---|---|---|---|
| Air temperature | Dry-bulb temperature in degC | Point, grid, admin area | Current and forecast | National meteorological APIs, global weather APIs | Hourly to sub-hourly | Station vs grid differences may create variance |
| Relative humidity | RH in percent | Point, grid, admin area | Current and forecast | National meteorological APIs, global weather APIs | Hourly to sub-hourly | Missingness common in sparse station networks |
| Heat index or feels-like | Derived apparent temperature in degC | Point, grid, admin area | Current and forecast | Sources exposing calculated index, or backend-derived from temp and RH | Hourly | Formula differences across providers must be documented |
| Heat duration | Consecutive hours or days above threshold | Admin area or grid aggregate | Historical and rolling recent window | Backend-derived metric from observations/forecasts | Recomputed per ingestion cycle | Depends on threshold definition and temporal gaps |
| Forecast lead time | Valid lead in hours or days | Same as forecast source | Forecast | Forecast APIs | Every provider cycle | Lead-time uncertainty increases with horizon |
| Alert level | Official category or dashboard illustrative level | Jurisdictional area | Current and near-term | Official heat warning feeds; policy references | Event-driven or scheduled | Must label official vs illustrative clearly |
| Vulnerability context | Aggregate population context fields | Country, province, district | Mostly static or periodic | Public demographic and vulnerability datasets | Monthly to annual | Resolution may not match weather grid |

## 4. Candidate data-source comparison

| Source class | Access method | Strengths | Risks | Best use in prototype |
|---|---|---|---|---|
| National meteorological agency APIs or bulletins | API, file, bulletin | Official and locally relevant definitions | Access limits, format inconsistency, availability windows | Primary local operational weather inputs |
| Open weather APIs | REST JSON | Fast integration, broad coverage, predictable formats | Licensing constraints, model differences, quota limits | Backup or rapid prototyping feed |
| Climate reanalysis datasets | NetCDF/CSV/API | Consistent long-term historical baseline | Not designed for real-time operational alerting | Baseline and trend context |
| Official heat alert pages or feeds | Web/API/document | Authoritative alert interpretation | Sometimes no stable machine-readable endpoint | Reference for official threshold labeling |
| Public health aggregate datasets | CSV/portal/API | Context for vulnerability and outcomes | Lagged release, coarse geography, definitional mismatch | Background context and retrospective panels |

## 5. Data dictionary for proposed dashboard (MVP)

| Field | Type | Example | Description |
|---|---|---|---|
| record_id | String | obs_20260819_0001 | Unique row identifier |
| source_id | String | tmd_obs | Data-source identifier |
| source_type | Enum | observation, forecast, alert, context | Category of data |
| indicator_name | String | temperature_c | Indicator key |
| indicator_value | Number | 35.4 | Numeric value |
| unit | String | degC | Unit for the value |
| observed_at_utc | Datetime | 2026-08-19T10:00:00Z | Observation timestamp |
| valid_from_utc | Datetime | 2026-08-19T10:00:00Z | Forecast/alert validity start |
| valid_to_utc | Datetime | 2026-08-19T13:00:00Z | Forecast/alert validity end |
| forecast_horizon_hours | Integer | 3 | Hours from run time to valid time |
| geography_level | Enum | province | Spatial level |
| geography_code | String | TH-10 | Stable area code |
| latitude | Number | 13.7563 | Optional point latitude |
| longitude | Number | 100.5018 | Optional point longitude |
| alert_level_raw | String | Heat Warning | As published by source |
| alert_level_normalized | Enum | none, advisory, watch, warning, extreme | Team-normalized level |
| quality_flag | Enum | valid, delayed, missing, outlier, stale | Validation status |
| ingest_status | Enum | success, partial, failed | Pipeline outcome |
| ingest_error_code | String | HTTP_429 | Error marker if failed |
| ingestion_run_id | String | run_20260819_1000 | Batch execution trace |
| license_note | String | attribution required | Redistribution/use note |
| assumptions_note | String | illustrative threshold | Explicit caveat field |

## 6. Data quality and conflict-handling rules

- Missing values: show as missing, never coerce to zero.
- Staleness: mark stale when source timestamp exceeds expected refresh window.
- Unit normalization: convert all temperature-like metrics to degC for display while preserving raw value in audit logs.
- Geographic alignment: map all feeds to stable geography_code to avoid merge errors.
- Source conflict policy: if two sources disagree, show both with provenance; do not silently overwrite.
- Threshold labeling: keep official thresholds separate from illustrative dashboard thresholds.

## 7. Backend ingestion feasibility note (prototype)

### 7.1 Recommended ingestion architecture

- Source adapter layer: one adapter per source class (observation, forecast, alert, context).
- Scheduler: interval-based pull plus retry backoff.
- Staging storage: raw payload archive for traceability.
- Transformation layer: normalize units, timestamps, geographies, and field names.
- Validation layer: schema checks, range checks, freshness checks, duplication checks.
- Serving layer: cache plus dashboard-facing API.

### 7.2 Minimum operational controls

- Caching: short TTL for current observations, longer TTL for context datasets.
- Error handling: fail one adapter without taking down all other feeds.
- Monitoring: per-source success rate, latency, and stale-data alarms.
- Idempotency: safe reruns using ingestion_run_id and source timestamps.
- Provenance: retain source_id, retrieval time, and license note on every served record.

### 7.3 Recommended update cadence

- Current weather observations: every 15 to 60 minutes, based on source limits.
- Near-term forecasts: every 1 to 3 hours.
- Official alert feeds: poll every 15 minutes and on-demand refresh.
- Vulnerability/context datasets: monthly or quarterly refresh.
- Reference thresholds and policy tables: on policy release or quarterly review.

## 8. Recommended mock-data fields for prototype demos

These fields are useful for demonstrating workflow while avoiding personal data:

- scenario_id
- area_name
- area_code
- simulated_priority_flag
- illustrative_trigger_reason
- handoff_owner_role
- handoff_channel
- acknowledgement_status
- fallback_path
- audit_comment

All mock fields must be visibly labeled mock or illustrative.

## 9. Risks, assumptions, and open questions

### Risks

- Overstating certainty from model-derived heat indicators.
- Mixing official warnings with illustrative thresholds without clear labels.
- Spatial mismatch between weather grids and administrative boundaries.
- API quota or outage causing stale dashboard state.

### Assumptions

- Prototype prioritizes reliability and transparency over predictive sophistication.
- Team accepts a multi-source strategy rather than a single source of truth.
- Clinical decisions remain outside dashboard scope.

### Open questions for team confirmation

1. Which local official source is primary for Thailand operational display?
2. Which geography level is the MVP default (province or district)?
3. What is the accepted stale-data timeout per indicator class?
4. Which alert-level vocabulary should be standardized for UI labels?
5. What minimum uptime target is expected for the prototype demo?

## 10. Inputs recommended for project matrices

- Data requirement matrix: include field-level provenance, update frequency, and quality checks.
- Feature feasibility-impact matrix: score adapters, caching, and fallback behavior as MVP-critical.
- Stakeholder contact-point matrix: define who acknowledges a high-priority operational signal.
- Risk governance matrix: track source licensing, stale data risk, and threshold interpretation risk.
- Roadmap decision log: capture chosen primary source, backup source, and cadence policy.

## 11. Traceability index to per-source summaries

| Source ID | Summary file | Role in this review | Evidence status |
|---|---|---|---|
| MY-S01 | My_source_01_summary.md | Official local observations for temperature and humidity | Scaffold ready, pending extracted citations |
| MY-S02 | My_source_02_summary.md | Official local forecast feed for short-horizon monitoring | Scaffold ready, pending extracted citations |
| MY-S03 | My_source_03_summary.md | Official alert-level wording and interpretation boundary | Scaffold ready, pending extracted citations |
| MY-S04 | My_source_04_summary.md | Open API fallback for rapid prototype integration | Scaffold ready, pending extracted citations |
| MY-S05 | My_source_05_summary.md | Historical baseline and retrospective climate context | Scaffold ready, pending extracted citations |
| MY-S06 | My_source_06_summary.md | Aggregate vulnerability context for non-PII planning | Scaffold ready, pending extracted citations |

Immediate next action:

- Fill each summary with source-located evidence entries, then revise Sections 3 to 9 with exact citations and confidence notes.

## Conclusion

The Heat Risk Dashboard MVP is feasible if the team treats indicator definitions, source provenance, update cadence, and validation status as first-class product requirements. The strongest architecture choice for Phase 0 is a transparent multi-source ingestion pipeline with explicit quality flags and clearly separated official versus illustrative alert interpretations.