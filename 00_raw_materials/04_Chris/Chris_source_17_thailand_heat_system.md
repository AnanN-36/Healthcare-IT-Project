# Chris Source 17 — Thailand's Heat Index, Institutional Ownership and National Alert Pipe

**Focus applied to this summary:** stakeholders, communication logistics, contact points, channels, handoffs, ownership, acknowledgement, fallback mechanisms, adoption, satisfaction and service usefulness. Contact-point level only.

## Citations

**(a)** Paengkaew, W., Limsakul, A., Kokkaew, E., Sooktawee, S., Muangnim, P., Naban, O., Aroonchan, N., Patpai, A., Kitpakornsanti, K. & Kammuang, A. (2023). Development of a hot weather warning tool for heat index monitoring in Thailand. *Journal of Public Health and Development*, 21(3). DOI: https://doi.org/10.55131/jphd/2023/210301 — **Source ID:** CS-96 · Full text: PARTIAL.

**(b)** กรมอนามัย / Department of Health, Ministry of Public Health, Thailand (2024, 30 April B.E. 2567). *กรมอนามัย เผย ภาคเหนือร้อนสุดขีด พบเสียชีวิต Heat Stroke 1 ราย ป่วย 5 ราย* ["Department of Health: Northern Region Experiences Extreme Heat; One Heat Stroke Death, Five Cases"]. **In Thai.** https://anamai.moph.go.th/th/news-anamai/43635 — **Source ID:** CS-107 · Full text: YES · Grey literature: government press release.

**(c)** Thailand.go.th, Public Relations Department, Office of the Prime Minister (2024, 8 August). *Stay Alert, Stay Safe! "Cell Broadcast Service" — The Emergency Alert System Reducing Risks and Losses*. https://thailand.go.th/visit-thailand-detail/stay-alert-stay-safe-cell-broadcast-service---the-emergency-alert-system-reducing-risks-and-losses — **Source ID:** CS-108 · Full text: YES · Grey literature: government portal article, promotional in tone.

**(d)** กรมอนามัย / Department of Health, Ministry of Public Health, Thailand (2024). *กรมอนามัย เผย รายงานผู้เสียชีวิตจากความร้อน กว่า 38 ราย* ["Department of Health Reports Over 38 Heat-Related Deaths; Advises Public on Self-Care"]. **In Thai.** https://anamai.moph.go.th/th/news-anamai/43642 — **Source ID:** CS-106 · Full text: YES · Grey literature: government press release. *(Date rendered inconsistently on the page; cite the year only.)*

**(e)** Thawillarp, S., Thammawijaya, P., Praekunnatham, H. & Siriruttanapruk, S. (2015). Situation of heat-related illness in Thailand, and the proposing of heat warning system. *OSIR Journal*. https://he02.tci-thaijo.org/index.php/OSIR/article/view/263275 — **Source ID:** CS-90 · Full text: PARTIAL.

**(f)** Wen, B., Kliengchuay, W., Suwanmanee, S., Aung, H.W., Sahanavin, N., Siriratruengsuk, W., Kawichai, S., Tawatsupa, B., Xu, R., Li, S., Guo, Y. & Tantrakarnapa, K. (2024). Association of cause-specific hospital admissions with high and low temperatures in Thailand: a nationwide time series study. *The Lancet Regional Health – Western Pacific*, 46, 101058. DOI: https://doi.org/10.1016/j.lanwpc.2024.101058 — **Source ID:** CS-97 · Full text: NO (repository record) · **Independently re-verified:** PASS.

## Research context

The Thai institutional and technical context HeatShield must align to, plus the burden evidence that justifies the project locally.

## Stakeholders

Thai Meteorological Department (TMD); Department of Health (กรมอนามัย) and Department of Disease Control, Ministry of Public Health; Environmental Research and Training Center, Department of Environmental Quality Promotion; **Department of Disaster Prevention and Mitigation (DDPM), Ministry of Interior**; Ministry of Digital Economy and Society; NBTC; mobile operators; the general public and tourists.

## Contact points

- TMD/ERTC → heat index product → health agencies
- Department of Health → public, during an active event
- MDES/NBTC/DDPM + operators → every handset in a target area (Cell Broadcast Service)

## Information transferred

The Thai heat index and its alert band; at-risk group guidance; in the CBS case, five alert categories (National Alert, Emergency Alert, Missing Person Alert, Public Safety, Test Alert).

## Channels

