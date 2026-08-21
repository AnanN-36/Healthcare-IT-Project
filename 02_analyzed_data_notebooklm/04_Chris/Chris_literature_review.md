# Chris Literature Review
## Stakeholders, Communication Logistics, Adoption, and CSAT-Style Evaluation

**Project:** HeatShield — Heat Risk Dashboard Roadmap Initiative
**Date:** 20 August 2026
**Citation convention:** inline canonical source IDs (`CS-nn`) traceable through `Chris_source_inventory.md` to the per-source summary files and the original source.

---

# Executive Summary

This review asked how heat-risk information moves through people, service touchpoints, channels and feedback loops. Nine findings hold up across the evidence.

**1. A heat service is a handoff between two owners, and the dashboard sits on the seam.** WMO and WHO define a heat–health warning system as a meteorological component owned by the national meteorological service and a societal-response component owned by health and social services (CS-01, p. vii). Threshold-setting is explicitly joint, because thresholds are "response-specific" (CS-01, p. xii). In Thailand this seam is also a **ministry boundary**: the health response sits with the Ministry of Public Health while the national alerting pipe is owned by DDPM, MDES and NBTC (CS-108).

**2. Ownership is defined against alert tiers and is ambiguous everywhere else.** The strongest empirical study of heat governance — 15 national plans and 68 interviews across nine countries — found roles "mainly defined and assigned in relation to the alert levels of the warning system, causing other role aspects and other roles to be vague and ambiguous", and that "the municipal level is rarely considered" despite carrying implementation (CS-04).

**3. Receipt, not transmission, is where systems break.** An independent evaluation of a mandated national heat plan found front-line nurses "unaware of any local heatwave plans" (CS-18). Even the most universal digital push channel misses about 9% under ideal test conditions, disproportionately older, rural and poorer users (CS-23). An opt-in heat alert service had a subscriber base of which only **7.9% were aged 65+, 6.6% worked outside and 2.4% in agriculture** (CS-54).

**4. Acknowledgement is required and almost never performed.** International guidance requires "feedback mechanisms in place to verify that warnings have been received" (CS-14). The same England evaluation found "few mechanisms… to monitor activities during and following a heatwave alert" (CS-18). **No source located in this review measures acknowledgement rates in public-health mass notification** — everything known about making acknowledgement work is transferred from clinical alerting by explicit analogy.

**5. A fallback that shares a failure mode is not a fallback.** During Hurricane Helene, 21.7% of cell sites were out — rising from 9.1% as backup power drained — with causes overwhelmingly power and backhaul rather than damage, while **796,999 wireline and cable subscribers were out simultaneously** and only 34 FM, 6 AM and 5 TV stations went off air (CS-31). SMS, push, email and a web dashboard are one channel wearing four costumes.

**6. Awareness saturates; action does not.** Sheridan found heat-warning awareness at 90% among adults 65+ but behaviour change at 46% (CS-13; n=908, response rate 5.4%). In New York City, 66% saw warnings, 43% believed indoor heat could make them ill, and 12% of those unable to keep their home cool went somewhere air-conditioned (CS-63). The binding constraints are **failure to personalise the risk** — "few respondents considered themselves either old or at risk" (CS-61) — and **feasibility**, with over a third citing energy costs as governing air-conditioner use (CS-13).

**7. The human channel outperforms the digital channel where connectivity is thin.** In the only setting where per-channel reach was measured, trained volunteers reached >72–90% of households while SMS and social media reached 17–40% (CS-30, cyclone). In the closest analogue to a heat event with complete outcome data, **50% of decedents were found during wellness checks**, 56% lived alone and 98% died indoors (CS-27).

**8. For Thailand, digital-first design excludes precisely the highest-risk group.** Among Thais aged 80+, **70.7% do not use the internet and 63.9% do not own a phone** (CS-93); only about **10.83%** of Thai over-60s use the internet for health purposes at all (CS-100). The national figure of 90.9% internet use (CS-95) is true and misleading simultaneously.

**9. A prototype evaluation can legitimately measure usability, clarity, trust and actionability — and must not claim health impact.** WHO instructs teams to match evaluation to maturity stage and "avoid embarking on premature assessments" (CS-87); the surveillance data needed for an outcome claim is incomplete, and occupational exposure "is not systematically captured" (CS-54).

**Implication for HeatShield.** The dashboard's defensible purpose is **coordination, interpretation and ownership visibility** — not delivery. Delivery belongs to a push channel and, for the highest-risk group in Thailand, to a person.

---

# Research Scope and Method

## Question

How does heat-risk information move between stakeholders, through which contact points and channels, with what handoffs, acknowledgement and fallback — and how should the usefulness of the resulting service be evaluated?

## Boundary

**In scope:** stakeholders; contact points; channels; handoffs and ownership; acknowledgement; escalation and fallback; response delays and coordination friction; adoption and satisfaction; trust, clarity, accessibility and usefulness; plain-language messaging; prototype evaluation measures.

**Out of scope:** detailed clinical, hospital, emergency or community-health workflow design; final vendor selection; clinical treatment recommendations; complete technical architecture; and any assumption that a digital channel reaches every vulnerable person.

## Method

Seven parallel evidence-gathering workstreams (stakeholders and governance; journey and contact points; channels and fallback; logistics and coordination risk; adoption and trust; evaluation instruments; Thailand and Southeast Asia), consolidated by a de-duplication and downgrade pass, then subjected to an adversarial verification pass over the 28 most load-bearing citations. Full search terms, platforms and inclusion decisions are in `Chris_research_log.md`.

## Source coverage

135 records were reduced to **117 canonical sources**: 99 included as core evidence, 15 downgraded to context only, 3 excluded. **Full text was not accessed for 20 sources**, and those claims are limited to what was visible. The adversarial pass returned **23 PASS, 4 PARTIAL and 1 FAIL**; all corrections are applied and itemised in `Chris_source_inventory.md`.

## Three limitations that shape everything below

1. **Publisher blocks skew the base toward open-access and government-hosted material.** PubMed/PMC, ScienceDirect, Europe PMC, WHO IRIS, Taylor & Francis, Wiley and others blocked retrieval. Named relevant sources that were consequently never opened are listed in `Chris_research_log.md` and are cited nowhere.
2. **The single largest gap is the full WHO Europe heat–health action plan guidance, second edition** (CS-03). Three workstreams independently hit HTTP 403 on every route; its sector briefs, message bank and evaluation framework are unverified.
3. **Very little heat-communication evidence is Thai.** A 2025 review of 53 Thai climate-health studies found the literature dominated by dengue and surfaced no Thai heat warning/response framework (CS-116). Where a claim rests on non-Thai evidence, this review says so.

## Separation of evidence, synthesis and recommendation

Throughout: statements citing a source ID are **evidence**; paragraphs beginning *Synthesis* are the reviewer's interpretation across sources; and anything in the "Implications for the Prototype" section is a **project recommendation**, not a finding.

---

# Stakeholder Ecosystem

## The published role taxonomy

Rather than invent stakeholder categories, this review adopts the seven roles derived empirically from 15 European national heat plans and 68 key informant interviews (CS-04): **author** (writes the plan), **activator** (triggers it), **coordinator** (holds the response together), **monitor** (watches conditions and effects), **informer** (communicates outward), **implementer** (delivers action), **evaluator** (assesses afterwards).

