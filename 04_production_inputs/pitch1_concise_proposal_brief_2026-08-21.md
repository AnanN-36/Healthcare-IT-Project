# HeatShield Pitch 1: Concise Proposal Brief

**Project:** HeatShield - Heat Risk Dashboard Roadmap Initiative
**Course:** Principles of Global Healthcare Information Technology Management
**Pitch focus:** Problem State and Phase 0 direction
**Primary user:** District-level public-health coordinator
**Prepared:** 2026-08-21

## 1. Proposal in One Sentence

HeatShield is a retrospective Heat Risk Dashboard and mock workflow simulator that connects fragmented heat-health evidence to accountable coordination, task ownership, acknowledgement, fallback, and post-event review.

## 2. The 30-Second Pitch

Extreme heat is a global and locally relevant health risk, especially for older adults, infants, outdoor workers, people with chronic disease, and people living alone. Heat-health evidence, weather information, advisories, and vulnerability context may already exist, but they are distributed across different sources, roles, and communication channels. A dashboard may show risk without showing who owns the next task, whether a handoff was acknowledged, or what remains unresolved.

HeatShield addresses this alert-to-action gap. It proposes a retrospective dashboard for a district-level public-health coordinator, supported by a mock workflow simulator that shows how evidence becomes a human-reviewed operational signal, a task, a handoff, an acknowledgement, a fallback or escalation, and a review. The first version is a Phase 0 feasibility prototype, not a live warning system or clinical decision tool.

## 3. Problem State

### Who is affected?

Heat exposure creates uneven health and social burdens. The initial population contexts are:

- older adults older than 65 years;
- infants younger than 1 year;
- outdoor workers;
- people with chronic disease; and
- people living alone.

The last two contexts will be represented as mock or future local-linkage fields unless an approved aggregate source is identified. None of these fields will be used to calculate a patient-level clinical risk score.

### Where does the process break?

The information journey should be:

```text
Evidence -> interpretation -> prioritization -> owner -> handoff
-> acknowledgement -> action or fallback -> review
```

In practice, these steps can be separated across systems and organizations. The result is an alert-to-action gap:

> Heat data may exist. Warnings may exist. But accountable health action is not always visible, traceable, or coordinated.

### Why is this a Healthcare IT Management problem?

The project is not primarily about producing another weather display. It is about managing:

- data meaning, provenance, quality, and freshness;
- role-based access and information views;
- task ownership and workflow state;
- communication handoffs and acknowledgement;
- fallback and escalation visibility; and
- Phase 0 evaluation and implementation readiness.

### How the problem elements are related

These are connected parts of one problem chain, not separate project topics:

```text
Heat-health burden
-> unequal exposure and vulnerable contexts
-> fragmented data, roles, and communication channels
-> unclear ownership and incomplete handoffs
-> limited visibility of action and coverage
-> alert-to-action gap
-> need for a coordinated information layer
```

The dashboard is therefore positioned between evidence and action. It does not replace the health system, communication channels, or responsible staff. It makes the relevant context, next contact point, task state, acknowledgement, and unresolved coverage visible to the coordinator.

### Access model at requirement level

Access should be role-based and limited to the information needed for each task:

| User | Intended access | Information visible in Phase 0 |
|---|---|---|
| District-level public-health coordinator | Authenticated web dashboard | Aggregate risk context, trends, source metadata, tasks, acknowledgement, and unresolved work |
| CHW or local contact | Mobile-friendly assigned-task view | Tasks assigned to the role, status update, acknowledgement, and fallback request |
| Facility contact | Restricted facility view | Facility recipient status and handoff confirmation |
| Resident or caregiver | Future simplified public or support view | General guidance or contact information; not part of the core Phase 0 workflow |
| Data administrator | Restricted upload and quality-control access | Source files, provenance, freshness, and validation flags |

The project should test whether the intended users can find the source, identify the affected area, understand the operational signal, and update or interpret task status. It should not claim that production access, authentication, or local permissions have already been validated.