**What the Department of Health actually used during an active heat emergency (CS-107, explicitly checked):** a **website** (http://www.rnd.tmd.go.th/heatindexanalysis/), **Facebook**, and **hotline 1669**. There was **no mention of อสม., LINE, village loudspeakers or a dedicated app.** This is an important corrective to any assumption about how Thai heat information currently flows.

**Cell Broadcast Service (CS-108)** requires **no pre-registration and no app**, reaching feature phones and non-app users — the only channel located that does so. It supports text, images, audio and text-to-speech for visually impaired users.

## Handoffs and ownership

Two ownership facts matter for the roadmap:

1. **The Thai heat index is an inter-agency product**, co-produced by the Environmental Research and Training Center with the Department of Health and the Department of Disease Control (CS-96).
2. **DDPM (Ministry of Interior), not MoPH, owns the national alerting pipe** (CS-108), with MDES and NBTC as lead agencies and the mobile operators as delivery partners. **HeatShield's health-side owner and its mass-alerting owner are in different ministries** — which is precisely the seam CS-04 warns becomes ambiguous.

## Acknowledgement or escalation

Escalation is carried by the heat index band. No acknowledgement mechanism is documented in any Thai source located.

## Failure points

**1. The heat-index banding is contested and unresolved.**

| Source | Bands | Top threshold |
|---|---|---|
| **CS-96** (peer-reviewed, co-authored with DoH and DDC) | **Five**: Normal <27 °C; Caution 27–<32; Extreme Caution 32–<41; Danger 41–<54; Extreme Danger ≥54 °C | **54 °C** |
| **CS-106** (Department of Health press release) | **Four**: Level 1 Green (Caution); Level 2 Yellow (Warning); Level 3 Orange (Danger); Level 4 Red (Extreme danger) | **>52 °C** |

The TMD heat index page could not resolve which is currently canonical. **HeatShield must pick one, state its source explicitly, and flag the discrepancy. This is a live design decision requiring human confirmation, not a citation problem.**

**2. A temperature-only dashboard would flag the wrong provinces.** CS-107 records maximum temperatures of 40–44 °C in the North and Northeast, peaking at **Phichit (Mueang) 44.1 °C** — while the **red-alert heat-index provinces were Phuket, Phang Nga, Krabi, Surat Thani, Trat, Chachoengsao and Chanthaburi**, on the humid coast. Humidity moves the risk geography.

**3. Language exclusion in the national alert pipe.** CBS supported languages are **Thai, English, Chinese, Japanese and Russian — not Burmese, Khmer or Lao.** Thailand's largest migrant worker populations are therefore outside the national alert system's language set. **No study located evaluates migrant heat-warning access**, so this exclusion is *inferable from the published language list*, not measured.

**4. Two irreconcilable official heat-death series.** The Department of Disease Control reports **139 deaths, 2018–2023** (M:F 7.2:1, median age 53); the Department of Health reports **"131 cumulative deaths" over 2019–2023, average 26.1 annually** (CS-107). Different agencies, overlapping windows, no published reconciliation. **Never quote a single authoritative Thai heat-death number without naming the agency and the period**, and note that both are likely substantial undercounts since heat is rarely coded as underlying cause.

## Adoption or satisfaction findings

None exist. **No Thai CSAT, adoption or usability study of any heat or disaster warning product was located.** Separately, a 2025 review of **53 Thai climate-health studies** found the literature dominated by dengue and **did not surface a Thai heat warning/response framework** — corroborating that this gap is real and documented rather than merely un-searched.

## Relevance to this project

1. **Consume the official Thai heat index; do not compute a new one.** HeatShield's role is interpretation and coordination, not meteorology.
2. **Align to Thai bands, not US NWS or European ones** — but resolve the four-versus-five band question with the team and a Thai authority first.
3. **The dashboard must be humidity-aware**, or it will prioritise the wrong provinces.
4. **Record the ministry split** (DDPM alerting versus MoPH health response) as a named coordination risk.
5. **Thai burden justifies the project:** CS-97 found **6.71% of 878,513,460 outpatient admissions across 77 provinces attributable to hot temperatures**, with greater burden in females and 0–19s — so Thai heat vulnerability is not confined to the elderly. CS-90 shows Thai heat-related illness concentrating in **skilled agricultural workers (35.7%)** and in the **Northern region (9.3/100,000)**, and records that a Thai heat warning system was formally *proposed* in the peer-reviewed literature as early as 2015. HeatShield addresses a documented, long-standing Thai gap.

## Limitations

CS-96 is an instrument-development and validation study, not an evaluation of dissemination or public response — it contains no data on whether anyone received or acted on a warning. CS-107 is a press release with provisional in-season figures at a single point in time. CS-108 is a government promotional article, **not an audited evaluation**; "expected completion early 2025" was forward-looking at publication and **the current operational status of Thai Cell Broadcast was not verified**; no delivery-rate or comprehension data exists. CS-90 uses data more than a decade old from passive surveillance, so under-ascertainment is likely, and its warning system is a *proposal* that the paper does not evaluate. CS-97 was accessed only as a repository record, so all its statistics are abstract-level.

## Supported claims

1. The peer-reviewed Thai heat index scale has five levels with an Extreme Danger threshold at ≥54 °C (CS-96); the Department of Health's public communication uses four levels with a red threshold above 52 °C (CS-106). The two are not reconciled.
2. The Thai heat index is an inter-agency product involving the Environmental Research and Training Center, the Department of Health and the Department of Disease Control.
3. During an active heat emergency the Department of Health named a website, Facebook and hotline 1669 as its channels, with no mention of อสม., LINE, loudspeakers or an app.
4. Peak Thai temperatures and red-alert heat-index provinces occur in different places: Phichit reached 44.1 °C while red-alert provinces were coastal and humid.
5. Thailand's national Cell Broadcast Service requires no pre-registration or app and supports Thai, English, Chinese, Japanese and Russian — not Burmese, Khmer or Lao.
6. DDPM, MDES and NBTC — not the Ministry of Public Health — are the lead agencies for the national alerting pipe.
7. Two Thai agencies publish different heat-death series (139 deaths 2018–2023 versus 131 deaths 2019–2023) with no published reconciliation.
8. 6.71% of 878,513,460 outpatient admissions across 77 Thai provinces were attributable to hot temperatures, with greater burden in females and those aged 0–19.
9. Thai heat-related illness concentrates in skilled agricultural workers (35.7% of cases) and in the Northern region (9.3 per 100,000).
10. A Thai heat warning system was formally proposed in the peer-reviewed literature in 2015, requiring MoPH–TMD collaboration.
