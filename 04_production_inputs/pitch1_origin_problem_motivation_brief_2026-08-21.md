# HeatShield Pitch 1: Origin, Problem, and Motivation

**Project:** HeatShield - Heat Risk Dashboard Roadmap Initiative  
**Course:** Principles of Global Healthcare Information Technology Management  
**Purpose:** narrative draft for the first pitch problem-state discussion  
**Status:** working draft for team review  
**Prepared:** 2026-08-21

## 1. Why This Topic Matters

Extreme heat is a global health issue because it can affect health across populations, places, and levels of the health system. The impact is not limited to one clinical condition or one emergency event. Heat exposure can create repeated and uneven burdens for people whose age, occupation, health status, social situation, or access to cooling makes self-protection more difficult.

For this project, the most useful vulnerable contexts are:

- infants younger than 1 year
- adults older than 65 years
- outdoor workers
- people with chronic disease
- people living alone

These groups are not being used to create a patient-level clinical risk score. They are population-level contexts that help a public-health or healthcare coordinator interpret historical heat-health information and consider where an operational response may need attention.

The topic is also relevant to Thailand and other settings where heat exposure is shaped by outdoor work, urban conditions, household resources, digital access, and the ability to reach people through trusted local contacts. This makes heat-health a suitable case for a global-health information technology project: the health problem is broad, while the proposed contribution is an information, coordination, and implementation problem.

## 2. Where the Problem Begins

Heat-health information is produced by different actors for different purposes. Historical health indicators, meteorological observations, heat-index information, official advisories, vulnerability context, and local response information may be stored in different formats and updated at different times.

The information journey therefore looks like this:

```text
Heat and health evidence
-> interpretation of risk context
-> prioritization for attention
-> assignment of a responsible role
-> communication and handoff
-> acknowledgement and action
-> review of unresolved work
```

The difficulty is that these steps are often separated. A source may provide a valid indicator but not an operational owner. A dashboard may display a map but not a task. A message may be sent but not acknowledged. A task may be assigned but not reviewed after the event. The problem is therefore not simply a lack of data; it is the weak connection between information and accountable action.

## 3. The Problem State

The central problem state for Pitch 1 is:

> Heat-health evidence and alerts can exist without a shared, traceable operational layer that shows what the signal means for a particular area or vulnerable context, who owns the next step, whether the handoff was acknowledged, and what remains unresolved.

This creates an **alert-to-action gap**:

1. A heat signal or historical trend is available.
2. A vulnerable context may be known.
3. A response may be expected.
4. The responsible role, task status, acknowledgement, fallback, or review status is not consistently visible in the same workflow.

The result is a management problem with practical consequences: teams may spend time reconciling sources, repeat communication, miss an unacknowledged handoff, or be unable to explain what happened during a response cycle.

## 4. Why Existing Information Displays Are Not Enough

Existing heat tools and public dashboards can be valuable for showing historical burden, current conditions, risk levels, public guidance, or geographic variation. The project does not claim that these tools are ineffective. The gap is that a risk display is not automatically an operational workflow.

For a coordinator, the information needed after seeing a concerning trend includes:

- What is the source, period, unit, and freshness of this information?
- Which area or vulnerable context requires review?
- Is this an observed, historical, forecast, official, illustrative, or mock value?
- Who should receive the next task?
- Has the recipient acknowledged the handoff?
- What is the fallback if the first channel fails?
- Is the task complete, overdue, escalated, or unresolved?
- What should be reviewed after the simulation or response period?

These questions show why HeatShield belongs to Healthcare IT Management. The proposed work is about managing data meaning, data quality, roles, access, workflow state, handoff visibility, and implementation feasibility.

## 5. The Motivation for HeatShield

The motivation is to test whether a health information system can make the operational layer visible without pretending to solve the entire heat-health response system.

HeatShield is motivated by five needs:

### 5.1 Convert evidence into a decision context

Users need to see historical heat-health indicators together with source, timestamp, unit, geography, and caveats. The dashboard should help a coordinator interpret a pattern before deciding whether it merits an operational signal.

### 5.2 Make the handoff accountable

The system should show who owns a task, who receives it, whether it was acknowledged, and whether a fallback or escalation is needed. This responds to the difference between sending a message, receiving a message, and taking action.

### 5.3 Keep vulnerable-population thinking practical and privacy-conscious

The prototype should represent vulnerable contexts at an aggregate or mock level. It should not require identifiable patient data or claim that a population label is a clinical diagnosis.

### 5.4 Design for real-world access constraints

The dashboard should be a coordination and confirmation destination, not the only delivery channel. Digital access may be uneven, particularly for some older adults or people with limited connectivity. The workflow therefore needs contact-point and fallback fields even when the actual communication channels remain future decisions.

### 5.5 Produce a credible Phase 0 roadmap

The first implementation should answer feasibility questions: can the data be organized, can users understand the view, can a signal become a task, can acknowledgement and completion be tracked, and can the team identify dependencies for a future live service?

## 6. What HeatShield Proposes

