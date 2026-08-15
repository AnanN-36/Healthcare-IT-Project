# HeatShield: Mod Literature Review
## Global-to-Local Heat-Health Operational Framework

เอกสารนี้เป็นผลการสังเคราะห์ในสายงานของ Mod โดยเน้น 4 เรื่อง: health problem framing, vulnerable-population context, safe operational scope และข้อมูลที่บุคลากรทางการแพทย์ใช้วิเคราะห์แนวโน้มย้อนหลังใน Heat Risk Dashboard

## 1. Project interpretation and decision boundary

### 1.1 Agreed purpose

Heat Risk Dashboard รุ่นแรกเป็น retrospective analysis dashboard สำหรับบุคลากรทางการแพทย์และสาธารณสุข ใช้ข้อมูลย้อนหลังจาก Lancet Countdown 2025 เพื่อ:

- เปรียบเทียบแนวโน้มความเสี่ยงจากความร้อนตามปี พื้นที่ และกลุ่มประชากร
- ทำให้เห็นความสัมพันธ์ระหว่าง heat exposure, heat stress, work capacity, sleep loss และ heat-related mortality ในระดับ population
- ใช้เป็นจุดเริ่มต้นของการกำหนดทิศทาง workflow และการส่งต่อ task ไปยัง 5 supporting components

รุ่นที่ทำในรายวิชานี้ไม่ใช่ live monitoring, weather prediction, diagnosis, treatment recommendation หรือ patient registry จริง ข้อมูลผู้ป่วยและข้อมูล social vulnerability ที่ไม่มีใน Lancet dataset จะใช้ได้เฉพาะ mock case เพื่อแสดงแนวทางการทำงานในอนาคต

### 1.2 Intended user and decision

Primary user ที่เหมาะกับ prototype คือบุคลากรทางการแพทย์หรือสาธารณสุขที่ทำงานวิเคราะห์และวางแผน เช่น public-health nurse, surveillance staff หรือ health-system coordinator การตัดสินใจที่ dashboard สนับสนุนคือ:

> ในช่วงเวลาและพื้นที่ใด แนวโน้ม heat-health มีความสำคัญพอที่จะเปิด task ประสานงานหรือเตรียมส่งต่อไปยัง contact point ใด

Dashboard ไม่ควรตอบคำถามว่า “ผู้ป่วยรายนี้เป็นโรคอะไร” หรือ “ต้องให้การรักษาอะไร”

### 1.3 Alert and handoff boundary

`Red alert` ใน concept นี้ควรเรียกว่า `high-priority operational signal` ในชั้น retrospective prototype เป็นสัญญาณให้ผู้ใช้ตรวจสอบข้อมูลและสร้าง task ไปยัง supporting component เช่น outreach, communication หรือ facility preparedness ไม่ใช่สีที่บอก diagnosis, prognosis หรือความรุนแรงทางคลินิกของบุคคล

เมื่อระบบพัฒนาเป็น live dashboard ในอนาคต การสร้าง task ต้องมี owner, contact point, information passed, channel, acknowledgement และ fallback ครบตาม concept file และต้องได้รับการยืนยันจากผู้รับผิดชอบในพื้นที่ก่อนใช้จริง

## 2. Evidence from the Lancet Countdown data files

ข้อสังเกตสำคัญคือแต่ละ indicator มีหน่วย ระดับพื้นที่ และช่วงเวลาไม่เหมือนกัน จึงไม่ควรนำค่าทั้งหมดมาบวกเป็น `overall clinical risk score` เดียวกัน การเปรียบเทียบใน prototype ควรใช้ trend chart, indicator cards และ source-aware filters แยกกัน