## Who holds which role

| Stakeholder | Typical role(s) | Information needs | Receives from | Hands off to | Evidence |
|---|---|---|---|---|---|
| National meteorological service (TH: **TMD**) | Monitor | Observations, forecasts | Own networks | Health authority | CS-01, CS-96, CS-115 |
| Health ministry / public-health authority (TH: **MoPH**, DoH, DDC) | Author, activator, informer | Threshold crossing, vulnerable-population context | Met service | Facilities, local government, media, public | CS-01, CS-02, CS-03, CS-96 |
| National alerting authority (TH: **DDPM / MDES / NBTC**) | Informer | Alert content, target area, languages | Health authority | The whole population | CS-108 |
| Local / municipal / sub-district government | Coordinator, implementer | Alert level, local actions, cascade duty | Health authority | Facilities, volunteers, residents | CS-04, CS-02, CS-18 |
| Healthcare facilities | Implementer | Preparedness notice, expected demand | Health authority | Staff, patients, caregivers | CS-02, CS-19 |
| Emergency medical services | Implementer | Anticipated demand | Health authority; public calls | Clinical response | CS-27, CS-01 |
| **Community health workers / volunteers (TH: อสม.)** | Implementer, informer | Priority household list, simple action script | Sub-district health office | Households; escalation upward | CS-05, CS-92, CS-102, CS-30 |
| Community and faith organisations | Informer, implementer | Alert level, culturally appropriate framing | Local government / health | Members | CS-34, CS-30, CS-61 |
| Caregivers and family | Implementer | What to check, when to escalate | Health service, volunteers, media | The at-risk person | CS-27, CS-02 |
| Residents / at-risk individuals | Implementer | Personalised risk, 1–3 feasible actions | All of the above | Themselves; others they check on | CS-13, CS-61, CS-63 |
| Employers (esp. outdoor work) | Implementer | Work modification guidance | Health authority, media | Workers | CS-01 (Ch. 6), CS-90, CS-99 |
| Schools | Implementer | Alert level, child-protection actions | Local government / health | Pupils, parents | CS-02, CS-05 |
| Media | Informer | Alert level, actions, spokesperson | Health authority | Public | CS-02, CS-05, CS-13 |
| Utilities and social services | Implementer | Demand and continuity risk | Coordinating group | Their own users | CS-02 |

**Agreement across sources.** The 2008 WHO Europe guidance provides the most complete published enumeration of the cascade — lead body → hospitals, care homes, GPs, pharmacies, local government, social services, retirement homes, schools, civil protection, transport, energy → media → public (CS-02) — and the Ahmedabad plan (CS-05), the India NDMA guidelines (CS-06) and current UKHSA operational guidance (CS-19) are all consistent with it. This is the most stable finding in the stakeholder literature.

## A genuine disagreement: who leads

WHO Europe in 2008 stated that "in most countries the lead agency is the health ministry or another health department" (CS-02). The 2026 second edition softens this: the lead body is "often, but not exclusively, a health authority" (CS-03). India's NDMA places heat plans with disaster management authorities (CS-06), and in Thailand **DDPM in the Ministry of Interior — not MoPH — owns the national alerting pipe** (CS-108).

*Synthesis:* this is doctrinal evolution plus real cross-country divergence, not a simple supersession. Presenting "health ministries lead heat plans" as settled would misrepresent both current WHO guidance and Thai institutional reality. HeatShield should describe a **named lead body with a named alerting partner**, and leave which ministry holds which to local confirmation.

## What the evidence does not tell us

- The 2026 WHO guidance requires that governance specify "clearly defined roles, responsibilities and accountability mechanisms" and financing (CS-03) — but the full 272-page volume was never opened, so its stakeholder matrices and sector briefs are unverified.
- **No memorandum of understanding or formal inter-agency agreement text was located** despite targeted searching. Do not claim that MoUs are standard practice in heat-health governance.
- **Who actually delivers community heat interventions is an open question.** The one abstract-only review of community heat adaptation does not name delivery agents (CS-11), leaving single-city evidence (CS-05) as the only source that does.

---

# Stakeholder Journey and Contact Points

The full stage-by-stage map, with owners, channels and failure risks, is in `Chris_stakeholder_journey.md`. This section states what the literature establishes about the shape of that journey.

**Issuance and dissemination are separate stages with different owners.** WMO/WHO structure them as distinct chapters — alert issuance in Chapter 4, dissemination in Chapter 5 (CS-01). Collapsing them, as a naive dashboard design would, hides a real handoff.

**A single named recipient works, and is the clearest published design.** Ahmedabad routed a daily seven-day forecast by e-mail to one named **AMC Nodal Officer**, who owned coordination and escalation; the Health Department owned overarching response coordination; and 64 urban health centres, 26 hospitals and over 1,000 community link workers formed the delivery layer (CS-05). India's NDMA guidelines likewise require nodal officers (CS-06). England's current system takes the opposite approach — joint UKHSA/Met Office issuance to an **opt-in registered** audience, with onward cascade explicitly delegated to local organisations (CS-19).

*Synthesis:* the named-recipient model concentrates accountability and is easier to instrument; the opt-in registered model scales but silently mis-selects its audience (CS-54). For a prototype, the named-recipient model is more testable.

**Channels must be pre-established, not improvised.** The Ahmedabad plan "required formal, pre-established communication channels among agencies, responders, providers, community groups and media, activated ahead of forecast high temperatures" (CS-05) — and the implementers' own stated improvement priorities were "improving formal communication channels" and clarifying agency roles *before* extreme heat events.

**Feedback cadence is wildly inconsistent in practice.** Post-event evaluation runs per-warning in some European countries and only after extreme years in others; and among eight Indian heat action plans, only three used surveillance to adjust measures (CS-21). A European survey found evaluation "was only mentioned in 7 of 18 countries" and surveillance "lacking in 44%" (CS-13/CS-53 group; specifically CS-51).

---

# Communication Channels

## What the measured evidence says

The comparative table in `Chris_channel_strategy.md` gives the full picture. Three measurements anchor it:

- **Cell broadcast reached 91%** of US adults with working cell phones under national-test conditions — the highest single-channel reach figure in this evidence base — but with a 23–52% age penalty, a 22–49% rural penalty, 17.5% opt-out, and **189% higher odds of opting out among subsidised-phone users** (CS-23).
- **Trained human volunteers reached >72–90%** of households in coastal Bangladesh while **SMS and social media reached only 17–40%** — the worst-performing channel measured — with mosque announcements at 40–45% and mass media at 30–67% (CS-30). *This is cyclone warning, not heat.*
- **Only 18 of 65 studies** in a systematic review of public health dashboards included any user study, and "the benefits of dashboards for risk reduction or risk behavior change will remain without evidence" without user research (CS-36).

## A genuine disagreement: is digital primary or last?

The ranking of channels **reverses between settings**. Cell broadcast is the best channel in the United States (CS-23) and digital is the worst in coastal Bangladesh (CS-30); Thai subgroup data sits closer to the Bangladesh end for older adults (CS-93, CS-100).

