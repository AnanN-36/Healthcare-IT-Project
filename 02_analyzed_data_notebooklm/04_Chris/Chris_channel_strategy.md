# Chris Channel Strategy — Primary and Fallback Channels

**Project:** HeatShield — Heat Risk Dashboard Roadmap Initiative
**Research stream:** Stakeholders, Communication Logistics, Adoption, and CSAT-Style Evaluation
**Date:** 20 August 2026

---

> ## Status of this document
>
> **These are evidence-informed prototype recommendations. They are not final vendor selections, not procurement decisions, and not operational commitments.** Selecting a communications vendor is explicitly out of scope for this course phase. Every recommendation below states its evidence strength, and several rest on evidence transferred from another hazard or another country — where that is the case it is stated in the row.

---

## The design rule this strategy is built on

**A fallback channel must have an *independent failure mode*, not merely be a different product.**

This is the single most important channel finding in the evidence base, and it invalidates the most common "multi-channel" design. During Hurricane Helene, **21.7% of cell sites in the affected area were out of service — up from 9.1% the previous day** as backup power drained — with North Carolina at **48.7%**. The dominant causes were **loss of commercial power and backhaul, not physical damage** (North Carolina: 338 power, 303 transport, only 3 damage). At the same time **796,999 wireline and cable subscribers were out**. Meanwhile only **34 FM, 6 AM and 5 TV stations** went off air across six states (CS-31).

**Consequence: SMS + push notification + email + dashboard is a single channel wearing four costumes.** They share a grid-power dependency. Broadcast radio and a human being do not.

Hazard-transfer note: CS-31 is a hurricane. The failure *mechanism* — loss of commercial power to cell sites — is hazard-agnostic, and heat events co-occur with grid stress from air-conditioning demand, so the mechanism transfers even though the event does not.

---

## Channel-by-channel evidence summary

| Channel | Measured reach where available | Requires | Independent of grid power? | Populations excluded |
|---|---|---|---|---|
| Cell broadcast (WEA-type) | **91%** of US adults with working cell phones, under national-test conditions (CS-23) | A compatible handset in the area; no registration, no app | No | ~9% missed; older adults 23–52% lower odds; rural 22–49% lower odds; 17.5% opted out (189% higher odds on subsidised phones); **[TH] non-Thai/English/Chinese/Japanese/Russian speakers** (CS-108) |
| SMS to a registered list | Not measured for heat | Handset, current number in a maintained registry | No | Anyone not on the registry — and **opt-in registries select away from the at-risk**: 7.9% aged 65+, 6.6% outdoor workers, 2.4% agricultural (CS-54) |
| Email | Not measured for heat | Device, internet, email habit | No | Same as SMS, plus non-email users |
| Messaging app (incl. LINE) **[TH]** | **No credible Thai user statistic was located.** All candidates were marketing material and were excluded | Smartphone, app, data | No | Non-smartphone users; **only ~10.83% of Thai over-60s use the internet for health purposes** (CS-100) |
| Dashboard (pull) | Not measured | Device, internet, deliberate visit | No | Everyone who does not visit. **Only 18 of 65 dashboard studies included any user study** (CS-36) |
| Telephone call | — | Working line, someone available to answer | Partly | **Saturates at peak**: 911 volume doubled, ambulance dispatch fell to 74–80%, six callers told none available (CS-27) |
| Broadcast radio / TV | Mass media reached 30–67% in Bangladesh (CS-30, cyclone) | A receiver; **a battery radio needs no grid** | **Yes** | Those not listening at the time; language mismatch |
| Loudspeaker / public address | **No Thailand-specific evidence located.** Religious-institution announcements reached 40–45% in Bangladesh (CS-30, cyclone) | Being within earshot | Depends on local power | Hearing-impaired; those indoors with windows shut; those outside coverage |
| Trained human volunteer network | **>72% in every district, peaking at 90%** in Bangladesh (CS-30, cyclone) | A trained, resourced volunteer network | **Yes** | Households the volunteers do not reach; depends on volunteer capacity |
| In-person wellness check | **50% of heat decedents were found during wellness checks** (CS-27) | Staff or volunteer time; a priority list | **Yes** | Those not on the priority list |

---

## Recommended pairings

### P1 — Public mass alert

