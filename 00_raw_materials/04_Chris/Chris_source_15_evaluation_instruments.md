# Chris Source 15 — Established Measurement Instruments for Prototype Evaluation

**Focus applied to this summary:** stakeholders, communication logistics, contact points, channels, handoffs, ownership, acknowledgement, fallback mechanisms, adoption, satisfaction and service usefulness. Contact-point level only.

## Citations

**(a)** Brooke, J. (1996). SUS: a quick and dirty usability scale. In P.W. Jordan, B. Thomas, B.A. Weerdmeester & I.L. McClelland (Eds.), *Usability Evaluation in Industry* (pp. 189–194). London: Taylor & Francis. Instrument sheet verified at AHRQ: https://digital.ahrq.gov/sites/default/files/docs/survey/systemusabilityscale%2528sus%2529_comp%255B1%255D.pdf — **Source ID:** CS-70 · Full text: YES · **Independently re-verified:** PASS.

**(b)** Brooke, J. (2013). SUS: a retrospective. *Journal of Usability Studies*, 8(2), 29–40. https://uxpajournal.org/wp-content/uploads/sites/7/pdf/JUS_Brooke_February_2013.pdf — **Source ID:** CS-72 · Full text: YES.

**(c)** Lewis, J.R. (2018). The System Usability Scale: past, present, and future. *International Journal of Human–Computer Interaction*, 34(7), 577–590. DOI: https://doi.org/10.1080/10447318.2018.1455307 — **Source ID:** CS-73 · Full text: YES (via mirror; **retrieve the publisher copy for the final reference list**) · **Independently re-verified:** PASS.

**(d)** Agency for Healthcare Research and Quality (n.d.). *Patient Education Materials Assessment Tool (PEMAT) and User's Guide*. https://www.ahrq.gov/health-literacy/patient-education/pemat2.html — **Source ID:** CS-80 · and the PEMAT-A/V instrument, **Source ID:** CS-81 · Full text: YES.

**(e)** Centers for Disease Control and Prevention (n.d.). *CDC Clear Communication Index*. https://www.cdc.gov/ccindex/index.html and score sheet https://www.cdc.gov/ccindex/pdf/full-index-score-sheet.pdf — **Source ID:** CS-83 · **Independently re-verified:** PARTIAL — the 20-item count is on the overview page; **the 90-point threshold is on the score sheet, not the overview page.**

**(f)** World Health Organization (2016). *Monitoring and evaluating digital health interventions: a practical guide to conducting research and assessment*. Geneva: WHO. ISBN 978 92 4 151176 6. https://www.who.int/publications/i/item/9789241511766 — **Source ID:** CS-87 · Full text: YES (via mirror).

**(g)** Keiningham, T.L., Cooil, B., Andreassen, T.W. & Aksoy, L. (2007). A longitudinal examination of Net Promoter and firm revenue growth. *Journal of Marketing*, 71(3), 39–51. DOI: https://doi.org/10.1509/jmkg.71.3.039 — **Source ID:** CS-77 · Full text: NO (abstract) · **Independently re-verified:** PASS on existence and critical framing.

## Research context

The measurement question for this project is narrow: which constructs can be measured with a published, citable instrument, and which must be newly proposed and labelled as such.

## Stakeholders

Prototype testers; the project team as evaluators; expert raters (for PEMAT and the CDC Index, which rate the *material*, not the user).

## Contact points / Information transferred / Channels / Handoffs / Acknowledgement

Not applicable — these are measurement instruments.

## Instruments verified

**System Usability Scale (CS-70, CS-72, CS-73).** Ten items, five-point agreement scale. Scoring verified verbatim: "For items 1,3,5,7,and 9 the score contribution is the scale position minus 1. For items 2,4,6,8 and 10, the contribution is 5 minus the scale position", then "multiply the sum of the scores by 2.5", giving 0–100. **All ten item wordings are verified and quotable.** Benchmarks: **"A SUS score of 70 is actually right around the average score of 68, meaning it is at or around the 50th percentile"** (CS-72); Lewis (CS-73) reports **"the overall SUS mean was 70.8"** across **11,855 questionnaires from 166 studies**, coefficient alpha 0.83–0.97 averaging ~0.91, and recommends treating SUS as **unidimensional** — "no longer routinely compute or report Usability and Learnability subscales." The Sauro–Lewis curved grading scale is verified in full (A ≥ 80.8; C = 65.0–71.0; F ≤ 51.6). **SUS is free to use provided the source is acknowledged.** Critically: **SUS scores are not percentages** — never write "our system scored 72%".