### Coverage boundary at requirement level

Coverage is defined across several dimensions rather than as a claim that the system covers everyone:

| Coverage dimension | Phase 0 position |
|---|---|
| Population | Five vulnerable contexts are considered, but chronic disease and living alone remain mock or future local-linkage fields unless approved aggregate data is available |
| Geography | Demonstration area or district-level concept; not a claim of nationwide coverage |
| Time | Historical aggregate evidence and mock workflow states; current and forecast integration remain future extensions |
| Workflow | Evidence review, operational signal, task, handoff, acknowledgement, fallback, and post-simulation review |
| Communication | Contact points and fallback are represented; the dashboard is not the only delivery channel |
| System integration | File-based or mock ingestion in Phase 0; no live EHR, hospital, or meteorological API dependency |

The coverage question for Pitch 1 is therefore:

> Can a limited district-level prototype make evidence, access, ownership, and response coverage visible enough to identify what should be validated in a future live phase?

### Open validation items

The following items are intentionally left open for feedback rather than presented as completed decisions:

- final primary-user organization and local role ownership;
- the first demonstration geography and its appropriate data resolution;
- which vulnerable contexts can be supported by approved aggregate data;
- access and authentication arrangements for a future pilot;
- which contact points are essential for the first workflow demonstration; and
- what evidence is required before current, forecast, or live data are introduced.

## 4. A Simple Scenario

> District A shows a concerning historical heat-health trend. The coordinator can see the indicator, source, period, and vulnerable context, but the current information view does not make the next owner, acknowledgement status, fallback route, or unresolved task visible in one place.

HeatShield would let the coordinator review the evidence, create a high-priority operational signal for human review, assign a simulated task, record whether the receiving role acknowledged it, and review what remains unresolved.

This scenario demonstrates the gap without claiming that the prototype can diagnose a person, predict the weather, or dispatch an emergency response.

## 5. Proposed Direction

### Main component

**Heat Risk Dashboard:** a retrospective analytical view for historical heat-health trends, source context, vulnerable-population context, data quality, and operational prioritization.

### Workflow layer

**Mock Workflow Simulator:** a safe demonstration of:

1. evidence review;
2. human-reviewed operational signal;
3. task creation and assignment;
4. handoff and acknowledgement;
5. fallback or escalation; and
6. post-simulation review.

### Supporting components

The other five components remain at contact-point level only:

| Component | Pitch 1 role |
|---|---|
| Vulnerable Population Registry | provide aggregate or mock population context |
| Action Workflow | receive the signal and show task ownership |
| Communication Center | show delivery, acknowledgement, and fallback contact points |
| Health Facility Preparedness | show facility recipient and status handoff |
| Post-Event Review | summarize completion, unresolved tasks, and gaps |

## 6. Phase 0 Scope

### In scope

- Historical aggregate heat-health indicators, including selected Lancet Countdown 2025 data.
- Source, unit, timestamp, geography, coverage, and quality metadata.
- Aggregate or mock vulnerable-population context.
- Coordinator overview and trend views.
- Mock task, owner, acknowledgement, fallback, and escalation states.
- Concept views for CHW and facility contacts.
- Feasibility, usability, clarity, task completion, acknowledgement, and traceability evaluation.

### Out of scope

- Live production monitoring or public warning dispatch.
- A new weather forecasting or heat-index model.
- Clinical diagnosis, treatment recommendation, or patient-level risk scoring.
- Identifiable patient registry or real personal data.
- Automated emergency dispatch.
- Final communication vendor, policy threshold, or response-time standard.
- Claims of reduced mortality, heatstroke, hospital admission, or emergency visits.

## 7. Evidence Anchors for the Pitch

These are candidate evidence points for the first problem slide. The final presentation should cite the original Lancet or Thai source directly.