*Synthesis:* **there is no universal channel hierarchy.** Channel choice is a local empirical question, and for Thailand the necessary reach study does not exist. Any HeatShield channel claim must be labelled as transferred evidence until measured locally.

## What is not known

- **No per-channel reach study exists for heat, anywhere.**
- **No per-channel cost data was located.**
- **No direct evaluation of IVR or reverse-911 was located.**
- **No credible LINE user statistic for Thailand was obtainable** — all candidates were marketing material and were excluded. LINE's institutional use is verified (the Thai Department of Health lists it among official channels, CS-106) and one Thai academic study found gain framing outperformed loss framing for Thai seniors on LINE (CS-104, convenience sample, not heat-specific) — but **no penetration number should be cited.**

---

# Primary and Fallback Channels

**The design rule: a fallback must have an independent failure mode.** The Hurricane Helene data (CS-31) shows why. Cell sites, wireline and home broadband failed together, from a common cause (loss of commercial power), and the outage **worsened on day two** as batteries and generator fuel depleted — the shape that matters most for a multi-day heatwave. Broadcast radio and television degraded far less.

**Telephone fallback saturates at peak.** During the BC heat dome, 911 volume roughly doubled, 52% of calls on one day took more than five seconds to answer, ambulance dispatch fell to 74–80%, and in six instances callers were told no ambulance was available (CS-27). A telephone route is least available exactly when it is most needed.

**The independent layers are broadcast and people.** A battery radio needs no grid (CS-31). A volunteer visit needs no network at all — and in the BC event, **50% of decedents were found during wellness checks** (CS-27).

*Synthesis:* the correct pairing structure for HeatShield is **registration-free push (cell broadcast) → broadcast radio → human contact for priority households**, with the dashboard as a confirmation destination rather than a delivery route. Full pairings, exclusions and dependencies are set out in `Chris_channel_strategy.md`.

**Multi-channel only works if messages agree.** Delivery through multiple channels improves understanding, belief and response — conditional on consistency. Where information conflicted at Three Mile Island, 83% of those who evacuated cited the conflict as a reason (CS-37). Ahmedabad's four-level colour-coded vocabulary existed precisely to hold the message identical across billboards, radio and print (CS-05); the Common Alerting Protocol is the technical mechanism for the same goal (CS-17).

---

# Handoffs, Ownership, and Acknowledgement

## What guidance requires

International guidance requires that "functions, roles and responsibilities of each actor in the warning dissemination process [be] enforced through government policy", that systems "reach the entire population… through multiple communication channels", that **"feedback mechanisms [be] in place to verify that warnings have been received"**, and that **"backup systems and processes [be] in place in the event of failure"** (CS-14). The 2026 WHO guidance adds that plans should "establish a decision pathway for alerts, including who receives warning information, who confirms or authorizes activation, and how escalation and stand-down decisions are made" (CS-03).

## What practice delivers

The England evaluation found the cascade functional at the top and invisible at the bottom: front-line nurses "unaware of any local heatwave plans"; the role of an intermediate commissioning body "not clear"; planners applying a discretionary "wait and see" approach before escalating; weekend alerts degrading response; and — decisively — **"few mechanisms… to monitor activities during and following a heatwave alert"**, with no formal post-alert performance assessment unless a major incident was declared (CS-18).

**This pairing — CS-14 requires it, CS-18 documents its absence — is the strongest available warrant for building acknowledgement into HeatShield.** It should be stated exactly that way: a requirement that operating systems were not observed to meet, not a measured failure rate.

## A genuine disagreement: is the alert threshold set in the right place?

Ownership of the *decision* is only half the question; the other half is whether the trigger point matches the onset of harm, and here an operating national system and an academic post-event review disagree.

**The operating position:** England's system issued alerts against regionally defined thresholds — reported in the evaluation as **30 °C daytime and 15 °C overnight for at least two consecutive days** — across five levels, with levels 2–3 triggering protective action (CS-18); the current system uses four colour levels with defined meanings (CS-19).

**The challenge:** a post-event review of the 2022 English heatwaves states those regional thresholds were "higher than, and hence misaligned with, the point at which excess deaths start to occur – which is at around 25 °C" (CS-52, a policy brief and therefore non-peer-reviewed grey literature). The 2025 systematic review adds that fixed thresholds ignore individual-level risk factors (CS-10, CS-54), and the alternative model exists in practice — a health agency supplying health-derived thresholds to a weather agency (CS-08).

*Synthesis:* this is a substantive disagreement about system design, not a citation problem, and it bears directly on HeatShield. If a threshold is set where the *alert* is comfortable rather than where the *harm* begins, every downstream stage — cascade, acknowledgement, protective action — operates on a signal that has already arrived late. The project cannot resolve this from the literature. What it can do is **make the threshold a visible, sourced, changeable parameter rather than a hidden constant**, and record the disagreement for the team. This compounds with the contested Thai band structure (CS-96 vs CS-106): HeatShield faces both an unresolved band *count* and an unresolved question about whether published bands sit at the right temperature at all.

## What clinical alerting adds, by explicit analogy

**No source located in this review measures acknowledgement rates in public-health mass notification.** Targeted searching returned only vendor material, which was excluded. The following are therefore cited as analogy, never as heat performance:

- **Escalation fails even when an objective trigger is met**, in 22.8%, 24.6%, 30.2% and 57% of cases across published cohorts, with delayed escalation carrying an adjusted odds ratio for death of 1.79 (95% CI 1.43–2.27, p<0.001) (CS-43).
- **Loops fail to close on already-generated information**, from 6.8% to 62% for laboratory tests and 1.0% to 35.7% for radiology — and the **lowest failure rate occurred where notification was attached to the originating order** (CS-45).
- **Ownership diffuses between plausible owners**, and alerts routed to a role-holder who has rotated away are "missed or found by chance"; flat prioritisation produces "a poor signal-to-noise ratio" (CS-46).
- **Prescribed acknowledgement is not performed acknowledgement**: closed-loop communication was coupled to 3.6% of real utterances against 7.7% in simulation (p ≤ 0.001) (CS-47).
- **Structuring the transfer point works**: a structured handoff programme cut errors 24.5 → 18.8 per 100 admissions and preventable adverse events 4.7 → 3.3, "without a negative effect on workflow" (CS-44).

*Synthesis:* four design positions follow, each analogy-informed rather than heat-evidenced — **route to a role, tier by urgency, attach acknowledgement to the alert record, and instrument confirmation rather than mandating it.**

**No source provides an acceptable response or acknowledgement window for a heat alert.** Every timing field in `Chris_contact_point_matrix.md` is therefore marked *To be defined and tested* — which converts the gap into a Phase 0 test plan rather than an invented standard.

---

# Service-Logistics Risks

The full register is in `Chris_risks_and_barriers.md`, organised under eight headings with cause, affected stakeholder, consequence, mitigation, evidence and confidence. The highest-confidence risks are:

