# Chris Contact-Point / Handoff / Channel Matrix

**Project:** HeatShield — Heat Risk Dashboard Roadmap Initiative
**Research stream:** Stakeholders, Communication Logistics, Adoption, and CSAT-Style Evaluation
**Date:** 20 August 2026

---

## How to read this matrix

- **Every interaction is at contact-point level.** No internal organisational procedure is specified.
- **"To be defined and tested"** appears wherever no source provides a response-time standard. **No source located in this review specifies an acceptable response or acknowledgement window for a heat alert.** These are prototype test parameters, not evidence-derived requirements, and inventing them would misrepresent the literature.
- **Evidence column** cites canonical source IDs from `Chris_source_inventory.md`.
- **Channel recommendations are evidence-informed prototype proposals**, not final vendor or operational decisions. See `Chris_channel_strategy.md`.
- Rows marked **[TH]** are Thailand-specific. Rows marked **[analogy]** rest on evidence transferred from another domain or hazard, and the transfer is stated.

---

## A. Upstream and institutional interactions

| Interaction | Trigger | Sender | Receiver | Information transferred | Primary channel | Fallback channel | Acknowledgement | Handoff owner | Expected response time | Failure risk | Evidence |
|---|---|---|---|---|---|---|---|---|---|---|---|
| A1. Forecast/observation delivery | Scheduled ingestion cycle | Meteorological service (TMD) | HeatShield ingestion layer | Temperature, humidity, heat index, geography, timestamp, provenance | Data feed (API/file/bulletin) | Cached last-good value with a visible staleness flag; secondary public feed | Machine-level: successful fetch logged; staleness surfaced on the dashboard | Service operator | To be defined and tested | Silent staleness presented as current; spatial gaps; feed outage | CS-01, CS-96, CS-115 |
| A2. Threshold interpretation | Heat index crosses a published band | Meteorological service | Health authority | Band crossed; area; validity period; forecast confidence | Pre-agreed decision rule + inter-agency contact | Standing working group convened by call | Explicit activation decision recorded | Health authority (activator) | To be defined and tested | Ambiguity over who may authorise; discretionary delay; **contested Thai band definition** | CS-01, CS-03, CS-18, CS-96 vs CS-106 |
| A3. Alert authorisation | Activation decision taken | Health authority communications | Joint sign-off partner (met service) | Draft message; level; area; actions | Internal authoring + joint sign-off | Single-agency issuance with the omission recorded | Sign-off recorded against the alert ID | Named alert author | To be defined and tested | Sign-off bottleneck out of hours; undifferentiated message | CS-01, CS-19, CS-03 |
| A4. Inter-ministry coordination **[TH]** | Season start; and each activation | MoPH health authority | DDPM / MDES / NBTC (national alerting pipe) | Requested alert content; target area; language variants | Standing inter-agency contact | Escalation to the coordinating committee | Confirmation that the request was accepted | Named liaison on both sides | To be defined and tested | **Health owner and mass-alerting owner sit in different ministries** — the classic ambiguity seam | CS-108, CS-04 |

---

## B. Institutional-to-institutional cascade

