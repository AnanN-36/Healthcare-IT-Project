# Belle: IT Use Case, User Needs, and Product Requirements

## Research mission

Translate the health problem into a clear IT use case and minimum product requirements, using clinical and public-health understanding to keep the proposed dashboard useful and safe.

## What to collect

- Evidence that heat alerts do not automatically become coordinated health actions.
- Existing heat-risk dashboards, alerting systems, or public-sector digital tools.
- User problems that a dashboard could address: awareness, prioritization, task visibility, escalation, or reporting.
- User needs and top decisions for public health officers, community health workers, facilities, residents, and caregivers.
- Minimum viable dashboard capabilities, acceptance criteria, and non-goals.
- Health and privacy considerations that should shape the product without becoming a clinical guideline.

## Out of scope

- Designing a clinical treatment protocol.
- Building a production system or selecting a final vendor.
- Designing detailed workflows for all five supporting components.

## Expected research output

- A short problem statement with evidence.
- A list of dashboard users and their top decisions.
- A must-have / should-have / out-of-scope feature list.
- A proposed IT use case, acceptance criteria, and success definition.

## NotebookLM prompt

For each source, use the shared source-summary prompt and add:

```text
Focus on the source's implications for a Heat Risk Dashboard as an IT and operational-support use case. Extract the problem gap, users, decisions, dashboard capabilities, implementation constraints, acceptance criteria, and evidence that supports or challenges the proposed scope. Use health context carefully, distinguish evidence from assumptions, and do not invent diagnosis or treatment advice.
```

Then combine all per-source summaries into `Belle_literature_review.md` using the shared literature-review prompt.

## File rule

Keep original files unchanged in this folder. Do not place real personal or patient-identifiable data in the repository. Name files clearly, for example:
`Belle_source_01_dashboard_use_case.pdf` or `Belle_source_02_user_needs.md`.
