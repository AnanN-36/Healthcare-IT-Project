# Chris Source 14 — Dashboards Are a Pull Channel with Almost No Behavioural Evidence Base

**Focus applied to this summary:** stakeholders, communication logistics, contact points, channels, handoffs, ownership, acknowledgement, fallback mechanisms, adoption, satisfaction and service usefulness. Contact-point level only.

## Citations

**(a)** Schulze, A., Brand, F., Geppert, J. & Böl, G.-F. (2023). Digital dashboards visualizing public health data: a systematic review. *Frontiers in Public Health*, 11, 999958. DOI: https://doi.org/10.3389/fpubh.2023.999958 — **Source ID:** CS-36 · Full text: YES (open access).

**(b)** Rojo, E.M. & Bosworth, H.B. (2026). Navigating the heat: implementation challenges and opportunities for heat alert communication and rural health data infrastructure. *Frontiers in Public Health*, 14, 1801198. DOI: https://doi.org/10.3389/fpubh.2026.1801198 — **Source ID:** CS-54 · Full text: YES (open access).

**(c)** Mileti, D.S. & Peek, L. (2000). The social psychology of public response to warnings of a nuclear power plant accident. *Journal of Hazardous Materials*, 75(2–3), 181–194 — **Source ID:** CS-37.

## Research context

CS-36 is a systematic review of 65 dashboard studies (2010–2020, nine databases). CS-54 is a peer-reviewed implementation article on a US state heat alert service. CS-37 is a foundational warning-response paper. Together they answer the question the whole project rests on: **what can a dashboard actually be expected to do?**

## Stakeholders

Epidemiologists, statisticians, data modellers, medical professionals and the general public (CS-36); heat alert subscribers, older adults, outdoor and agricultural workers, rural clinics (CS-54).

## Contact points

A dashboard is a **pull** contact point: it reaches only people who choose to visit it. An alert is a **push** contact point. The two are not substitutes.

## Information transferred

Risk status, location, timestamp, provenance — and, in CS-54's case, the alert email itself.

## Channels

CS-54 documents a real single-channel dependency: the service "delivers alerts via email notifications when forecasted temperatures are expected to reach unhealthy levels."

## Handoffs and ownership

CS-54 quantifies the **contact-registry problem** — the most directly transferable finding in this summary. In an opt-in, email-only heat alert channel, **only 7.9% of subscribers were aged 65+, 6.6% worked outside and 2.4% worked in agriculture.** The service had a subscriber base that was not the at-risk population. Opt-in registration silently selects *away* from the people the service exists for.

## Acknowledgement or escalation

Not addressed by CS-36. CS-54 identifies the feedback-loop failure instead: "gaps remain in settings where care-seeking occurs outside traditional emergency pathways", so "surveillance data may underestimate the true burden, timing, and geographic distribution" of heat-related illness — and **"occupational information—an essential determinant of heat exposure risk—is not systematically captured within the surveillance system."** The data needed to evaluate whether the service worked is systematically incomplete.

## Failure points

- **Only 18 of 65 dashboard studies included any user study**, and studies evaluating dashboard content against risk-communication constructs such as risk perception or health literacy are "comparatively rare".
- **"The benefits of dashboards for risk reduction or risk behavior change will remain without evidence"** if user needs remain unexamined.
- Methodological quality of the user studies that did exist was low (MMAT average ~40%; qualitative 55%, quantitative 29%).
- Access barriers: rural infrastructure limits access; "small screen for displaying complex tables"; user acceptance is gated by technical understanding and training; compatibility with existing workflows is essential for adoption.
- CS-54: "rural and low-resource areas—particularly those with large farmworker populations—experience more variable internet access and lower digital literacy."

## Adoption or satisfaction findings

CS-36 records a **user-expressed requirement**: users asked for interactive features, **notifications**, and networking capability. Dashboard users themselves say the pull channel needs a push layer.

CS-37 supplies the complementary mechanism: people seek **confirmation** from a second source before acting, which makes a dashboard a good confirmation destination — **but only if it is consistent with the push message.** CS-37 reports that 83% of those who left during the Three Mile Island incident cited conflicting information as a reason. Multi-channel delivery improves understanding, belief and response *only if messages are consistent across channels*.

## Relevance to this project

This is the most important source for keeping HeatShield's claims honest:

1. **The dashboard alone cannot be claimed to change behaviour.** The systematic review says the evidence does not exist. The project's honest claim is that the dashboard supports coordination and interpretation, and that a paired push channel does the reaching.
2. **The dashboard's best-evidenced role is as the confirmation destination** people go to after a push alert — which raises consistency between channels from a nicety to a requirement.
3. **Opt-in is a structural receipt failure.** CS-54 quantifies exactly how badly an opt-in list can mis-select. HeatShield should not assume its registered users are its at-risk users.
4. **The under-evaluation gap is an opportunity.** Only 18 of 65 dashboard studies did any user testing — the CSAT-style prototype evaluation in `Chris_csat_adoption_evaluation.md` legitimately addresses a documented gap.

## Limitations

CS-36 covers 2010–2020 and so predates most heat-specific dashboards; dashboard definitions are heterogeneous; the review notes it cannot guarantee it found all eligible studies. CS-54 is a perspective/implementation article rather than a primary empirical study, covers a single US state programme, and was published in 2026 with no replication. CS-37 concerns a nuclear incident, not heat.

## Supported claims

1. Only 18 of 65 studies in a systematic review of public health dashboards included any user study.
2. The benefits of dashboards for risk reduction or risk behaviour change will remain without evidence if user needs remain unexamined.
3. Dashboard users request notifications — a pull channel needs a paired push layer.
4. An opt-in, email-only heat alert channel reached a subscriber base of which only 7.9% were aged 65+, 6.6% worked outside and 2.4% worked in agriculture.
5. Occupational information, an essential determinant of heat exposure risk, is not systematically captured in the surveillance system used to evaluate such services.
6. Multi-channel delivery improves understanding, belief and response only if messages are consistent across channels; 83% of those who evacuated during the Three Mile Island incident cited conflicting information as a reason.
