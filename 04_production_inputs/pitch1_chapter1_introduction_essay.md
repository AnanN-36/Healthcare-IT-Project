# Chapter 1 Introduction

## HeatShield: A Heat Risk Dashboard Roadmap Initiative for Evidence-Based Healthcare Coordination

**Course:** Principles of Global Healthcare Information Technology Management  
**Project type:** Phase 0 roadmap initiative  
**Main component:** Retrospective Heat Risk Dashboard with mock workflow simulator  
**Document status:** Draft for Pitch 1 and team review  
**Prepared:** 2026-08-27

## 1.1 Background and Rationale

Extreme heat is increasingly recognized as a global health concern because its effects extend beyond temporary discomfort or environmental exposure. Heat can influence population health, occupational safety, healthcare demand, social protection, and the ability of communities to maintain essential services. The burden is also unevenly distributed. Age, occupation, chronic disease, living arrangements, housing conditions, cooling access, social support, and access to health information can all influence how people experience and respond to heat.

The global evidence used in this project demonstrates the scale of the issue. The Lancet Countdown 2025 evidence reports that, in 2024, heatwave exposure increased by 304% among adults older than 65 years and by 389% among infants compared with the 1986-2005 baseline. It also reports 640 billion potential labour hours lost in 2024 and estimates that approximately 1.5 billion people, or 25.3% of the working-age population, worked in conditions associated with outdoor exposure. In addition, average annual heat-related deaths were estimated at 546,000 during 2012-2021, representing a 63.2% increase compared with the 1990-1999 baseline.

These indicators describe more than a temperature problem. They show that heat is related to health vulnerability, work capacity, economic pressure, service demand, and equity. Older adults and infants may have reduced physiological capacity to cope with heat. Outdoor workers may experience unavoidable exposure because their livelihoods depend on outdoor activity. People with chronic disease may face additional health vulnerability, while people living alone may have less immediate support when conditions become unsafe. In Thailand and other settings, local age patterns, occupational exposure, chronic disease, household conditions, and communication access may further shape the impact.

The evidence also highlights an important implementation challenge. Heat-health information is produced by different organizations for different purposes. Historical health indicators, meteorological observations, heat-index information, official advisories, vulnerable-population context, facility information, and local response records may be distributed across separate files, systems, formats, and governance arrangements. Information may be available without being connected to an accountable operational process.

This project therefore approaches heat-health as a Global Health Issue and a Healthcare IT Management problem. The global issue establishes the need, while the IT management perspective focuses on how evidence can be organized, interpreted, shared, acted upon, and reviewed across health-system levels.

## 1.2 Problem Statement

The central problem is that heat-health evidence and alerts can exist without a shared, traceable operational layer that shows what the signal means for a particular area or vulnerable context, who owns the next step, whether the handoff was acknowledged, and what remains unresolved.

The information journey required for coordinated heat-health action can be represented as follows:

```text
Heat and health evidence
-> interpretation of risk context
-> prioritization for attention
-> assignment of a responsible role
-> communication and handoff
-> acknowledgement and action
-> review of unresolved work
```

In practice, these stages may be separated across data sources, departments, organizations, and communication channels. A source may provide a valid indicator but not an operational owner. A dashboard may show a map or risk level but not a task. A message may be sent without confirmation that it was received or acknowledged. A task may be acknowledged without evidence that the action was completed. If a communication channel fails, the fallback route may be unclear or may depend on the same infrastructure.

These conditions create an alert-to-action gap. The gap does not necessarily mean that data or warnings are absent. Rather, it means that information is not consistently connected to a visible and accountable workflow. As a result, public-health and healthcare teams may need to reconcile multiple sources manually, repeat communication, spend time clarifying responsibility, or remain uncertain about unresolved work after a response period.

The problem can therefore be summarized as a connected chain:

```text
Heat-health burden
-> unequal exposure and vulnerability
-> fragmented information
-> unclear prioritization and ownership
-> incomplete handoff
-> invisible unresolved work
-> alert-to-action gap
```

The project does not assume that existing heat-risk tools are ineffective. Risk displays and public dashboards can provide valuable information about historical burden, current conditions, geographic variation, or public guidance. However, a risk display alone does not necessarily answer the operational questions that follow: Who reviews this information? Who owns the next task? Was the handoff acknowledged? What happens if the first channel fails? Is the task complete, escalated, or unresolved?

## 1.3 Significance of the Problem

The significance of this problem can be considered across health, workforce, social, financial, organizational, and technological dimensions.

