# HeatShield Full-Team Problem State Synthesis
## Pitch 1 paper-ready brief from six research streams

**Status:** full-team synthesis draft  
**Date:** 2026-08-21  
**Project phase:** Pitch 1 / Problem State  
**Purpose:** prepare the base argument for the first pitch paper and slide narrative.

## 1. Inputs Reviewed

| Member | Main analyzed file | Contribution to the synthesis |
|---|---|---|
| Mod | `00_raw_materials/01_Mod/Mod_literature_review.md` | Health problem framing, vulnerable-population scope, safe retrospective dashboard boundary |
| My | `00_raw_materials/02_My/My_literature_review.md` | Heat-risk indicators, source feasibility, backend ingestion, quality flags, provenance |
| Belle | `00_raw_materials/03_Belle/Belle_literature_review.md` | IT use case, dashboard users, product requirements, role-based screens, user stories |
| Chris | `00_raw_materials/04_Chris/Chris_literature_review.md` | Stakeholders, contact points, channels, handoffs, acknowledgement, adoption, evaluation |
| Com | `00_raw_materials/05_Com/Com_literature_review-v2.md` | IT architecture, governance, privacy, audit, file-based ingestion, future interoperability |
| June | `00_raw_materials/06_June/June_evidence_review_notes.docx` | WHO/WMO policy framing, heat-health action logic, Phase 0 evaluation and feasibility |

Analyzed copies for Belle and Chris have been organized under:

- `02_analyzed_data_notebooklm/03_Belle/`
- `02_analyzed_data_notebooklm/04_Chris/`

## 2. Final Problem Statement for Pitch 1

Extreme heat is a global and local public-health problem, especially for vulnerable groups such as infants, older adults, outdoor workers, people with chronic disease, and people living alone. However, the strongest project gap is not simply the lack of heat information. Heat, climate, weather, vulnerability, and policy evidence already exist across multiple sources, but they are fragmented by format, geography, time scale, update cadence, data quality, source ownership, and operational accountability.

Current health information systems and public dashboards often show risk levels, maps, or historical burden, but they do not consistently show who should act, who owns the handoff, whether the message was acknowledged, whether a task was completed, and what failed during the response. This creates a digital operational gap between heat-risk evidence and public-health action.

**Working thesis:**

> HeatShield is not another weather dashboard. It is a Healthcare IT Management initiative that explores how fragmented heat-health evidence can be converted into a retrospective dashboard and mock workflow simulator for planning, prioritization, task ownership, handoff visibility, acknowledgement, and Phase 0 feasibility evaluation.

## 3. Integrated Findings

### 3.1 Health and Vulnerability

Mod and June establish that heat-health risk is legitimate as a global health issue and locally relevant to Thailand. The dashboard should focus on population-level evidence and vulnerable contexts, not patient-level diagnosis.

The agreed vulnerable contexts are:

- infants younger than 1 year
- older adults older than 65 years
- outdoor workers
- people with chronic disease
- people living alone

Chris adds an important Thailand-specific correction: Thai risk should not be framed only as frail older adults indoors. Outdoor and working-age exposure matters, and digital exclusion among older adults means a digital-first strategy may miss the very people the system intends to protect.

### 3.2 Data and Indicator Problem

My and Mod show that the dashboard must separate different evidence types:

- retrospective Lancet aggregate indicators
- local weather or heat-index data candidates
- official alert or advisory wording
- aggregate vulnerability context
- mock workflow and task data
- data provenance and quality metadata

The prototype should not merge these into one clinical risk score. Instead, it should show source-aware indicators, trends, quality flags, units, timestamp, and assumptions.

### 3.3 Product and User Problem

Belle clarifies the missing product layer. Existing heat tools often stop at "risk level" or "historical burden." HeatShield should answer the operational question:

> When heat risk is visible, who needs to do what, by when, and how do we know whether it happened?

The core users for the dashboard are:

- public health officer
- community health worker
- facility contact
- resident or at-risk individual
- caregiver

For Pitch 1, the most defensible primary user remains the public-health or healthcare coordinator. Resident and caregiver views can be described as future or simplified supporting views.

### 3.4 Stakeholder and Communication Problem

Chris makes the operational gap much sharper. A heat service is a chain of handoffs, not a single alert. Important handoffs include:

- meteorological service to health authority
- health authority to local government
- health authority to facilities
- local health office to community health workers
- community health workers to households
- dashboard or service operator to post-event review owner

Chris's central finding for this project:

> The dashboard should be a coordination and confirmation destination, not the delivery channel itself.

Delivery belongs to push channels, broadcast channels, institutional channels, and human contact. For Thailand, human contact through local actors may be especially important for older adults and digitally excluded groups, but use of อสม. for heat warnings is not locally proven and must be treated as an assumption to validate.

