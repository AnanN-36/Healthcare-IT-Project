# HeatShield Pitch 1: From Heat-Health Problem to IT-Enabled Coordination

**Project:** HeatShield - Heat Risk Dashboard Roadmap Initiative  
**Course:** Principles of Global Healthcare Information Technology Management  
**Purpose:** 15-20 minute narrative script for Pitch 1  
**Pitch level:** evidence and problem overview; solution direction, not a finished implementation  
**Prepared:** 2026-08-27  

## How to use this script

This is a speaking draft rather than a paper to read word-for-word. The story is deliberately built around a fictional district review so that the audience can follow the information and coordination problem. The scenario is illustrative. The historical evidence is used to establish the problem, not to claim a live warning, clinical diagnosis, or health outcome improvement.

Suggested length: 14 slides, approximately 1-1.5 minutes per slide, with longer pauses on the evidence, problem-chain, and proposed-workflow slides. This gives an overall speaking time of approximately 15-20 minutes, including transitions and questions.

## One-sentence thesis

> Extreme heat is a global health problem with unequal effects, but the practical information gap is local and operational: evidence, vulnerability context, and communication channels are often disconnected from clear ownership, acknowledgement, fallback, and review. HeatShield proposes a retrospective Heat Risk Dashboard with a mock workflow simulator to make that connection visible and testable.

## Story arc

```text
One district review
-> an apparently simple heat signal
-> unequal health and social burden
-> a chain of connected problems
-> why this is global health
-> the alert-to-action gap
-> HeatShield as a focused IT response
-> Phase 0 boundary and roadmap
```

## Slide-by-slide speaking draft

### Slide 1 - A heat signal is not yet an action

**On-slide message:**

> A risk signal becomes useful only when the system can support the next accountable action.

**Speaker script, approximately 2 minutes:**

Imagine that we are public-health coordinators reviewing the previous hot season in District A. We open a historical dashboard and see a concerning heat-health pattern. The chart tells us the period, the indicator, and the affected area. We can also see that the area includes older adults, outdoor workers, and people who may have more difficulty protecting themselves from heat.

At first, this seems like a data problem. Perhaps we need a better chart, a larger map, or another warning indicator. But after looking at the information, the coordinator has more practical questions. Who should review this signal? Which role owns the next task? Has the receiving person acknowledged the handoff? What happens if the first communication channel fails? Which work is complete, and which work remains unresolved?

This is the starting point for HeatShield. The project is not asking whether a chart can display heat. It is asking whether health information can support accountable coordination after the pattern has been identified.

**Transition:**

To understand why this matters, we first need to see the scale and unevenness of the heat-health problem.

### Slide 2 - Extreme heat creates an unequal burden

**On-slide message:**

> Heat exposure is not experienced equally across age, work, health, and social context.

**Speaker script, approximately 2 minutes:**

The global evidence shows that heat is not a minor environmental inconvenience. It is a health, workforce, and equity issue.

The Lancet Countdown 2025 evidence used by our team reports that, in 2024, heatwave exposure increased by 304 percent for adults older than 65 and by 389 percent for infants, compared with the 1986-2005 baseline. The same evidence reports 640 billion potential labour hours lost in 2024. It also estimates that outdoor workers represented about 1.5 billion people, or 25.3 percent of the working-age population.

These figures describe different dimensions of the same problem. Older adults and infants may have less physiological ability to cope with heat. Outdoor workers may have unavoidable exposure because their livelihood depends on being outside. People with chronic disease may have additional health vulnerability. People living alone may have less immediate support when conditions become unsafe.

For HeatShield, these are population contexts for planning and prioritization. They are not a clinical risk score, and the prototype will not diagnose or predict an individual patient's outcome.

**Evidence note:** Use the original Lancet Countdown source on the slide. The current trace is `00_raw_materials/01_Mod/Mod_literature_review.md`, E1, E2, and E4.

### Slide 3 - This is a global health issue, not only a weather issue

**On-slide message:**

> Heat crosses borders, but its effects are shaped by local health systems and social conditions.

**Speaker script, approximately 2 minutes:**

Why do we describe this as a Global Health Issue?

First, extreme heat is a cross-border and increasingly recurring threat. The evidence is produced across countries and allows us to see changes in exposure, mortality, work capacity, and vulnerability at population level.