| Risk | Core evidence | Confidence |
|---|---|---|
| Roles defined only against alert tiers; municipal layer absent | CS-04 | High |
| Intermediate cascade node with no onward owner | CS-18 | High |
| Front-line receipt failure inside notified organisations | CS-18 | High |
| Fallback sharing a failure mode with the primary channel | CS-31 | High (mechanism) |
| Telephone escalation saturating at peak | CS-27 | High |
| Opt-in registration selecting away from the at-risk | CS-54 | Moderate |
| Awareness saturating while action does not | CS-13, CS-63 | High |
| No mechanism verifying receipt | CS-14 + CS-18 | High (as a pairing) |
| Post-event review not happening unless owned and scheduled | CS-18, CS-02 | High |
| Data-to-leadership latency of 5–10 days in a real heat event | CS-39 | Moderate |

**A note on one commonly assumed risk.** *Contact-registry decay* is a named mechanism (CS-46) but **no source located quantifies its rate**, so it is recorded at Low confidence and proposed as a Phase 0 measurement rather than asserted.

---

# Adoption and Satisfaction

## The awareness–action gap

The most-replicated finding in this literature is that **receiving a warning is not acting on one**. Sheridan: 90% aware, **46% acted**, among 908 adults aged 65+ (CS-13; response rate 5.4%, so self-selection risk is substantial). Madrigano: 66% aware → 43% believing indoor heat could make them ill → 12% *of the subgroup unable to keep their home cool* going somewhere air-conditioned (CS-63). Erens et al.: 51.0% of English adults aware of hot-weather health publicity, ~25% of at-risk adults changing behaviour (CS-28).

## A genuine disagreement: how big is the awareness base?

The figure "~90% aware" is widely repeated, but the **largest national survey in this evidence base found roughly half** — 51.0% of all adults and 63.9% of the 75+ group (CS-28) — and NYC found 66% (CS-63). These measure different constructs (recall of a specific warning versus awareness of general publicity versus encountering an alert) in different populations.

*Synthesis:* present the range **51–90% with the measurement differences stated.** The common claim that "awareness is saturated, so reach is not the problem" is **not supported** by the largest survey available. Reach and action are both problems.

## Why people do not act

1. **They do not personalise the risk.** "Few respondents considered themselves either old or at risk from the effects of heat, even though many had some form of relevant chronic illness" (CS-61, n=73, aged 72–94), replicated across 13 studies in five countries (CS-62) and 41 studies (CS-29). In NYC, general climate concern ran at 68% against personal indoor-heat risk belief at 43% (CS-63).
2. **The recommended action is not feasible.** Over a third cited energy costs as governing air-conditioner use (CS-13); 13% lacked working AC and 15% used it rarely (CS-63). In Bangladesh, action conversion averaged 52.1% and tracked **shelter quality** (CS-30) — the direct analogue being cooling-centre access.
3. **The referral layer is invisible.** Only 4–12% recalled cooling centres or hotlines and under 2% sought a cooler place (CS-13).
4. **The messenger is not trusted.** Many older respondents thought state intervention "unnecessary, intrusive and unlikely to be effective", and were "more positive about the value of appropriately disseminated advice and solutions by communities themselves" (CS-61). Among immigrant communities, fear of authorities suppresses response (CS-34).

## What predicts adoption

The meta-analysis matched to the target population — 41 studies, 11,574 participants, mean age 67.58 — gives **perceived usefulness r=0.607 (95% CI 0.543–0.665)**, **social influence r=0.551 (0.468–0.624)** and **perceived ease of use r=0.525 (0.462–0.583)**, all p<.001, with behavioural intention (CS-58).

*Synthesis:* two consequences. First, **usefulness must be measured before usability** — it is the stronger predictor in this group. Second, **social influence is nearly as strong as usefulness**, which independently converges with the trusted-messenger findings (CS-61, CS-34) and the volunteer-reach findings (CS-30) to support routing heat messages through people the recipient already trusts.

## Attrition

Voluntary digital services shed users continuously: one-month survival of **3.4%** for apps requiring active engagement versus **27.3%** for passive ones (CS-68), and "~71% disengage within 90 days" as reported within a review (CS-67), against the foundational distinction between dropout and non-usage attrition (CS-66).

*Caveat:* neither CS-68 nor CS-67 is a comparable service — CS-68 is a Taiwanese work-hours app with mean user age 33.8. Use these for **direction and order of magnitude only.** The transferable design implication is that **every action the service requires is a point of attrition**, which argues for passive channels for the highest-risk group.

## A genuine disagreement: does alert fatigue exist?

Three positions do not reconcile:

- **Against.** The best-powered direct public test (N=4,162) found perceived false-alarm ratios were uncorrelated with actual county false-alarm ratios and that **higher perceived false-alarm ratios were associated with *more* protective action**; actual false-alarm ratios did not predict action at all (CS-49). A federal synthesis of over 200 studies lists "the 'cry wolf' syndrome" among **myths** about public warning response (CS-60).
- **For.** Modelling treats repeated false alarms as eroding collective trust, strongest for infrequent hazards (CS-50); an editorial warns of "public desensitization" (CS-12, downgraded to framing); and a 2025 systematic review names "inadequate addressing of heat warning fatigue" as a **gap** (CS-10).
- **Demonstrated, but elsewhere.** Clinical alarm literature provides the only measured desensitization anywhere in this base — 87.1% of PICU and 99.0% of ward alarms non-actionable with a dose–response slowing of response time (CS-41), 72–99% false-alarm rates (CS-40), 90% override (CS-42) — **at volumes of tens of thousands per unit per fortnight, against a heat alert issued a handful of times per season.**

*Synthesis:* warning fatigue is theoretically well-motivated, **empirically contested for public warnings, demonstrated only in high-volume clinical alerting, and untested for heat.** Do not design HeatShield around an assumed fatigue effect; do not assert it has been disproven; and **never transfer clinical false-alarm rates to a heat dashboard**, which would imply a heat false-alarm rate no source supports.

---

# Trust, Clarity, and Message Usefulness

**Message content does not survive.** Recall collapsed to three themes, and only 5% mentioned drinking more water unprompted against 51% when asked directly (CS-13). Warning response is a multi-stage funnel in which reception, attention and comprehension all precede threat perception, and situational impediments can block action even after a correct decision (CS-59).

**Guidance is consistent on what a good message contains:** "clear, unambiguous language", bespoke to recipient type (CS-01); "clear guidance to trigger reactions" with the issuing authority identified (CS-14); pre-specified audience, means, contents and delivery time (CS-02).

## A genuine disagreement: are colour tiers a solution or a problem?

**For:** colour tiers are near-universal in operating systems (CS-05, CS-06, CS-15, CS-19, CS-22, CS-96, CS-106) and colour coding "produced the greatest differentiation between low- and high-impact levels" for the public (CS-65).

**Against:** participants misread "level 3" as mid-range rather than high, and colour/number literacy "relies on prior familiarity with the cultural practice of using colours and numbers to calibrate abstract qualities like risk" (CS-64). The same experiment found colour coding acted in the **opposite direction** on emergency managers (CS-65). And colour alone is non-conformant without a text equivalent (CS-38).

*Synthesis:* the design response follows from the disagreement rather than from either side — **use the official tier, always render it as "Level N of 4 — [word]", and comprehension-test it with older and non-native speakers.**

