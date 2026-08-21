# Chris Service-Logistics Risks and Adoption Barriers

**Project:** HeatShield — Heat Risk Dashboard Roadmap Initiative
**Research stream:** Stakeholders, Communication Logistics, Adoption, and CSAT-Style Evaluation
**Date:** 20 August 2026

---

## How to read this register

- **Evidence** cites canonical source IDs from `Chris_source_inventory.md`.
- **Confidence** reflects how well the evidence supports *this risk in this project's context*, after the verification downgrades recorded in the inventory. It is not the quality of the source in the abstract.
  - **High** — directly evidenced, in a comparable context.
  - **Moderate** — well evidenced, but transferred from another hazard, country or domain, or resting on a single study.
  - **Low** — mechanism is plausible and named in the literature, but not measured in a comparable context.
- **[analogy]** marks a risk whose evidence comes from clinical alerting rather than public-health heat alerting. No source located in this review measures acknowledgement or escalation rates in public-health mass notification.
- **[TH]** marks Thailand-specific rows.
- Mitigations are **evidence-informed prototype proposals**, not operational commitments.

---

## 1. Stakeholder and ownership risks

| Risk | Cause | Affected stakeholder | Likely consequence | Possible mitigation | Evidence | Confidence |
|---|---|---|---|---|---|---|
| Roles defined only against alert tiers, leaving everything else ambiguous | Plans specify who does what *at each level* and nothing outside that grid | All institutional stakeholders | Tasks outside the tier grid have no owner; nobody notices until an event | Define ownership per **contact point**, not per alert level; use the seven-role vocabulary (author, activator, coordinator, monitor, informer, implementer, evaluator) | CS-04 | **High** |
| The municipal/local implementation layer is absent from the plan | National plans rely on local delivery but rarely name the municipal level | District and sub-district administrations | The layer that does the work is not resourced or instructed | Name the local owner explicitly for every cascade step in the contact-point matrix | CS-04, CS-18 | **High** |
| An intermediate body sits in the cascade with no defined onward responsibility | Cascade design assumes forwarding happens automatically | Commissioning or coordinating bodies; front-line staff downstream | The cascade stops silently at the intermediate node | Every intermediate node must have a **named onward-cascade owner** and an acknowledgement obligation | CS-18 | **High** |
| Health-side owner and mass-alerting owner sit in different ministries **[TH]** | MoPH owns the health response; DDPM/MDES/NBTC own the national alerting pipe | MoPH; DDPM; the public | Requests stall at the ministry boundary; no single accountable party for public alerting | Name a standing liaison on both sides; record the dependency in the roadmap as a coordination risk HeatShield does not control | CS-108, CS-04 | **Moderate** |
| Assigned actors lack the autonomy to perform the assigned role | The task deviates from the actor's regular organisational duties | Front-line health and care staff | The action is assigned but not permitted, so it does not happen | Confirm authority alongside responsibility when assigning any contact-point owner | CS-04 | **High** |
| Collaboration does not extend beyond the health sector | Organisations coordinate within their own networks | Social services, civil protection, employers, education | Non-health stakeholders receive alerts they cannot act on, or none at all | Use the published cascade list as a coverage checklist; test one non-health recipient in the prototype | CS-04, CS-02 | **Moderate** |
| Lead-body doctrine is genuinely unsettled | WHO 2008 said health ministries lead; WHO 2026 says "often, but not exclusively"; India places it with disaster management; Thailand's alerting pipe sits outside MoPH | Project team; governance design | Presenting "health ministries lead" as settled misrepresents both current WHO guidance and Thai reality | State the divergence; do not assert a single correct lead body | CS-02, CS-03, CS-06, CS-108 | **High** |

---

## 2. Handoff and coordination risks

