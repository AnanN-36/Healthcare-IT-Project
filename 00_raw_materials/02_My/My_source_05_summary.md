# My Source 05 Summary

## Source metadata

- Source ID: MY-S05
- Working title: ERA5 reanalysis data overview
- Organization: ECMWF Copernicus Climate Data Store
- Publication or service date: Ongoing dataset updates
- URL or identifier: https://cds.climate.copernicus.eu/
- Source type: Climate reanalysis dataset
- Status: Draft template, pending variable set and extraction method confirmation

## Research question addressed

How can historical climate baselines support retrospective heat-risk context for the dashboard?

## Key findings with source location

- Pending extraction from finalized source artifact.
- Required location format for later update: variable catalog, temporal resolution notes, and license text.

## Indicator extraction table

| Indicator | Definition | Unit | Time horizon | Geography | Source location |
|---|---|---|---|---|---|
| air_temperature | Pending dataset-specific definition | degC or K | historical hourly | global grid | pending |
| dewpoint_or_humidity_proxy | Pending dataset-specific definition | source dependent | historical hourly | global grid | pending |
| derived_heat_metric | Derived by backend | degC or index | historical window | admin aggregate from grid | pending |

## Data usability and backend ingestion notes

- Expected format: NetCDF/GRIB via CDS workflow.
- Ingestion mechanism: batch extraction, transform, and area aggregation.
- Identifier requirements: dataset version, variable key, spatial resolution.
- Validation needs: temporal completeness and conversion consistency checks.
- Failure handling: queue retry and partial-batch checkpoint resume.

## Threshold and alert interpretation

- Reanalysis data supports context and trends, not live operational warnings.
- Threshold overlays on this data are analytical and must be labeled accordingly.

## Limitations and uncertainty

- May lag real-time operations.
- Requires heavier ETL compared with standard REST APIs.

## Implications for Heat Risk Dashboard

- Strong candidate for baseline and long-term trend panels.
- Best used as background context paired with near-real-time operational sources.

## Follow-up questions

1. What baseline period should the team standardize for anomalies?
2. Which spatial aggregation method is acceptable for province-level views?
3. Is storage budget sufficient for retained historical slices?