At the health level, extreme heat can contribute to illness and mortality, particularly among people whose age, health, or social circumstances reduce their ability to protect themselves. At the workforce level, heat exposure can reduce safe working capacity and create productivity and income pressure. At the service level, healthcare facilities and community health teams may need to prepare for outreach, assessment, referral, transport, supplies, and follow-up. At the household level, individuals may have unequal access to cooling, information, transportation, healthcare, or social support.

These effects can generate financial and administrative consequences even when a project does not attempt to calculate a monetary impact. Organizations may need to allocate staff time, outreach resources, transport, supplies, communication capacity, and emergency preparedness budgets. Finance, accounting, procurement, insurers, funders, and administrative data teams may become relevant to planning and accountability. Logistics teams may need to coordinate supplies, transport, and field access. The information required by these groups is not identical, but their activities are connected through the health-system response.

The problem is also significant from an equity perspective. A digital-first response can exclude people with limited connectivity, limited digital literacy, older age, disability, language barriers, or reduced access to trusted communication channels. For this reason, a dashboard should not be treated as the only delivery channel. It should function as a coordination and confirmation layer that can reference human contacts and independent fallback routes.

From an IT management perspective, the problem involves data meaning, provenance, quality, access, workflow state, role ownership, communication handoff, auditability, and implementation feasibility. This makes the topic suitable for a Healthcare IT Management initiative: it requires the team to connect technology decisions with health-system roles, governance, resources, and real-world constraints.

## 1.4 Target Users and Affected Populations

The primary user for the first prototype is a district-level public-health or healthcare coordinator. This user is positioned at the point where heat-health evidence must be interpreted, prioritized, and connected to downstream coordination. The coordinator needs to understand the source and meaning of data, identify relevant population context, create or review an operational signal, assign a task, monitor acknowledgement, and identify unresolved work.

Supporting role concepts include community health workers or local contacts and healthcare facility contacts. These roles would receive focused views related to assigned tasks, status updates, handoff confirmation, and fallback requests. A data administrator would have restricted access to source files, provenance, freshness, validation, and quality flags. A resident or caregiver view may be considered in a future phase, but it is not part of the core Phase 0 workflow.

The initial vulnerable-population contexts are adults older than 65 years, infants younger than 1 year, outdoor workers, people with chronic disease, and people living alone. These contexts cover age-related vulnerability, occupational exposure, health vulnerability, and social support. In Phase 0, they will be represented through aggregate or mock fields. They will not be used to generate a patient-level clinical risk score, and the prototype will not contain names, addresses, personal identifiers, or identifiable patient records.

## 1.5 Stakeholders and Related Systems

Heat-health action involves multiple stakeholders across system levels. At the global level, organizations such as the World Health Organization, World Meteorological Organization, and global health evidence groups may provide evidence, frameworks, indicators, and policy direction. At the national level, health ministries, meteorological services, disaster-management authorities, and national policy or data units may provide warnings, governance, and data.

At provincial, regional, district, and local levels, health offices, local governments, public-health coordinators, facilities, and community networks translate broader direction into local action. Healthcare workers, nurses, clinicians, community health workers, emergency services, facility managers, pharmacy and supply staff may interpret, receive, perform, or report a task. Non-health stakeholders such as employers, schools, community leaders, NGOs, utilities, telecommunications providers, media, transport, and logistics teams may influence exposure, communication, infrastructure, access, or fallback support.

Finance and administration stakeholders, including budget owners, finance and accounting teams, procurement units, insurers, funders, and administrative data teams, may influence resource allocation and accountability. Data and technology stakeholders may manage source ingestion, access controls, audit trails, data quality, interoperability, and future integration. The affected population and caregivers remain the intended beneficiaries of the broader response.

Related systems may include climate and weather data, public-health surveillance, facility readiness information, administrative and financial tracking, communication systems, logistics systems, civil registration, and future interoperability services. HeatShield is not intended to replace these systems. It is positioned as a coordination and information layer that makes relationships, context, ownership, and workflow status more visible.

## 1.6 Proposed Concept: HeatShield

HeatShield proposes a retrospective Heat Risk Dashboard combined with a mock workflow simulator. The dashboard will organize historical heat-health indicators and related population context so that a coordinator can review trends and understand the meaning of each value. The display should include source, unit, time period, geography, coverage, freshness, and data-quality information. It should also clearly distinguish historical evidence, official advisory context, illustrative labels, and mock workflow data.

