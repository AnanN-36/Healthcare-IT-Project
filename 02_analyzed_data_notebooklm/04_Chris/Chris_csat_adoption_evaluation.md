# Chris CSAT-Style Prototype Evaluation Framework

**Project:** HeatShield — Heat Risk Dashboard Roadmap Initiative
**Research stream:** Stakeholders, Communication Logistics, Adoption, and CSAT-Style Evaluation
**Date:** 20 August 2026

---

**Contents.** Part **G** (the limits of what this evaluation can show) is placed first deliberately, because it governs how every other part must be reported. The parts then run **F** (which measures are literature-supported versus newly proposed), **A** (Likert survey items), **B** (task-based measures), **C** (acknowledgement and completion indicators), **D** (open-ended questions), **E** (calculation and interpretation).

---

## G. Read this first — what this framework can and cannot show

> **A CSAT-style evaluation cannot demonstrate real-world health impact.**
>
> This is not a disclaimer added for form. It is the central methodological finding of this workstream, and it rests on three independent sources:
>
> 1. **Satisfaction and reach are not protection.** Sheridan (CS-13; n=908, response rate 5.4%) found heat-warning awareness at 90% among adults aged 65+ and behaviour change at 46%. A service can be well received, well understood and well liked while leaving the outcome unchanged.
> 2. **WHO explicitly warns against premature outcome assessment.** The WHO guide on monitoring and evaluating digital health interventions (CS-87) places a prototype on a maturity continuum and instructs teams to determine appropriate evaluation activities so as to **"avoid embarking on premature assessments."** Usability, feasibility and acceptability are the correct evaluation targets at this stage.
> 3. **The data needed for an outcome claim does not exist.** Heat surveillance underestimates burden where care is sought outside emergency pathways, and occupational exposure — the dominant Thai risk factor — **"is not systematically captured within the surveillance system"** (CS-54).
>
> **What this framework legitimately produces:** evidence about whether the prototype is understandable, usable, trusted, relevant and actionable to the people it is for, and which channels they can actually receive it through. That is a real and defensible Phase 0 contribution, and it addresses a documented gap — only **18 of 65** public health dashboard studies included any user study at all (CS-36).
>
> **What it must never be reported as:** evidence that HeatShield reduces heat-related illness or death.

---

## F. Which measures are literature-supported and which are newly proposed

This distinction is applied to every item in Part A and must be preserved in any reporting.

| Construct | Validated instrument available? | Instrument and source | Status of our items |
|---|---|---|---|
| Overall usability | **Yes** | System Usability Scale (CS-70; norms CS-72, CS-73) | **VERIFIED** — items reproducible verbatim, scoring and benchmarks verified |
| Actionability | **Yes** | PEMAT actionability items (CS-81); scoring CS-80 | **VERIFIED** — four item wordings verified verbatim (expert-rated, not a user survey) |
| Clarity of a risk message | **Yes** (material-level) | CDC Clear Communication Index, 20 scored items incl. a dedicated risk section (CS-83) | **VERIFIED** — expert-rated, not a user survey |
| Usefulness | **Yes** (construct) | Perceived usefulness, Davis 1989 (CS-55); performance expectancy, Venkatesh et al. 2003 (CS-56); effect size in older adults CS-58 | **ADAPTED** — construct is validated; **original item wording could not be retrieved and is not reproduced** |
| Ease of use | **Yes** (construct) | Perceived ease of use (CS-55); effort expectancy (CS-56) | **ADAPTED** — same caveat |
| Continuance intention | **Yes** (construct) | Behavioural intention (CS-55, CS-56, CS-76) | **ADAPTED** — same caveat |
| Social influence | **Yes** (construct) | Social influence (CS-56); r=0.551 with intention in older adults (CS-58) | **ADAPTED** — same caveat |
| Satisfaction | **Yes** | PSSUQ/CSUQ (CS-75); ACSI (CS-79) | **ADAPTED** — item wording unverified for both |
| Trust | **Partial only** | McKnight et al. 2002 (CS-86) — abstract only, items not retrieved. **The Jian et al. trust-in-automation scale is EXCLUDED** (items not publicly available; independent review rated its psychometric evidence at 46%) | **NEW** — no usable validated item wording was obtained |
| Timeliness | **No validated instrument located** | — | **NEW** |
| Relevance | **No validated instrument located** | — | **NEW** |
| Channel preference | **No validated instrument located** | — | **NEW** |
| Task completion | Not a questionnaire construct | Observed success rate | **Behavioural measure, see Part B** |
| Accessibility | **Yes** (objective audit, not a survey) | WCAG 2.2, W3C Recommendation 12 December 2024 (CS-38); ADA dual-modality guidance (CS-32) | **VERIFIED** — conformance check, not a user item |