**PEMAT (CS-80, CS-81).** Understandability and actionability are scored **separately** as (points ÷ total possible applicable points) × 100, with N/A items excluded from the denominator. **AHRQ publishes no pass/fail threshold** — any threshold the project adopts is a project decision and must be labelled as such. The four **actionability** items are verified verbatim and are the only quotable validated actionability wording located in this review: (1) "The material clearly identifies at least one action the user can take."; (2) "The material addresses the user directly when describing actions."; (3) "The material breaks down any action into manageable, explicit steps."; (4) **"The material explains how to use the charts, graphs, tables, or diagrams to take actions."** — the fourth is directly applicable to a heat-risk dashboard.

**CDC Clear Communication Index (CS-83).** Four introductory unscored questions plus **20 scored items** in four parts: Part A core/message clarity (11), Part B behavioural recommendations (3), Part C numbers (3), **Part D risk (3)**. The dedicated risk-communication section makes it directly applicable to a heat-risk message. The **90-point "Excellent" threshold is confirmed on the score sheet**, not the overview page.

**WHO M&E guidance (CS-87).** Establishes a maturity continuum — pre-prototype → prototype → pilot → demonstration → scale-up — and states that teams must agree where an intervention sits "in order to determine the appropriate evaluation activities and **avoid embarking on premature assessments**."

**Net Promoter Score (CS-77, CS-78).** Keiningham et al. examined 21 firms and 15,500+ interviews and **failed to replicate the claimed NPS superiority**. The originating HBR article (CS-78) is **excluded from core evidence**: practitioner magazine, paywalled, and its calculation could not be verified from any admissible source.

## Failure points

**Constructs with no validated instrument located: timeliness, relevance, and channel preference.** Trust is only *partially* covered — the McKnight et al. (2002) items were behind a paywall and the Jian et al. (2000) trust-in-automation scale is excluded (items not publicly available; independent review rated its psychometric evidence at 46%). **No instrument located in this review has been validated for heat-warning services.** Every one was validated in another domain.

Item wording could **not** be verified for TAM, UTAUT, UTAUT2, UMUX, UMUX-LITE, PSSUQ/CSUQ, ACSI, McKnight or NASA-TLX. Those instruments are therefore named as construct sources but **their items are not reproduced anywhere in the Chris deliverables.**

## Adoption or satisfaction findings

The framing finding: WHO explicitly warns against premature outcome assessment. Combined with Sheridan's 90%-aware / 46%-acted result (CS-13), this supports the project's central caution — **satisfaction and reach are not health impact.**

## Relevance to this project

Justifies the design of `Chris_csat_adoption_evaluation.md`: a short usability/clarity/acceptability evaluation appropriate to a prototype, built on SUS (or a subset), PEMAT actionability, and the CDC Index risk section, with newly proposed items clearly flagged where no validated instrument exists — and an explicit statement that CSAT does not demonstrate health impact.

## Limitations

PEMAT and the CDC Index rate the **material**, not the audience's actual comprehension, and require trained raters; PEMAT's binary rating gives coarse resolution. SUS measures perceived usability only — not trust, relevance, timeliness or outcome. CS-73 was read via a third-party mirror. CS-87 is consensus guidance, not empirical evidence, and prescribes no specific survey instrument. Two provenance flags apply: the PEMAT-A/V PDF was read at a university mirror and the WHO guide at a third-party mirror, because the canonical paths returned HTTP 403.

## Supported claims

1. SUS is a 10-item, 0–100 instrument scored by subtracting 1 from odd-item positions and subtracting even-item positions from 5, summing and multiplying by 2.5.
2. The average SUS score is approximately 68, and a score of 70 sits near the 50th percentile; Lewis (2018) reports an overall mean of 70.8 across 11,855 questionnaires from 166 studies.
3. SUS scores are not percentages, and SUS should be treated as unidimensional rather than reported as Usability and Learnability subscales.
4. SUS is free to use provided the source is acknowledged.
5. PEMAT scores understandability and actionability separately as percentages of applicable items, and AHRQ publishes no pass/fail threshold.
6. PEMAT actionability comprises four binary expert-rated items, including whether the material explains how to use charts, graphs, tables or diagrams to take actions.
7. The CDC Clear Communication Index comprises 20 scored items across four parts including a dedicated risk-communication section; the score sheet identifies 90+ as "Excellent".
8. WHO guidance states that evaluation activities must match the maturity stage of a digital health intervention and warns teams to avoid embarking on premature assessments.
9. A longitudinal examination of 21 firms and over 15,500 interviews failed to replicate the claimed superiority of the Net Promoter Score.
10. No instrument located in this review has been validated specifically for heat-warning services.
