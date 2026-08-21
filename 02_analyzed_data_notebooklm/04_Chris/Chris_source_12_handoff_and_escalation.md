# Chris Source 12 — Escalation Failure, Loop Closure and the Acknowledgement Gap

**Focus applied to this summary:** stakeholders, communication logistics, contact points, channels, handoffs, ownership, acknowledgement, fallback mechanisms, adoption, satisfaction and service usefulness. Contact-point level only.

> **Domain-transfer caveat — applies to this entire summary.** These are clinical-alerting and clinical-handoff studies, not public-health heat alerting. They are included because **no source located in this review measures acknowledgement rates in public-health mass notification** — targeted searching returned only vendor material, which was excluded. The mechanisms below are cited as **explicitly labelled analogy**, never as measured heat-alert performance.

## Citations

**(a)** Difonzo, M. (2019). Performance of the afferent limb of rapid response systems in managing deteriorating patients: a systematic review. *Critical Care Research and Practice*, 2019, 6902420. DOI: https://doi.org/10.1155/2019/6902420 — **Source ID:** CS-43 · Full text: PARTIAL.

**(b)** Callen, J.L., Westbrook, J.I., Georgiou, A. & Li, J. (2012). Failure to follow-up test results for ambulatory patients: a systematic review. *Journal of General Internal Medicine*, 27(10), 1334–1348. DOI: https://doi.org/10.1007/s11606-011-1949-5 — **Source ID:** CS-45 · Full text: PARTIAL.

**(c)** Zimolzak, A.J., Shahid, U., Giardina, T.D., Memon, S.A., Mushtaq, U., Zubkoff, L., Murphy, D.R., Bradford, A. & Singh, H. (2022). Why test results are still getting "lost" to follow-up: a qualitative study of implementation gaps. *Journal of General Internal Medicine*, 37(1), 137–144. DOI: https://doi.org/10.1007/s11606-021-06772-y — **Source ID:** CS-46 · Full text: PARTIAL.

**(d)** Fornander, L., Garrido Granhagen, M., Molin, I., Laukkanen, K., Björnström Karlsson, K., Berggren, P. & Nilsson, L. (2024). The use of specific coordination behaviours to manage information processing and task distribution in real and simulated trauma teamwork. *Scandinavian Journal of Trauma, Resuscitation and Emergency Medicine*, 32, 51. DOI: https://doi.org/10.1186/s13049-024-01287-x — **Source ID:** CS-47 · Full text: PARTIAL.

**(e)** Starmer, A.J., Spector, N.D., Srivastava, R., West, D.C., Rosenbluth, G., et al. for the I-PASS Study Group (2014). Changes in medical errors after implementation of a handoff program. *New England Journal of Medicine*, 371(19), 1803–1812. DOI: https://doi.org/10.1056/NEJMsa1405556 — **Source ID:** CS-44 · Full text: NO (record only) · **Independently re-verified:** PASS on the headline figures.

## Research context

Five studies covering the four logistics questions this project must answer: does escalation happen when a trigger is met; do loops close on information already generated; who owns the next step; and does prescribed acknowledgement actually occur.

## Stakeholders

Clinicians expected to escalate; rapid response teams; ordering providers, attendings and primary care physicians; trauma teams. **By analogy:** whoever in a heat service is expected to act on a threshold crossing.

## Contact points and handoffs

The analogous contact point is the moment responsibility transfers from the party that detected a signal to the party expected to act on it.

## Information transferred

A threshold crossing that has already been detected and is already available to a named recipient. This is exactly the HeatShield situation: the risk is known, and the question is whether the handoff completes.

## Acknowledgement or escalation — the core findings

**Escalation fails even when an objective trigger is met (CS-43).** Across published cohorts, escalation was missed or delayed in **"22.8% (131/575)"**, **"30.2% (947/3,135)"**, **"57% (977/1,725)"** and **"24.6% (203/826)"** of cases. Delay carried consequences: **"Delayed calls increased…death (adjusted OR 1.79, 95% CI 1.43–2.27, p<0.001)"**; unplanned ICU admission OR 1.79 (95% CI 1.33–2.93); 30-day mortality 61.8% (152/246) delayed versus 41.9% (378/902) timely, p<0.001.