Second, the consequences are unequal. Health effects depend not only on temperature, but also on age, occupation, chronic disease, housing, cooling access, social support, infrastructure, and the ability to receive and act on guidance.

Third, no single organization owns the entire response. Global and national bodies may provide evidence, policy, or warning information. Meteorological services provide environmental data. Health authorities interpret the public-health meaning. Local health teams coordinate action. Healthcare workers, community health workers, employers, schools, local government, logistics teams, finance teams, and communication providers may all be part of the response.

This is why heat-health is an appropriate Healthcare IT Management case. The challenge is not only to know that heat is dangerous. The challenge is to organize information across system levels so that a responsible person can interpret it, coordinate a response, and learn from what happened.

### Slide 4 - The burden reaches health, work, finance, and equity

**On-slide message:**

> A heat event can become a health burden, a workforce burden, a service burden, and a coordination burden at the same time.

**Speaker script, approximately 1.5 minutes:**

The problem also has consequences beyond a temperature chart.

At the population level, heat is associated with illness and mortality. At the workforce level, exposure can reduce safe working capacity and create income and productivity pressure. At the health-service level, vulnerable people may need advice, outreach, clinical assessment, transport, supplies, or escalation. At the household level, people may face unequal access to cooling, information, care, or financial protection.

This creates a management challenge for organizations that have different responsibilities and different data. Finance and accounting teams may need information for resource planning. Logistics teams may need to coordinate supplies, transport, or field support. Healthcare workers need usable context, not an unexplained alert. Non-health actors may control the channels that reach people at work, at school, or in the community.

We are not proposing to build all of these functions in Phase 0. We are showing why the information layer must acknowledge that these functions are related.

### Slide 5 - The problems are connected in one chain

**On-slide message:**

```text
Heat burden
-> unequal exposure and vulnerability
-> fragmented information
-> unclear prioritization and ownership
-> incomplete handoff
-> invisible unresolved work
-> alert-to-action gap
```

**Speaker script, approximately 2 minutes:**

The individual problems in our research are not separate topics. They are connected stages of one system problem.

The first stage is the heat-health burden. The second is unequal exposure and vulnerability. The third is fragmentation: heat-health indicators, weather information, advisories, vulnerable-population context, facility information, and communication records may live in different places.

Fragmentation then affects prioritization. A user may see a concerning pattern but lack enough context to know whether it is historical, current, official, illustrative, or mock. Even when a decision is made, the next owner may not be visible. A message can be sent without being acknowledged. A recipient can acknowledge it without completing the task. If the first channel fails, the fallback may not be independent. Finally, the team may have no clear post-event view of unresolved work.

This chain explains our problem statement:

> Heat-health evidence and alerts can exist without a shared, traceable operational layer that shows what the signal means, who owns the next step, whether the handoff was acknowledged, and what remains unresolved.

That is the alert-to-action gap.

### Slide 6 - A risk display answers only part of the question

**On-slide message:**

| A risk display shows | An operational workflow must also show |
|---|---|
| What is happening? | Who reviews it? |
| Where and when? | Who owns the next task? |
| What is the source? | Was the handoff acknowledged? |
| How large is the signal? | What is the fallback? |
|  | What remains unresolved? |

**Speaker script, approximately 1.5 minutes:**

A dashboard can be accurate and still be insufficient for coordination. A risk display answers questions such as what is happening, where it happened, when it was measured, and which source produced the value.

An operational workflow must answer additional questions. Who is responsible for reviewing the signal? Who receives the task? Was the handoff acknowledged? What happens when the first channel fails? Is the task pending, completed, escalated, or unresolved?

Chris's research stream made an important distinction for this project: transmission is not receipt, receipt is not acknowledgement, and acknowledgement is not action. We therefore treat acknowledgement as a first-class workflow field. Belle's work adds a second important distinction: heat-risk state and task state must be displayed separately. A severe-looking risk state does not mean the response task is complete, and a completed task does not mean that the risk has disappeared.

### Slide 7 - Who is the primary user, and who is connected?

**On-slide message:**

> One primary user, many connected stakeholders.

**Speaker script, approximately 2 minutes:**

