# June: Evidence Synthesis, Policy References, and Phase 0 Evaluation

## Research mission

Build a traceable evidence base that helps the team justify the project, compare sources, identify gaps, and define how a Phase 0 roadmap or prototype should be evaluated. Keep the work descriptive and evidence-led, without requiring deep clinical or production-IT expertise.

## What to collect

- WHO, public-health, climate-health, digital health, implementation, or policy references that support the Heat Risk Dashboard concept.
- Evidence that heat risk creates operational coordination problems, not only clinical problems.
- Evaluation examples for dashboards, warning systems, public-health digital tools, or pilot initiatives.
- Implementation or Phase 0 planning examples: scope, stakeholders, readiness, feasibility, risks, and roadmap assumptions.
- Source quality, limitations, contradictions, and evidence gaps across all team streams.
- Matrix-ready statements that are clearly tied to source evidence.

## Out of scope

- Acting as the final clinical reviewer.
- Making production technical decisions.
- Filling gaps by inventing evidence where the sources are weak.

## Expected research output

- A policy and literature source inventory.
- A cross-source evidence matrix.
- A source-quality and evidence-gap summary.
- Phase 0 feasibility assumptions and roadmap dependencies.
- Prototype evaluation measures linked to evidence.

## NotebookLM prompt

For each source, use the shared source-summary prompt and add:

```text
Focus on evidence synthesis, policy relevance, implementation feasibility, Phase 0 planning, roadmap assumptions, and prototype evaluation for a Heat Risk Dashboard. Extract claims, evidence strength, source limitations, contradictions, relevant metrics, and gaps. Distinguish evidence from assumptions and do not invent unsupported claims.
```

Then combine all per-source summaries into `June_literature_review.md` using the shared literature-review prompt.

## File rule

Keep original files unchanged in this folder. Name files clearly, for example:
`June_source_01_policy_reference.pdf`, `June_source_02_evaluation_framework.md`, or `June_evidence_review_notes.md`.
