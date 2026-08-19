# My Source 02 Summary

## Source metadata

- Source ID: MY-S02
- Working title: Thailand Meteorological Department forecast products
- Organization: Thai Meteorological Department (TMD)
- Publication or service date: Ongoing service, verify issue cycle
- URL or identifier: https://www.tmd.go.th/
- Source type: Official weather forecast source
- Status: Draft template, pending final source record and endpoint verification

## Research question addressed

How can official forecast feeds support short-horizon heat-risk situational awareness in the dashboard?

## Key findings with source location

- Pending extraction from finalized source artifact.
- Required location format for later update: page/section/table/endpoint field name.

## Indicator extraction table

| Indicator | Definition | Unit | Time horizon | Geography | Source location |
|---|---|---|---|---|---|
| forecast_temperature | Pending | degC | next hours to days | area grid or administrative area | pending |
| forecast_humidity | Pending | percent | next hours to days | area grid or administrative area | pending |
| forecast_period | Pending | hours or days | forecast lead | source dependent | pending |

## Data usability and backend ingestion notes

- Expected format: JSON, XML, CSV, or published bulletin text (to verify).
- Ingestion mechanism: cycle-aware pull and reingestion when updates are revised.
- Identifier requirements: model run time, valid-from, valid-to.
- Validation needs: monotonic lead-time checks and duplicate-cycle handling.
- Failure handling: fallback to latest valid forecast with stale flag.

## Threshold and alert interpretation

- Forecast values are not diagnoses.
- Dashboard threshold overlays must be labeled illustrative unless mapped to official policy text.

## Limitations and uncertainty

- Forecast uncertainty increases by horizon.
- Potential differences between forecast products for the same area and period.

## Implications for Heat Risk Dashboard

- Supports near-term planning tiles and trend projections.
- Requires clear display of model run time and forecast validity window.

## Follow-up questions

1. What is the preferred forecast horizon for MVP, 24h or 72h?
2. How often are official forecast products updated?
3. Which forecast product should be designated as primary in conflict cases?