**Trust is a separate failure mode from reach**, and improving reach does not fix it (CS-61, CS-34, CS-30 — institutional trust ranged 3.5/5 to 2.0/5 across districts).

---

# Plain Language and Accessibility

**Structural exclusion sets the ceiling.** 2.2 billion people (~25% of the world) remain offline; rural 58% versus urban 85%; low-income countries 23% versus high-income 94%; and the age skew (15–24 at 82% versus 72% for everyone else) runs directly against heat vulnerability (CS-26). Coverage is not usage — 5G covers 55% of the global population but 4% in low-income countries, and mobile broadband is unaffordable in roughly 60% of low- and middle-income countries (CS-26).

**Translation is a documented failure mode, not a formality.** 53.2% of alerting agencies report multilingual capability; **83.9% of those that translate use machine translation**, producing "inaccurate or confusing" messages ("Eagle County" → "bird County"); certified interpreters take **5–10 minutes**, "insufficient for fast-moving emergencies"; and **"pre-translated templates remain underutilised despite proven effectiveness"** (CS-34). Funding is the top barrier, cited by 64% of agencies.

**Modality and presentation.** US ADA guidance requires both visual and audible alerts (CS-32); WCAG 2.2 (W3C Recommendation, **12 December 2024**) requires a text equivalent for information conveyed by colour (CS-38). *The claim that WCAG Level AA is legally required was not verified from any legal source and is not asserted here.*

**Receipt is not accessibility.** The WEA evaluation found no significant difference in *receipt* among people with disabilities but explicitly separates receipt from usability, flagging font legibility, text-to-speech and plain language as needing further research (CS-23). Paraphrasing that finding as "the channel is accessible" would misstate it.

---

# Thailand and Southeast Asia Considerations

## The burden justifies the project

**6.71% of 878,513,460 outpatient admissions across 77 Thai provinces were attributable to hot temperatures**, with greater burden in females and those aged 0–19 (CS-97, abstract-level) — so Thai heat vulnerability is **not confined to the elderly**. Thai heat-related illness concentrates in skilled agricultural workers (35.7% of cases) and in the Northern region (9.3 per 100,000) (CS-90), and Thai heat deaths are dominated by working-age and older **men with outdoor occupational exposure** — male:female 7.2:1, median age 53 (CS-89). Sugarcane workers were measured above the ACGIH threshold limit value **90.9% of working time** in the hot month (CS-98). A Thai heat warning system was formally *proposed* in the peer-reviewed literature as early as **2015** (CS-90): HeatShield addresses a documented, long-standing gap.

*Synthesis:* the Thai risk profile is **not** the frail-elderly-indoors archetype that dominates the European and North American literature. Any HeatShield vulnerability model imported wholesale from those settings would target the wrong people.

## The digital-exclusion finding that governs channel design

| Measure (Thais aged 60+, ~14.6 million) — all figures CS-93 | Overall | 70–79 | **80+** |
|---|---|---|---|
| Internet use | 69.8% | 57.2% | **29.3%** |
| Mobile phone ownership | 77.8% | 70.2% | **36.1%** |

Regionally, older-adult internet use runs from **Bangkok 85.8% to North 63.4%** (CS-93). And connectivity is not reachability: **only ~10.83%** of Thai over-60s use the internet for health-related purposes at all (CS-100).

**A genuine disagreement in the same statistical system.** National internet use is **90.9%** (CS-95) — true, and useless for this decision. The education gradient within it is 64.4% (no/below-primary education) versus 99.6% (higher education) (CS-95). *Every connectivity figure must carry its subgroup and its year* — older-adult internet use moved 52.4% → 69.8% in three years (CS-94 → CS-93).

## The last-mile channel: อสม.

Thailand has **more than 1 million village health volunteers responsible for primary healthcare of 23 million households in 75,032 villages** (CS-92). *(Correction applied: the precise figure "1,039,729" is **not** in that source; see `Chris_source_inventory.md`.)* During COVID-19 the network achieved population-scale contact within weeks — 12.6 million household visits between late March and April 2020 (CS-92; this figure was not part of the independently re-verified set).

**But the channel is not free to use.** Thai VHVs "deliver what they have been trained on" and **heat is not in the curriculum**; workload is already described as overwhelming; and capability differs markedly between VHV leaders and general VHVs (CS-102).

**And, critically: no evidence was found that อสม. have ever delivered a heat warning.** Searched in Thai and English; result null. **This is the project's largest unevidenced local assumption.**

## Institutional and technical context

- The Thai heat index is an **inter-agency product** (Environmental Research and Training Center with the Department of Health and the Department of Disease Control) (CS-96).
- **The band structure is contested:** five levels with an Extreme Danger threshold ≥54 °C (peer-reviewed, CS-96) versus four levels with red above 52 °C (Department of Health, CS-106). The TMD page could not resolve it (CS-115). **HeatShield must pick one, name its source, and flag the discrepancy — a live design decision requiring human confirmation.**
- **Humidity moves the risk geography.** Peak temperature was inland (Phichit 44.1 °C) while red-alert heat-index provinces were coastal (Phuket, Phang Nga, Krabi, Surat Thani, Trat, Chachoengsao, Chanthaburi) (CS-107). **A temperature-only dashboard would flag the wrong provinces.**
- **What the Department of Health actually used** during an active heat emergency: a website, Facebook and hotline 1669 — with **no mention of อสม., LINE, loudspeakers or an app** (CS-107, explicitly checked).
- **Thailand's national Cell Broadcast Service** requires no registration and no app, reaching feature phones, and is owned by DDPM/MDES/NBTC — **but supports Thai, English, Chinese, Japanese and Russian, not Burmese, Khmer or Lao** (CS-108), against a population of 5.3 million non-Thai nationals including over 2.3 million regular migrant workers and 1.8 million irregular Myanmar migrants (CS-111). The exclusion is **inferable from the published language list, not measured** — no study evaluates migrant heat-warning access.
- **Two Thai heat-death series do not reconcile:** 139 deaths 2018–2023 (Department of Disease Control, CS-89) versus 131 deaths 2019–2023, average 26.1 annually (Department of Health, CS-107). **Never quote a single Thai heat-death figure without naming the agency and the period**, and note that both are likely substantial undercounts.
- **Regional context:** Southeast Asian early warning systems use "multiple channels including SMS, sirens, social media, and community-based intermediaries", with multi-hazard coverage rising from 25% (2015) to 67% (2023); the binding constraint is community awareness rather than technical warning quality; and Thailand hosts RIMES as a regional technical centre (CS-112). *This is predominantly geophysical and hydrometeorological hazard evidence, not heat.*
- **Message framing for connected Thai seniors:** gain framing outperformed loss framing on LINE (CS-104, n=303, convenience sample, not heat-specific).

## What has no Thailand-specific evidence at all

อสม. delivering heat warnings; reach, comprehension or behavioural effect of any Thai heat warning; any Thai CSAT/adoption/usability study of a heat or disaster product; village loudspeakers (หอกระจายข่าว); temple announcements and community radio for health; the current operational status of Thai Cell Broadcast; any credible LINE penetration statistic; a peer-reviewed evaluation of หมอพร้อม; migrant-language heat communication; motorcycle taxi riders as a risk group; and a consolidated Thai heat action plan.