| Indicator | สิ่งที่ข้อมูลวัดจริง | ข้อค้นพบที่ใช้ได้ | การใช้ใน dashboard | ข้อจำกัด |
|---|---|---|---|---|
| 1.1.1 Vulnerable populations | Heatwave exposure ของ infants อายุต่ำกว่า 1 ปี และประชากรอายุมากกว่า 65 ปี โดยมีทั้ง person-days และ average days | ปี 2024 exposure สูงเป็นประวัติการณ์เมื่อเทียบกับ baseline 1986-2005: older adults เพิ่ม 304% และ infants เพิ่ม 389% | แสดง trend ของ vulnerable exposure และใช้เป็น population context | เป็น population estimate ไม่ใช่รายชื่อผู้ป่วยและไม่ใช่ระดับตำบลในทุกประเทศ |
| 1.1.1 Attributable heatwave days | Observed, counterfactual และ attributable-to-climate-change heatwave days ในปี 2020-2024 | โดยเฉลี่ย 84% ของ heatwave days ที่คนเผชิญในปี 2020-2024 ไม่คาดว่าจะเกิดใน counterfactual ที่ไม่มี human-caused climate change | แสดง climate-attributable context แยกจาก exposure ของกลุ่มเปราะบาง | ไม่ควรเปลี่ยนเป็น risk score หรือใช้เป็น clinical threshold |
| 1.1.2 Heat and physical activity | ชั่วโมงต่อคนต่อปีที่มี heat-stress risk ระดับ low, moderate, high และ extreme สำหรับ activity class 1 และ 3 | ปี 2024 มีอย่างน้อย moderate risk ระหว่างกิจกรรมเบาเฉลี่ย 1,609 ชั่วโมงต่อคน เพิ่ม 35.8% จากค่าเฉลี่ย 1990-1999 | ใช้เป็น trend ของ activity-related heat stress และ worker/outreach context | เป็นแบบจำลองตาม ambient temperature, humidity, activity และ clothing ไม่ใช่คำสั่งห้ามออกกำลังกาย |
| 1.1.3 Change in labour capacity | Potential work hours lost จากอุณหภูมิ ความชื้น รังสี และ metabolic rate แยก sector | ปี 2024 สูญเสีย potential labour hours 640 billion ชั่วโมง เพิ่ม 98% จากค่าเฉลี่ย 1990-1999 | ใช้เป็น socioeconomic and occupational context โดยเฉพาะ agriculture/construction | เป็น country-average และเน้น formal employment จึงไม่ใช่จำนวนคนป่วยหรือชั่วโมงงานจริงของพื้นที่ย่อย |
| 1.1.3 Outdoor workers | จำนวนและสัดส่วน outdoor workers ในประชากรวัยทำงานอายุ 15 ปีขึ้นไป | ปี 2024 มี outdoor workers ประมาณ 1.5 billion คน หรือ 25.3% ของ working-age population | ใช้เป็น population context สำหรับ worker pathway | ไม่ควรใช้แทนข้อมูลรายชื่อหรือความเสี่ยงของ worker รายบุคคล |
| 1.1.4 Nighttime temperatures and sleep | Global percentage change in sleep hours lost relative to 1986-2005 baseline | sleep time lost เพิ่ม 6% ในช่วง 2020-2024 และถึง 9% ในปี 2024 | ใช้เป็น contextual trend ประกอบ prolonged heat exposure | เป็น global model จาก sleep-tracker study ไม่ใช่ผลตรวจการนอนของผู้ใช้ dashboard |
| 1.1.5 Heat-related mortality | Attributable fraction และ attributable number of deaths | ปี 2012-2021 มี heat-related deaths เฉลี่ย 546,000 รายต่อปี เพิ่ม 63.2% จาก 335,000 รายในปี 1990-1999 | ใช้เป็น population outcome และ post-event evaluation context | เป็น model estimate ระดับประชากร ไม่ใช่ real-time death notification หรือ patient-level outcome |
| 1.2.5 Extreme weather and sentiment | ผลของ extreme heat ต่อ expressed online sentiment | ปี 2024 มีผลทำให้ sentiment แย่ลง 132% เทียบกับ baseline 2006-2022 | เก็บเป็น optional future context ถ้าทีมต้องการพูดถึง mental-wellbeing signal | ไม่ใช่ clinical mental-health measure และไม่ใช่ vector-borne disease suitability; ไม่ควรอยู่ใน MVP core |