### 3.5 IT Architecture and Governance Problem

Com and My frame HeatShield as an IT management problem:

- source adapters and file-based ingestion
- static or mock data for Phase 0
- role-based access
- audit trail
- data minimization
- source traceability
- quality flags
- future interoperability direction

FHIR, LOINC, SNOMED CT, and ICD-11 can be mentioned only as future interoperability directions. They should not be presented as MVP implementation requirements.

### 3.6 Evaluation Problem

June and Chris agree that Phase 0 evaluation should measure feasibility and usability, not health impact. Suitable evaluation targets include:

- task completion
- alert-to-task conversion
- acknowledgement rate in simulated institutional handoffs
- data completeness
- traceability
- user comprehension
- perceived usefulness
- clarity
- trust
- actionability
- ease of use

The project must not claim reduced mortality, reduced heatstroke, or reduced hospital visits during Phase 0.

## 4. Review Notes on Chris

### Strongest contributions

Chris's work is the strongest current source for Pitch 1 on stakeholder and communication logic. The most useful contributions are:

- clear separation between alert issuance, dissemination, acknowledgement, action, and review
- contact-point matrix with sender, receiver, channel, fallback, acknowledgement, owner, and failure risk
- strong warning that transmission is not receipt, and receipt is not action
- evidence-informed channel strategy showing why SMS, app, email, and dashboard may share the same failure mode
- Thailand-specific cautions on older-adult digital exclusion, migrant-language limitations, and the unproven assumption that อสม. can deliver heat warnings
- evaluation framework that measures usability, clarity, trust, relevance, actionability, acknowledgement, and task completion without claiming health outcomes

### What to use directly in Pitch 1

- "The dashboard is a coordination and confirmation destination, not a delivery channel."
- "Acknowledgement should be a first-class field."
- "A fallback must have an independent failure mode."
- "Digital reach is not equal to vulnerable-population reach."
- "Every response-time or acknowledgement window is a Phase 0 test parameter, not an evidence-based standard."

### What to handle carefully

- Do not overclaim that อสม. is a validated Thai heat-warning channel. Present it as a plausible local contact point requiring confirmation.
- Do not present US, UK, Bangladesh, or hurricane evidence as direct Thailand heat evidence. Use them as analogies or transferable mechanisms only.
- Do not quote one Thai heat death number without naming agency and period, because Chris identifies conflicting agency figures.
- Do not let the channel section dominate the pitch. For Pitch 1, use it to prove the operational gap, not to finalize communication strategy.

## 5. Review Notes on Belle

### Strongest contributions

Belle fills the missing product/use-case layer. The strongest contributions are:

- clear user groups and top decisions
- strong statement that existing tools are mostly read-only risk or burden displays
- IT use case: Heat Risk Task Coordination Dashboard
- distinction between risk state and task state
- must-have features: zone risk, task registry, assignment, escalation state, data freshness, role-based views
- user stories and acceptance criteria that can later become prototype requirements
- frontend feasibility notes: mock states, empty states, mobile-first CHW/facility view, component boundaries

### What to use directly in Pitch 1

- The dashboard closes the "last-mile operational layer" between alert and action.
- Public health officers need to see zones at risk, unresolved tasks, and escalation points.
- CHWs need a priority task list, not a complex analytical dashboard.
- Facilities need a limited status/report-up view.
- Risk level and task completion must be visually distinct.

### What to handle carefully

- Belle's current-risk and real-time task flow should be reframed for this course phase as a mock workflow simulator. The main analytical dashboard remains retrospective.
- Resident and caregiver views are useful, but they may expand the scope. Present them as future simplified views unless the team chooses otherwise.
- Auto-escalation should be presented as a simulated state change, not an operational mandate.
- Any heat-risk level should be official only if mapped to a confirmed source. Otherwise, label it illustrative.

## 6. Updated Scope After Six Inputs

### In Scope for Pitch 1

- Problem-state framing for heat-health as a global and local issue.
- Retrospective dashboard concept using historical aggregate indicators.
- Mock workflow simulator showing how a signal becomes a task.
- Role-based concept views for public health officer, CHW, and facility contact.
- Contact-point and handoff layer for five supporting components.
- Data provenance, freshness, quality flag, assumptions, and auditability.
- Phase 0 feasibility and usability evaluation.

### Out of Scope for Pitch 1

- Production live warning system.
- New weather forecast or new heat-index model.
- Clinical diagnosis, treatment, or patient-level risk scoring.
- Real patient registry.
- Automated emergency dispatch.
- Final communication vendor or final public-alert channel.
- Proof of health outcome improvement.