| Interaction | Trigger | Sender | Receiver | Information transferred | Primary channel | Fallback channel | Acknowledgement | Handoff owner | Expected response time | Failure risk | Evidence |
|---|---|---|---|---|---|---|---|---|---|---|---|
| B1. Alert to health facilities | Alert issued | Health authority | Hospitals, health centres, sub-district health promoting hospitals | Level; area; validity; facility preparedness notice | Dashboard notification + email/SMS to a **registered role**, not a person | Telephone call to the facility duty line | **Required** — confirmation against the alert ID | Named facility duty holder | To be defined and tested | Alert routed to a role-holder who has moved on and disappears silently **[analogy]**; opt-in registry decay | CS-02, CS-19, CS-46 [analogy], CS-54 |
| B2. Alert to local government | Alert issued | Health authority | Municipal / district / sub-district administration | Level; area; expected local actions; onward cascade responsibility | Dashboard + email/SMS | Telephone; standing coordination meeting | **Required** | **Named** local onward-cascade owner | To be defined and tested | **Intermediate node with undefined onward responsibility** — the documented CCG-shaped gap | CS-18, CS-04, CS-02 |
| B3. Alert to emergency services | Alert issued at higher bands | Health authority | Emergency medical services; disaster management | Level; area; anticipated demand | Existing operational channel | Telephone | **Required** | Emergency service duty officer | To be defined and tested | Message formatted for media rather than operations | CS-01 (§5.3.1–5.3.2), CS-27 |
| B4. Alert to employers and schools | Alert issued | Health authority / local government | Employers of outdoor workers; schools | Level; area; work/schedule modification guidance | Email/SMS to registered contacts; sector association channels | Local government visit or call | Optional in prototype; **to be tested** | Employer safety officer; school head | To be defined and tested | No registry of outdoor-worker employers; informal workers have no employer to notify | CS-01 (Ch. 6), CS-99, CS-90 |
| B5. Preparedness notice to care facilities | Higher-band alert | Health authority | Care homes, elderly care providers | Level; resident-protection actions; escalation route | Dashboard + email/SMS | Telephone | **Required** | Facility manager | To be defined and tested | Front-line staff unaware the plan exists even when the facility was notified | CS-18, CS-02, CS-27 |

---

## C. Last-mile and public interactions

| Interaction | Trigger | Sender | Receiver | Information transferred | Primary channel | Fallback channel | Acknowledgement | Handoff owner | Expected response time | Failure risk | Evidence |
|---|---|---|---|---|---|---|---|---|---|---|---|
| C1. Public broadcast alert | Alert issued | Health authority / national alerting authority | General public in the area | Level; plain-language meaning; 1–3 specific actions; issuing authority | **Cell broadcast** (no registration, no app) **[TH: DDPM/NBTC pipe]** | Radio and television broadcast | **None technically possible** — one-way channel | Individual recipient | To be defined and tested | ~9% miss even under test conditions; older, rural and subsidised-phone users disproportionately missed; **Thai CBS supports no Burmese, Khmer or Lao** | CS-23, CS-108, CS-111 |
| C2. Media briefing | Alert issued | Health authority press function | Television, radio, press | Level; actions; interview availability | Press release + briefing | Direct call to newsroom | Coverage monitored, not acknowledged | Press officer | To be defined and tested | Message drift between media and official channels | CS-02, CS-05, CS-37 |
| C3. Community volunteer outreach **[TH]** | Higher-band alert | Sub-district health office | **อสม. / village health volunteers** | Level; priority household list; simple action script | Volunteer app / group message + verbal briefing | In-person briefing at the health office | **Required** — volunteer reports visits completed | Sub-district health office; **specified VHV tier** | To be defined and tested | **Heat is not in the อสม. training curriculum; workload already described as overwhelming; capability differs between VHV leaders and general VHVs** | CS-92, CS-102, CS-30 [analogy: cyclone] |
| C4. Volunteer-to-household visit **[TH]** | Volunteer tasked | อสม. | Priority household (older adult living alone, chronic illness, no AC) | Verbal warning; check on condition; practical help | **In-person visit** | Telephone call to household or family | **Required** — visit outcome recorded | อสม.; escalate to health centre | To be defined and tested | Volunteer capacity is finite; priority list may be absent or out of date | CS-27 (50% found during wellness checks), CS-92, CS-02 |
| C5. Public announcement | Higher-band alert | Local administration / village head | Village residents | Level; actions; where to go for help | **Loudspeaker / public address / community radio** | Door-to-door notification | None | Village head / local administration | To be defined and tested | **No Thailand-specific evidence located on loudspeaker reach or effectiveness**; the only comparable study found was from China | CS-30 (religious announcements 40–45%, Bangladesh), CS-05 |
| C6. Caregiver and family contact | Alert issued | Health service / volunteer / resident | Family caregiver | Level; what to check; when to escalate | Messaging app / SMS / call | In-person via volunteer | Optional | Caregiver | To be defined and tested | Caregiver not registered anywhere; caregiver also excluded digitally | CS-27, CS-02, CS-93 |
| C7. Dashboard consultation | User chooses to look | HeatShield | Health staff, local officials, informed public | Current and forecast status; area; timestamp and source; priority indicator; ownership and handoff status | **Dashboard (pull)** | Printed daily status sheet at the facility | Page view logged; not an acknowledgement | The viewer | Not applicable | **A pull channel reaches only those who visit; the evidence base for dashboards changing behaviour is essentially absent** | CS-36, CS-37 |

