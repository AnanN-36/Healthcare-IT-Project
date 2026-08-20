# Chris Source 08 — Why "Multi-Channel" Digital Designs Contain No Real Redundancy

**Focus applied to this summary:** stakeholders, communication logistics, contact points, channels, handoffs, ownership, acknowledgement, fallback mechanisms, adoption, satisfaction and service usefulness. Contact-point level only.

## Citations

**(a)** US Federal Communications Commission, Public Safety and Homeland Security Bureau (2024). *Communications Status Report for Areas Impacted by Hurricane Helene*, 1 October 2024, 9:00 a.m. EDT (Disaster Information Reporting System).
URL: https://docs.fcc.gov/public/attachments/DOC-406055A1.pdf — **Source ID:** CS-31 · Full text: YES.

**(b)** British Columbia Coroners Service (2022). *Extreme Heat and Human Mortality: A Review of Heat-Related Deaths in B.C. in Summer 2021*. Death Review Panel report, 7 June 2022. Burnaby, BC.
URL: https://www2.gov.bc.ca/assets/gov/birth-adoption-death-marriage-and-divorce/deaths/coroners-service/death-review-panel/extreme_heat_death_review_panel_report.pdf — **Source ID:** CS-27 · Full text: YES · **Independently re-verified:** PASS (619 / 67% / 56% / 98% all confirmed verbatim).

## Research context

Two official investigations that together answer the fallback question. CS-31 is primary regulator data on how communications infrastructure fails. CS-27 is a statutory death-review panel covering the **complete population** of heat deaths in a jurisdiction during the June 2021 heat dome — the closest thing in this evidence base to a controlled observation of who a heat warning fails to reach.

> Hazard-transfer note: CS-31 is a hurricane, not a heat event. The failure *mechanism* — loss of commercial power to cell sites — is hazard-agnostic, and heat events co-occur with grid stress, so the mechanism transfers even though the event does not.

## Stakeholders

CS-31: all residents of the disaster area; 911 call centres; broadcasters; carriers. CS-27: 619 heat-death decedents; socially isolated older adults; families and support workers; 911 and ambulance services; Environment and Climate Change Canada; local governments.

## Contact points

Alert originator → network → device → individual (CS-31); and person-to-person wellness check → isolated individual (CS-27).

## Information transferred

Heat alerts and public health messaging; and, in the fallback case, direct observation of a person's condition.

## Channels and their correlated failure

The decisive finding for channel strategy is **common-cause failure**:

- **21.7% of all cell sites in the affected area were out of service — up from 9.1% the previous day.** The outage *worsened* on day two as generator fuel and batteries ran down.
- North Carolina: **707 of 1,452 cell sites out — 48.7% (down from 54.0%).**
- **The dominant cause was loss of commercial power, not damage:** North Carolina 338 power / 303 transport-backhaul / **only 3 damage**; South Carolina 416 power / 76 transport / 8 damage. (The verification pass separately recorded region-wide totals of 692 power and 624 transport/backhaul against 20 damage.)
- **796,999 wireline/cable subscribers were out of service simultaneously** — landline, home broadband, email and any web dashboard failed at the same time, from the same cause.
- **Broadcast degraded far less:** only 5 TV, 34 FM and 6 AM stations off air across six states.

**Implication: SMS + email + dashboard is not a redundant set.** They share a single point of failure (grid power). A battery radio needs no grid and is a genuinely independent layer.

## Handoffs and ownership

CS-27 documents the handoff that actually saved or would have saved lives: **50% of the deceased were found during wellness checks** by family, friends, support workers, health workers or police; a further 32% during routine contact and 12% when someone witnessed an event.

## Acknowledgement or escalation

CS-27 shows the escalation channel **saturating precisely at peak demand**: 911 calls doubled (**11,970 on 28 June versus a typical 6,000–7,000**); **52% of calls on 29 June took more than 5 seconds to answer**; ambulance dispatch rates fell to **74–80%** against 90%+ normally; and in **six instances callers were told no ambulance was available.** A telephone-based fallback is least available exactly when it is most needed.

## Failure points

CS-27 states the exclusion problem in its own words: **"not everyone accesses social media, has a phone, can read signage or speaks English as their primary language."** It also records that "there was a lag between the heat alerts issued by Environment and Climate Change Canada (ECCC) and public agencies and the public response" — broadcast and digital alerts were issued and still failed to move the most vulnerable.

## Adoption or satisfaction findings

The decedent profile is the adoption finding in its starkest form: **619 deaths; 67% aged 70+; 90% over 60; 56% lived alone; 98% died indoors; 91% had at least one chronic disease registry listing**, and over 60% had seen a health professional in the prior month. The people the service most needed to reach were reachable through the health system and were not reached by broadcast alerts.

## Relevance to this project

Three direct consequences for HeatShield: (a) a fallback channel must have an **independent failure mode**, not merely a different app; (b) telephone escalation must be assumed to degrade during the event it is meant to serve; (c) the highest-value contact point for isolated older adults is a **person**, and the registry data to target those visits already exists inside the health system.

## Limitations

CS-31 is a hurricane; DIRS reporting is a snapshot and percentages are of reporting carriers. CS-27 is a single jurisdiction and a single extreme event; a retrospective death review cannot establish the counterfactual and does not measure per-channel receipt rates.

## Supported claims

1. 21.7% of cell sites in the affected area were out of service, rising from 9.1% the previous day; North Carolina reached 48.7%.
2. The dominant cause of cell-site outage was loss of commercial power and backhaul, not physical damage.
3. 796,999 wireline/cable subscribers were out of service at the same time — cellular, wireline and home broadband fail together from a common cause.
4. Broadcast radio and TV degraded far less (5 TV, 34 FM, 6 AM stations off air across six states).
5. In the 2021 BC heat dome there were 619 heat-related deaths; 67% were aged 70+, 56% lived alone and 98% died indoors.
6. 50% of the deceased were found during wellness checks.
7. Telephone-based escalation saturated: 911 volume roughly doubled, ambulance dispatch fell to 74–80%, and in six instances callers were told no ambulance was available.
8. The panel stated that not everyone accesses social media, has a phone, can read signage, or speaks the majority language.