HeatShield will use a district-level public-health or healthcare coordinator as the primary user for the first prototype. This role sits at the point where evidence must become prioritization and coordination.

The coordinator does not work alone. At the global and national levels, organizations such as WHO, WMO, health ministries, meteorological services, disaster-management authorities, and policy units may provide evidence, guidance, or governance. At regional and district levels, public-health offices and local governments translate that direction into local coordination.

Healthcare workers, community health workers, facility contacts, emergency services, and supply staff may receive or update tasks. Non-health actors such as employers, schools, community leaders, NGOs, utilities, telecom providers, media, transport, and logistics teams may provide access, communication, infrastructure, or fallback support. Finance, accounting, procurement, insurers, funders, and administrative data teams may influence whether a response is resourced and accountable.

The affected population remains central: older adults, infants and caregivers, outdoor workers, people with chronic disease, people living alone, and other residents. The prototype will represent their context through aggregate or mock fields. It will not create an identifiable population registry.

### Slide 8 - Access and coverage must be explicit

**On-slide message:**

> Access is role-based. Coverage is bounded.

**Speaker script, approximately 1.5 minutes:**

The dashboard is not intended to expose the same information to everyone.

The coordinator view would show aggregate trends, source metadata, quality flags, operational signals, tasks, acknowledgement, and unresolved work. A community health worker or local contact would see assigned tasks and status updates in a focused, mobile-friendly view. A facility contact would see the limited handoff and confirmation information needed for that role. A data administrator would manage source, provenance, freshness, and quality fields. A resident or caregiver view is a future simplified access layer, not part of the core Phase 0 workflow.

Coverage is also deliberately bounded. Phase 0 uses historical aggregate data and a demonstration district or area. It does not claim national coverage, real-time monitoring, live weather integration, or complete coverage of every vulnerable group. Chronic disease and living alone may remain mock or future local-linkage fields unless an approved aggregate source is confirmed.

The key question is not “Does this dashboard cover everyone?” The Phase 0 question is “Can a limited prototype make data context, access, ownership, and response coverage visible enough to identify what must be validated next?”

### Slide 9 - What HeatShield proposes

**On-slide message:**

> A retrospective Heat Risk Dashboard plus a mock workflow simulator.

**Speaker script, approximately 2 minutes:**

HeatShield has two connected parts.

The first is the Heat Risk Dashboard. It organizes historical heat-health indicators and related context. Each value should be accompanied by its source, unit, period, geography, coverage, and data-quality status. The user should be able to distinguish observed historical evidence from official advisory context, illustrative labels, and mock workflow data.

The second is a mock workflow simulator. After reviewing the evidence, the coordinator can create a high-priority operational signal for human review. The simulator can then show task creation, assignment, handoff, acknowledgement, fallback or escalation, completion, and post-simulation review.

This allows us to demonstrate the central IT management question without claiming authority to send a public warning or dispatch an emergency response. The dashboard does not replace existing weather systems, healthcare systems, communication channels, or responsible staff. It acts as a coordination and confirmation layer around them.

### Slide 10 - How the proposed workflow works

**On-slide message:**

```text
Evidence review
-> human-reviewed operational signal
-> task creation
-> owner and assignee
-> handoff
-> acknowledgement
-> action, fallback, or escalation
-> post-simulation review
```

**Speaker script, approximately 2 minutes:**

Let us return to District A. The coordinator reviews a historical trend and checks the source, time period, unit, geography, and quality flags. The coordinator sees an aggregate vulnerable context, but not a patient identity or clinical score.

The coordinator then marks a high-priority operational signal for human review. This signal is intentionally not called a clinical risk score. It creates a task with an owner, an assignee, priority, and status. The task is handed to a relevant contact point, such as a community health worker or facility contact, through a channel that can be represented in the prototype.

The workflow records whether the task was sent, received, acknowledged, acted on, or completed. If acknowledgement does not occur, the simulator can show a fallback or escalation state. The fallback should not simply repeat the same failed channel. Finally, the coordinator reviews what was completed and what remains unresolved.

The output is not a medical decision. It is a visible, traceable coordination sequence.

### Slide 11 - The five other components remain supporting contact points

**On-slide message:**