> **No instrument located in this review has been validated for heat-warning services.** Every one was validated in another domain. Adapted items must be described as adapted, and new items as new, in any write-up.

---

## A. Core prototype survey — 10 items, 1–5 Likert

Response scale for items 1–9: **1 = Strongly disagree, 2 = Disagree, 3 = Neither agree nor disagree, 4 = Agree, 5 = Strongly agree.** Item 10 uses its own scale.

Rationale for the length: the meta-analytic evidence in the target population (CS-58) shows **perceived usefulness (r=0.607)** and **social influence (r=0.551)** are the strongest correlates of intention, with **ease of use (r=0.525)** third — so those constructs are protected in the short form, and constructs with no validated instrument are given one item each rather than several.

| # | Construct | Item | Status |
|---|---|---|---|
| 1 | **Usefulness** | "This heat information helps me decide what to do." | **ADAPTED** from perceived usefulness (CS-55, CS-56) |
| 2 | **Clarity** | "I understood what the heat level shown here means." | **ADAPTED** from CDC Clear Communication Index Part A / PSSUQ information quality (CS-83, CS-75) |
| 3 | **Actionability** | "This information clearly tells me at least one thing I can do." | **ADAPTED** from PEMAT actionability item 1, verified wording "The material clearly identifies at least one action the user can take." (CS-81) |
| 4 | **Actionability — charts** | "The chart or map here is explained well enough for me to act on it." | **ADAPTED** from PEMAT actionability item 4, verified wording "The material explains how to use the charts, graphs, tables, or diagrams to take actions." (CS-81) |
| 5 | **Trust** | "I trust the heat information shown here." | **NEW** — no usable validated item wording obtained |
| 6 | **Timeliness** | "I received this heat information in time to do something about it." | **NEW** |
| 7 | **Relevance** | "This heat information applies to me and where I am." | **NEW** — targets the personalisation failure documented in CS-61 and CS-63 |
| 8 | **Ease of use** | "It was easy to find what I needed." | **ADAPTED** from perceived ease of use (CS-55) |
| 9 | **Continuance intention** | "I would use this heat information again next time it is hot." | **ADAPTED** from behavioural intention (CS-55, CS-56) |
| 10 | **Overall satisfaction** | "Overall, how satisfied are you with this heat information service?" — **1 = Very dissatisfied … 5 = Very satisfied** | **ADAPTED** from single-item CSAT convention; ACSI (CS-79) item wording unverified |

### Optional follow-up items (use only if respondent time allows)

| # | Construct | Item | Status |
|---|---|---|---|
| 11 | **Social influence** | "People I trust would want me to pay attention to this heat information." | **ADAPTED** from social influence (CS-56); justified by r=0.551 in older adults (CS-58) |
| 12 | **Feasibility of the action** | "I am able to do what this information asks me to do." | **NEW** — targets the documented capacity barrier: over a third said energy cost governed AC use (CS-13); action conversion tracked shelter quality (CS-30) |
| 13 | **Personalised risk** | "Hot weather like this could make me ill." | **NEW** — measures the personalisation gap directly (CS-61, CS-63: 43% believed indoor heat could make them ill) |
| 14 | **Accessibility (self-report)** | "I could read, hear or understand this information without needing help." | **NEW** |
| 15 | **Channel preference** | "Which way would you most like to receive heat warnings?" — select one: mobile phone alert / SMS / messaging app / phone call / radio / television / village loudspeaker / community health volunteer in person / family member / dashboard or website / other | **NEW** — categorical, not Likert; no validated instrument located |

### Optional standalone module: System Usability Scale

Where the team wants a comparable usability benchmark for the dashboard interface specifically, administer the **full 10-item SUS** (CS-70) as a separate module. Do **not** cherry-pick SUS items — the instrument is scored as a whole.