### 2.1 Corrections to the previous draft

- `3.5 billion hours` และ claim ว่า construction/agriculture รวมกันกว่า 80% ไม่ตรงกับ `1.1.3 PWHL` ในไฟล์ที่ตรวจแล้ว ควรใช้ 640 billion potential work hours lost in 2024 และระบุหน่วย/ข้อจำกัดให้ครบ
- `1.1.2` ไม่ได้วัด `daily_unsafe_exercise_hours` หรือสร้าง rule “ห้ามทำกิจกรรมกลางแจ้ง” โดยตรง แต่เป็น annual person-hours ตาม risk category และ activity class
- `1.2.5` เป็น extreme heat and sentiment ไม่ใช่ drought หรือ vector-borne disease suitability
- `1.1.1` และ `1.1.1 attributable` เป็นคนละไฟล์และคนละความหมาย ต้องแยกใน data model
- `1.1.4` สนับสนุน sleep-loss trend แต่ยังไม่ควรสรุปว่า heat ทำให้ acute morning complications ในผู้ป่วย hypertension หรือ heart disease เพิ่มขึ้นโดยตรงจากไฟล์นี้
- `1.1.5` ควรใช้ 546,000 deaths และ 63.2% พร้อมช่วงเวลา 2012-2021 และ baseline 1990-1999 แทน “เกือบ 500,000” และ “63-68%”

## 3. Vulnerable populations for the prototype

เพื่อให้ขอบเขตพอดีกับเวลาของทีมและสอดคล้องกับ data ที่มี ให้ล็อกกลุ่มหลักไว้ดังนี้:

1. Infants younger than 1 year: ตรงกับ Lancet indicator 1.1.1
2. Older adults older than 65 years: ตรงกับ Lancet indicator 1.1.1 และสอดคล้องกับหลักฐานไทยหลายแหล่ง
3. Outdoor workers: ตรงกับ indicator 1.1.3 Workers และ PWHL โดยเฉพาะ agriculture/construction
4. People with chronic disease: ใช้เป็น mock context field หรือ future local linkage เท่านั้น เพราะ Lancet files ที่ใช้ไม่ได้ให้รายชื่อหรือ prevalence รายบุคคลของโรคเรื้อรัง
5. People living alone: ใช้เป็น mock social-vulnerability field หรือ future local linkage เท่านั้น เพราะไม่มีใน Lancet aggregate files

`cooling_access` เป็น context field ที่มีประโยชน์ต่อ equity analysis แต่ต้องระบุว่าเป็น mock/future local data เช่นเดียวกัน ไม่ควรทำให้ผู้ใช้เข้าใจว่าเป็นค่าที่คำนวณจาก Lancet

หลักฐานในไทยสนับสนุนการคงกลุ่มเหล่านี้ไว้: งาน surveillance ประเทศไทยปี 2018-2023 รายงาน 139 heat-related deaths, median age 53 ปี, กลุ่มอายุ 51-60 และ 60+ มีจำนวนสูง, outdoor occupation มีความสัมพันธ์กับสถานที่เสียชีวิต และพบโรคประจำตัว เช่น diabetes และ cardiovascular disease ในบางกรณี อย่างไรก็ตาม ผลนี้ใช้เพื่อ local context และการตั้งคำถามเชิง workflow ไม่ควรใช้ calibrate clinical risk score ของ prototype โดยตรง

## 4. Proposed retrospective dashboard data model

### 4.1 Evidence-backed fields