| Risk | Cause | Affected stakeholder | Likely consequence | Possible mitigation | Evidence | Confidence |
|---|---|---|---|---|---|---|
| Escalation fails even when an objective trigger is met **[analogy]** | Discretionary judgment inserted at a point the plan treats as automatic | Recipients awaiting escalation | Delay at exactly the moment the system was designed to prevent it | Make the escalation trigger explicit and log every non-escalation with a reason | CS-43 (23–57% missed/delayed; delay adjusted OR 1.79, 95% CI 1.43–2.27), CS-18 ("wait and see") | **Moderate** (clinical evidence; the heat instance in CS-18 is qualitative) |
| Loops stay open on information already generated **[analogy]** | No mechanism ties a notification back to its originating record | Everyone downstream | The signal exists in the system and never reaches action | Attach acknowledgement to the alert record itself — the design with the lowest observed failure rate | CS-45 (6.8–62% labs; 1.0–35.7% radiology; lowest with order-linked alerts) | **Moderate** |
| Alerts routed to an individual who has moved on disappear silently **[analogy]** | Contact registry holds people rather than roles | The vacated role; the population it serves | Nobody receives; nobody notices | **Address every institutional alert to a role, not a person**, with a named registry review cycle | CS-46 | **Moderate** |
| Diffusion of responsibility between plausible owners **[analogy]** | Several parties could reasonably own the next step, so none does | All institutional recipients | The handoff falls between owners | Single named owner per handoff; make ownership a visible dashboard field | CS-46 | **Moderate** |
| Contact registry decays | Staff turnover, reorganisation, changed numbers | All institutional contact points | Silent non-delivery to nodes believed to be covered | Scheduled pre-season registry verification; treat non-acknowledgement as a registry signal | CS-46 [analogy], CS-19 | **Low** — **no source located quantifies registry decay rates** |
| Out-of-hours or weekend arrival degrades response | Alert lands when duty holders are absent | Facilities; local government | Delayed or absent action | Define an out-of-hours route for every institutional contact point and test it | CS-18 | **Moderate** |
| Multi-agency information silos and fragmentation | Each agency uses its own tools and formats | All coordinating agencies | Conflicting pictures of the same event | Common alert vocabulary; a shared status view is the dashboard's clearest justified purpose | CS-04, CS-02 | **Moderate** |
| Data-to-leadership latency | Manual aggregation between surveillance and decision-makers | Health authority leadership | Decisions made on stale information | Timestamp everything; display data age on the dashboard face | CS-39 (5–10 day lag documented in a heat-event after-action review) | **Moderate** |

---

## 3. Channel and infrastructure risks

| Risk | Cause | Affected stakeholder | Likely consequence | Possible mitigation | Evidence | Confidence |
|---|---|---|---|---|---|---|
| **The declared fallback shares a failure mode with the primary** | SMS, push, email and dashboard all depend on grid-powered network infrastructure | Everyone in the affected area | The whole "multi-channel" design fails at once | **Every fallback must have an independent failure mode.** Pair digital with broadcast radio and with in-person contact | CS-31 (21.7% of cell sites out, rising from 9.1%; NC 48.7%; causes dominated by power and backhaul; 796,999 wireline subscribers out; only 34 FM / 6 AM / 5 TV off air) | **High** for the mechanism (hurricane — mechanism transfers, event does not) |
| Outage worsens on day two | Generator fuel and batteries deplete | Everyone | The fallback is least available late in a multi-day event — exactly the shape of a heatwave | Assume degradation over event duration; front-load in-person contact for priority households | CS-31 | **High** (mechanism) |
| Telephone escalation saturates at peak | Call volume spikes when the hazard peaks | Callers needing emergency help | Escalation is least available when most needed | Do not designate telephone as the sole fallback for high-risk contacts; use in-person visits for priority households | CS-27 (911 volume doubled; ambulance dispatch fell to 74–80%; six callers told none available) | **High** |
| Even the most universal digital push channel misses ~9%, skewed against the at-risk | Handset compatibility, opt-out, carrier and device variation | Older, rural and lower-income recipients | The people most likely to die are least likely to be reached | Treat cell broadcast as a floor, not a guarantee; pair with human contact | CS-23 (91% receipt; 23–52% lower odds 36+; 22–49% lower odds rural; 17.5% opt-out, 189% higher odds on subsidised phones) | **High** |
| Opt-in registration silently selects away from the at-risk population | People register if they are already engaged and connected | Older adults; outdoor and agricultural workers | The subscriber base is not the target population | Do not rely on opt-in for the primary public channel; use registration-free broadcast plus intermediaries | CS-54 (7.9% aged 65+, 6.6% outdoor, 2.4% agricultural) | **Moderate** (single US programme) |
| Channel ranking is assumed to be universal | Designers import a hierarchy from another setting | Everyone | The wrong primary channel is chosen | Treat channel choice as a local empirical question; **for Thailand the necessary reach study does not exist** | CS-23 vs CS-30 (ranking reverses between the USA and coastal Bangladesh) | **High** |
| Dashboard treated as a delivery channel | Confusing a pull channel with a push channel | The at-risk public | The service reaches only those who already visit | Pair the dashboard with a push channel; describe the dashboard as a coordination and confirmation destination | CS-36 (only 18 of 65 dashboard studies did any user study), CS-37 | **High** |
| No Thailand-specific channel reach data exists **[TH]** | The studies have not been done | Project team | Channel decisions rest on transferred evidence | State this explicitly in every channel recommendation; make channel reach a Phase 0 measurement | CS-116 (53 Thai climate-health studies surfaced no heat warning framework); the workstream gap lists | **High** (evidence of absence, presented as such) |