After reviewing the evidence, the coordinator can create a high-priority operational signal for human review. The term operational signal is intentional: the prototype will support coordination and prioritization, not clinical diagnosis or individual medical risk prediction. The signal can lead to a simulated task with an owner, assignee, priority, and status.

The simulated workflow will represent the following sequence:

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

The workflow will distinguish between sending a message, receiving it, acknowledging it, taking action, and completing the task. It will also separate heat-risk state from task state. A high-priority risk state does not mean that the response task is complete, and a completed task does not mean that the heat risk has disappeared.

The dashboard is designed as a coordination and confirmation destination, not as the only delivery channel. The prototype can represent communication channels, contact points, acknowledgement, and fallback without committing the project to a particular vendor, public-warning channel, policy threshold, or response-time standard.

## 1.7 Access and Coverage Boundary

Access will be considered role-based and limited to the information needed for each task. The district coordinator view may include aggregate trends, risk context, source metadata, quality flags, tasks, acknowledgement, fallback, and unresolved work. A community health worker or local contact view may include assigned tasks, status update, acknowledgement, and fallback request. A facility contact view may contain the limited information needed to confirm a handoff. A data administrator view may contain source, provenance, freshness, and validation information. A future resident or caregiver view would provide simplified guidance or contact information rather than operational detail.

The coverage boundary is equally important. Phase 0 will use historical aggregate data and a demonstration area or district-level concept. It will not claim national coverage, complete population coverage, live monitoring, or real-time weather integration. Chronic disease and living alone may remain mock or future local-linkage fields unless an approved aggregate source is identified. The system will also not assume that a dashboard reaches every affected person directly.

The practical Phase 0 question is therefore not whether the system covers everyone. It is whether a limited prototype can make evidence context, access, ownership, and response coverage visible enough to identify what should be validated before a future live phase.

## 1.8 Health-System Strengthening and Future Opportunity

The dashboard requirement concept provides a broader monitoring and evaluation lens in which inputs and processes lead to outputs, outcomes, and impact. Relevant domains include governance, financing, ICT and infrastructure, workforce, supply chain, information, service readiness, intervention coverage, equity, financial risk protection, responsiveness, and efficiency.

For HeatShield, this framework is a roadmap extension rather than a Phase 0 outcome claim. Inputs and processes may include data sources, information quality, governance, ICT, workforce, and contact points. Outputs may include task creation, acknowledgement, facility or contact status, and visible response coverage. Outcomes may later include intervention coverage, protective behaviour, service utilization, or unresolved risk. Impact may eventually relate to health outcomes, equity, social and financial risk protection, responsiveness, and efficiency.

The broader opportunity is a climate-health information and coordination platform that could support four health-service dimensions. Promotion could include consistent heat-health information, heat literacy, and community awareness. Prevention could include vulnerability context, outreach coordination, readiness monitoring, and coverage review. Treatment could include a clearer operational handoff to healthcare facilities or emergency services while preserving clinical judgment. Recovery could include post-event review, unresolved-task follow-up, resource learning, and policy improvement.

Policy, law, privacy, accessibility, financing, accountability, and interoperability are cross-cutting conditions for this future platform. They will remain roadmap and validation topics unless the team explicitly brings them into a later implementation phase.

## 1.9 Scope of the Phase 0 Initiative

The Phase 0 initiative will focus on historical aggregate heat-health evidence, selected Lancet Countdown data, candidate weather and heat-related data fields, source and quality metadata, aggregate or mock vulnerable-population context, and role-based concept views. It will demonstrate a mock signal-to-task-to-handoff workflow with acknowledgement, fallback, escalation, and post-simulation review. It will also evaluate feasibility, usability, comprehension, task completion, acknowledgement visibility, and traceability.

The initiative will not develop a new weather-forecasting or heat-index model. It will not operate as a live public-warning service, clinical decision-support system, diagnosis tool, treatment recommendation system, patient-level risk-scoring system, identifiable population registry, or automated emergency-dispatch system. It will not establish a final communication vendor, official local threshold, response-time policy, or claim reductions in mortality, heatstroke, hospital admission, or emergency visits.

This scope is necessary because the project is a four-month course initiative and a roadmap investigation. A focused Phase 0 can demonstrate a meaningful IT management contribution while making the requirements for future clinical, policy, data, security, and stakeholder validation explicit.

## 1.10 Expected Contribution

