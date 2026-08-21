# HeatShield Pitch 1 Integrated Problem-State Brief
## Full-team consolidated input for the first pitching paper

**Project:** HeatShield — Heat Risk Dashboard Roadmap Initiative  
**Course focus:** Principles of Global Healthcare Information Technology Management  
**Prepared date:** 2026-08-21  
**Prepared from:** Mod, My, Belle, Chris, Com, and June research streams  
**Document status:** working draft for Pitch 1 paper and slide narrative

## 1. Executive Summary

HeatShield is a Healthcare IT Management initiative focused on the digital operational gap in heat-health response. Extreme heat is already recognized as a public-health threat, especially for vulnerable populations. The project does not attempt to create a new weather forecast, clinical diagnosis tool, treatment protocol, or real patient registry. Instead, it proposes a Phase 0 retrospective Heat Risk Dashboard with a mock workflow simulator.

The key problem is that heat, climate, vulnerability, policy, and operational data exist across multiple sources, but they are fragmented and not consistently translated into action. Existing heat-risk tools and public-health dashboards often show risk levels, maps, or historical burden, but they rarely show who owns the response, whether a task was created, whether the handoff was acknowledged, whether action was completed, and what failed during the response.

For Pitch 1, the recommended thesis is:

> HeatShield is not another weather dashboard. It explores how fragmented heat-health evidence can be converted into a usable, traceable, privacy-conscious operational workflow for public-health planning, prioritization, task ownership, handoff, acknowledgement, and Phase 0 feasibility evaluation.

## 2. Core Problem Statement

Extreme heat is a global and local public-health problem, but the operational gap is digital. Public-health teams may have heat-risk data, weather alerts, vulnerable-population evidence, and policy guidance, yet these inputs are often separated by source, format, geography, update cadence, governance boundary, and operational owner.

The result is an "alert-to-action gap":

1. A heat-risk signal exists.
2. Vulnerable contexts may be known.
3. A public-health response is expected.
4. But the system may not clearly show who should act, who received the alert, whether the action was acknowledged, whether the task was completed, or how the event should be reviewed.

HeatShield frames this as a Healthcare IT Management problem: how to structure data, dashboard views, role-based actions, contact points, governance, and evaluation so heat-risk evidence can support coordinated public-health action.

## 3. Contribution From Each Research Stream

| Member | Main contribution | How it shapes the integrated brief |
|---|---|---|
| Mod | Health problem framing, vulnerable groups, Lancet indicator interpretation, safe retrospective scope | Keeps the project grounded in health impact while avoiding diagnosis or patient-level risk scoring |
| My | Data-source feasibility, indicators, ingestion cadence, quality flags, source provenance | Defines what data the dashboard can consume and what must be labelled as candidate, mock, stale, or illustrative |
| Belle | IT use case, product requirements, users, role-based screens, user stories | Converts the concept into a dashboard people can use: map, task list, CHW view, facility view, summary view |
| Chris | Stakeholders, contact points, channels, fallback, acknowledgement, adoption, CSAT-style evaluation | Shows that the real gap is handoff, receipt, trust, actionability, and confirmation, not only display |
| Com | Architecture, governance, privacy, audit trail, file-based ingestion, future interoperability | Provides the technical structure for Phase 0 without overbuilding live production integration |
| June | WHO/WMO policy framing, heat-health action plan logic, Phase 0 feasibility, evaluation boundary | Connects heat warning to health action and keeps evaluation appropriate for prototype maturity |

## 4. Evidence Synthesis

### 4.1 Heat is a valid global-health issue

The team has enough evidence to justify heat as a global health issue and a local Thailand-relevant public-health problem. The vulnerable contexts most useful for the prototype are:

- infants younger than 1 year
- older adults older than 65 years
- outdoor workers
- people with chronic disease
- people living alone

The first three groups are directly supported by the main evidence base and dashboard data streams. Chronic disease and living alone are important operational contexts, but should be represented as mock or future local-linkage fields in the prototype unless an approved local aggregate source is identified.

### 4.2 The core gap is not lack of heat data

The team identified multiple candidate data classes:

- retrospective Lancet Countdown aggregate indicators
- official meteorological and heat-index information
- candidate weather API or historical climate datasets
- official alert or advisory wording
- aggregate vulnerability context
- mock vulnerable cohort data
- mock task and acknowledgement states

The challenge is that these data classes have different meanings. Some are observations, some are model estimates, some are forecasts, some are official advisories, and some are mock workflow states. They should not be merged into a single clinical risk score.

### 4.3 Existing dashboards often stop before operational ownership

Belle's review of comparable tools shows that many existing heat-risk tools provide risk visualization, zip-code lookup, historical burden, or surveillance data. Their common gap is that they do not usually show:

- task ownership
- task assignment
- acknowledgement status
- escalation state
- completion status
- end-of-period operational review

This supports the product gap: HeatShield should not compete with weather dashboards. It should provide the operational layer after risk is visible.

### 4.4 Warning transmission is not the same as action

Chris's review makes this point central. A heat service is a chain of handoffs. Issuing an alert, disseminating it, receiving it, understanding it, acting on it, confirming it, and reviewing it are separate steps.

Important implications:

- The dashboard should be a coordination and confirmation destination, not the main delivery channel.
- Acknowledgement should be a first-class field.
- Fallback channels should not share the same failure mode.
- Human contact may be necessary for digitally excluded groups.
- In Thailand, using อสม. for heat warnings is plausible but not yet locally validated, so it must be framed as an assumption to test.

### 4.5 Healthcare IT management is the right course framing

The strongest IT management issues are:

- data ingestion and source adapters
- data provenance and timestamp visibility
- quality flags for missing, stale, delayed, conflicting, or outlier data
- separation of evidence-backed fields from mock fields
- role-based dashboard views
- access control and data minimization
- audit trail for simulated task actions
- contact-point ownership and acknowledgement tracking
- Phase 0 evaluation and roadmap dependencies

This fits the course better than a narrow clinical or technical build because it asks how a health system should manage digital information, workflow, governance, and implementation readiness.

## 5. Proposed Initiative

### 5.1 Initiative name

**HeatShield: Heat Risk Dashboard and Mock Workflow Simulator**

### 5.2 One-sentence description

HeatShield is a Phase 0 dashboard concept that helps public-health and healthcare personnel review heat-health trends, understand vulnerable contexts, and simulate how a high-priority operational signal becomes a traceable task and handoff.

### 5.3 Primary user

The primary user for Pitch 1 should be:

> Public-health or healthcare coordinator responsible for interpreting heat-health information and coordinating local response tasks.

Other users can be described as supporting or future role-based views:

- community health worker
- facility contact
- local government or sub-district coordinator
- resident or caregiver in a simplified future view

### 5.4 Main decision supported

The dashboard should help the user answer:

> Which area, time period, or vulnerable context shows enough heat-health concern to create or review an operational task, and who should own the next handoff?

## 6. Phase 0 Scope

### In Scope

- Retrospective dashboard using historical aggregate heat-health indicators.
- Mock workflow simulator showing signal-to-task-to-handoff logic.
- Mock vulnerable cohort fields for demonstration only.
- Role-based concept views for public-health officer, CHW, and facility contact.
- Data provenance, timestamp, source, quality flag, and assumptions.
- Contact-point and handoff fields for the five supporting components.
- Phase 0 evaluation of feasibility, usability, clarity, traceability, and workflow completion.

### Out of Scope

- New weather forecasting model.
- Live production alert system.
- Clinical diagnosis or treatment recommendation.
- Patient-level clinical risk score.
- Real patient registry or identifiable personal data.
- Automated emergency dispatch.
- Final communication vendor selection.
- Legal compliance certification.
- Claiming reduced heat illness, mortality, hospital admission, or emergency visits.

## 7. Dashboard Concept

### 7.1 Core information hierarchy

The dashboard should prioritize:

1. **Heat-risk context:** area, period, indicator, level or trend.
2. **Evidence provenance:** source, unit, timestamp, data coverage, quality flag.
3. **Vulnerable context:** population or mock cohort context.
4. **Operational signal:** high-priority operational signal or outreach priority, not clinical risk score.
5. **Task layer:** owner, assignee, status, acknowledgement, fallback, escalation, review.

### 7.2 Key screens for prototype discussion