---

## 4. Message and comprehension risks

| Risk | Cause | Affected stakeholder | Likely consequence | Possible mitigation | Evidence | Confidence |
|---|---|---|---|---|---|---|
| Message content is not retained | Warnings carry a level but weak, unrepeated action content | The public | People know a warning exists and cannot say what to do | Limit to 1–3 specific actions; test unprompted recall in the prototype | CS-13 (recall collapsed to three themes; 5% mentioned water unprompted vs 51% when asked) | **High** |
| Alert tiers are misread | Numbered/coloured tiers are culturally acquired, not self-explanatory | The public; and differently, professionals | People underestimate a high-tier warning | Always render as "Level N of 4 — [word]"; comprehension-test with older and non-native speakers | CS-64 ("level 3" read as mid-range), CS-65 (colour coding acted in opposite directions on public and emergency managers), CS-38 | **Moderate** — **the evidence genuinely disagrees; see `Chris_literature_review.md`** |
| Messages conflict across channels | Each channel is authored separately | The public | Conflicting information becomes a reason to disregard or to act wrongly | One alert vocabulary, one source of truth, identical level wording everywhere | CS-37 (83% at Three Mile Island cited conflicting information), CS-05 | **Moderate** |
| Heat advice is confused with other advisories | Multiple advisories run concurrently | The public | Wrong protective action taken | Distinct visual and verbal identity for heat messaging; test for confusion | CS-13 (heat precautions conflated with ozone advice; 28% of fan users kept windows shut) | **Moderate** |
| Live translation is too slow or corrupts the message | Machine translation used under time pressure | Non-majority-language speakers | The message arrives unusable or not at all | **Pre-translate templates before the season** | CS-34 (83.9% use machine translation; "Eagle County" → "bird County"; interpreters take 5–10 minutes; templates "underutilised despite proven effectiveness") | **Moderate-High** |
| The recommended action is not feasible for the recipient | Advice assumes access to cooling, transport or time off | Low-income households; outdoor and informal workers | Correct comprehension, no action | Recommend only actions verified as available locally; measure feasibility, not just clarity | CS-13 (over a third said energy cost governed AC use), CS-63, CS-30 (action conversion ~52%, gated by shelter quality) | **High** |

---

## 5. Trust and credibility risks

| Risk | Cause | Affected stakeholder | Likely consequence | Possible mitigation | Evidence | Confidence |
|---|---|---|---|---|---|---|
| The state is not a trusted messenger for some recipients | Perceived intrusiveness; prior experience; immigration status | Older adults; migrant and undocumented communities | The message is received and disregarded | Route through community intermediaries alongside the official channel | CS-61 ("many thought state intervention was unnecessary, intrusive and unlikely to be effective"), CS-34 (fear-driven reluctance among undocumented residents) | **Moderate-High** |
| Social influence is under-used | Design assumes an individual, rational recipient | Older adults especially | A strong adoption lever is left unpulled | Route messages through family, volunteers and community figures — social influence correlated r=0.551 with intention in older adults | CS-58, CS-61, CS-34, CS-30 | **Moderate-High** |
| Perceived low usefulness suppresses adoption | The service does not visibly help the user do something | All users | Non-adoption regardless of technical quality | Measure perceived usefulness first — the strongest correlate of intention in this population (r=0.607) | CS-58 | **High** (for the correlation; intention is not behaviour) |
| Trust erosion from repeated or false alarms | Assumed "cry wolf" effect | The public | **Contested** — could cut either way | **Do not design around an assumed fatigue effect, and do not assert it has been disproven.** Measure alert volume and perceived usefulness in the prototype | CS-49 (N=4,162: higher *perceived* false-alarm ratio associated with *more* protective action), CS-60 (cry wolf listed among warning myths), against CS-50, CS-12 (editorial), CS-10 | **Low** — genuinely contested; **no heat-specific test exists** |
| Institutional trust varies sharply by locality | Local history and relationships | Communities | The same message performs very differently between districts | Measure trust locally rather than assuming it | CS-30 (institutional trust ranged 3.5/5 to 2.0/5 across districts — cyclone) | **Moderate** |

