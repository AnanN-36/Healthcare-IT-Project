# Com: IT Architecture, Data Model, Integration, and Governance Controls

## Research mission

Define the conceptual technical structure that connects source data, mock vulnerable-population context, dashboard views, alerts, and governance controls for a Phase 0 Heat Risk Dashboard prototype.

## What to collect

- High-level architecture patterns for dashboards that combine environmental, operational, and health-context data.
- Logical data model or schema examples for dashboard-friendly data: area, time, indicator, alert level, vulnerable group, action status, source freshness.
- Integration boundaries between data ingestion, processing, storage, dashboard frontend, notification layer, and audit/logging.
- Identity, access control, audit trail, data retention, source traceability, and data-quality controls.
- Governance, privacy, security, ownership, and accountability requirements relevant to a roadmap-level prototype.

## Out of scope

- Writing production code or selecting a final cloud or software vendor.
- Making legal or compliance claims without authoritative local review.
- Building a complete health information system.
- Designing detailed workflows for the five supporting components.

## Expected research output

- A conceptual architecture diagram or component list.
- A logical data model and dashboard data object list.
- An integration-boundary and data-flow list.
- An access, audit, source-traceability, and governance checklist.
- A Phase 0 technical feasibility note with assumptions and dependencies.

## NotebookLM prompt

For each source, use the shared source-summary prompt and add:

```text
Focus on IT architecture, logical data model, integration boundaries, interoperability, data quality, access control, audit, traceability, governance, security, privacy, and Phase 0 technical feasibility for a Heat Risk Dashboard. Separate requirements, recommendations, evidence, and assumptions. Do not claim legal compliance or production readiness from this source alone.
```

Then combine all per-source summaries into `Com_literature_review.md` using the shared literature-review prompt.

## File rule

Keep original files unchanged in this folder. Name files clearly, for example:
`Com_source_01_architecture.pdf`, `Com_source_02_data_model.md`, or `Com_governance_notes_YYYY-MM-DD.md`.
