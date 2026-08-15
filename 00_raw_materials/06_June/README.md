# June: IT Architecture, Governance, Evaluation, and Phase 0 Feasibility

## Research mission

Identify what is needed to make the Heat Risk Dashboard a credible IT roadmap initiative: data flow, integration boundaries, governance, security, evaluation, and a realistic Phase 0 path.

## What to collect

- High-level architecture patterns for dashboards that combine external risk data and health-system or community information.
- Interoperability, data exchange, identity, access control, audit, and data-retention considerations.
- Governance requirements for public-sector or health-related data use.
- Measures of usefulness: timeliness, coverage, acknowledgement, outreach completion, usability, and equity.
- Pilot, implementation, or Phase 0 planning examples.
- Technical, organizational, and operational dependencies.

## Out of scope

- Writing production code or choosing a final cloud platform.
- Designing a national-scale architecture.
- Making legal claims without an authoritative source or local review.

## Expected research output

- A conceptual data-flow and integration boundary list.
- A risk and governance checklist.
- A small evaluation framework for the prototype or pilot.
- A Phase 0 roadmap with assumptions, dependencies, and next decisions.

## NotebookLM prompt

For each source, use the shared source-summary prompt and add:

```text
Focus on IT architecture, data governance, interoperability, security, evaluation, implementation dependencies, and Phase 0 feasibility. Extract what the source implies for a Heat Risk Dashboard roadmap initiative. Separate requirements, recommendations, evidence, and assumptions. Do not claim legal compliance or production readiness from this source alone.
```

Then combine all per-source summaries into `June_literature_review.md` using the shared literature-review prompt.

## File rule

Keep original files unchanged in this folder. Name files clearly, for example:
`June_source_01_interoperability.pdf`, `June_source_02_governance_guidance.md`, or `June_phase0_notes.md`.