---

## 6. Accessibility and inclusion risks

| Risk | Cause | Affected stakeholder | Likely consequence | Possible mitigation | Evidence | Confidence |
|---|---|---|---|---|---|---|
| **Digital-first design excludes exactly the highest-risk group [TH]** | Assumption that everyone has a smartphone and internet | Thai adults aged 80+; rural and northern older adults | The people most likely to die are structurally unreachable | Human and broadcast channels as primary for this group, not as fallback | CS-93 (**over-80s: 29.3% internet use, 36.1% phone ownership**; North 63.4% vs Bangkok 85.8%), CS-100 (only ~10.83% of over-60s use the internet for health) | **High** |
| National connectivity averages mask subgroup exclusion **[TH]** | 90.9% national internet use is true and misleading at the same time | Project team; decision-makers | A channel decision justified by an irrelevant statistic | **Every connectivity figure must carry its subgroup and its year** | CS-95 vs CS-93 vs CS-100 | **High** |
| Global structural exclusion | A quarter of the world is offline, skewed rural, older, poorer, female | Vulnerable populations everywhere | Internet-dependent channels cannot be universal | State the ceiling explicitly in the roadmap | CS-26 (2.2 billion offline; rural 58% vs urban 85%; low-income 23% vs high-income 94%) | **High** |
| Language exclusion in the national alert pipe **[TH]** | Thai CBS supports Thai, English, Chinese, Japanese and Russian | Burmese, Khmer and Lao-speaking migrant workers (2.3 million regular, 1.8 million irregular Myanmar migrants among 5.3 million non-Thai nationals) | A large, highly heat-exposed population is outside the national alert system's language set | Pre-translated variants through employers and community organisations; request language additions | CS-108, CS-111, CS-110 | **Moderate-High** — the exclusion is inferable from the published language list; **no study evaluates migrant heat-warning access** |
| Colour-only risk encoding | Tier conveyed by colour alone | Colour-blind and low-vision users; screen-reader users | The risk level is not perceivable | Text equivalent for every tier (WCAG 2.2, W3C Recommendation 12 December 2024) | CS-38 | **High** (normative) |
| Single-modality alerting | Visual-only or audible-only delivery | Deaf/hard-of-hearing and blind/low-vision users | Non-receipt | Both visual and audible modalities for every public alert | CS-32 (ADA guidance) | **High** (normative, US) |
| Receipt mistaken for accessibility | Equal delivery rates read as equal usability | People with disabilities | Real usability barriers go unmeasured | Measure comprehension and usability separately from receipt | CS-23 (the report itself separates the two) | **High** |

---

## 7. Adoption and alert-fatigue risks

| Risk | Cause | Affected stakeholder | Likely consequence | Possible mitigation | Evidence | Confidence |
|---|---|---|---|---|---|---|
| **Awareness saturates while action does not** | Warnings inform without enabling | The at-risk public | Reach metrics look excellent and outcomes do not change | Measure action and feasibility, never reach alone | CS-13 (90% aware, 46% acted), CS-63 (66% aware → 43% believing indoor heat could make them ill; 12% *of the subgroup unable to keep their home cool* went somewhere air-conditioned), CS-28 (51% of adults aware nationally) | **High** |
| At-risk people do not personalise the risk | Self-image does not match the risk category | Older adults | Correct receipt, no self-directed action | Message the person's situation ("living alone", "taking these medicines"), not the demographic label; measure personalised risk perception | CS-61, CS-62, CS-29, CS-13, CS-63 | **High** |
| Flat alert prioritisation destroys signal-to-noise **[analogy]** | All alerts weighted equally | Institutional recipients | Overload and disregard | Tier by urgency; route by role | CS-46, CS-42, CS-40 | **Moderate** |
| Every user action is a point of attrition | Voluntary services shed users at each required step | All users | Steady decline in use across a season | Minimise required actions; prefer passive channels for the highest-risk group | CS-68 (one-month survival 3.4% active vs 27.3% passive), CS-67 (~71% disengage within 90 days, as reported in the review), CS-66 | **Moderate** — direction and order of magnitude only; **neither source is a comparable service** |
| Assuming clinical alarm-fatigue rates apply to a heat dashboard | Transferring 72–99% false-alarm figures across domains | Project team | A heat-alert false-alarm rate is implied that no source supports | **Never transfer these figures.** Cite as explicitly labelled analogy or not at all | CS-40, CS-41, CS-42 (volumes are orders of magnitude higher than a seasonal heat alert) | **High** (as a rule about citation) |
| Adding a heat task to an already-overloaded volunteer network **[TH]** | อสม. workload described as overwhelming; heat not in the curriculum | อสม.; the households they serve | The channel is nominally available and practically unused | Cost the training addition; specify the volunteer tier; propose a workload offset | CS-102 | **High** for the qualitative claim; single-province qualitative study, so do not generalise statistically |