- **Primary channel:** Cell broadcast (in Thailand, the DDPM/NBTC national Cell Broadcast Service)
- **Fallback channel:** Broadcast radio and television
- **Why this combination is appropriate:** Cell broadcast is the only push channel located that requires **no registration and no app**, so it is immune to registry decay and reaches feature phones (CS-108). Its measured ceiling is 91% under ideal conditions (CS-23). Radio is the fallback because it is the only mass channel that survives grid failure at the receiver — a battery radio needs no power infrastructure — and broadcast degraded far less than cellular in the one event where both were measured (CS-31).
- **Population reached:** Anyone in the target area holding a compatible handset; plus radio listeners.
- **Population potentially excluded:** The ~9% who miss even a national test, skewed older, rural and poorer; the 17.5% who have opted out; **[TH] Burmese, Khmer and Lao speakers, whose languages the Thai CBS language set does not include** (CS-108, CS-111).
- **Accessibility considerations:** Message must be plain-language and short; colour tier must carry a text equivalent (CS-38); Thai CBS reportedly supports text-to-speech for visually impaired users (CS-108, unaudited).
- **Operational dependency:** Requires a working relationship with DDPM/NBTC and the mobile operators — an inter-ministry dependency HeatShield does not control.
- **Evidence strength:** **High** for the reach ceiling and the failure mechanism (CS-23, CS-31). **Moderate** for the Thai CBS specifics — CS-108 is a government portal article, promotional in tone, with **no audit, no delivery-rate data, and current operational status unverified**.

### P2 — Institutional alert to health facilities and local government

- **Primary channel:** Dashboard notification plus email/SMS **addressed to a registered role, not to a named individual**
- **Fallback channel:** Telephone call to the organisation's duty line
- **Why:** The dominant documented failure is not transmission but ownership. Alerts routed to an individual who has rotated away disappear silently (CS-46, clinical analogy), and an intermediate body with an undefined onward responsibility becomes a gap (CS-18). Role-addressing plus a call fallback attacks both. The lowest loop-closure failure rate observed anywhere was where notification was attached to the originating record (CS-45, clinical analogy).
- **Population reached:** Registered institutional recipients.
- **Population potentially excluded:** Any facility not registered; front-line staff inside registered facilities who never see the cascade — **the documented failure in England, where nurses were unaware of any local heatwave plan** (CS-18).
- **Accessibility considerations:** Institutional; standard workplace accessibility applies.
- **Operational dependency:** A maintained contact registry with a named review cycle. Registry decay is the silent killer here, and **no source located quantifies contact-registry decay rates** — an evidence gap.
- **Evidence strength:** **Moderate.** The failure modes are well evidenced but the corrective evidence is clinical and transferred by analogy.

### P3 — Reaching isolated and digitally excluded older adults **[TH priority]**

- **Primary channel:** **Community health volunteer (อสม.) in-person contact**, tasked from the sub-district health office
- **Fallback channel:** Telephone call to the household or a registered family member
- **Why:** This is the pairing the Thai data forces. **Among Thais aged 80+, 70.7% do not use the internet and 63.9% do not own a phone** (CS-93), and only ~10.83% of Thai over-60s use the internet for health purposes at all (CS-100). In the only setting where per-channel reach was measured, trained volunteers reached **>72–90%** while digital channels reached **17–40%** (CS-30). And in the closest analogue to a heat event with complete outcome data, **50% of decedents were found during wellness checks**, with 56% living alone and 98% dying indoors (CS-27). A person is not a courtesy fallback here — **it is the primary channel**.
- **Population reached:** Households on a priority visit list within volunteer coverage.
- **Population potentially excluded:** Households not on the list; areas with thin volunteer coverage; **migrant workers, who may be outside the อสม. relationship entirely**.
- **Accessibility considerations:** In-person contact is the most accessible channel for low-literacy, low-vision, hearing-impaired and cognitively impaired recipients — and the only one that can verify a person's actual condition.
- **Operational dependency:** **This is the largest dependency in the whole strategy.** The อสม. network is large (>1 million volunteers, 23 million households, 75,032 villages — CS-92), but **heat is not in their training curriculum, their workload is already described as overwhelming, and capability differs between VHV leaders and general VHVs** (CS-102). A "train the อสม." assumption is not free and must be costed and specified in the roadmap.
- **Evidence strength:** **Moderate.** The Thai exclusion data is High (official national statistics). The volunteer-reach evidence is High but from **cyclone warning in Bangladesh**, not heat in Thailand. **No source located documents อสม. ever delivering a heat warning** — this is the project's largest unevidenced local assumption and must be presented as such.

### P4 — Reaching outdoor and informal workers **[TH priority]**

- **Primary channel:** Employer or worksite notification where an employer exists; **cell broadcast** where one does not
- **Fallback channel:** Worker-organisation networks and community intermediaries
- **Why:** Thai heat mortality is dominated by working-age and older **men with outdoor occupational exposure** — the Department of Disease Control series shows a **male:female ratio of 7.2:1 with a median age of 53** — not the frail-elderly-indoors archetype (CS-89). Thai heat-related illness concentrates in skilled agricultural workers (**35.7%** of cases, CS-90). But **42% of Bangkok's workforce is informal** (CS-99), so an employer-based channel structurally misses a large fraction, leaving cell broadcast as the only universal route.
- **Population reached:** Formally employed outdoor workers; plus any worker in the broadcast area.
- **Population potentially excluded:** Informal workers with no employer; migrant workers facing language and documentation barriers (CS-110, CS-111).
- **Accessibility considerations:** Message must be in the worker's language — which for Burmese, Khmer and Lao speakers the national alert system does not currently provide.
- **Operational dependency:** No registry of outdoor-worker employers was located.
- **Evidence strength:** **Moderate.** The burden shape is well evidenced. The channel recommendation is inference from the burden data plus the exclusion data, and **no study located measures whether Thai outdoor or migrant workers receive heat warnings at all**. CS-99 is a non-random, organisation-linked sample and its 77–91% heat-illness figures must be presented as self-reported findings from a worker-organisation sample, not Bangkok prevalence.