HeatShield proposes a retrospective Heat Risk Dashboard with a mock workflow simulator.

The dashboard would allow a public-health or healthcare coordinator to:

1. review historical heat-health trends and risk context;
2. inspect source, timestamp, unit, coverage, and quality flags;
3. consider vulnerable population context at aggregate or mock level;
4. mark a high-priority operational signal for human review;
5. create a simulated task with owner, assignee, priority, and due state;
6. record acknowledgement, fallback, escalation, and completion states;
7. review unresolved work and lessons at the end of the simulation period.

The main product idea is therefore not “another weather dashboard.” It is an information-management layer that connects evidence, interpretation, coordination, and review.

## 7. Why the Scope Is Deliberately Limited

The project is a four-month course initiative with a Phase 0 objective. A defensible first version must demonstrate the concept without requiring production weather integration, clinical validation, or deployment authority.

### In scope for Pitch 1 and Phase 0

- historical aggregate heat-health data, including the selected Lancet evidence base;
- candidate heat and weather data fields with provenance and quality metadata;
- mock vulnerable-population context;
- role-based concept views for coordinator, CHW, and facility contact;
- mock signal-to-task-to-handoff workflow;
- contact points for the five supporting components;
- usability, comprehension, task completion, acknowledgement, and traceability evaluation.

### Out of scope

- a new weather forecasting model;
- a live public warning service;
- clinical diagnosis or treatment recommendations;
- patient-level risk scoring or an identifiable registry;
- automated emergency dispatch;
- a final communication vendor or channel decision;
- claims of reduced mortality, heatstroke, hospital admission, or emergency visits.

This boundary protects the credibility of the initiative. It lets the team show a meaningful IT management contribution while clearly naming what would require later clinical, policy, data, and stakeholder validation.

## 8. The Five Supporting Components

Heat Risk Dashboard is the main component. The other five components complete the concept at contact-point level only:

| Supporting component | Role in the concept | Pitch 1 depth |
|---|---|---|
| Vulnerable Population Registry | supplies aggregate or mock population context | owner, fields, privacy boundary |
| Action Workflow | receives an operational signal and creates a task | task owner and handoff only |
| Communication Center | supports delivery, acknowledgement, and fallback | contact point and channel only |
| Health Facility Preparedness | receives a facility-facing notice and reports status | recipient and status only |
| Post-Event Review | summarizes completion, unresolved tasks, and gaps | review fields only |

The five components are intentionally not separate products in this phase. They are the surrounding handoff points that make the dashboard workflow plausible and show where later initiatives could connect.

## 9. The Value of the Initiative

The immediate value of HeatShield is not a promise of health outcome improvement. Its value is that it makes an otherwise invisible management problem discussable and testable.

The initiative can help the team and stakeholders examine:

- whether fragmented evidence can be presented with enough context to support review;
- whether the difference between heat-risk state and task state is understandable;
- whether users can identify the next responsible role;
- whether an acknowledgement and fallback state can be represented clearly;
- whether source quality and assumptions remain visible;
- whether the concept is feasible enough to justify a later pilot.

This creates a practical bridge between global-health evidence and implementation planning.

## 10. Working Motivation Statement

The team can use the following statement in the first pitch:

> We chose heat-health because extreme heat is a global and locally relevant health problem, but the information needed for action is distributed across sources, roles, and communication channels. Existing tools can show risk or historical burden without showing who owns the next task, whether the handoff was acknowledged, or what remains unresolved. HeatShield is motivated by the opportunity to design a retrospective, privacy-conscious Heat Risk Dashboard and mock workflow simulator that connects evidence to accountable coordination and provides a realistic Phase 0 roadmap for future live implementation.

## 11. Questions the Pitch Should Invite

The first pitch should close by inviting feedback on the decisions that require stakeholder validation:

- Is the public-health or healthcare coordinator the right primary user?
- Which heat-health indicators are sufficiently authoritative for the retrospective prototype?
- Which vulnerable contexts should remain in the first demo?
- What should count as a high-priority operational signal in the simulation?
- Which contact points and handoffs are essential to show without expanding scope?
- What evidence would be needed before testing live data or local thresholds?

These questions make the pitch a roadmap initiative rather than an overclaimed finished system.

## 12. Traceability

This narrative is synthesized from:

- `00_raw_materials/01_Mod/Mod_literature_review.md`
- `00_raw_materials/02_My/My_literature_review.md`
- `00_raw_materials/03_Belle/Belle_literature_review.md`
- `00_raw_materials/04_Chris/Chris_literature_review.md`
- `00_raw_materials/04_Chris/Chris_contact_point_matrix.md`
- `00_raw_materials/04_Chris/Chris_channel_strategy.md`
- `00_raw_materials/05_Com/Com_literature_review-v2.md`
- `00_raw_materials/06_June/June_evidence_review_notes.docx`
- `04_production_inputs/pitch1_integrated_problem_state_brief_2026-08-21.md`

The member files remain the source of detailed citations. This document is a narrative aid for the problem-state pitch, not a replacement for the underlying references.