| Evidence point | Why it matters | Source trace |
|---|---|---|
| In 2024, heatwave exposure increased 304% for older adults and 389% for infants compared with the 1986-2005 baseline | shows vulnerable-population relevance | Lancet Countdown 2025, indicator 1.1.1; `Mod_literature_review.md`, E1 |
| In 2024, 640 billion potential labour hours were lost and outdoor workers were estimated at 1.5 billion people, or 25.3% of the working-age population | shows occupational and socioeconomic relevance | Lancet Countdown 2025, indicators 1.1.3; `Mod_literature_review.md`, E2 |
| Average annual heat-related deaths were estimated at 546,000 during 2012-2021, 63.2% higher than the 1990-1999 baseline | shows population-level health burden | Lancet Countdown 2025, indicator 1.1.5; `Mod_literature_review.md`, E4 |
| Thai surveillance and temperature-mortality sources provide local context for age, outdoor occupation, chronic disease, and cross-sector warning | supports local validation without creating a clinical score | `Mod_literature_review.md`, E5-E6; Thai sources E02-E04 |

The evidence is used to establish need and context. It is not used to define a patient-level threshold or automate clinical action.

## 8. Suggested Pitch Slides

### Slide 1 - Why Heat-Health Matters

Extreme heat is a global and local health risk with unequal effects on vulnerable and exposed populations.

### Slide 2 - The Current Information Journey

Show: `Evidence -> interpretation -> prioritization -> owner -> handoff -> acknowledgement -> review`.

### Slide 3 - Problem State: The Alert-to-Action Gap

Heat data and warnings may exist, but ownership, acknowledgement, fallback, and unresolved work are not consistently visible.

### Slide 4 - Why a Risk Display Is Not Enough

Risk visualization answers “what is happening?” An operational workflow must also answer “who acts, what is the status, and what happens next?”

### Slide 5 - Proposed Direction: HeatShield

Introduce the retrospective dashboard plus mock workflow simulator.

### Slide 6 - Phase 0 Boundary

Show historical aggregate data, mock workflow, provenance, privacy boundary, role-based access, coverage boundary, and feasibility evaluation. State clearly what is deferred.

### Slide 7 - Feedback Requested

Ask the committee to validate the primary user, indicators, vulnerable contexts, access model, coverage boundary, operational signal definition, essential handoffs, and requirements for a future live phase.

## 9. Decision Questions for the Committee

1. Is the district-level public-health coordinator the correct primary user?
2. Which historical indicators are most useful for the first prototype?
3. Which vulnerable contexts should appear in the first demonstration?
4. What should a coordinator review before creating a high-priority operational signal?
5. Which handoffs are essential to show while keeping the five supporting components lightweight?
6. Which roles should have access to each dashboard view, and what information should remain restricted?
7. What geographic, population, temporal, and workflow coverage is realistic for the Phase 0 demonstration?
8. What local evidence, threshold authority, data access, and stakeholder ownership would be required before a live pilot?

## 10. Closing Statement

> HeatShield does not attempt to solve the entire heat-health response system in one course project. It tests a focused Healthcare IT Management question: can fragmented heat-health evidence be organized into a privacy-conscious, traceable workflow that helps a district-level coordinator move from evidence review to accountable coordination? Phase 0 will show what is feasible, what remains uncertain, and what must be validated before a future live implementation.

## 11. Traceability

This concise proposal is synthesized from:

- `00_raw_materials/01_Mod/Mod_literature_review.md`
- `00_raw_materials/02_My/My_literature_review.md`
- `00_raw_materials/03_Belle/Belle_literature_review.md`
- `00_raw_materials/04_Chris/Chris_literature_review.md`
- `00_raw_materials/04_Chris/Chris_contact_point_matrix.md`
- `00_raw_materials/05_Com/Com_literature_review-v2.md`
- `00_raw_materials/06_June/June_evidence_review_notes.docx`
- `04_production_inputs/pitch1_integrated_problem_state_brief_2026-08-21.md`
- `04_production_inputs/pitch1_origin_problem_motivation_brief_2026-08-21.md`

Detailed citations should be added to the final slides from the original source files listed in the member inventories.