**A 2025 review of 53 Thai climate-health studies (2013 onward) found the literature dominated by dengue and surfaced no Thai heat warning/response framework** (CS-116) — corroborating that this gap is real and documented, not an artefact of insufficient searching.

---

# Evidence Gaps

**Structural gaps in the global literature**

1. No study measures acknowledgement rates in public-health mass notification.
2. No heat-specific empirical test of warning fatigue exists (CS-10 names it as a gap).
3. No operating heat warning system was documented performing receipt verification, despite CS-14 requiring it.
4. No source quantifies contact-registry decay.
5. No evidence-based response-time or acknowledgement-window standard exists for a heat alert.
6. No per-channel reach study exists for heat anywhere; no per-channel cost data; no direct IVR/reverse-911 evaluation.
7. Heat health warning systems are "broadcast-shaped", lack targeting and actionable content for at-risk groups, and the literature contains **no studies on the role of timing** — "we did not find any studies that discuss how time plays a role" (CS-10).
8. No instrument located has been validated for heat-warning services; and **no validated instrument exists for timeliness, relevance or channel preference**, with trust only partially covered.
9. Only 18 of 65 public health dashboard studies did any user study (CS-36).

**Access gaps in this review**

10. The **full WHO Europe heat–health action plan guidance, second edition** was never opened (CS-03) — the largest single substantive gap.
11. Twenty sources were accessible only as abstracts, landing pages or executive summaries, including the original TAM, UTAUT, UMUX, ACSI, McKnight and NASA-TLX papers, meaning **no adoption or trust instrument's original item wording could be verified** except SUS and PEMAT.
12. Publisher blocks skew the base toward open-access and government-hosted material; the named unopened sources are listed in `Chris_research_log.md`.

**Thailand gaps** — the fifteen items listed in the previous section, of which the most consequential is that **no evidence exists that Thai village health volunteers have ever delivered a heat warning.**

---

# Implications for the Prototype

> Everything in this section is a **project recommendation**, not a finding. Each states the evidence it rests on and its strength.

## For the dashboard itself

1. **Position the dashboard as a coordination and confirmation destination, not a delivery channel.** Evidence: dashboards are a pull channel with essentially no behavioural evidence base (CS-36), but people seek a second source before acting (CS-37). *Strength: High for the under-evaluation claim; Moderate for the confirmation role.*
2. **Make ownership and acknowledgement a first-class dashboard field** — showing not only that an alert was sent but whether it was received and by which role. Evidence: acknowledgement is a formal requirement (CS-14) documented as absent in practice (CS-18); loop closure improves when notification is tied to the originating record (CS-45, analogy). *Strength: High for the requirement; Moderate for the mechanism.*
3. **Render every risk tier as "Level N of 4 — [word]", never colour alone.** Evidence: CS-64, CS-65, CS-38. *Strength: Moderate — the underlying evidence disagrees; this design resolves the disagreement.*
4. **Display data age and provenance on the dashboard face.** Evidence: CS-01 (timestamp and source as core fields); CS-39 (5–10 day data-to-leadership lag in a real heat event). *Strength: Moderate.*
5. **Consume the official Thai heat index; do not compute a new one; be humidity-aware.** Evidence: CS-96, CS-115, CS-106, CS-107. *Strength: High for the institutional facts; the band count is contested (CS-96 vs CS-106).*

## For contact points and channels

6. **Address every institutional alert to a role, not a person, with a scheduled registry review.** Evidence: CS-46 (analogy). *Strength: Moderate.*
7. **Name an onward-cascade owner for every intermediate node.** Evidence: CS-18, CS-04. *Strength: High.*
8. **Pair every primary channel with a fallback that has an independent failure mode.** Evidence: CS-31, CS-27, CS-14. *Strength: High for the mechanism.*
9. **Treat human contact as a primary channel for isolated older adults in Thailand, not a courtesy fallback.** Evidence: CS-93, CS-100, CS-27, CS-30. *Strength: Moderate — the exclusion data is High and Thai; the volunteer-reach data is High but from cyclone warning in Bangladesh, and no Thai heat evidence exists.*
10. **Pre-translate message templates before the season**, in Thai plus Burmese, Khmer and Lao. Evidence: CS-34, CS-108, CS-111. *Strength: Moderate-High.*
11. **Do not rely on opt-in registration for the public channel.** Evidence: CS-54, CS-23. *Strength: Moderate.*

## For messaging

12. **Limit each alert to one to three specific, locally feasible actions**, and test unprompted recall. Evidence: CS-13, CS-30, CS-63. *Strength: High.*
13. **Message the person's situation, not the demographic label.** Evidence: CS-61, CS-63, CS-29. *Strength: High.*
14. **Hold one alert vocabulary identical across every channel.** Evidence: CS-37, CS-05, CS-17. *Strength: Moderate-High.*
15. **Route through trusted intermediaries alongside the official channel.** Evidence: CS-61, CS-34, CS-58 (social influence r=0.551), CS-30. *Strength: Moderate-High.*

## For evaluation

16. **Scope Phase 0 evaluation to usability, clarity, acceptability and actionability — not health outcomes.** Evidence: CS-87, CS-54, CS-13. *Strength: High.*
17. **Use the framework in `Chris_csat_adoption_evaluation.md`**: a 10-item core survey, 6 task measures, 8 service-generated indicators and 6 open-ended questions, with adapted and newly proposed items clearly distinguished.
18. **Measure perceived usefulness before usability.** Evidence: CS-58 (PU r=0.607 vs PEOU r=0.525 in older adults). *Strength: High.*
19. **Report the respondent profile against the target profile before any satisfaction number.** Evidence: CS-54, CS-13 (5.4% response rate). *Strength: High.*
20. **Do not use Net Promoter Score as an effectiveness measure.** Evidence: CS-77; CS-78 excluded. *Strength: High.*
21. **Schedule the post-event review before the season, with a named owner.** Evidence: CS-18, CS-01, CS-02. *Strength: High.*
22. **Treat the unmeasurable as a test plan.** Acknowledgement windows, channel reach, registry decay and Thai อสม. heat delivery are all unknown — measure them in Phase 0 rather than assuming values.

## Five decisions requiring human confirmation

1. Which Thai heat-index band structure to adopt (CS-96 vs CS-106).
2. Whether the อสม. channel can be used, which volunteer tier, and with what training and workload offset (CS-102).
3. Whether Thai Cell Broadcast is currently operational and whether languages can be added (CS-108).
4. Who owns inter-ministry liaison between MoPH and DDPM/MDES/NBTC (CS-108, CS-04).
5. Acknowledgement windows for each institutional contact point (no evidence-based standard exists).

---

# References

Full metadata, geography, stakeholder group, evidence strength, inclusion status and reason for all 117 canonical sources are in `Chris_source_inventory.md`. The following are the sources carrying the load-bearing claims in this review, in the form independently verified.