---

## 8. Feedback and evaluation risks

| Risk | Cause | Affected stakeholder | Likely consequence | Possible mitigation | Evidence | Confidence |
|---|---|---|---|---|---|---|
| **No mechanism verifies that warnings were received** | Acknowledgement is required by guidance and rarely implemented | The whole service | The operator cannot distinguish "not sent" from "sent and ignored" | Instrument acknowledgement at every contact point where it is technically possible; treat silence as an escalation trigger | CS-14 (requirement), CS-18 (documented absence) | **High** for the pairing; **the absence is an evidence gap, not a measured rate** |
| Prescribed acknowledgement is not performed **[analogy]** | Mandating confirmation does not produce it | Institutional recipients | A false sense of closure | Instrument and monitor rather than mandate | CS-47 (closed-loop coupled to 3.6% of real utterances vs 7.7% simulated, p ≤ 0.001) | **Moderate** |
| Post-event review does not happen | Nobody owns it and it is not scheduled | The whole initiative | The same failures repeat every season | Schedule the review before the season with a named owner and a standing agenda | CS-18 (no formal post-alert assessment unless a major incident was declared), CS-01, CS-02 | **High** |
| Surveillance cannot support evaluation | Care sought outside emergency pathways is missed; occupational exposure not captured | Evaluation team | Burden, timing and distribution are underestimated | Do not promise outcome evaluation the data cannot support; scope Phase 0 to process measures | CS-54 | **Moderate-High** |
| Premature outcome claims | Pressure to show impact from a prototype | Project credibility | The initiative over-claims and loses credibility | WHO: match evaluation to maturity stage and **"avoid embarking on premature assessments"** | CS-87 | **High** |
| Satisfaction mistaken for effectiveness | CSAT is easy to measure and easy to over-read | Project team; stakeholders | A well-liked service that changes nothing | State the limitation in every reporting of the CSAT results | CS-87, CS-13, CS-77 | **High** |
| Net Promoter Score used as an effectiveness indicator | NPS is familiar and looks rigorous | Project team | An unvalidated headline number drives decisions | Do not use NPS as an effectiveness measure | CS-77 (21 firms, 15,500+ interviews; failed to replicate NPS superiority); CS-78 excluded from core evidence | **High** |
| Evaluation survey reaches only the digitally included | The survey is delivered digitally | Evaluation team | Results are biased toward the least excluded users | Offer volunteer-assisted and in-person completion; report the response profile against the target profile | CS-54, CS-13 (5.4% response rate), CS-26 | **Moderate** |

---

## The five risks the team should treat as highest priority

1. **Receipt failure is silent** (§2, §3, §8). Without acknowledgement, the service cannot tell success from failure. This is both the best-evidenced failure mode and the one the dashboard is best placed to fix.
2. **Digital-first design excludes the highest-risk Thai population** (§6). The over-80 statistics are not a caveat; they are a design constraint.
3. **The fallback is not a fallback if it shares a failure mode** (§3). This invalidates the most common multi-channel design.
4. **Awareness saturates while action does not** (§7). Any success metric built on reach will mislead the team.
5. **The อสม. channel is the best Thai option and is not free** (§7, §3). Training, workload and volunteer tier must be specified and costed, and **no evidence exists that อสม. have ever delivered a heat warning.**
