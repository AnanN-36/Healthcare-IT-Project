# Chris: Dashboard UX, Visualization, Accessibility, and Adoption

## Research mission

Study how heat-risk information can be presented so that users can understand urgency, location, affected groups, and next action quickly, while also considering adoption, satisfaction, and communication patterns familiar from CSAT SaaS and marketing work.

## What to collect

- Examples of heat, emergency, public-health, or risk dashboards.
- Visualization patterns for maps, trends, alert levels, counts, task status, and data freshness.
- User-interface needs for desktop and mobile use in operational settings.
- Accessibility and plain-language requirements for public-sector or community users.
- Common dashboard usability problems: alarm fatigue, excessive detail, unclear status, misleading color, or missing context.
- Adoption and satisfaction signals: comprehension, task completion, trust, feedback, and reasons users may ignore or abandon a dashboard.

## Out of scope

- Producing the final visual design before the research is synthesized.
- Building all six pages of a complete system.
- Treating color alone as the alert mechanism.

## Expected research output

- A dashboard pattern and feature comparison.
- A proposed information hierarchy for the Heat Risk Dashboard.
- A list of essential widgets and their purpose.
- Accessibility and visualization rules for the prototype.
- A small set of user-adoption or satisfaction measures for evaluating the prototype.

## NotebookLM prompt

For each source, use the shared source-summary prompt and add:

```text
Focus on dashboard UX, information hierarchy, visualization, accessibility, adoption, satisfaction, and decision-oriented presentation. Extract what a user needs to see, compare, filter, or act on. Identify risks of misleading visualization, alarm fatigue, low trust, or poor adoption. Translate findings into prototype requirements and evaluation measures without inventing new evidence.
```

Then combine all per-source summaries into `Chris_literature_review.md` using the shared literature-review prompt.

## File rule

Keep original files unchanged in this folder. Name files clearly, for example:
`Chris_source_01_dashboard_case.pdf`, `Chris_source_02_accessibility_guidance.md`, or `Chris_comparable_tool_notes.md`.