- Scoring, verified verbatim: "For items 1,3,5,7,and 9 the score contribution is the scale position minus 1. For items 2,4,6,8 and 10, the contribution is 5 minus the scale position", then "multiply the sum of the scores by 2.5", producing 0–100.
- Interpretation: **the average SUS score is approximately 68**, and "a SUS score of 70 is actually right around the average score of 68, meaning it is at or around the 50th percentile" (CS-72). Lewis reports an overall mean of **70.8** across 11,855 questionnaires from 166 studies (CS-73).
- Treat SUS as **unidimensional** — Lewis recommends no longer computing Usability and Learnability subscales (CS-73).
- **SUS scores are not percentages.** Never write "the dashboard scored 72%."
- SUS is **free to use provided the source is acknowledged** (CS-72, CS-73).

---

## B. Short task-based usability measures

Questionnaires measure perception; tasks measure capability. Both are needed, and task completion is a behavioural measure rather than a survey construct — no validated questionnaire for it was located.

| # | Task | What it measures | Recorded as |
|---|---|---|---|
| T1 | "Show me today's heat risk level for your area." | Basic comprehension and orientation | Completed unaided / completed with prompt / not completed; time to complete |
| T2 | "Tell me in your own words what that level means." | **Unprompted comprehension** — directly targets the finding that recall collapses without prompting (CS-13) | Correct / partially correct / incorrect, against the official band definition |
| T3 | "Name one thing you would do today because of this." | **Unprompted action recall** — the measure that exposed the 5% vs 51% gap in CS-13 | Number of correct actions named unprompted |
| T4 | "Find who to contact if someone in your care becomes unwell." | Escalation-route findability | Completed / not completed; time |
| T5 | "Show me when this information was last updated." | Provenance and staleness awareness | Completed / not completed |
| T6 | *(Institutional users only)* "Show me whether this alert has been acknowledged, and by whom." | Whether the ownership and acknowledgement field is usable | Completed / not completed |

**Report task completion as a success rate** (proportion completing unaided) alongside median time. Do not convert task results into a satisfaction score.

---

## C. Acknowledgement and completion indicators

These are **service-generated** indicators, not survey items. They are the operational counterpart to the survey, and they exist because the evidence shows self-report alone is insufficient: prescribed acknowledgement was coupled to only 3.6% of real utterances against 7.7% in simulation (CS-47, clinical analogy) — **"we told them to confirm" is not evidence that confirmation happens.**

| Indicator | Definition | Why it is measured | Evidence |
|---|---|---|---|
| **Alert acknowledgement rate** | Institutional contact points confirming receipt ÷ contact points sent, per alert | Verifying receipt is a formal early-warning requirement (CS-14) that was absent in an operating national heat system (CS-18) | CS-14, CS-18 |
| **Time to acknowledgement** | Median and 90th-percentile interval from send to confirmation | Establishes the empirical basis for a future acknowledgement window | CS-43 [analogy] |
| **Non-acknowledgement escalation rate** | Proportion of non-acknowledgements that triggered a fallback attempt | Tests whether the fallback path actually fires | CS-14, CS-43 [analogy] |
| **Fallback success rate** | Proportion of fallback attempts that produced an acknowledgement | Tests whether the fallback works, not just whether it exists | CS-31, CS-27 |
| **Registry currency** | Proportion of institutional contacts verified within the last review cycle | Registry decay is a named failure mode; **no source quantifies its rate**, so this is a new measure | CS-46 [analogy] |
| **Channel mix actually used** | Distribution of first successful contact by channel | The only way to learn Thai channel reach, since no Thai study exists | CS-30, CS-23 |
| **Recipient profile vs target profile** | Age, region, occupation of those reached, against the intended at-risk profile | Directly tests the opt-in selection failure: 7.9% aged 65+, 6.6% outdoor, 2.4% agricultural in a real programme (CS-54) | CS-54 |
| **Dashboard return use** | Proportion of users returning within a defined window | Continuance, measured rather than self-reported | CS-66, CS-67, CS-68 |

> **Note on the last indicator.** Attrition benchmarks from the literature — one-month survival of 3.4% for active-engagement apps versus 27.3% for passive (CS-68), and "~71% disengage within 90 days" as reported in CS-67 — should be used for **direction and order of magnitude only**. Neither source is a comparable service; CS-68 is a Taiwanese work-hours app with a mean user age of 33.8.

---

## D. Open-ended interview questions

Six questions, for a 10–15 minute follow-up with a purposive subsample (older adults, outdoor workers, volunteers, non-users). Their purpose is to explain the numbers, especially the low ones.

