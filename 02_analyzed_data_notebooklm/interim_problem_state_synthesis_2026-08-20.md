# HeatShield Interim Problem State Synthesis
## Pitch 1 working draft from Mod, My, June, and Com v2

**Status:** interim synthesis while waiting for Belle and Chris  
**Date:** 2026-08-20  
**Project phase:** Pitch 1 / Problem State  
**Intended use:** use this file as the shared base for combining the remaining team inputs into the first pitching narrative.

## 1. Source Inputs Used

This synthesis uses only summarized or analyzed materials currently available in the repository:

| Member | File | Role in this synthesis | Current status |
|---|---|---|---|
| Mod | `00_raw_materials/01_Mod/Mod_literature_review.md` | Health problem framing, vulnerable-population scope, retrospective dashboard boundary, Lancet indicator interpretation | Ready for Pitch 1 |
| My | `00_raw_materials/02_My/My_literature_review.md` | Heat-risk indicators, data-source feasibility, ingestion cadence, quality flags, source provenance | Phase 0 scaffold; citations still need final verification |
| June | `00_raw_materials/06_June/June_evidence_review_notes.docx` | WHO/WMO policy framing, heat-health action logic, Phase 0 feasibility, prototype evaluation | Ready for Pitch 1 with assumptions clearly labelled |
| Com | `00_raw_materials/05_Com/Com_literature_review-v2.md` | IT architecture, governance, privacy, audit trail, file-based ingestion, future interoperability direction | v2 aligns well with agreed scope |
| Belle | Pending | IT use case / user needs / workflow interpretation | Waiting for input |
| Chris | Pending | Stakeholders, contact points, communication channels, adoption and CSAT-style evaluation | Waiting for input |

## 2. Consolidated Problem Statement

Heat-health risk is a global and local public-health problem, but the operational gap is digital. Heat, climate, weather, vulnerability, and policy evidence exist across multiple sources, but they are fragmented by format, geography, time scale, data quality, update cadence, and ownership. Current health information systems are not designed to combine environmental heat-risk data, vulnerable-population context, task assignment, communication status, source traceability, access control, and auditability into one operational decision workflow.

For Pitch 1, the strongest framing is:

> HeatShield is not another weather dashboard. It addresses the digital operational gap between heat-risk evidence and public-health action by turning fragmented heat, climate, and vulnerability data into a retrospective dashboard and mock workflow simulator for planning, prioritization, task handoff, and Phase 0 feasibility evaluation.

## 3. Problem State Layers for Pitch 1

### 3.1 Health Problem

Extreme heat affects population health and disproportionately impacts vulnerable groups. The agreed vulnerable contexts for the prototype are:

- infants younger than 1 year
- older adults older than 65 years
- outdoor workers
- people with chronic disease
- people living alone

The first three groups are strongly supported by available Lancet and heat-health evidence. Chronic disease and living alone are important public-health contexts but should be treated as mock or future local-linkage fields in the course prototype.

### 3.2 Data Problem

The dashboard must handle different classes of data without collapsing them into one clinical score:

- historical Lancet Countdown aggregate indicators
- weather and heat-index candidates for future/live or mock data
- demographic and vulnerability context
- official alert or advisory wording
- workflow and task-status data
- source, timestamp, licence, and quality metadata

Key issue: the same dashboard may display observations, model estimates, forecast candidates, official warnings, illustrative thresholds, and mock workflow states. These must be visibly separated.

### 3.3 Operational Problem

A warning or dashboard view is not enough. The missing operational layer is:

`Heat Data -> Identify Vulnerability -> Prioritize -> Assign Action -> Follow-up -> Escalate -> Review`

The dashboard should support questions such as:

- Which time period, geography, or population context shows a meaningful heat-health trend?
- Is the signal evidence-backed, illustrative, mock, stale, missing, or uncertain?
- Is the signal important enough for a human user to create an operational task?
- Who receives the task?
- What information is passed?
- What channel is used?
- Who acknowledges the task?
- What fallback or escalation exists?
- What is reviewed after the event or simulated event?

### 3.4 IT Management Problem

The project is strongest when framed as a Healthcare IT Management initiative, not a clinical protocol. The IT management gaps are:

- source integration and ingestion design
- provenance and source traceability
- missing, stale, delayed, conflicting, or outlier data handling
- separation of evidence-backed data from mock/future context
- access control and role-based views
- audit trail for simulated task actions
- privacy-by-design and data minimization
- interoperability direction without overbuilding the prototype
- evaluation of workflow feasibility rather than clinical outcome claims

## 4. Agreed Scope for Phase 0 Prototype

### In Scope

- Retrospective heat-risk dashboard using historical aggregate data.
- Mock workflow simulator showing how a high-priority operational signal may become a task.
- Evidence-backed trend views for heat exposure, activity heat stress, labour capacity, outdoor workers, sleep loss, and heat-related mortality.
- Mock vulnerable cohort fields for workflow demonstration only.
- Static or file-based ingestion concept for prototype data.
- Source provenance, quality flag, and traceability fields.
- Role-based concept views, audit trail concept, and handoff status.
- Phase 0 evaluation: feasibility, usability, task completion, traceability, workflow fit.

### Out of Scope

- Live production weather prediction.
- Diagnosis, treatment advice, or clinical risk scoring.
- Real patient registry or identifiable patient data.
- Automated emergency dispatch.
- Wearable or biometric device integration.
- Claiming legal compliance or production readiness.
- Claiming reduced mortality, reduced heatstroke, or reduced hospital visits during Phase 0.