---

## D. Escalation, fallback and feedback interactions

| Interaction | Trigger | Sender | Receiver | Information transferred | Primary channel | Fallback channel | Acknowledgement | Handoff owner | Expected response time | Failure risk | Evidence |
|---|---|---|---|---|---|---|---|---|---|---|---|
| D1. Non-acknowledgement escalation | Acknowledgement window elapses | HeatShield / service operator | The non-acknowledging recipient | Restated alert; explicit request to confirm | Telephone call | In-person via local government or volunteer | **This interaction exists to obtain acknowledgement** | Service operator | **To be defined and tested — this is a core prototype test parameter** | Escalation is missed or delayed in 23–57% of cases even with an objective trigger **[analogy: clinical]**; no heat-specific rate exists | CS-43 [analogy], CS-14, CS-18 |
| D2. Channel-failure fallback | Primary channel unavailable | Service operator | All affected recipients | Same alert, same level, same actions | **Radio broadcast** (independent of grid power at the receiver) | In-person / loudspeaker | Not possible for broadcast | Service operator; named fallback owner | To be defined and tested | **A "fallback" that shares a failure mode is not a fallback** — cellular, wireline and broadband fail together from loss of power | CS-31, CS-14, CS-27 |
| D3. Clinical escalation | Suspected heat illness | Resident / caregiver / volunteer | Emergency medical services **[TH: 1669]** | Location; symptoms; person at risk | Telephone | In-person transport; nearest facility | Call logged by the service | EMS | Governed by emergency service standards — **out of scope for this project** | **Telephone escalation saturates at peak**: 911 volume doubled, ambulance dispatch fell to 74–80%, six callers told none available | CS-27, CS-107 |
| D4. In-event surveillance feedback | During the alert period | Facilities and surveillance systems | Health authority | Heat-illness presentations; service load | Existing surveillance reporting | Manual facility report | Report receipt confirmed | Surveillance team | To be defined and tested | Care sought outside emergency pathways is missed; **occupational exposure not systematically captured** | CS-02, CS-54 |
| D5. Post-event review | Season or event ends | Lead body | All participating stakeholders | What was sent, acknowledged, done; what failed; who owns each fix | Structured review meeting | Written return | Attendance and actions recorded | Lead body (evaluator) | To be defined and tested | **Review does not happen unless scheduled and owned** — no formal post-alert assessment occurred in a mandated national system unless a major incident was declared | CS-18, CS-01, CS-02 |
| D6. User feedback collection | After an alert, or at prototype test | HeatShield | Users and recipients | Usefulness, clarity, trust, timeliness, actionability, accessibility, satisfaction | Short survey (see `Chris_csat_adoption_evaluation.md`) | Structured interview; volunteer-assisted completion | Response counted | Evaluation lead | To be defined and tested | Survey reaches only the digitally included, biasing results toward the least excluded users | CS-87, CS-36, CS-13 |

---

## Summary of what the matrix shows

1. **Acknowledgement is required at every institutional contact point and technically impossible at the broadcast contact points.** This is not a defect to design around — it is why C1 must be paired with C3/C4, where confirmation is possible.
2. **Every "handoff owner" cell names a role, not a person.** This follows directly from the documented failure mode where alerts routed to an individual who has moved on disappear silently (CS-46, clinical analogy).
3. **Every fallback in column 7 was chosen for an independent failure mode**, not merely for being a different product. Cellular, wireline and broadband share a power dependency (CS-31).
4. **Every response-time cell is "to be defined and tested."** This is the honest position given the evidence, and it converts a gap into a prototype test plan.
5. **Four interactions have no supporting Thailand-specific evidence at all**: C3 and C4 (อสม. delivering heat warnings), C5 (loudspeaker reach), and D6 (Thai user satisfaction with a heat product). These are flagged in `Chris_literature_review.md` as evidence gaps and must not be presented to the team as locally validated.