The expected contribution of HeatShield is a practical and testable connection between global-health evidence and healthcare coordination. The project will investigate whether historical heat-health information can be organized into a usable view that helps a district-level coordinator understand the source and context of a signal, identify a responsible role, create a task, track acknowledgement, represent fallback, and review unresolved work.

The project is not expected to prove health outcome improvement. Its Phase 0 contribution is to make an operational information gap visible and to produce a defensible roadmap for future implementation. The expected outputs are a retrospective dashboard concept, a mock workflow simulator, data and stakeholder matrices, governance controls, evaluation measures, and a set of decisions that must be validated before live deployment.

## 1.11 Working Conceptual Framework

The conceptual direction of the initiative can be summarized as:

```text
Global and local heat-health evidence
-> data context and quality interpretation
-> aggregate vulnerability context
-> human-reviewed operational signal
-> accountable task and handoff
-> acknowledgement, fallback, and escalation
-> post-event review and future learning
```

The framework connects the public-health problem with the IT management intervention. Heat-health evidence establishes the need. Data context and vulnerability information support interpretation. The dashboard makes the relevant information accessible to the intended role. The workflow simulator tests whether information can be connected to ownership, communication, acknowledgement, fallback, and review. The results inform the next phase without claiming that the prototype itself produces clinical or population-health impact.

## 1.12 Conclusion

Extreme heat is a global health issue because it produces unequal health, occupational, social, and economic burdens across populations and places. The available evidence establishes the importance of the problem, but evidence alone does not guarantee coordinated action. Information may remain distributed across sources, roles, organizations, and communication channels. The critical operational gap is the connection between seeing a signal and knowing what happens next.

HeatShield addresses this gap through a focused Healthcare IT Management proposal: a retrospective Heat Risk Dashboard with a mock workflow simulator for a district-level public-health or healthcare coordinator. The proposed concept connects historical evidence and aggregate vulnerability context to a human-reviewed operational signal, task ownership, handoff, acknowledgement, fallback, and review. The five supporting components remain at contact-point level so that the broader health-system context is visible without expanding Phase 0 into five additional products.

The first pitch should therefore present HeatShield as a roadmap initiative rather than a completed health intervention. Its purpose is to establish the problem, clarify the system relationships, define a realistic boundary, and test whether an information layer can make the path from evidence to accountable coordination visible enough to support future implementation decisions.

## 1.13 Questions for Further Validation

The following questions remain open for discussion with the team, instructor, and future stakeholders:

1. Is the district-level public-health or healthcare coordinator the correct primary user for the first prototype?
2. Which historical indicators are sufficiently authoritative and understandable for the first dashboard demonstration?
3. Which vulnerable contexts should be shown in the first version, and which should remain mock or future fields?
4. What information should a coordinator review before creating a high-priority operational signal?
5. Which handoffs are essential to demonstrate while keeping the five supporting components at contact-point level?
6. What access roles, geography, time period, and population coverage are realistic for Phase 0?
7. Which local authority, data access arrangement, threshold source, and stakeholder ownership must be confirmed before a future live pilot?

## 1.14 Evidence Traceability

| Content area | Primary project trace |
|---|---|
| Global heat-health burden and vulnerable contexts | `00_raw_materials/01_Mod/Mod_literature_review.md`, E1-E6 |
| Data sources, indicators, provenance, and quality fields | `00_raw_materials/02_My/My_literature_review.md` |
| User roles, task state, risk-state/task-state separation, and dashboard requirements | `00_raw_materials/03_Belle/Belle_literature_review.md` |
| Communication, acknowledgement, fallback, digital exclusion, and contact points | `00_raw_materials/04_Chris/Chris_literature_review.md`; `Chris_contact_point_matrix.md`; `Chris_channel_strategy.md` |
| Architecture, governance, privacy, auditability, and future interoperability | `00_raw_materials/05_Com/Com_literature_review-v2.md` |
| Phase 0 feasibility, thresholds, APIs, ownership, and evaluation boundary | `00_raw_materials/06_June/June_evidence_review_notes.docx` |
| Health-system strengthening inputs/processes -> outputs -> outcomes -> impact framework | `00_raw_materials/dashboard requirement concept.png` |
| Consolidated design decisions and boundaries | `03_matrices/feature_feasibility_impact_matrix.md`; `data_requirement_matrix.md`; `stakeholder_ecosystem_matrix.md`; `risk_governance_matrix.md`; `roadmap_decision_log.md` |

Detailed citations for final academic submission should be added from the original source documents. This chapter draft is a synthesized introduction based on the project's current evidence and design matrices.
