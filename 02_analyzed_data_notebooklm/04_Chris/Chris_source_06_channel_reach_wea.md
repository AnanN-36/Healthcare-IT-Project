# Chris Source 06 — Measured Reach of the Most Universal Digital Push Channel

**Focus applied to this summary:** stakeholders, communication logistics, contact points, channels, handoffs, ownership, acknowledgement, fallback mechanisms, adoption, satisfaction and service usefulness. Contact-point level only.

## Citation

Parker, A.M., Steratore, R., Bradley, M.A., LaForce, S., Woods, D., Setodji, C.M., Hassler, G.W., Tierney, D., Villegas, C.A. & Cecchine, G. (2024). *Assessing Public Reach of the 2023 National Test of the Wireless Emergency Alerts (WEA) System: Results of a National Survey*. RAND Homeland Security Operational Analysis Center, for FEMA/DHS.
DOI: https://doi.org/10.7249/RRA2451-1
**Source ID:** CS-23 · **Source type:** Government-commissioned warning-system evaluation (national probability survey) · **Full text:** YES.

## Research context

A national probability survey measuring who actually received the 4 October 2023 nationwide WEA test in the United States. Because it measures a *nationwide test at a known time*, it is a **best case** — the ceiling for cell-broadcast reach, not a typical emergency.

## Stakeholders

US adults with working cell phones, disaggregated by age, metropolitan status, carrier, device generation, disability status and subsidised-phone status; FEMA as the alert originator.

## Contact points

Alert originator → mobile network → handset → individual. No registration and no app are required, which is why cell broadcast is the highest-reach digital channel available.

## Information transferred

A short broadcast alert message to every compatible handset in the target area.

## Channels

Cell broadcast (Wireless Emergency Alerts), i.e. a push channel that is independent of a contact list.

## Handoffs and ownership

Originating authority owns issuance; carriers own delivery; the individual owns the response. Notably, the individual also owns an **opt-out** — which is where the channel leaks.

## Acknowledgement or escalation

None. Cell broadcast is one-way and provides no receipt confirmation to the sender. Reach had to be measured by an after-the-fact national survey, which is itself an argument for building acknowledgement into any channel where it is technically possible.

## Failure points

- **9% did not receive it** even under ideal test conditions.
- **Age gradient:** adults aged 36–65 and 65+ had **23–52% lower odds** of receipt than 18–35s — the gradient runs against heat vulnerability.
- **Rural penalty:** non-metropolitan residents had **22–49% lower odds** of receipt.
- **Device and carrier variation:** uncommon phone brands 24% lower odds than iPhones; WEA 3.0 devices 42% higher odds than WEA 1.0.
- **Opt-out leakage:** ~**17.5%** had opted out of at least one WEA alert type, and respondents with **subsidised phones had 189% higher odds of opting out** — the free, universal channel is least reliable among the poorest users.
- Only **67%** had heard of WEA before the test.

## Adoption or satisfaction findings

The 67% prior-awareness figure is an adoption finding: a third of the population did not know the channel existed before receiving from it. The report explicitly separates receipt from usability — "no significant differences were observed in WEA receipt among people with disabilities", **but the report flags that receipt is not accessibility**, and that font legibility, text-to-speech and plain language need further research. This distinction must be preserved in any citation.

## Relevance to this project

Sets a realistic ceiling. If the single most universal digital push channel in a high-income country misses ~9% under test conditions, and misses disproportionately older, rural and poorer users, then **no digital channel alone can be the delivery guarantee for a heat service targeting exactly those groups.** This is the quantitative basis for the fallback requirement in `Chris_channel_strategy.md`.

## Limitations

Self-reported receipt, so recall error is possible; a single national test at a pre-announced time is a best case rather than a representative emergency; does not measure comprehension or protective action; disability categories are broad. United States only — Thai cell-broadcast reach is not measured anywhere (see CS-108).

## Supported claims

1. 91% of US adults with working cell phones received the 4 October 2023 national WEA test alert.
2. Adults aged 36–65 and 65+ had 23–52% lower odds of receipt than adults aged 18–35.
3. Non-metropolitan residents had 22–49% lower odds of receipt.
4. Approximately 17.5% had opted out of at least one WEA alert type, and respondents with subsidised phones had 189% higher odds of opting out.
5. Only 67% had heard of WEA before the test.
6. No significant difference in WEA *receipt* was observed among people with disabilities — but the report states that receipt is not the same as accessibility.