| Field | Type/unit | Source-aligned meaning |
|---|---|---|
| `indicator_id` | Enum | 1.1.1 vulnerable, 1.1.1 attributable, 1.1.2, 1.1.3 PWHL, 1.1.3 workers, 1.1.4, 1.1.5 |
| `geography_level` | Enum | Global, WHO region, Lancet region, country, or HDI group according to source sheet |
| `geography_name` | String | Country or aggregate group name |
| `year` | Integer | Historical observation year; do not label as current or forecast |
| `metric_name` | String | Exact workbook column name |
| `metric_value` | Number | Value in the unit defined by the workbook |
| `unit` | Enum/String | Days, person-days, hours, percent, or deaths |
| `source_file` | String | Exact raw filename |
| `source_sheet` | String | Exact worksheet name |
| `source_row_or_range` | String | Row/range or data-guidance row used for traceability |
| `data_status` | Enum | Observed estimate, model estimate, aggregated estimate, missing, or not applicable |

### 4.2 Mock or future-context fields

These fields may appear in a mock scenario to demonstrate the future workflow, but they must be visually and technically separated from Lancet evidence:

| Field | Status | Use |
|---|---|---|
| `mock_case_id` | Mock only | Demonstration identifier; never a real patient ID |
| `age_group` | Mock/future local | Connect a scenario to infant or older-adult context without identifying a person |
| `chronic_condition_group` | Mock/future local | Broad category only; no full EHR or diagnosis inference |
| `living_alone` | Mock/future local | Social vulnerability context for future outreach planning |
| `cooling_access` | Mock/future local | Equity context; do not infer from temperature data |
| `occupation_group` | Mock/future local | Agriculture, construction, outdoor, indoor or unknown |
| `operational_signal` | Derived display | Informational priority for review; not a clinical risk score |
| `task_status` | Workflow state | Draft, assigned, acknowledged, completed or escalated |

### 4.3 Fields to remove from the MVP

Remove or defer `mortality_risk_indicator`, `climate_attributable_risk_score`, `vector_borne_disease_suitability`, `forecast_heat_index`, `patient_id` and `reported_symptoms` from the retrospective core. They either imply individual clinical prediction, are not present in the selected Lancet files, or belong to the future live/handoff layer. If a mock case needs symptoms, keep them in a clearly labelled scenario fixture outside the analytical dataset.

## 5. Evidence-to-workflow implications

### 5.1 Retrospective analysis flow for the course prototype

1. User selects indicator, geography and historical year range.
2. Dashboard displays the raw metric, unit, trend, source and data timestamp/coverage.
3. User compares vulnerable-population, worker and outcome views without merging them into one clinical score.
4. User records an interpretation note such as “rising population-level signal” or “insufficient data”.
5. User may create a mock `high-priority operational signal` to demonstrate the future handoff.
6. The signal opens a task stub to one of the five supporting components with contact point, information passed, owner, channel and acknowledgement state.

### 5.2 Future live-dashboard extension

When current/realtime data are added in a later phase, the dashboard can extend the same structure with refresh time, data-quality status, local thresholds and an approved task rule. The future Red alert should trigger coordination, not automated treatment:

`validated heat signal` -> `human review` -> `operational task` -> `contact point / supporting component` -> `acknowledgement` -> `fallback or escalation` -> `post-event review`

The emergency referral example in the earlier draft should be treated as an escalation caveat, not a rule invented by the software. Any 1669 or local emergency pathway must be verified against the responsible Thai health/emergency authority before implementation.

## 6. Safety, privacy and equity boundaries

- Use historical aggregate Lancet data and synthetic mock cases only in the course prototype.
- Do not upload real names, national IDs, addresses, phone numbers, full medical records or identifiable household information.
- Keep aggregate evidence separate from mock/future local fields in the schema, UI and documentation.
- Show missing, uncertain and not-applicable states explicitly. A blank value is not the same as zero in the Lancet files.
- Do not use country-average estimates to make claims about a province, facility or individual without local validation.
- Do not label any derived display as a medical risk score, diagnosis, treatment recommendation or automatic referral decision.
- Make the dashboard understandable to users with different levels of data literacy by showing source, unit, period, geography and caveat beside each metric.
- Treat worker, older-adult, chronic-disease and living-alone contexts as equity-sensitive. The dashboard should support outreach planning, not stigmatize a population or rank people as less valuable.