### P5 — The dashboard itself

- **Primary role:** **Confirmation and coordination destination — not a delivery channel**
- **Paired with:** A push channel (P1 or P2), which does the reaching
- **Why:** A dashboard is a pull channel that reaches only those who choose to visit. The systematic review is unambiguous: only **18 of 65** dashboard studies included any user study, and "the benefits of dashboards for risk reduction or risk behavior change will remain without evidence" absent user research (CS-36). What a dashboard *is* well suited to is the confirmation behaviour people exhibit before acting — they seek a second source (CS-37). **But that only works if the dashboard says exactly the same thing as the push message.** Where information conflicted at Three Mile Island, 83% of those who left cited the conflict as a reason (CS-37). Dashboard users themselves asked for notifications (CS-36).
- **Population reached:** Health staff, local officials, and the motivated informed public.
- **Population potentially excluded:** Everyone else — which is most of the at-risk population.
- **Accessibility considerations:** WCAG 2.2 (W3C Recommendation, 12 December 2024) requires a text equivalent for anything conveyed by colour — every heat tier needs a label such as "Level 3 of 4 — High" (CS-38). Small screens display complex tables poorly (CS-36).
- **Operational dependency:** Internet access, which excludes 2.2 billion people globally, skewed rural, older, poorer and female (CS-26).
- **Evidence strength:** **High** for "dashboards are under-evaluated as behaviour-change tools"; **Moderate** for the confirmation-destination role, which is inferred from general warning-response research rather than from dashboard studies.

---

## Cross-cutting requirements

**1. Message consistency across channels is not optional.** Multi-channel delivery improves understanding, belief and response **only if the messages agree** (CS-37). A common alert vocabulary — a fixed set of levels used identically on the dashboard, the broadcast, the volunteer's script and the loudspeaker announcement — is what makes multi-channel work. Ahmedabad used a four-level colour-coded vocabulary for exactly this purpose across billboards, radio and printed material (CS-05).

**2. Colour tiers need a text equivalent, and are not self-explanatory.** The evidence genuinely disagrees here. Colour coding "produced the greatest differentiation between low- and high-impact levels" for the public — yet participants misread "level 3" as mid-range rather than high, and the same coding acted in the *opposite* direction on emergency managers. Colour-number literacy "relies on prior familiarity with the cultural practice of using colours and numbers to calibrate abstract qualities like risk" (CS-64, CS-65). The design response that follows from the disagreement — not from either side alone — is: **use the official Thai tier, always render it as "Level N of 4 — [word]", and comprehension-test it with older and non-native speakers.**

**3. Pre-translate before the season.** Live translation is a documented failure mode: **83.9%** of translating agencies use machine translation (which produced "bird County" for "Eagle County"), certified interpreters take **5–10 minutes**, and "pre-translated templates remain underutilised despite proven effectiveness" (CS-34). For Thailand this means preparing Thai plus, at minimum, Burmese, Khmer and Lao variants — because the national alert pipe does not carry them.

**4. Both visual and audible modalities.** US ADA guidance requires emergency alerts in both visual and audible form (CS-32). *(The claim that WCAG Level AA is legally required was not verified from any legal source and is not asserted here.)*

**5. Do not present a single universal channel hierarchy.** The ranking of channels **reverses between settings**: cell broadcast reached 91% in the United States (CS-23) while digital channels were the *worst* performer at 17–40% in coastal Bangladesh (CS-30). Channel choice is a local empirical question, and for Thailand the necessary reach study **does not exist**.

---

## Open decisions requiring human confirmation

1. **Which Thai heat-index band structure to adopt** — the peer-reviewed five-level scale (top band ≥54 °C) or the Department of Health's four-level scale (red above 52 °C). The literature does not resolve this (CS-96 vs CS-106).
2. **Whether the อสม. channel can be used at all**, and if so which volunteer tier, with what training addition and what workload offset (CS-102).
3. **Whether Thai Cell Broadcast is currently operational**, and whether additional languages can be requested (CS-108 — status unverified).
4. **Who owns the inter-ministry liaison** between the health-side owner (MoPH) and the alerting-pipe owner (DDPM/MDES/NBTC).
5. **Acknowledgement windows for every institutional contact point** — no evidence-based standard exists; these must be set by the team and tested.