| Screen | Purpose | Primary user |
|---|---|---|
| Overview / Map or Area List | See heat-risk context and zones needing review | Public-health officer |
| Indicator Trend View | Review historical heat-health trends and source caveats | Public-health officer |
| Task Registry | See tasks by area, owner, assignee, status, overdue state | Public-health officer |
| My Tasks | Simple list of assigned tasks and status update | CHW or facility contact |
| Zone Detail | Show risk context, vulnerable context, and task counts | Officer / coordinator |
| Summary / Post-Event Review | Review completion, unresolved tasks, acknowledgement, and lessons | Coordinator / evaluator |

### 7.3 Two state systems that must not be confused

| State system | Meaning | UI implication |
|---|---|---|
| Heat-risk state | How concerning the heat signal is | Use map/list color and text label such as `Level N - label` |
| Task state | Whether work has been done | Use badges/icons such as not started, in progress, done, overdue |

This distinction is important because "how hot is it" and "has the work been completed" are different questions.

## 8. Data Concept

### 8.1 Evidence-backed data

Evidence-backed data should include fields such as:

- indicator ID
- metric name
- metric value
- unit
- geography level
- geography name or code
- year or period
- source file
- source sheet or locator
- data status
- quality flag

### 8.2 Mock or future fields

Mock or future fields should be visibly separated from evidence-backed data:

- mock case ID
- mock age group
- mock chronic-condition group
- mock living-alone status
- mock cooling access
- mock occupation group
- task status
- acknowledgement status
- fallback path
- audit comment

### 8.3 Data rules

- Missing values must not be converted to zero.
- Official alert levels must be separated from illustrative alert levels.
- Forecast, historical, and mock data must be labelled distinctly.
- Every processed record should preserve source and timestamp.
- Any threshold used in the demo should be labelled illustrative unless confirmed by an authoritative local source.

## 9. Operational Workflow Concept

The Phase 0 workflow can be described as:

```text
Heat data or historical trend
-> vulnerable context review
-> high-priority operational signal
-> human review
-> task creation
-> role-based handoff
-> acknowledgement
-> action or fallback
-> post-event or post-simulation review
```

For Pitch 1, the team should present this as a concept workflow, not as a finalized operational protocol.

## 10. Five Supporting Components at Contact-Point Level

The team agreed that Heat Risk Dashboard is the main component. The other five components should remain at contact-point level for Pitch 1.

| Supporting component | What to describe | What not to over-design |
|---|---|---|
| Vulnerable Population Registry | Who owns population context, what mock fields are used, what data is passed | Real patient registry or individual risk scoring |
| Action Workflow | What kind of task can be created and who owns it | Detailed clinical or field workflow |
| Communication Center | Which role sends which message through which channel | Final vendor or full public-alert strategy |
| Health Facility Preparedness | Which facility contact receives a notice and what status is reported | Clinical surge protocol |
| Post-Event Review | What completion, acknowledgement, and unresolved-task data is reviewed | Health outcome attribution |

## 11. Stakeholder and Handoff Summary

| Handoff | Sender | Receiver | Information passed | Phase 0 field to show |
|---|---|---|---|---|
| Meteorological data to dashboard | Weather or heat-data source | HeatShield data layer | Temperature, humidity, heat index, timestamp, source | source, timestamp, freshness |
| Heat signal to health coordinator | Dashboard | Public-health officer | Area, level/trend, caveat, vulnerable context | operational signal |
| Coordinator to local/facility role | Public-health officer | CHW, facility, local contact | Task, area, priority, action note | owner, assignee, status |
| Recipient acknowledgement | CHW/facility/local role | Dashboard/coordinator | Received or not received | acknowledgement status |
| Escalation or fallback | Coordinator/system operator | Backup role or channel | Unacknowledged or overdue task | fallback path |
| Review | Dashboard/evaluator | Team/stakeholders | completed, overdue, unresolved, gaps | review summary |

## 12. Phase 0 Evaluation

The prototype can legitimately evaluate:

- whether users understand the heat-risk information
- whether users can find source and timestamp
- whether users can identify which area or group needs attention
- whether users can create or interpret a task
- whether handoff owner and acknowledgement are visible
- whether task completion can be tracked
- whether the dashboard feels useful and understandable
- whether gaps are traceable for future roadmap decisions