## 7. Evidence, assumptions and recommendations

### Evidence

- `E1`: Lancet 2025 reports record-high heatwave exposure for infants and older adults in 2024 relative to the 1986-2005 baseline.
- `E2`: Lancet 2025 reports 640 billion potential labour hours lost in 2024 and 1.5 billion outdoor workers, but these are different indicators and must not be conflated.
- `E3`: Lancet 2025 reports 1,609 hours per person of at least moderate heat-stress risk during light outdoor exercise in 2024.
- `E4`: Lancet 2025 reports 9% sleep-loss increase in 2024 relative to the 1986-2005 baseline and 546,000 average annual heat-related deaths in 2012-2021.
- `E5`: Thai surveillance and Thailand temperature-mortality sources show local relevance for older adults, outdoor workers, chronic disease context and cross-sector heat-health warning.
- `E6`: The Bangkok study links self-reported heat stress with socioeconomic and urban-environment conditions, supporting an equity and geography lens rather than a patient-only lens.
- `E7`: Emergency-nursing and nurse-emergency-response sources support human review, clear communication, training and escalation boundaries when information is incomplete or time is limited.

### Assumptions for the prototype

- `A1`: The team will use historical aggregate data as the analytical base and mock data only to demonstrate future handoff.
- `A2`: The primary user is a healthcare/public-health professional who needs evidence provenance and trend comparison.
- `A3`: `operational_signal` and `task_status` are workflow states created by the user or prototype rule, not clinical predictions.
- `A4`: Chronic disease, living alone and cooling access will be shown as future/mock context until an approved local aggregate source is identified.
- `A5`: Any threshold or Red alert rule used in the demo is illustrative and must be labelled as such.

### Recommendations for the team matrix

1. Make the retrospective trend view the MVP acceptance criterion; defer live ingestion and real-time alerts.
2. Use exact Lancet column names in the data dictionary and keep `source_file`, `source_sheet`, `metric`, `unit` and `coverage_years` in every processed record.
3. Build the first matrix around five locked population contexts: infants, older adults, outdoor workers, chronic disease mock context and living-alone mock context.
4. Do not create an overall risk score. Use separate indicator trends and a user-created operational signal.
5. Keep the five supporting components at contact-point/handoff level: who receives the signal, what information is passed, which channel is used, who acknowledges, and what fallback exists.
6. Add a Phase 0 check for source licensing, data provenance, local validation, user interpretation, accessibility and whether the task handoff can be completed without exposing identifiable data.

## 8. Reference table and traceability

The raw files remain in `00_raw_materials/01_Mod/`. The table below distinguishes authoritative data/evidence from summary documents and records the locator needed for later matrix work.