1. "Tell me about the last time you heard a heat warning. What did you do?"
2. "Who would you believe most if they told you it was dangerously hot today — and why them?" *(Targets the trusted-messenger finding: many older respondents thought state intervention "unnecessary, intrusive and unlikely to be effective" — CS-61.)*
3. "Was there anything the warning asked you to do that you could not do? What stopped you?" *(Targets the feasibility barrier — CS-13, CS-30, CS-63.)*
4. "If you did not act on the warning, what was going through your mind?" *(Targets the personalisation gap — CS-61.)*
5. "How would you want to be told about dangerous heat — and is there anyone who should be told instead of, or as well as, you?" *(Targets channel preference and the caregiver/volunteer route.)*
6. "Is there anything about this service that would make you stop using it?" *(Targets abandonment reasons directly, since no validated instrument for this was located.)*

**For institutional respondents, substitute:** "When an alert arrives, what do you do next, and who do you hand it to?" and "Has an alert ever arrived and nothing happened? What happened that time?"

---

## E. Suggested calculation and interpretation method

### Calculation

1. **Per-item mean and distribution.** Report the mean (1 decimal place), the standard deviation, and **the full 1–5 distribution**. With prototype-sized samples the distribution is more informative than the mean, and a bimodal result would be invisible in a mean alone.
2. **Top-2-box percentage.** For each item, the proportion answering 4 or 5. This is the conventional CSAT-style headline and is easy for the team to read. **Report it alongside the mean, never instead of it.**
3. **Bottom-2-box percentage.** The proportion answering 1 or 2. For a safety-relevant service this matters more than the average — a mean of 4.0 that hides 15% at the bottom is a finding, not a success.
4. **Do not compute an overall composite score across items 1–10.** These items are drawn from different constructs and different instruments; summing them would create an unvalidated composite with no interpretation. Report constructs separately.
5. **SUS, if used, is scored by its own published formula only** (see Part A) and reported as 0–100 against the ~68 mean — never as a percentage.
6. **PEMAT and the CDC Index are expert-rated**, scored on the material rather than by users. PEMAT: (points ÷ total possible applicable points) × 100, with N/A items excluded from the denominator; **AHRQ publishes no pass/fail threshold**, so any threshold the project adopts is a project decision and must be labelled as such (CS-80). The CDC Index score sheet identifies **90 or above** as "Excellent" (CS-83, score sheet).
7. **Task measures** are reported as unaided completion rate and median time, separately from perception.
8. **Segment every result** by age band, region (urban/rural), occupation and channel of receipt. The entire evidence base says the average conceals the exclusion — Thai internet use is 90.9% nationally and 29.3% among the over-80s (CS-95 vs CS-93).

### Interpretation

- **Report the response profile against the target profile first, before any satisfaction number.** If the respondents are not the at-risk population, the satisfaction result describes the wrong people. This is the single most likely way this evaluation could mislead the team (CS-54, CS-13's 5.4% response rate).
- **Prefer within-prototype comparison over external benchmarking.** No benchmark exists for a heat information service. SUS's ~68 mean is the only external benchmark available and applies only to the interface module.
- **Do not use Net Promoter Score as an effectiveness indicator.** A longitudinal examination of 21 firms and over 15,500 interviews failed to replicate the claimed NPS superiority (CS-77), and the originating article is excluded from core evidence in this project (CS-78).
- **Treat low scores on trust, timeliness, relevance and channel preference as the most informative results**, because those constructs have no validated instrument and the project's items are new. A low score there identifies where measurement development is needed as much as where the service is weak.
- **Interpret task and survey results together.** High satisfaction with low unprompted action recall (T3) is the specific pattern the literature predicts (CS-13) and would be the most important single finding this evaluation could produce.

### Sample and administration notes

- Purposive rather than representative sampling is appropriate at prototype stage; **state this as a limitation** rather than implying generalisability.
- **Offer volunteer-assisted and in-person completion.** A digitally administered survey will reach the digitally included and systematically miss the population the service exists for.
- Administer in Thai; prepare Burmese, Khmer and Lao variants if migrant workers are included, since the national alert pipe does not carry those languages (CS-108, CS-111).
- Record which channel each respondent actually received the alert through, so results can be read by channel.

---

## Summary

- **Core survey: 10 items** (Part A), plus 5 optional follow-ups and an optional 10-item SUS module.
- **6 task measures** (Part B) and **8 service-generated indicators** (Part C).
- **6 open-ended questions** (Part D).
- **4 constructs — trust, timeliness, relevance and channel preference — have no validated instrument** and their items are newly proposed for this project.
- **No instrument in this framework has been validated for heat-warning services.**
- **CSAT does not demonstrate health impact**, and this evaluation must not be reported as if it does.
