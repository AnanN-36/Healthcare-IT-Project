# Mod: Scope, IT Use Case, and Product Requirements

## Research mission

Define the problem and the minimum IT initiative that the team will propose:

> Heat Risk Dashboard: a digital dashboard that translates heat-risk information into actionable, coordinated health-related operations.

Keep the project focused on IT enablement and operational support. Do not turn this stream into a clinical guideline or a complete healthcare information system.

## What to collect

- Evidence that heat alerts do not automatically become coordinated health actions.
- Existing heat-risk dashboards, alerting systems, or public-sector digital tools.
- User problems that a dashboard could address: awareness, prioritization, task visibility, escalation, or reporting.
- Minimum viable dashboard capabilities and non-goals.
- Examples of implementation or roadmap language suitable for a Phase 0 initiative.

## Out of scope

- Designing a clinical treatment protocol.
- Building a production system or selecting a final vendor.
- Deep investigation of all five supporting components.

## Expected research output

- A short problem statement with evidence.
- A list of dashboard users and their top decisions.
- A must-have / should-have / out-of-scope feature list.
- A proposed initiative statement and success definition.

## NotebookLM prompt

For each source, use the shared source-summary prompt and add:

```text
Focus on the source's implications for a Heat Risk Dashboard as an IT and operational-support initiative. Extract the problem gap, users, decisions, dashboard capabilities, implementation constraints, and any evidence that supports or challenges the proposed scope. Do not invent clinical recommendations.
```

Then combine all per-source summaries into `Mod_literature_review.md` using the shared literature-review prompt.

## File rule

Keep original files unchanged in this folder. Name files clearly, for example:
`Mod_source_01_title.pdf`, `Mod_source_02_title.md`, or `Mod_meeting_notes_YYYY-MM-DD.md`.