The prototype should not evaluate:

- mortality reduction
- heatstroke reduction
- hospital admission reduction
- emergency service reduction
- clinical treatment appropriateness

## 13. Known Gaps and Assumptions

| Gap or assumption | Why it matters | How to present in Pitch 1 |
|---|---|---|
| Thai heat-index band differences | The team may find different official or published band structures | Human-confirmed decision required |
| Production data access | API, cadence, licence, and format may not be confirmed | Use file-based or mock ingestion in Phase 0 |
| อสม. heat-warning role | Locally plausible but not evidenced as heat-specific | Treat as assumption to validate |
| Digital exclusion | High-risk groups may not receive app/dashboard/SMS messages | Dashboard coordinates; delivery needs channel strategy |
| Acknowledgement timing | No evidence-based heat alert response window found | Define and test as Phase 0 parameter |
| Clinical risk scoring | No validated score for this prototype | Use outreach priority or operational signal only |
| Legal/privacy compliance | Cannot be certified by a course prototype | Use privacy-by-design and mock data only |

## 14. Recommended Pitch 1 Paper Structure

1. **Introduction:** heat as a global-health problem and why it belongs in Healthcare IT Management.
2. **Problem Statement:** fragmented heat-health data and the alert-to-action gap.
3. **Evidence and Local Relevance:** vulnerable populations, Thailand context, data and communication limitations.
4. **Current Tool Gap:** existing dashboards usually show risk or burden, not task ownership and acknowledgement.
5. **Proposed Initiative:** HeatShield retrospective dashboard and mock workflow simulator.
6. **Target Users:** public-health coordinator as primary user, with CHW/facility supporting views.
7. **Data and Governance Concept:** evidence-backed data, mock fields, provenance, quality flags, access, audit.
8. **Workflow Concept:** signal to task to handoff to acknowledgement to review.
9. **Phase 0 Evaluation:** usability, clarity, usefulness, task completion, traceability, acknowledgement.
10. **Assumptions and Roadmap Dependencies:** thresholds, data access, stakeholder ownership, local validation.
11. **Conclusion:** HeatShield tests whether heat-risk evidence can become a usable operational workflow.

## 15. Slide Narrative Draft

### Slide 1: Why Heat

Extreme heat is increasingly important as a global health issue. It affects vulnerable populations and creates preventable health risks when public-health action is delayed or poorly coordinated.

### Slide 2: The Real Gap

The issue is not only that heat data is missing. Heat-risk information exists, but it is fragmented and often stops at warning or visualization. It does not reliably become assigned, acknowledged, traceable action.

### Slide 3: Current Tool Gap

Existing tools show risk levels, historical burden, or public guidance. They rarely show ownership, task status, acknowledgement, fallback, and completion.

### Slide 4: Our Initiative

HeatShield proposes a retrospective Heat Risk Dashboard and mock workflow simulator for public-health coordination.

### Slide 5: Who Uses It

The primary user is a public-health or healthcare coordinator. Supporting role-based views can help CHWs and facilities see only the tasks relevant to them.

### Slide 6: How It Works

The dashboard shows heat-risk context, vulnerable context, source and timestamp, then supports a high-priority operational signal that can become a task and handoff.

### Slide 7: Safety Boundary

The prototype is not a weather model, not a clinical diagnosis tool, not a treatment protocol, and not a real patient registry.

### Slide 8: Phase 0 Evaluation

The project evaluates feasibility, usability, clarity, task completion, acknowledgement, traceability, and workflow fit, not health outcome improvement.

## 16. Working References and Traceability

Detailed source traceability remains in the member literature reviews and inventories:

- `00_raw_materials/01_Mod/Mod_literature_review.md`
- `00_raw_materials/02_My/My_literature_review.md`
- `00_raw_materials/03_Belle/Belle_literature_review.md`
- `00_raw_materials/04_Chris/Chris_literature_review.md`
- `00_raw_materials/04_Chris/Chris_source_inventory.md`
- `00_raw_materials/05_Com/Com_literature_review-v2.md`
- `00_raw_materials/06_June/June_evidence_review_notes.docx`

For the final paper, citations should be pulled from the member files rather than this integrated brief alone.

