# Mod: Healthcare Context, Vulnerable Population, and Safe Operational Scope

## Research mission

Define the health problem, vulnerable-population context, and safe operational boundary for the initiative:

> Heat Risk Dashboard: a digital dashboard that translates heat-risk information into actionable, coordinated health-related operations.

Use nursing and healthcare experience to keep the project clinically sensible while staying at roadmap level. Do not turn this stream into a treatment protocol, patient registry, or legal compliance claim.

## What to collect

- Heat-health problem framing: why heat alerts need health-related operational support.
- Vulnerable groups and practical outreach context, especially older adults, chronic disease groups, outdoor workers, people living alone, and people with limited cooling access.
- Health-related data fields that could be used in mock cases, with a data-minimization mindset.
- Boundaries between public-health support, nursing judgment, emergency referral, and clinical treatment.
- Safety, privacy, equity, and non-goal statements that prevent the dashboard from being framed as diagnosis or treatment.

## Out of scope

- Designing a clinical treatment protocol.
- Collecting or using real patient-identifiable data.
- Assigning medical risk scores without local clinical authority.
- Designing detailed workflows for the five supporting components beyond handoff context.

## Expected research output

- A concise health problem statement and safe scope boundary.
- A vulnerable-population profile and rationale for dashboard prioritization.
- A minimum mock data-field list with privacy and equity notes.
- Clinical/public-health non-goals and escalation caveats for the prototype.

## NotebookLM prompt

For each source, use the shared source-summary prompt and add:

```text
Focus on the source's implications for heat-health problem framing, vulnerable populations, safe operational scope, mock health-related data fields, privacy, equity, and boundaries between public-health support and clinical care. Separate evidence, assumptions, and recommendations. Do not create diagnosis, treatment advice, or real patient-risk scoring rules.
```

Then combine all per-source summaries into `Mod_literature_review.md` using the shared literature-review prompt.

## File rule

Keep original files unchanged in this folder. Name files clearly, for example:
`Mod_source_01_heat_health_context.pdf`, `Mod_source_02_vulnerable_groups.md`, or `Mod_scope_notes_YYYY-MM-DD.md`.