## 5. Evidence-to-Problem Matrix

| Problem dimension | Evidence or team input | Meaning for pitch | Boundary |
|---|---|---|---|
| Heat affects vulnerable populations | Mod and June | Heat is a valid global health issue with local relevance | Do not claim patient-level prediction |
| Vulnerability is multidimensional | Mod and June | Age, occupation, chronic disease, living alone, cooling access, and geography may matter | Some fields are mock/future local linkage only |
| Data exists but is fragmented | My and Com | The core problem is data integration, source interpretation, and operational use | Do not imply every data source is production-ready |
| Warning must link to action | June and Com | Dashboard should lead to task handoff, acknowledgement, escalation, and review | Phase 0 demonstrates the concept, not a live response system |
| HIS and EHR systems are siloed | Com | Existing systems do not naturally combine environmental data and public-health tasks | Avoid claiming final integration with hospital systems |
| Data governance is central | My, June, and Com | Need provenance, quality flags, access control, privacy, and auditability | Do not claim full PDPA/HIPAA/GDPR compliance |
| Thresholds are not finalized | My and June | Use illustrative alert levels only | Avoid calling prototype levels official clinical thresholds |
| Evaluation should be feasible | June | Measure workflow completion, usability, traceability, and data completeness | Do not use mortality reduction as Phase 0 KPI |

## 6. Proposed Pitch 1 Narrative

### Opening

Extreme heat is already recognized as a major health threat, especially for infants, older adults, outdoor workers, people with chronic disease, and people living alone. However, the issue for a healthcare IT management project is not simply that temperatures are rising. The operational challenge is that heat-health data remains fragmented and difficult to convert into public-health action.

### Problem

Current systems often separate weather data, health data, vulnerable population context, communication tasks, and evaluation logs. As a result, decision-makers may see a heat warning or a historical trend, but the system does not clearly answer who should act, who should be contacted, what information should be passed, and how the action should be tracked.

### Opportunity

HeatShield proposes a Phase 0 retrospective dashboard and mock workflow simulator. The dashboard helps healthcare and public-health personnel review historical heat-health trends, understand vulnerable contexts, and simulate how a high-priority operational signal could become a coordinated task.

### Boundary

The prototype is not a live weather system, not a diagnosis tool, not a treatment protocol, and not a real patient registry. It uses historical aggregate data and mock workflow data to test whether a digital operational layer can support planning, prioritization, handoff, acknowledgement, and post-event review.

### Phase 0 Question

Can a heat-risk dashboard translate fragmented heat-health evidence into a usable, traceable, and privacy-conscious public-health workflow?

## 7. Recommended Slide Structure for Pitch 1

1. **Global Health Problem:** heat as a growing health threat.
2. **Who Is Vulnerable:** infants, older adults, outdoor workers, chronic disease, living alone.
3. **Current Gap:** data exists, but operational linkage is weak.
4. **Digital Operational Gap:** fragmented sources, unclear ownership, no task/handoff/audit layer.
5. **Project Concept:** HeatShield retrospective dashboard and mock workflow simulator.
6. **What Dashboard Does in Phase 0:** trend review, source display, priority signal, task stub.
7. **What It Does Not Do:** no diagnosis, no treatment, no real patient registry, no live production alert.
8. **Future Roadmap:** from retrospective analysis to validated live dashboard and coordinated response.
9. **Evaluation:** usability, workflow completion, task traceability, data completeness, feasibility.
10. **Next Step:** integrate Belle and Chris inputs for user workflow, stakeholders, communication, and adoption.

## 8. Items to Add When Belle and Chris Inputs Arrive

### Belle

Expected contribution:

- user needs and IT use case
- who uses the dashboard and for what decision
- required screen actions or feature concepts
- what information the user must see before creating a task
- how the dashboard avoids clinical overclaiming

Suggested merge target:

- add to Section 3.3 Operational Problem
- add to Section 6 Proposed Pitch 1 Narrative
- add a new `User / IT Use Case Matrix`

### Chris

Expected contribution:

- stakeholder and contact-point map
- handoff owner and communication channel
- primary and fallback channels
- adoption barriers and CSAT-style evaluation
- message clarity and accessibility considerations

Suggested merge target:

- add to Section 3.3 Operational Problem
- add to Section 7 Recommended Slide Structure
- add a new `Stakeholder / Contact Point / Channel Matrix`

## 9. Working Decision Log

| Decision | Current position |
|---|---|
| Main initiative | Heat Risk Dashboard |
| Prototype type | Retrospective dashboard plus mock workflow simulator |
| Primary user | Healthcare or public-health personnel involved in analysis, planning, and coordination |
| Main signal term | High-priority operational signal or Outreach Priority |
| Avoided term | Clinical risk score |
| Core data | Historical aggregate data and mock workflow data |
| Future data | Live weather/API feeds, local vulnerable registry, official thresholds |
| Core IT concern | Data provenance, ingestion, quality, privacy, access, audit, and handoff |
| Pitch 1 focus | Problem state, gap, scope, and Phase 0 feasibility |

## 10. Short Version for Team Discussion

HeatShield should be framed as a Healthcare IT Management project that addresses the digital operational gap in heat-health response. Heat and vulnerability data exist, but they are fragmented and not consistently converted into public-health tasks. The Phase 0 prototype should therefore focus on a retrospective dashboard and mock workflow simulator that can show trends, preserve source traceability, separate evidence from mock assumptions, support human-in-the-loop task creation, and evaluate whether the workflow is understandable and feasible.