| Ref | Source file | Type | Traceability locator | Use in this project |
|---|---|---|---|---|
| L01 | `Indicator-1.1.1_Vulnerable_Data-Download_2025-Lancet-Countdown-Report-1.xlsx` | Lancet Countdown 2025 data | `DATA GUIDANCE` rows 4, 8, 10-11, 26-31; global/country sheets | Infants and older-adult heatwave exposure |
| L02 | `Indicator-1.1.1_Attributable_Data-Download_2025-Lancet-Countdown-Report-1.xlsx` | Lancet Countdown 2025 data | `DATA GUIDANCE` rows 4, 8, 10-11, 26-28; country/global sheets | Observed, counterfactual and attributable heatwave days |
| L03 | `Indicator-1.1.2_Data-Download_2025-Lancet-Countdown-Report-1.xlsx` | Lancet Countdown 2025 data | `DATA GUIDANCE` rows 4, 8, 10-12, 27-36; country/global/WHO/LC/HDI sheets | Activity-related heat-stress hours |
| L04 | `Indicator-1.1.3_PWHL_Data-Download_2025-Lancet-Countdown-Report_v2-1.xlsx` | Lancet Countdown 2025 data | `DATA GUIDANCE` rows 4, 8, 10-12, 26-42; sector and regional sheets | Potential work hours lost and sector context |
| L05 | `Indicator-1.1.3_Workers_Data-Download_2025-Lancet-Countdown-Report.xlsx` | Lancet Countdown 2025 data | `DATA GUIDANCE` rows 4, 8, 10-12, 26-27; country/global/WHO/LC/HDI sheets | Outdoor-worker population context |
| L06 | `Indicator-1.1.4_Data-Download_2025-Lancet-Countdown-Report-1.xlsx` | Lancet Countdown 2025 data | `DATA GUIDANCE` rows 4, 8, 10-12, 21-22; global sheet | Sleep-loss trend; global contextual indicator |
| L07 | `Indicator-1.1.5_Data-Download_2025-Lancet-Countdown-Report-1.xlsx` | Lancet Countdown 2025 data | `DATA GUIDANCE` rows 4, 8, 10-12, 25-26; global/WHO/LC/HDI sheets | Population-level heat-related mortality outcome |
| L08 | `Indicator-1.2.5_Data-Download_2025-Lancet-Countdown-Report-1.xlsx` | Lancet Countdown 2025 data | `DATA GUIDANCE` rows 4, 8, 10-12, 21-22; global sheet | Optional online-sentiment context only |
| E01 | `Health and heat.pdf` | Lancet 2021 Heat and Health Series paper | Abstract and sections on vulnerable populations, workers, urban heat and prevention; Lancet 398:698-708 | Global health problem framing and prevention rationale |
| E02 | `08_Duangnate+copy.pdf` | Thai original research, 2025 | Abstract, results and discussion; DOI `10.14456/dcj.2025.54` | Thailand surveillance context, occupations, age and chronic disease signals |
| E03 | `1-s2.0-S0013935120302917-main.pdf` | Environmental Research original research, 2020 | Abstract and results; Bangkok survey of 505 respondents; DOI `10.1016/j.envres.2020.109398` | Urban heat, socioeconomic context and equity lens |
| E04 | `1.-Heat-and-health-in-Thailand-17-12-61.pdf` | Thailand Ministry of Public Health presentation | Methods and recommendations; 20 provinces, 2009-2015 | Thailand temperature-mortality context and cross-sector warning rationale |
| E05 | `Boundaries.pdf` | Integrative review of emergency nursing, 2025 | Abstract and discussion; DOI `10.2174/0118744346378311250320070725` | Human review, incomplete information, communication and safety boundary |
| E06 | `fpubh-13-1612790.pdf` | Frontiers in Public Health original research, 2025 | Abstract, methods and discussion; DOI `10.3389/fpubh.2025.1612790` | Training, readiness and adoption considerations for health personnel |
| S01 | `Untitled document.pdf` | Project/Lancet summary document | Sections 1.1.1-1.2.5 | Navigation aid only; verify every claim against L01-L08 |
| S02 | `Heat and health.pdf` | One-page project summary | Sections 1.1.1-1.2.5 | Scope orientation only; not an independent data source |

Lancet data files state a CC BY-NC-SA 4.0 licence and require attribution; the team should confirm the licence conditions and preserve source attribution before redistributing transformed data or publishing a prototype. The suggested citation in the data guidance is: Romanello M, Walawender M, Hsu S-C, et al. *The 2025 report of the Lancet Countdown on health and climate change*. Lancet 2025; published online Oct 29. DOI: `10.1016/S0140-6736(25)01919-1`.

---

เอกสารนี้เป็น research and prototype guidance ไม่ใช่ clinical protocol การใช้ข้อมูลจริงในระบบ live ต้องผ่านการอนุมัติจากผู้รับผิดชอบด้านสาธารณสุข ความปลอดภัยข้อมูล การคุ้มครองข้อมูลส่วนบุคคล และผู้มีอำนาจทางคลินิกในพื้นที่ก่อนเสมอ
