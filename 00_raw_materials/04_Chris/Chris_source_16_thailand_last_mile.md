# Chris Source 16 — Thailand's Last Mile: Village Health Volunteers and Digital Exclusion

**Focus applied to this summary:** stakeholders, communication logistics, contact points, channels, handoffs, ownership, acknowledgement, fallback mechanisms, adoption, satisfaction and service usefulness. Contact-point level only.

## Citations

**(a)** Krassanairawiwong, T., Suvannit, C., Pongpirul, K. & Tungsanga, K. (2021). Roles of subdistrict health office personnel and village health volunteers in Thailand during the COVID-19 pandemic. *BMJ Case Reports*, 14(9), e244765. DOI: https://doi.org/10.1136/bcr-2021-244765 — **Source ID:** CS-92 · Full text: PARTIAL · **Independently re-verified:** **FAIL on the figures originally recorded — see correction below.**

**(b)** Khanthavudh, C., Grealish, A., Tzouvara, V. & Leamy, M. (2025). Supporting healthcare in rural communities in Thailand: an exploratory qualitative study to understand the role and current mental health practices of village health volunteers. *PLOS ONE*, 20(4), e0320559. DOI: https://doi.org/10.1371/journal.pone.0320559 — **Source ID:** CS-102 · Full text: YES.

**(c)** National Statistical Office of Thailand (2026). *การมีการใช้ไอซีทีของผู้สูงอายุ พ.ศ. 2568* [ICT Usage Among Elderly Persons, 2025]. Bangkok: Ministry of Digital Economy and Society. **In Thai.** https://www.nso.go.th/nsoweb/storage/survey_detail/2026/20260727143041_96531.pdf — **Source ID:** CS-93 · Full text: PARTIAL (key-findings summary) · **Independently re-verified:** PASS on all four figures.

**(d)** Robru, K., Setthasuravich, P., Pukdeewut, A. & Wetchakama, S. (2024). Internet use for health-related purposes among older people in Thailand: an analysis of nationwide cross-sectional data. *Informatics*, 11(3), 55. DOI: https://doi.org/10.3390/informatics11030055 — **Source ID:** CS-100 · Full text: YES · **Independently re-verified:** PASS.

> **Verification correction, applied throughout the Chris deliverables.** The figures "1,039,729 VHVs" and "23.7 million households" are **not present** in CS-92. The paper states: **">1 million village health volunteers (VHVs) are responsible for primary healthcare of 23 million households in 75 032 villages."** The precise figure 1,039,729 appears to originate in Kaweenuttayanon et al. (2021), *Bulletin of the World Health Organization* 99(5):393–397, DOI 10.2471/BLT.20.274308 — metadata confirmed, but the full text could not be opened, so **the precise number is not used anywhere in these deliverables.**

## Research context

Thailand-specific evidence on the two questions that determine whether HeatShield can reach vulnerable Thais at all: is there a human last-mile network, and can a digital channel substitute for it?

## Stakeholders

อสม. / Village Health Volunteers (VHVs); sub-district (tambon) health office personnel; nurses; caregivers; older Thai adults; the Ministry of Public Health.

## Contact points

VHV-to-household is the defining Thai last-mile contact point: home visits, liaison with the health system, direct instruction. CS-92 documents this operating at national scale.

## Information transferred

Health instruction, risk identification and referral. During COVID-19, VHVs conducted **3.9 million household visits in March 2020 and 12.6 million between late March and April 2020**, gave hygiene instruction to over **7.4 million residents**, identified **834,000 high-risk individuals** by April 2020, and recorded **799,894** people complying with 14-day home quarantine.

## Channels

Face-to-face household visit, supported by the Smart อสม. mobile application. **This is a channel that requires no household smartphone and no household internet connection** — which the exclusion data below shows is decisive.

## Handoffs and ownership

VHVs sit between the sub-district health office and the household. The ownership question HeatShield must answer is *which* อสม. — see the capability finding below.

## Acknowledgement or escalation

Not documented for heat. VHV activity reporting exists for other programmes; whether it could carry heat acknowledgement is untested.

## Failure points — the อสม. channel is not free to use

CS-102 is the single most important adoption-risk finding for this channel:

1. **Volunteers deliver only what they are trained on, and heat is not in the curriculum.** Verbatim: *"training has been about hypertension, diabetes, elderly care…Mental health has not been part of my training."*
2. **Workload is already described as overwhelming**, spanning elderly care, disability support and wound care. Adding a heat task without removing something else is an adoption risk that must be designed for, not assumed away.
3. **Capability is unevenly distributed between VHV leaders and general VHVs.** General VHVs self-limit ("we're not doctors"); advanced tasks are reserved for VHV leaders. A "train the อสม." plan must therefore specify *which* อสม.

## Digital exclusion — testing "everyone has a smartphone"

**CS-93 (official national statistics, 2025 data), among Thais aged 60+ (~14.6 million people):**

| Measure | Overall | 60–64 | 65–69 | 70–79 | **80+** |
|---|---|---|---|---|---|
| Internet use | **69.8%** (10.2 m) | 87.8% | 78.8% | 57.2% | **29.3%** |
| Mobile phone ownership | **77.8%** (11.4 m) | 91.4% | 86.8% | 70.2% | **36.1%** |

So **~30.2% of Thai over-60s (≈4.4 million people) do not use the internet at all**, and **among the over-80s, 70.7% do not use the internet and 63.9% do not own a phone.** Regionally, older-adult internet use runs from **Bangkok 85.8%** down to **North 63.4%** — a 22.4-point gap; ownership from Bangkok 91.0% to Northeast 70.7%.

**CS-100 goes further: connectivity is not the same as being reachable by a health message.** Of 4,652 Thais aged 60+, **only ~10.83% used the internet for health-related purposes** — in a year when NSO recorded 52.4% of over-60s using the internet at all. Urban 7.03% versus rural 4.35% (p<0.001).

## Adoption or satisfaction findings

No study located measures Thai satisfaction with, or adoption of, any heat warning product. The COVID-19 mobilisation in CS-92 shows the VHV network *can* achieve population-scale behavioural contact within weeks when mobilised by the Ministry of Public Health — but it is a descriptive case report with no counterfactual, so it demonstrates reach, not effectiveness.

## Relevance to this project

1. **A Thai heat service cannot be digital-first for the population most likely to die of heat.** The over-80 figures alone settle it.
2. **The อสม. network is the best-evidenced Thai last-mile channel** and should be treated as a primary channel in the prototype's channel strategy, not a courtesy fallback.
3. **But the อสม. channel carries a training and workload dependency** that must appear explicitly in the risk register and the roadmap.
4. **National connectivity averages must never be used** to justify a channel decision for older adults. See the aggregate-versus-subgroup contradiction in `Chris_literature_review.md`.

## Limitations

CS-92 is a descriptive case report, not an effectiveness trial, with no counterfactual, self-reported programme data, and COVID-specific content. CS-102 is a small qualitative study (19 interviews) in one sub-district of Lampang province, and is **about mental health rather than heat** — the training and workload findings transfer as mechanism, not as measurement. CS-93 is a self-reported household survey, and "internet use" does not equal reliable connectivity, affordability, or the ability to act on a push alert; the summary carries no disability or literacy breakdown. CS-100 is a secondary analysis of an online-skewed behaviour survey, so the true population rate is likely *lower* still; its percentages are of the whole sample, not of internet users, and must be quoted carefully.

**No Thailand-specific evidence was found that อสม. have ever delivered a heat warning.** This is the project's largest unevidenced local assumption and is recorded as such.

## Supported claims

1. More than 1 million village health volunteers are responsible for primary healthcare of 23 million households in 75,032 villages in Thailand.
2. Thai VHVs achieved population-scale behavioural contact during COVID-19, including 12.6 million household visits between late March and April 2020.
3. Thai VHVs deliver what they have been trained on; heat is not currently in their training curriculum.
4. Thai VHVs describe their existing workload as overwhelming, and capability is unevenly distributed between VHV leaders and general VHVs.
5. Among Thais aged 60+, 69.8% use the internet and 77.8% own a mobile phone; among the over-80s these fall to 29.3% and 36.1%.
6. Older-adult internet use ranges from 85.8% in Bangkok to 63.4% in the North.
7. Only about 10.83% of Thai older adults use the internet for health-related purposes.
8. No study located in this review documents อสม. delivering heat warnings, or measures Thai satisfaction with any heat warning product.