**Loops fail to close on information already generated (CS-45).** Failure to follow up ranged **6.8% (79/1163) to 62% (125/202)** for laboratory tests and **1.0% (4/395) to 35.7% (45/126)** for radiology. **The lowest failure rate involved alerts delivered through computerised provider order entry** — i.e. attaching an explicit electronic notification to the originating order improved closure.

**Prescribed acknowledgement is not observed acknowledgement (CS-47).** Closed-loop communication was coupled to **"3.6% of all utterances"** in real trauma resuscitations versus **"7.7%"** in simulation, **"p ≤ 0.001"**. Trained teams under direct observation acknowledged informally rather than completing check-back loops. *(Note the denominator: this is utterance-level, so it is not "3.6% of instructions were acknowledged.")* The design lesson is blunt: **"we told them to confirm" is not evidence that confirmation happens** — acknowledgement must be instrumented, not assumed.

**Structuring the transfer point works (CS-44).** After implementing a structured handoff programme, medical errors fell from **24.5 to 18.8 per 100 admissions (−23%, P<0.001)** and preventable adverse events from **4.7 to 3.3 (−30%, P<0.001)**, "without a negative effect on workflow."

## Failure points — ownership

CS-46 names the mechanism in providers' own words: there is "a lack of clarity among providers (including themselves) about whether the responsible clinician… should be the ordering provider, the inpatient attending of record, or the PCP"; **"the VA lacks a backup system for tracking EHR notifications related to abnormal test results"**; providers "are overwhelmed by the number of EHR notifications"; and the system "lacks a more compelling visualization to prioritize notifications based on urgency; many are given the same weight and volume, which leads to a poor signal-to-noise ratio." Most directly relevant to HeatShield: alerts routed to a role-holder who has rotated away **silently disappear** — results were "missed or found by chance" when notifications went to "trainees who had completed their rotations."

## Adoption or satisfaction findings

CS-44's "without a negative effect on workflow" is the closest thing to an adoption finding: structured handoff did not cost the users time, which is why it was sustained.

## Relevance to this project

Four design positions follow, each labelled as analogy-informed rather than heat-evidenced:

1. **Route alerts to a role, not a person.** The rotated-trainee failure in CS-46 is precisely what happens when a contact registry ages.
2. **Tier alerts by urgency.** Flat prioritisation destroys signal-to-noise.
3. **Instrument acknowledgement rather than mandating it.** CS-47 shows mandating alone does not produce it.
4. **Attach acknowledgement to the originating record.** CS-45 found the lowest loop-closure failure where notification was tied to the order itself.

## Limitations

All five are clinical. Escalation-delay definitions differ across the studies pooled in CS-43, and all are observational, so confounding by severity is plausible. CS-45's studies predate 2012 and use heterogeneous definitions of "follow-up". CS-46 is qualitative, single health system, with no incidence rates. CS-47 is single-country, utterance-level. CS-44 is pre–post without a concurrent control, and only the record was accessed. **None of these figures may be presented as a heat-alert acknowledgement or escalation rate.**

## Supported claims

1. Even where an objective trigger threshold is met and a named response team exists, escalation is missed or delayed in roughly 23–57% of cases across published clinical cohorts.
2. Delayed escalation was associated with increased odds of death (adjusted OR 1.79, 95% CI 1.43–2.27, p<0.001).
3. Failure to close the loop on an already-generated result ranged from 6.8% to 62% for laboratory tests and 1.0% to 35.7% for radiology; the lowest rates involved alerts delivered through computerised order entry.
4. Diffusion of responsibility between ordering clinician, attending and primary care physician is a provider-acknowledged cause of lost results, and alerts routed to a role-holder who has rotated away silently disappear.
5. Undifferentiated alert priority produces a poor signal-to-noise ratio and provider overload.
6. Closed-loop communication was coupled to only 3.6% of utterances in real trauma teamwork versus 7.7% in simulation (p ≤ 0.001) — prescribed acknowledgement is not observed acknowledgement.
7. A structured handoff programme reduced medical errors by 23% and preventable adverse events by 30% without a negative effect on workflow.
8. All of the above are clinical findings cited by analogy; no source located in this review measures acknowledgement rates in public-health mass notification.
