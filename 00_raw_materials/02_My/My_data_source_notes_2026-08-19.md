# My Data Source Notes (2026-08-19)

Purpose: working register for the My stream (heat-risk indicators, data usability, backend ingestion feasibility).

## 1. Source register template

Use one row per source before running NotebookLM one-source summary.

| Source ID | Title | Organization | Date | URL or identifier | Source type | Why relevant | Raw format | Access method | Update frequency | Geography | Licensing note | Status |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| MY-S01 | Thailand Meteorological Department observational weather feed | Thai Meteorological Department | Ongoing service | https://www.tmd.go.th/ | Official weather source | Local official temperature and humidity observations | JSON or CSV or bulletin table, verify | API or documented download, verify | Near real-time, verify exact interval | Thailand station or area level | License and attribution pending verification | summary scaffold created |
| MY-S02 | Thailand Meteorological Department forecast products | Thai Meteorological Department | Ongoing service | https://www.tmd.go.th/ | Official weather source | Near-term temperature and humidity forecasts | JSON or XML or bulletin text, verify | API or documented download, verify | Per forecast cycle, verify | Thailand area level | License and attribution pending verification | summary scaffold created |
| MY-S03 | Official heat alert or heat-health advisory publication | Thai public authority, pending exact owner | Pending verification | https://ddc.moph.go.th/ | Official policy or warning reference | Official wording for alert interpretation | Webpage or PDF or bulletin, verify | Web pull or manual capture | Event-driven or scheduled, verify | Jurisdictional administrative area | Reuse terms pending verification | summary scaffold created |
| MY-S04 | Open-Meteo weather API | Open-Meteo | Ongoing service | https://open-meteo.com/ | Open weather API | Rapid integration and fallback data source | JSON | REST API | Hourly endpoints available, verify | Coordinate grid | Attribution and terms pending verification | summary scaffold created |
| MY-S05 | ERA5 reanalysis data | ECMWF Copernicus Climate Data Store | Ongoing dataset updates | https://cds.climate.copernicus.eu/ | Climate dataset | Historical baseline and retrospective context | NetCDF or GRIB | CDS API or download workflow | Batch periodic pulls | Global grid aggregated to admin area | Copernicus terms and attribution pending verification | summary scaffold created |
| MY-S06 | Public demographic context dataset candidate | WorldPop, candidate | Ongoing releases | https://www.worldpop.org/ | Population context dataset | Aggregate vulnerability context without personal data | CSV or GeoTIFF or shapefile, source dependent | Download or API when available | Annual or periodic, source dependent | Grid or admin area | Licensing and redistribution pending verification | summary scaffold created |

## 2. One-source summary checklist

- Metadata complete: title, organization, date, URL/identifier.
- Indicators extracted: definition, unit, horizon, geography.
- Operational details extracted: format, endpoint/file, refresh model, identifiers.
- Quality constraints extracted: missingness, latency, resolution, conflicts.
- Threshold interpretation separated: official vs illustrative.
- Safety boundary preserved: no diagnosis, no treatment rule, no PII.

## 3. Candidate source shortlist (to verify)

| Candidate ID | Candidate source class | Primary indicators | Likely feasibility | Key verification needed |
|---|---|---|---|---|
| MY-C01 | National meteorological observations | Temperature, humidity | High | API/document access and terms |
| MY-C02 | National meteorological forecasts | Forecast temperature/humidity | High | Forecast cycle and horizon definitions |
| MY-C03 | Official heat alert publications | Alert level and advisory text | Medium | Machine-readable access and cadence |
| MY-C04 | Open weather API fallback | Temperature, humidity, feels-like | High | Licensing and quota limits |
| MY-C05 | Climate baseline dataset | Historical heat context | Medium | Spatial resolution and timeliness |
| MY-C06 | Public demographic context dataset | Vulnerability context fields | Medium | Matching admin codes and update lag |

## 4. Per-source output file naming

Use these names when source summaries are generated:

- My_source_01_summary.md
- My_source_02_summary.md
- My_source_03_summary.md
- My_source_04_summary.md
- My_source_05_summary.md
- My_source_06_summary.md

After summaries are complete, consolidate into:

- My_literature_review.md

## 5. Backend ingestion minimum acceptance checklist

- Adapter implemented for each selected source.
- Unit conversion and timestamp normalization tested.
- Geography mapping tested for every record.
- Validation flags produced: valid, missing, stale, outlier.
- Cache policy documented for each endpoint.
- Fallback behavior tested when one source fails.
- Provenance fields visible in dashboard payload.
- Official versus illustrative threshold labeling verified.
