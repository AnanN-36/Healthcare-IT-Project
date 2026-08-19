# My Source 03 Summary

## Source metadata

- Source ID: MY-S03
- Working title: Official heat alert or heat-health advisory publication
- Organization: Thai public authority, to confirm exact owner
- Publication or service date: Pending verification
- URL or identifier: https://ddc.moph.go.th/ (candidate)
- Source type: Official warning or advisory reference
- Status: Draft template, pending exact source selection and citation

## Research question addressed

How should the dashboard represent heat alert levels so official definitions remain distinct from illustrative rules?

## Key findings with source location

- Pending extraction from finalized source artifact.
- Required location format for later update: page/section/table/official wording.

## Indicator extraction table

| Indicator | Definition | Unit | Time horizon | Geography | Source location |
|---|---|---|---|---|---|
| alert_level | Pending official category definitions | category label | current or advisory period | jurisdictional area | pending |
| advisory_text | Pending | text | advisory period | jurisdictional area | pending |
| effective_period | Pending | datetime range | advisory period | jurisdictional area | pending |

## Data usability and backend ingestion notes

- Expected format: webpage, PDF, bulletin, or feed (to verify).
- Ingestion mechanism: periodic polling and content-diff detection.
- Identifier requirements: publication ID, issue time, region code.
- Validation needs: parse integrity checks and provenance tagging.
- Failure handling: retain last verified advisory and mark stale.

## Threshold and alert interpretation

- Official categories must remain verbatim in alert_level_raw.
- Any normalized UI tiers must be mapped with an auditable lookup table.

## Limitations and uncertainty

- Some official advisories may not have stable machine-readable formats.
- Publication timing may be event-driven, not fixed interval.

## Implications for Heat Risk Dashboard

- Provides authoritative language for warning interpretation.
- Reduces risk of users treating illustrative thresholds as official mandates.

## Follow-up questions

1. Which agency is the canonical source for heat warning categories?
2. Is there a machine-readable feed, or do we need document parsing?
3. What is the escalation rule when advisory text changes without clear level code?
