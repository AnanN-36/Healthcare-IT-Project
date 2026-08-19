# My Source 04 Summary

## Source metadata

- Source ID: MY-S04
- Working title: Open-Meteo API documentation
- Organization: Open-Meteo
- Publication or service date: Ongoing service
- URL or identifier: https://open-meteo.com/
- Source type: Open weather API
- Status: Draft template, pending endpoint selection and terms confirmation

## Research question addressed

Can an open API serve as a backup or rapid prototype source for temperature, humidity, and apparent-temperature indicators?

## Key findings with source location

- Pending extraction from finalized source artifact.
- Required location format for later update: endpoint docs, parameter list, and terms section.

## Indicator extraction table

| Indicator | Definition | Unit | Time horizon | Geography | Source location |
|---|---|---|---|---|---|
| temperature_2m | Pending exact provider definition | degC | hourly current and forecast | coordinate grid | pending |
| relative_humidity_2m | Pending exact provider definition | percent | hourly current and forecast | coordinate grid | pending |
| apparent_temperature | Pending exact provider definition | degC | hourly current and forecast | coordinate grid | pending |

## Data usability and backend ingestion notes

- Expected format: REST JSON.
- Ingestion mechanism: scheduler with coordinate batching and cache.
- Identifier requirements: latitude, longitude, timezone, model run metadata.
- Validation needs: schema-version checks and value plausibility checks.
- Failure handling: quota-aware retry and fallback source switching.

## Threshold and alert interpretation

- API weather variables are not official warning categories.
- UI threshold mapping must be explicitly labeled illustrative unless linked to official policy.

## Limitations and uncertainty

- Model choices and updates may change outputs.
- Licensing and attribution requirements must be reviewed before redistribution.

## Implications for Heat Risk Dashboard

- Useful as fallback feed and for faster MVP integration.
- Must be paired with provenance and source confidence display.

## Follow-up questions

1. Which model and resolution are acceptable for prototype quality?
2. What are the request-rate constraints at expected dashboard traffic?
3. What attribution text is mandatory in the UI or documentation?
