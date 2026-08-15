# My: Heat-Risk Indicators and Data Sources

## Research mission

Identify what heat-risk information a dashboard needs, where it can come from, and how it can be represented without pretending to provide weather prediction or clinical diagnosis.

## What to collect

- Heat-related indicators: temperature, humidity, heat index or equivalent, duration, forecast horizon, and geographic level.
- Public data sources, APIs, open datasets, or official monitoring sources.
- Definitions, units, update frequency, coverage, and known limitations for each indicator.
- Existing alert levels or thresholds, clearly marking whether they are official, illustrative, or context-dependent.
- Data quality issues such as missingness, latency, spatial resolution, and conflicting sources.

## Out of scope

- Creating a new weather-forecasting model.
- Treating an alert threshold as a medical diagnosis rule.
- Collecting personally identifiable patient data.

## Expected research output

- A source-to-indicator inventory.
- A data dictionary for the proposed dashboard.
- A comparison of candidate data sources.
- A recommendation for mock-data fields and an update cadence.

## NotebookLM prompt

For each source, use the shared source-summary prompt and add:

```text
Focus on heat-risk indicators and data usability. Extract each indicator's definition, unit, time horizon, geographic level, source, update frequency, threshold or alert interpretation, and limitations. Separate officially defined information from illustrative or inferred rules. Do not convert heat metrics into clinical advice.
```

Then combine all per-source summaries into `My_literature_review.md` using the shared literature-review prompt.

## File rule

Keep original files unchanged in this folder. Name files clearly, for example:
`My_source_01_heat_index_definition.pdf`, `My_source_02_data_catalogue.html`, or `My_data_source_notes_YYYY-MM-DD.md`.
