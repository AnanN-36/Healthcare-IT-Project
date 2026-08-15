# Chris: Dashboard UX, Visualization, and Accessibility

## Research mission

Study how heat-risk information can be presented so that users can understand urgency, location, affected groups, and next action quickly.

## What to collect

- Examples of heat, emergency, public-health, or risk dashboards.
- Visualization patterns for maps, trends, alert levels, counts, task status, and data freshness.
- User-interface needs for desktop and mobile use in operational settings.
- Accessibility and plain-language requirements for public-sector or community users.
- Common dashboard usability problems: alarm fatigue, excessive detail, unclear status, misleading color, or missing context.

## Out of scope

- Producing the final visual design before the research is synthesized.
- Building all six pages of a complete system.
- Treating color alone as the alert mechanism.

## Expected research output

- A dashboard pattern and feature comparison.
- A proposed information hierarchy for the Heat Risk Dashboard.
- A list of essential widgets and their purpose.
- Accessibility and visualization rules for the prototype.

## NotebookLM prompt

For each source, use the shared source-summary prompt and add:

```text
Focus on dashboard UX, information hierarchy, visualization, accessibility, and decision-oriented presentation. Extract what a user needs to see, compare, filter, or act on. Identify risks of misleading visualization or alarm fatigue. Translate findings into prototype requirements without inventing new evidence.
```

Then combine all per-source summaries into `Chris_literature_review.md` using the shared literature-review prompt.

## File rule

Keep original files unchanged in this folder. Name files clearly, for example:
`Chris_source_01_dashboard_case.pdf`, `Chris_source_02_accessibility_guidance.md`, or `Chris_comparable_tool_notes.md`.