| Supporting component | What we show in Pitch 1 |
|---|---|
| Vulnerable Population Registry | context, data owner, privacy boundary |
| Action Workflow | task owner and handoff |
| Communication Center | channel, acknowledgement, fallback |
| Health Facility Preparedness | facility recipient and status |
| Post-Event Review | completion and unresolved gaps |

**Speaker script, approximately 1.5 minutes:**

The Heat Risk Dashboard is the only main product component. The other five components remain deliberately lightweight. We will describe their contact point, the information passed, the owner, acknowledgement, and fallback. We will not design five detailed workflows in this phase.

This gives the concept enough system context to be credible while keeping the implementation focused. It also leaves a roadmap for later development: a population-context service, action workflow, communication layer, facility preparedness connection, and post-event review function could be connected progressively.

The dashboard requirement concept adds another future lens: Inputs and processes can lead to outputs, outcomes, and impact across governance, financing, ICT, workforce, supply chain, information, service readiness, coverage, equity, responsiveness, and efficiency. We will use this as a roadmap and monitoring lens, not as evidence that this prototype already improves health outcomes.

### Slide 12 - Phase 0: what we will prove and what we will not claim

**On-slide message:**

> Phase 0 tests feasibility, usability, traceability, and workflow clarity.

**Speaker script, approximately 2 minutes:**

Our Phase 0 is intentionally feasible for a four-month course project.

We will use historical aggregate heat-health evidence, including the selected Lancet data, together with source and quality metadata. We will create aggregate or mock vulnerable-population context. We will build a coordinator overview and trend view, and demonstrate a mock signal-to-task-to-handoff workflow. We will evaluate whether users can find the source, understand the signal, identify the owner, locate acknowledgement, and recognize unresolved work.

We will not build a new weather forecast model. We will not claim a live warning service, clinical diagnosis, treatment recommendation, patient-level risk score, identifiable registry, automated emergency dispatch, or reduced mortality and hospital utilization. We will not treat an illustrative threshold or simulated response time as official policy.

This boundary is part of the solution. It protects privacy, limits clinical and governance risk, and allows the team to learn what must be validated before a future live implementation.

### Slide 13 - The opportunity is a platform roadmap, not only a screen

**On-slide message:**

> Evidence can become a shared coordination layer for climate and health.

**Speaker script, approximately 1.5 minutes:**

The future opportunity is larger than the first dashboard, but it begins with the same information chain.

For promotion, the platform could support consistent heat-health information and community awareness. For prevention, it could support vulnerability context, outreach coordination, and readiness review. For treatment, it could support a clearer handoff to healthcare facilities or emergency services, without replacing clinical judgment. For recovery, it could support post-event review, unresolved-task follow-up, resource learning, and policy improvement.

Policy, law, privacy, accessibility, financing, accountability, and interoperability are cross-cutting requirements. They are not all features for Phase 0, but they determine whether the concept could become a responsible live service.

The opportunity is therefore a climate-health information and coordination platform. HeatShield is the first focused initiative that tests whether the operational information layer is useful and feasible.

### Slide 14 - Closing: from evidence to accountable coordination

**On-slide message:**

> HeatShield does not solve the whole heat-health system. It tests the missing connection between evidence and action.

**Speaker script, approximately 1.5 minutes:**

Let us return to the coordinator in District A. The dashboard does not tell the coordinator that every resident is safe. It does not diagnose a patient, issue an official warning, or dispatch an ambulance. What it does is make the information chain easier to inspect.

The coordinator can see what the evidence is, where it applies, which vulnerable context is relevant, who owns the next task, whether the handoff was acknowledged, what fallback is available, and what remains unresolved.

That is the contribution we want to test in Pitch 1. Heat is the global health problem. Fragmented evidence and disconnected responsibilities create the operational problem. HeatShield is our proposed IT management response: a retrospective dashboard and mock workflow simulator that makes coordination visible, traceable, and ready for future validation.

## Closing questions for the audience

Use these questions to turn the end of the pitch into a roadmap discussion:

1. Is the district-level public-health or healthcare coordinator the correct primary user for the first prototype?
2. Are the selected historical indicators sufficient to establish the problem, or should one indicator be removed for clarity?
3. Which vulnerable contexts should be visible in the first demonstration: older adults, infants, outdoor workers, chronic disease, and living alone?
4. What should a coordinator review before creating a high-priority operational signal?
5. Which handoffs are essential to show while keeping the five supporting components at contact-point level?
6. What access roles and coverage boundary should be treated as realistic for Phase 0?
7. Which local authority, threshold source, data access, and stakeholder ownership must be validated before a future live pilot?

## Evidence and traceability notes

### Evidence used for the problem opening

| Claim | Use in pitch | Current trace |
|---|---|---|
| Heatwave exposure increased 304% for adults older than 65 and 389% for infants in 2024 compared with the 1986-2005 baseline | unequal exposure and vulnerable population relevance | `00_raw_materials/01_Mod/Mod_literature_review.md`, E1 |
| 640 billion potential labour hours were lost in 2024; outdoor workers were estimated at 1.5 billion people or 25.3% of the working-age population | workforce and socioeconomic burden | `00_raw_materials/01_Mod/Mod_literature_review.md`, E2 |
| Average annual heat-related deaths were estimated at 546,000 during 2012-2021, 63.2% above the 1990-1999 baseline | population-level health burden | `00_raw_materials/01_Mod/Mod_literature_review.md`, E4 |
| Thai sources provide context for age, outdoor occupation, chronic disease, and cross-sector warning | local relevance and validation need | `00_raw_materials/01_Mod/Mod_literature_review.md`, E5-E6 |
| Transmission, receipt, acknowledgement, and action are different states | workflow and communication gap | `00_raw_materials/04_Chris/Chris_literature_review.md` |
| Risk state and task state must be separated; task registry and role views are required | dashboard and simulator design | `00_raw_materials/03_Belle/Belle_literature_review.md` |
| Provenance, audit, data minimization, file-based ingestion, and future standards are governance requirements | IT management and Phase 0 boundary | `00_raw_materials/05_Com/Com_literature_review-v2.md` |
| Thresholds, APIs, privacy, ownership, and outcome evaluation remain unresolved | feasibility and roadmap boundary | `00_raw_materials/06_June/June_evidence_review_notes.docx` |
| Inputs/processes -> outputs -> outcomes -> impact provides a future M&E lens | roadmap extension | `00_raw_materials/dashboard requirement concept.png` |

### Claims to avoid during Pitch 1

- Do not describe the retrospective prototype as a live or real-time warning system.
- Do not imply that the Lancet data defines an official local alert threshold.
- Do not call the operational signal a patient-level clinical risk score.
- Do not claim that the dashboard will reduce mortality, heatstroke, admissions, or emergency visits.
- Do not imply that the dashboard replaces healthcare workers, public authorities, communication channels, or emergency systems.
- Do not present mock vulnerable-population fields as a real registry.

## Suggested presenter split

This split is optional and should be adjusted to the team's speaking style:

| Segment | Suggested lead | Supporting role |
|---|---|---|
| Story opening, global health framing, problem statement | Mod | evidence clarification |
| Burden across workforce, finance, access, and equity | Chris | stakeholder examples |
| Connected problem chain and dashboard/workflow gap | Mod + Belle | user and task logic |
| Stakeholders, access, coverage, and related systems | Com + June | governance and feasibility |
| Proposed dashboard, mock workflow, and Phase 0 boundary | Belle + My | data and implementation detail |
| Roadmap opportunity and closing questions | Mod | whole team |

## Final one-minute version

> Extreme heat is a global health issue because it creates unequal health, work, social, and economic burdens across populations and places. The evidence already exists in many forms, but it is distributed across organizations, data sources, roles, and communication channels. The practical gap is what happens after a signal is seen: who reviews it, who owns the next task, whether the handoff is acknowledged, what happens when a channel fails, and what remains unresolved. HeatShield proposes a retrospective Heat Risk Dashboard with a mock workflow simulator for a district-level public-health coordinator. It connects historical heat-health evidence and aggregate vulnerability context to a human-reviewed operational signal, task, handoff, acknowledgement, fallback, and review. Phase 0 will test feasibility, usability, and traceability. It will not claim to be a live warning system, clinical decision tool, or replacement for the health system. The goal is to make the path from evidence to accountable coordination visible enough to support the next implementation decision.