1. Abrahamson, V., Wolf, J., Lorenzoni, I., Fenn, B., Kovats, S., Wilkinson, P., Adger, W.N. & Raine, R. (2009). Perceptions of heatwave risks to health: interview-based study of older people in London and Norwich, UK. *Journal of Public Health*, 31(1), 119–126. https://doi.org/10.1093/pubmed/fdn102 · **CS-61**
2. Agency for Healthcare Research and Quality (n.d.). *The Patient Education Materials Assessment Tool (PEMAT) and User's Guide*. Rockville, MD: AHRQ. https://www.ahrq.gov/health-literacy/patient-education/pemat2.html · **CS-80, CS-81**
3. Bonafide, C.P., Lin, R., Zander, M., Graham, C.S., Paine, C.W., Rock, W., Rich, A., Roberts, K.E., Fortino, M., Nadkarni, V.M., Localio, A.R. & Keren, R. (2015). Association between exposure to nonactionable physiologic monitor alarms and response time in a children's hospital. *Journal of Hospital Medicine*, 10(6), 345–351. https://doi.org/10.1002/jhm.2331 · **CS-41**
4. British Columbia Coroners Service (2022). *Extreme Heat and Human Mortality: A Review of Heat-Related Deaths in B.C. in Summer 2021*. Death Review Panel report, 7 June 2022. Burnaby, BC. · **CS-27**
5. Brooke, J. (1996). SUS: a quick and dirty usability scale. In P.W. Jordan, B. Thomas, B.A. Weerdmeester & I.L. McClelland (Eds.), *Usability Evaluation in Industry* (pp. 189–194). London: Taylor & Francis. · **CS-70**
6. Brooke, J. (2013). SUS: a retrospective. *Journal of Usability Studies*, 8(2), 29–40. · **CS-72**
7. Callen, J.L., Westbrook, J.I., Georgiou, A. & Li, J. (2012). Failure to follow-up test results for ambulatory patients: a systematic review. *Journal of General Internal Medicine*, 27(10), 1334–1348. https://doi.org/10.1007/s11606-011-1949-5 · **CS-45**
8. Centers for Disease Control and Prevention (n.d.). *CDC Clear Communication Index*. Atlanta, GA: CDC. https://www.cdc.gov/ccindex/index.html (threshold: score sheet, https://www.cdc.gov/ccindex/pdf/full-index-score-sheet.pdf) · **CS-83**
9. Chandra N, S.V.S. & Lee, J. (2025). A systematic review of heat health warning systems: enhancing the framework towards effective health outcomes. *Current Environmental Health Reports*, 12(1), 31. https://doi.org/10.1007/s40572-025-00496-5 · **CS-10**
10. Davis, F.D. (1989). Perceived usefulness, perceived ease of use, and user acceptance of information technology. *MIS Quarterly*, 13(3), 319–340. https://doi.org/10.2307/249008 · **CS-55**
11. Difonzo, M. (2019). Performance of the afferent limb of rapid response systems in managing deteriorating patients: a systematic review. *Critical Care Research and Practice*, 2019, 6902420. https://doi.org/10.1155/2019/6902420 · **CS-43**
12. Doherty, F.C., Rao, S., Traver, A. & Dabelko-Schoeny, H. (2025). Extreme heat preparedness and coping among older adults: a rapid review. *PLOS Climate*, 4(8), e0000689. https://doi.org/10.1371/journal.pclm.0000689 · **CS-29**
13. Erens, B., Williams, L., Exley, J., Hajat, S., Rubin, G.J., O'Connor, D.B. & Mays, N. (2021). Public attitudes to, and behaviours taken during, hot weather by vulnerable groups: results from a national survey in England. *BMC Public Health*, 21, 1631. https://doi.org/10.1186/s12889-021-11668-x · **CS-28**
14. Eysenbach, G. (2005). The law of attrition. *Journal of Medical Internet Research*, 7(1), e11. https://doi.org/10.2196/jmir.7.1.e11 · **CS-66**
15. Federal Communications Commission (2024). *Communications Status Report for Areas Impacted by Hurricane Helene*, 1 October 2024. https://docs.fcc.gov/public/attachments/DOC-406055A1.pdf · **CS-31**
16. Fornander, L., Garrido Granhagen, M., Molin, I., Laukkanen, K., Björnström Karlsson, K., Berggren, P. & Nilsson, L. (2024). The use of specific coordination behaviours to manage information processing and task distribution in real and simulated trauma teamwork. *Scandinavian Journal of Trauma, Resuscitation and Emergency Medicine*, 32, 51. https://doi.org/10.1186/s13049-024-01287-x · **CS-47**
17. Hossain, M.L. (2026). Beyond warnings and shelters: local institutions and trust build cyclone resilience in Bangladesh. *npj Natural Hazards*, 3, 17. https://doi.org/10.1038/s44304-026-00177-9 · **CS-30**
18. International Telecommunication Union (2025). *Measuring digital development: Facts and Figures 2025*. Geneva: ITU. https://www.itu.int/itu-d/reports/statistics/facts-figures-2025/ · **CS-26**
19. Keiningham, T.L., Cooil, B., Andreassen, T.W. & Aksoy, L. (2007). A longitudinal examination of Net Promoter and firm revenue growth. *Journal of Marketing*, 71(3), 39–51. https://doi.org/10.1509/jmkg.71.3.039 · **CS-77**
20. Khanthavudh, C., Grealish, A., Tzouvara, V. & Leamy, M. (2025). Supporting healthcare in rural communities in Thailand: an exploratory qualitative study to understand the role and current mental health practices of village health volunteers. *PLOS ONE*, 20(4), e0320559. https://doi.org/10.1371/journal.pone.0320559 · **CS-102**
21. Knowlton, K., Kulkarni, S.P., Azhar, G.S., Mavalankar, D., Jaiswal, A., Connolly, M., et al. (2014). Development and implementation of South Asia's first heat-health action plan in Ahmedabad (Gujarat, India). *International Journal of Environmental Research and Public Health*, 11(4), 3473–3492. https://doi.org/10.3390/ijerph110403473 · **CS-05**
22. Krassanairawiwong, T., Suvannit, C., Pongpirul, K. & Tungsanga, K. (2021). Roles of subdistrict health office personnel and village health volunteers in Thailand during the COVID-19 pandemic. *BMJ Case Reports*, 14(9), e244765. https://doi.org/10.1136/bcr-2021-244765 · **CS-92**
23. Lewis, J.R. (2018). The System Usability Scale: past, present, and future. *International Journal of Human–Computer Interaction*, 34(7), 577–590. https://doi.org/10.1080/10447318.2018.1455307 · **CS-73**
24. Lim, J.R., Liu, B.F. & Egnoto, M. (2019). Cry wolf effect? Evaluating the impact of false alarms on public responses to tornado alerts in the southeastern United States. *Weather, Climate, and Society*, 11(3), 549–563. https://doi.org/10.1175/WCAS-D-18-0080.1 · **CS-49**
25. Lindell, M.K. & Perry, R.W. (2012). The Protective Action Decision Model: theoretical modifications and additional evidence. *Risk Analysis*, 32(4), 616–632. · **CS-59**
26. MacPherson-Krutsky, C., Painter, M.A. & Villarreal, M. (2024). *Inclusive Emergency Alerts for Colorado*. Boulder, CO: Natural Hazards Center. https://hazards.colorado.edu/uploads/freeform/final-report-12-8-24-eng-report-only.pdf · **CS-34**
27. Madrigano, J., Lane, K., Petrovic, N., Ahmed, M., Blum, M. & Matte, T. (2018). Awareness, risk perception, and protective behaviors for extreme heat and climate change in New York City. *International Journal of Environmental Research and Public Health*, 15(7), 1433. https://doi.org/10.3390/ijerph15071433 · **CS-63**
28. Matthies, F., Bickler, G., Cardeñosa Marín, N. & Hales, S. (Eds.) (2008). *Heat–Health Action Plans: Guidance*. Copenhagen: WHO Regional Office for Europe. ISBN 978 92 890 7191 8. · **CS-02**
29. Mileti, D.S. & Peek, L. (2000). The social psychology of public response to warnings of a nuclear power plant accident. *Journal of Hazardous Materials*, 75(2–3), 181–194. · **CS-37**
30. Mileti, D.S. & Sorensen, J.H. (1990). *Communication of Emergency Public Warnings* (ORNL-6609). Oak Ridge National Laboratory. https://doi.org/10.2172/6137387 · **CS-60**
31. National Statistical Office of Thailand (2026). *การมีการใช้ไอซีทีของผู้สูงอายุ พ.ศ. 2568* [ICT Usage Among Elderly Persons 2025]. Bangkok: Ministry of Digital Economy and Society. **In Thai.** https://www.nso.go.th/nsoweb/storage/survey_detail/2026/20260727143041_96531.pdf · **CS-93**
32. Paengkaew, W., Limsakul, A., Kokkaew, E., Sooktawee, S., Muangnim, P., Naban, O., et al. (2023). Development of a hot weather warning tool for heat index monitoring in Thailand. *Journal of Public Health and Development*, 21(3). https://doi.org/10.55131/jphd/2023/210301 · **CS-96**
33. Parker, A.M., Steratore, R., Bradley, M.A., LaForce, S., Woods, D., Setodji, C.M., et al. (2024). *Assessing Public Reach of the 2023 National Test of the Wireless Emergency Alerts (WEA) System*. Santa Monica, CA: RAND. https://doi.org/10.7249/RRA2451-1 · **CS-23**
34. Robru, K., Setthasuravich, P., Pukdeewut, A. & Wetchakama, S. (2024). Internet use for health-related purposes among older people in Thailand. *Informatics*, 11(3), 55. https://doi.org/10.3390/informatics11030055 · **CS-100**
35. Rojo, E.M. & Bosworth, H.B. (2026). Navigating the heat: implementation challenges and opportunities for heat alert communication and rural health data infrastructure. *Frontiers in Public Health*, 14, 1801198. https://doi.org/10.3389/fpubh.2026.1801198 · **CS-54**
36. Schulze, A., Brand, F., Geppert, J. & Böl, G.-F. (2023). Digital dashboards visualizing public health data: a systematic review. *Frontiers in Public Health*, 11, 999958. https://doi.org/10.3389/fpubh.2023.999958 · **CS-36**
37. Sheridan, S.C. (2007). A survey of public perception and response to heat warnings across four North American cities. *International Journal of Biometeorology*, 52(1), 3–15. https://doi.org/10.1007/s00484-006-0052-9 · **CS-13**
38. Starmer, A.J., Spector, N.D., Srivastava, R., West, D.C., Rosenbluth, G., et al. (2014). Changes in medical errors after implementation of a handoff program. *New England Journal of Medicine*, 371(19), 1803–1812. https://doi.org/10.1056/NEJMsa1405556 · **CS-44**
39. Tang, C. (2022). "Level 3": interpreting risk-level terminology in UK weather warnings. *Applied Linguistics*, 43(2), 227–250. · **CS-64**
40. Thawillarp, S., Thammawijaya, P., Praekunnatham, H. & Siriruttanapruk, S. (2015). Situation of heat-related illness in Thailand, and the proposing of heat warning system. *OSIR Journal*. https://he02.tci-thaijo.org/index.php/OSIR/article/view/263275 · **CS-90**
41. Thailand.go.th (2024). *Stay Alert, Stay Safe! "Cell Broadcast Service" — The Emergency Alert System Reducing Risks and Losses*. Royal Thai Government portal. · **CS-108**
42. UK Health Security Agency (2026). *Heat-Health Alert action card for health and social care providers*. https://gov.uk/guidance/heat-health-alert-action-card-for-health-and-social-care-providers · **CS-19**
43. Vanderplanken, K., van den Hazel, P., Marx, M., Shams, A.Z., Guha-Sapir, D. & van Loenhout, J.A.F. (2021). Governing heatwaves in Europe. *Health Research Policy and Systems*, 19, 20. https://doi.org/10.1186/s12961-020-00645-2 · **CS-04**
44. Venkatesh, V., Morris, M.G., Davis, G.B. & Davis, F.D. (2003). User acceptance of information technology: toward a unified view. *MIS Quarterly*, 27(3), 425–478. https://doi.org/10.2307/30036540 · **CS-56**
45. Wen, B., Kliengchuay, W., Suwanmanee, S., Aung, H.W., Sahanavin, N., Siriratruengsuk, W., et al. (2024). Association of cause-specific hospital admissions with high and low temperatures in Thailand. *The Lancet Regional Health – Western Pacific*, 46, 101058. https://doi.org/10.1016/j.lanwpc.2024.101058 · **CS-97**
46. Williams, L., Erens, B., Ettelt, S., Hajat, S., Manacorda, T. & Mays, N. (2019). *Evaluation of the Heatwave Plan for England: Final report*. London: PIRU, LSHTM. · **CS-18**
47. World Health Organization (2016). *Monitoring and evaluating digital health interventions*. Geneva: WHO. ISBN 978 92 4 151176 6. · **CS-87**
48. World Health Organization Regional Office for Europe (2026). *Heat–health action plans: guidance, second edition*. ISBN 9789289062930. **[Executive summary only — full text not accessed]** · **CS-03**
49. World Meteorological Organization (2018). *Multi-hazard Early Warning Systems: A Checklist*. Geneva: WMO. · **CS-14**
50. World Meteorological Organization & World Health Organization (2015). *Heatwaves and Health: Guidance on Warning-System Development* (WMO-No. 1142). Geneva: WMO/WHO. ISBN 978-92-63-11142-5. · **CS-01**
51. World Wide Web Consortium (2024). *Web Content Accessibility Guidelines (WCAG) 2.2*. W3C Recommendation, 12 December 2024. https://www.w3.org/TR/WCAG22/ · **CS-38**
52. Yang, H.J., Lee, J.-H. & Lee, W. (2025). Factors influencing health care technology acceptance in older adults based on TAM and UTAUT: meta-analysis. *Journal of Medical Internet Research*, 27, e65269. https://doi.org/10.2196/65269 · **CS-58**
53. Zimolzak, A.J., Shahid, U., Giardina, T.D., Memon, S.A., Mushtaq, U., Zubkoff, L., Murphy, D.R., Bradford, A. & Singh, H. (2022). Why test results are still getting "lost" to follow-up. *Journal of General Internal Medicine*, 37(1), 137–144. https://doi.org/10.1007/s11606-021-06772-y · **CS-46**
