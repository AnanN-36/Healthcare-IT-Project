# My Source 06 Summary

## Source metadata

- Source ID: MY-S06
- Working title: Public population-context dataset
- Organization: Candidate options include national statistics or global population datasets
- Publication or service date: Pending source choice
- URL or identifier: https://www.worldpop.org/ (candidate)
- Source type: Demographic or vulnerability context data
- Status: Draft template, pending final source and variable selection

## Research question addressed

What aggregate context variables can be joined safely with heat indicators to improve prioritization without using personally identifiable data?

## Key findings with source location

- Pending extraction from finalized source artifact.
- Required location format for later update: variable definition table and release notes.

## Indicator extraction table

| Indicator | Definition | Unit | Time horizon | Geography | Source location |
|---|---|---|---|---|---|
| population_total | Pending source definition | persons | annual or periodic | admin area or grid | pending |
| older_adults_share | Pending source definition | percent | annual or periodic | admin area or grid | pending |
| infant_population_proxy | Pending source definition | persons or percent | annual or periodic | admin area or grid | pending |

## Data usability and backend ingestion notes

- Expected format: CSV, GeoTIFF, shapefile, or API (source dependent).
- Ingestion mechanism: periodic batch import and key-based joins.
- Identifier requirements: stable geography code and release version.
- Validation needs: schema drift checks and join-coverage checks.
- Failure handling: serve previous verified snapshot with timestamp warning.

## Threshold and alert interpretation

- Context data should inform planning and communication priorities.
- Context values must not be interpreted as patient-level risk.

## Limitations and uncertainty

- Possible mismatch between weather grid and admin boundaries.
- Update lag can reduce current-year precision.

## Implications for Heat Risk Dashboard

- Enables vulnerability-aware views at aggregate level.
- Supports handoff context while preserving privacy boundaries.

## Follow-up questions

1. Which geography code standard should be canonical for joins?
2. What minimum refresh interval is realistic for demographic context?
3. Which context variables are essential versus optional for MVP?
