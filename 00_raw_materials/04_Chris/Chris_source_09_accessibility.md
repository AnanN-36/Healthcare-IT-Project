# Chris Source 09 — Accessibility, Language and Digital Exclusion

**Focus applied to this summary:** stakeholders, communication logistics, contact points, channels, handoffs, ownership, acknowledgement, fallback mechanisms, adoption, satisfaction and service usefulness. Contact-point level only.

## Citations

**(a)** MacPherson-Krutsky, C., Painter, M.A. & Villarreal, M. (2024). *Inclusive Emergency Alerts for Colorado: An Assessment and Recommendations for Language and Disability Considerations*. Natural Hazards Center, University of Colorado Boulder.
URL: https://hazards.colorado.edu/uploads/freeform/final-report-12-8-24-eng-report-only.pdf — **Source ID:** CS-34 · Full text: YES.

**(b)** International Telecommunication Union (2025). *Measuring digital development: Facts and Figures 2025*.
URL: https://www.itu.int/itu-d/reports/statistics/facts-figures-2025/ — **Source ID:** CS-26 · Full text: PARTIAL (landing page and full press release; statistical annex not opened).

**(c)** World Wide Web Consortium (2024). *Web Content Accessibility Guidelines (WCAG) 2.2*. W3C Recommendation, **12 December 2024**.
URL: https://www.w3.org/TR/WCAG22/ — **Source ID:** CS-38 · **Independently re-verified:** PARTIAL — the live Recommendation is dated 12 December 2024, not the commonly cited 5 October 2023.

## Research context

Three complementary sources: an agency-survey assessment of who can actually issue a non-English alert; the authoritative global statistics on who is reachable by any internet-dependent channel at all; and the normative technical standard for accessible presentation.

## Stakeholders

Limited-English-proficiency communities including undocumented immigrants; people with disabilities; alerting agencies; community-based organizations; globally, the 2.2 billion people who are offline.

## Contact points

Agency → translation capability → recipient; and, where the agency route fails, agency → community-based organization → recipient.

## Information transferred

The alert text, plus whatever survives translation. CS-34's worked example of machine-translation failure — **"Eagle County" rendered as "bird County"** — shows the information can arrive corrupted rather than not at all.

## Channels

All channels, considered from the exclusion side rather than the reach side.

## Handoffs and ownership

CS-34's central argument is that for immigrant communities the effective owner of the last mile is **not the agency but a community-based organization with an established trust relationship**. The agency owns issuance; trust determines whether anyone acts.

## Acknowledgement or escalation

Not addressed. CS-34 does note that LEP communities "must seek out emergency information from other sources that may be informal or unreliable" — i.e. absent an accessible official channel, people improvise one.

## Failure points

**Translation capacity and latency (CS-34):**
- **53.2%** of agencies report multilingual capability; **36%** are uncertain; **7.2%** know they lack it.
- Of those that translate, **83.9% use automatic translation**, which produces "inaccurate or confusing" messages; 29.7% rely on multilingual staff; 17.8% contract real-time interpretation.
- Certified interpreter services take **5–10 minutes**, "insufficient for fast-moving emergencies".
- **"Pre-translated templates remain underutilised despite proven effectiveness."**
- **Funding is the top barrier, cited by 64% of agencies.**
- Five documented LEP barriers: English-only distribution; translation delay; loss of cultural context; trust deficit; unfamiliarity with the hazard among recent immigrants.

**Structural digital exclusion (CS-26):**
- **6 billion people (~75%) use the internet in 2025; 2.2 billion (~25%) remain offline.**
- High-income countries **94%** online versus low-income **23%**; **96% of the offline population lives in low- and middle-income countries.**
- Rural **58%** versus urban **85%**. Men **77%** versus women **71%**. Ages 15–24 **82%** versus everyone else **72%** — the age skew runs directly against heat vulnerability.
- Coverage is not usage: 5G covers 55% of the global population but only **4% in low-income countries**, and data-only mobile broadband is unaffordable in roughly **60%** of low- and middle-income countries.

**Presentation (CS-38):** colour-coded risk tiers require a non-colour text equivalent to conform.

## Adoption or satisfaction findings

CS-34's trust finding is an adoption finding: undocumented residents show "reluctance to respond to messages or seek help due to fear." Reach and trust are separate failure modes, and improving reach does not fix trust.

## Relevance to this project

Supplies four concrete prototype requirements: (a) **pre-translated message templates** prepared before the season, since live translation is too slow and machine translation is unreliable; (b) every colour tier carries a text equivalent (e.g. "Level 3 of 4 — High"); (c) a community-organization delivery route for populations that will not act on a state message; (d) an explicit statement in the roadmap that a quarter of the world — skewed rural, older, poorer and female — cannot be reached by any internet-dependent channel.

## Limitations

CS-34 is single-state, agency self-report, and does not directly measure LEP residents' receipt rates. CS-26 uses country-level estimates of varying quality, and its press release does not numerically separate the coverage gap from the usage gap. CS-38 is a technical standard, not evidence of comprehension; the claim that WCAG Level AA is *legally* required was **not** verified from any legal source and is not asserted here.

## Supported claims

1. 53.2% of surveyed alerting agencies report multilingual capability; of those that translate, 83.9% use automatic translation, which produces inaccurate or confusing messages.
2. Certified interpreter services take 5–10 minutes, which is insufficient for fast-moving emergencies; pre-translated templates remain underutilised despite proven effectiveness.
3. Funding is the top barrier to inclusive alerting, cited by 64% of agencies.
4. Trust, not technology, is the binding constraint for immigrant communities, and community-based organizations are the recommended delivery route.
5. In 2025, 2.2 billion people (~25% of the world) remain offline; rural 58% versus urban 85%; low-income countries 23% versus high-income 94%.
6. WCAG 2.2 (W3C Recommendation, 12 December 2024) requires a text equivalent for information conveyed by colour.