## 7. Suggested Paper Structure for Pitch 1

1. **Introduction:** extreme heat as a global health issue and why it matters to healthcare IT.
2. **Problem State:** data and alerts exist, but the operational layer is fragmented.
3. **Evidence of Need:** vulnerable groups, Thailand context, fragmented sources, handoff failure, digital exclusion.
4. **Current Tool Gap:** existing dashboards show risk or burden but rarely show ownership, tasks, acknowledgement, and completion.
5. **Proposed Initiative:** HeatShield retrospective dashboard plus mock workflow simulator.
6. **Target Users and Decisions:** public-health officer as primary user; CHW and facility as operational views.
7. **Data and Governance Boundary:** historical aggregate data, mock workflow data, provenance, quality flag, privacy, no patient identifiers.
8. **Operational Concept:** signal to task to handoff to acknowledgement to review.
9. **Phase 0 Evaluation:** usability, comprehension, task completion, acknowledgement, traceability, data completeness.
10. **Known Gaps and Assumptions:** Thai thresholds, stakeholder ownership, อสม. heat role, channel reach, response windows, legal review.
11. **Conclusion:** HeatShield tests whether heat-risk evidence can be translated into a usable and accountable public-health coordination workflow.

## 8. One-Paragraph Pitch Draft

Extreme heat is a growing global health threat, but the gap our team identified is not simply a lack of heat data. Weather, climate, vulnerability, and public-health evidence exist, yet they are fragmented across sources and rarely connected to operational workflows. Existing dashboards usually show risk levels or historical burden, but they do not show who owns the response, whether a task was assigned, whether the alert was acknowledged, and whether the action was completed. HeatShield therefore proposes a Phase 0 retrospective Heat Risk Dashboard with a mock workflow simulator. The goal is to help healthcare and public-health personnel interpret heat-health trends, identify vulnerable contexts, create high-priority operational signals, assign or hand off tasks, and evaluate whether the workflow is feasible, understandable, traceable, and privacy-conscious before any future live implementation.

## 9. Decision Points for the Team

| Decision | Why it matters | Current recommendation |
|---|---|---|
| Primary user for pitch | Keeps scope focused | Public-health or healthcare coordinator |
| CHW/facility views | Useful but can expand scope | Include as mock role-based supporting views |
| Resident/caregiver view | High value but may be too broad | Defer to future simplified public view |
| Thai heat-index band | Conflicting source descriptions | Treat as a human-confirmed decision, not solved by prototype |
| อสม. channel | Locally plausible but unproven for heat | Mention as assumption to validate |
| Alert wording | Risk of confusion and colour-only interpretation | Use text plus level, never colour alone |
| Data source status | Some sources are scaffold or candidate | Separate confirmed evidence, candidate source, and mock data |
| Evaluation claim | Avoid overclaiming | Measure workflow and usability, not morbidity or mortality |

## 10. Matrix Seeds for Next Step

### Feature Feasibility and Impact

| Feature | Impact | Feasibility | Source stream |
|---|---|---|---|
| Retrospective trend dashboard | High | High | Mod, My |
| Source provenance and data freshness | High | High | My, Com, Chris |
| Mock high-priority operational signal | High | High | Mod, June, Belle |
| Task registry and status | High | Medium | Belle, Chris, Com |
| Acknowledgement field | High | Medium | Chris, June |
| Role-based views | Medium-High | Medium | Belle, Com |
| Channel fallback matrix | Medium-High | Medium | Chris |
| Public resident/caregiver view | Medium | Low-Medium | Belle, Chris |

### Risk and Governance

| Risk | Why it matters | Mitigation for Pitch 1 |
|---|---|---|
| Clinical overclaiming | Could make the project unsafe or clinically indefensible | Use operational signal, not clinical risk score |
| Data source ambiguity | Different sources have different units, timing, and geography | Show provenance, unit, timestamp, and quality flag |
| Thai threshold disagreement | Alert bands may not align across sources | Label as decision requiring confirmation |
| Digital exclusion | High-risk groups may not use internet or phones | Dashboard supports coordination; delivery needs human or non-digital channels |
| Unproven อสม. heat role | Locally plausible but not validated | Treat as Phase 0 assumption to test |
| Acknowledgement window unknown | No evidence-based heat standard found | Define as prototype parameter and evaluate |

## 11. Immediate Next Step

Use this synthesis to draft the Pitch 1 paper. The paper should not try to prove that HeatShield reduces heat illness. It should prove that the team has identified a meaningful global-health problem, translated it into a Healthcare IT Management gap, scoped a safe Phase 0 initiative, and knows which assumptions must be tested before any live implementation.

