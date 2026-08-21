# Belle: IT Use Case, Product Requirements, and Frontend Dashboard Behavior — Heat Risk Dashboard

## 1. Problem Statement (with evidence)

Heat-health early warning systems now exist at national and regional scale (CDC/NWS HeatRisk, UKHSA Heat-Health Alerts, WHO/WMO-backed national systems), and their core job is to raise awareness and trigger a public health response before a heat wave causes illness or death.[^1][^2] But the evidence shows a persistent gap between an alert being issued and a coordinated action actually happening on the ground:

- **Intention–behavior gap at the individual level.** A 2026 study of public responses to heat-health alerts in England found that although 91% of people said they were willing to change their routine during a heat alert, only 41.6% actually reported taking protective action — and exposure to alerts was itself unequal, skewed against older adults, lower-income groups, and people with less education.[^3]
- **Coordination/implementation gap at the institutional level.** Governance research in Western Cape, South Africa found that health institutions are frequently limited to "reactive" activities like issuing warnings, rather than being embedded in preparedness, vulnerability mapping, or cross-sector response; multiple studies note that national/local heat action plans exist on paper but lack the structure to coordinate execution.[^4][^5]
- **Data/reporting gap.** Researchers at the University of Kansas note that inconsistent local data collection makes it hard to translate weather forecasts into a measurable human-health picture, which in turn makes it hard to target interventions (e.g., some neighborhoods have far less AC access than others in the same city, but this isn't visible in a single heat map).[^6]
- **A "reactive playbook" gap compared to other hazards.** Commentary on U.S. heat preparedness contrasts heat's lack of engineered institutional response with mature systems for cold-weather and hurricane response (vulnerability registries, wellness-check protocols, tiered mandated actions) — heat has the alert layer but not the operational-response layer.[^7]

**Working problem statement:** Public health officers, community health workers, and facilities currently receive heat-risk *information* (via HeatRisk-style forecasts/alerts), but there is no shared operational layer that turns a forecast into who-does-what-by-when — task assignment, escalation when action doesn't happen, and visibility into which vulnerable people/areas have actually been checked on. The dashboard's job is to close that last-mile gap, not to generate a new heat forecast.

## 2. Existing Tools Reviewed

| Tool | Type | Relevant features | Gap vs. this use case |
|---|---|---|---|
| NWS HeatRisk Forecast | Forecast map, decision-maker facing | 7-day, 5-level color-numeric risk index by location; built for state/local health officials | Read-only forecast — no task, assignment, or status layer[^8] |
| CDC HeatRisk Dashboard | Public-facing | Zip-code lookup, personalized guidance, links to resources | Consumer tool, no operational/coordination features[^9] |
| CDC Heat & Health Tracker | Surveillance dashboard | County-level ED visit rates (from NSSP), historical HRI burden, vulnerability/ZCTA data | Historical/epidemiological, not real-time task coordination[^10] |
| Harris County (Houston) Heat and Health Dashboard | Regional public health dashboard | 4-page dashboard; interactive ZCTA map layering illness data, social vulnerability, built-environment factors; daily updates (1-day data lag) | Designed for planners/officials to view patterns, not to assign or track field-level response tasks[^11] |
| HHS/NEMSIS heat-EMS dashboard | Federal surveillance | State/county heat-related EMS activation counts, demographic breakdowns from 911 data | Downstream (post-incident) signal, not a prospective coordination tool[^12] |
| UKHSA Weather Health Alerting System | Regional alert status board | Region-by-region alert level (color state) updated ~daily, tied to an Adverse Weather and Health Plan | Shows current alert *level*, not who is acting on it or task completion[^13] |

**Pattern across all reviewed tools:** every existing tool stops at "here is the risk level / here is the historical burden." None of them show task ownership, escalation state, or confirmation that an at-risk person, facility, or area was actually reached. That is the specific product gap this dashboard should fill.

## 3. Dashboard Users and Their Top Decisions

| User | Top decisions the dashboard should support |
|---|---|
| **Public health officer** (oversight/coordination) | Which zones are at elevated risk today? Which teams/facilities have unresolved tasks? Where do I need to escalate coverage? |
| **Community health worker (CHW)** | Which residents on my list need a check today? What's the priority order? How do I mark a check complete or flag a problem? |
| **Facility (clinic, shelter, cooling center)** | Are we in an alert period that changes our protocol? Do we have capacity/status to report up? |
| **Resident (at-risk individual)** | Am I at risk today? What should I do? Has someone been assigned to check on me (if enrolled in a program)? |
| **Caregiver** | Is the person I care for at risk today? Do I need to act, or has a CHW/facility already been assigned? |

Across all five, the recurring decision categories are: **awareness** (is there risk, and for whom), **prioritization** (who/where first), **task visibility** (what's assigned, what's done), and **escalation** (what happens when nothing is done in time).

## 4. Feature List: Must-have / Should-have / Out-of-scope

**Must-have (MVP)**
- Current heat-risk level by zone/area, sourced from an existing forecast (e.g., HeatRisk-style index), displayed on a map and as a list
- A registry of tasks tied to an alert (e.g., "check on resident X," "confirm cooling center Y is open") with status: not started / in progress / done / overdue
- Assignment of tasks to a CHW or facility
- Escalation state: a task that passes its time threshold without being marked done visibly changes state (e.g., overdue/red) and notifies the officer
- Data freshness indicator (when was this risk level / task list last updated)
- Role-based views: officer sees all zones/tasks; CHW sees only their assigned list; facility sees only their own status

**Should-have**
- Filters by zone, risk level, task status, and population vulnerability category
- Reporting/export view (e.g., end-of-day summary of completed vs. overdue tasks per zone)
- Historical view of past alert periods and completion rates (supports the "did the alert become action" question directly)
- Caregiver/resident-facing simplified view (risk today + assigned contact, if any)

**Out-of-scope (explicitly excluded from this track)**
- Designing a clinical treatment protocol
- Building a production system or selecting a final vendor
- Designing detailed workflows for all five supporting components beyond the dashboard itself
- Owning final visual design or service communication strategy (copy, branding, outreach channel strategy)
- Generating the underlying heat forecast/risk model — the dashboard consumes an existing risk index, it does not calculate one

## 5. Proposed IT Use Case

**Use case name:** Heat Risk Task Coordination Dashboard

**Actors:** Public health officer, Community health worker, Facility contact, Resident/Caregiver (view-only)

**Trigger:** A heat-risk alert (external forecast feed, e.g., HeatRisk-style index) reaches a defined threshold for a zone.

**Basic flow:**
1. System ingests/receives the current risk level per zone.
2. System surfaces the zone(s) at elevated risk to the officer.
3. Officer (or a pre-configured rule) generates tasks for CHWs/facilities in affected zones.
4. CHW/facility sees assigned tasks, works them, and updates status.
5. System tracks time-to-completion; tasks not completed within a defined window escalate (visible state change + notification to officer).
6. Officer monitors overall coverage in real time and can reassign or escalate further.
7. At alert close, system produces a summary of coverage (tasks completed vs. overdue) by zone.

**Success definition:** For a given alert period, the officer can answer, without leaving the dashboard: which zones were at risk, who was assigned to respond, what fraction of tasks were completed before escalation was needed, and where the response broke down. This directly targets the evidenced gap — that an alert does not reliably become a coordinated action — by making the action (or its absence) visible and trackable rather than assumed.

## 6. User Stories and Acceptance Criteria

**US-1 — Officer sees today's risk picture**
*As a public health officer, I want to see current risk level by zone on a map, so I can decide where coordinated action is needed.*
- AC: Map renders all configured zones with a color-coded risk level matching the ingested forecast data.
- AC: Each zone shows a "last updated" timestamp; if data is older than a configured threshold, the zone is visibly flagged as stale.
- AC: Clicking/tapping a zone opens a detail panel with task counts by status.

**US-2 — Officer assigns/reviews tasks**
*As a public health officer, I want to see all tasks across zones with their status, so I can identify where coverage is falling behind.*
- AC: List/table view of all tasks, filterable by zone, status, and assignee.
- AC: Overdue tasks are visually distinct (e.g., color + icon) and sortable to the top.
- AC: Officer can reassign a task to a different CHW/facility.

**US-3 — CHW works their list**
*As a community health worker, I want to see only my assigned tasks in priority order, so I know who to check on first.*
- AC: CHW view shows only tasks assigned to them, default-sorted by risk level then by time remaining before escalation.
- AC: CHW can mark a task done, add a short note, or flag an issue (e.g., "resident not home") in no more than two taps/clicks.
- AC: Status update reflects in the officer's view within a defined sync window.

**US-4 — Escalation on missed tasks**
*As a public health officer, I want tasks that are not completed in time to escalate automatically, so nothing silently falls through.*
- AC: Each task has a configurable time threshold; when exceeded without a "done" status, the task state changes to "overdue" automatically (no manual step required).
- AC: Overdue tasks generate a visible alert in the officer's view (e.g., badge count, top-of-list placement).
- AC: Non-goal: the MVP does not need to auto-reassign overdue tasks; surfacing the overdue state is sufficient for this scope.

**US-5 — Facility reports status**
*As a facility contact (e.g., cooling center), I want to report my current open/closed and capacity status, so the officer has an accurate operational picture.*
- AC: Facility can update a small, fixed set of status fields (open/closed, capacity indicator).
- AC: Facility view shows only their own record, not other facilities' internal data.

**US-6 — End-of-period summary**
*As a public health officer, I want a summary of task completion by zone at the end of an alert period, so I can report on and improve coverage.*
- AC: Summary view shows completed vs. overdue task counts by zone for a selected date range.
- AC: Summary is exportable (e.g., CSV) for reporting outside the tool.

## 7. Screen-Level Requirements

**Screen: Map/Overview (officer default view)**
- Map with zone polygons/markers colored by current risk level (5-level scale, consistent with HeatRisk-style conventions, to reduce training burden)[^8]
- Toggle between map and list view of zones
- Filter bar: risk level, task status, vulnerability category
- Data freshness indicator (global + per-zone)
- Empty state: if no zones are currently at elevated risk, show a clear "no active alerts" state rather than a blank map

**Screen: Task List**
- Table/list with columns: zone, task type, assignee, status, time remaining/overdue
- Status filter chips (not started / in progress / done / overdue)
- Sort default: overdue first, then soonest deadline
- Empty state: "no tasks yet for this alert" with a prompt to generate tasks (officer view only)

**Screen: My Tasks (CHW/facility view)**
- Simplified list, no map required for mobile-first use
- One-tap/click status update control
- Responsive requirement: must work on a small mobile screen in the field, single-column layout, large tap targets
- Empty state: "no tasks assigned to you today"

**Screen: Zone Detail**
- Current risk level + trend (rising/falling/steady over the past few days)
- Task counts by status for that zone
- List of facilities/CHWs active in that zone

**Screen: Summary/Report**
- Date-range selector
- Completion-rate chart by zone
- Export control

**Alert/status states used consistently across screens:** No alert (gray/neutral) → Low/Moderate/High/Extreme risk (matching an existing color scale) for *risk*, and Not started → In progress → Done → Overdue for *tasks*. Keeping these two state systems visually distinct (e.g., risk = background/map color, task = icon/badge) avoids users conflating "how hot is it" with "is the work done."

## 8. Frontend Feasibility Notes

- **Mock states needed for prototype:** at least one zone in each risk level, at least one task in each status (including overdue), one stale-data zone, one facility with each open/closed status.
- **Empty states needed:** no active alerts (map view), no tasks yet (task list), no tasks assigned (CHW view) — all three must be explicit designed states, not just a blank screen.
- **Responsive requirement:** CHW/facility views are mobile-first (field use); officer map/summary views can assume a larger screen but should not break below tablet width.
- **Component boundaries:** Risk-level badge, Task-status badge, Zone card, Task row, and Summary chart should be built as independent components so the same risk/task states can be reused consistently across the map, list, and detail screens.

## Sources

[^1]: NWS/CDC HeatRisk collaboration overview — https://www.cdc.gov/media/releases/2024/p0422-heat-protection.html
[^2]: WHO Early Warning and Response System (EWARS) / climate-health toolkit — https://www.who.int/teams/environment-climate-change-and-health/climate-change-and-health/capacity-building/toolkit-on-climate-change-and-health/early-warning-systems
[^3]: "The heat is on: Understanding public responses to heat-health alerts in England," ScienceDirect (2026) — https://www.sciencedirect.com/science/article/pii/S2214629626001568
[^4]: "The Implementation Gap: Cross-Sector Management of Heat-related Health Risks in Western Cape, South Africa" — https://www.medrxiv.org/content/10.1101/2025.05.08.25327279.full.pdf
[^5]: "Strengthening Heat Action Plans in the United States," PMC — https://pmc.ncbi.nlm.nih.gov/articles/PMC10088943/
[^6]: Kansas researchers on lack of cohesive government heat response, Kansas Reflector — https://kansasreflector.com/2026/05/07/kansas-researchers-issue-warning-about-lack-of-cohesive-government-response-to-heat-waves/
[^7]: "How Old Extreme Weather Playbooks Can Save Us From Future Heat," Forbes (2026) — https://www.forbes.com/sites/nicoleroberts/2026/07/29/how-old-extreme-weather-playbooks-can-save-us-from-future-heat/
[^8]: NWS HeatRisk overview — https://www.wpc.ncep.noaa.gov/heatrisk/ and https://www.weather.gov/media/safety/NWS-HeatRisk-X3-2024.pdf
[^9]: CDC HeatRisk Dashboard — https://ephtracking.cdc.gov/Applications/HeatRisk/ ; https://time.com/6970280/extreme-heat-risk-cdc-national-weather-service-tool/
[^10]: CDC Heat & Health Tracker (NSSP data) — https://cdc.gov/nssp/php/partnerships/cdc-heat-health-tracker-uses-nssp-data.html
[^11]: Harris County (Houston) Heat and Health Dashboard — https://experience.arcgis.com/experience/be9c2bb39005443ca0af5a7dc692f854/page/CDC-NWS-Heat-Risk-Tool ; https://www.houstonhealth.org/data-dashboards
[^12]: HHS/NEMSIS national heat-illness tracking system — https://www.axios.com/2023/08/09/biden-extreme-heat-illness-tracking-system
[^13]: UKHSA Weather Health Alerting System — https://ukhsa-dashboard.data.gov.uk/weather-health-alerts/heat?type=heat

---
*Note per file rule: this document consolidates public, non-identifiable secondary sources only. No real personal or patient-identifiable data is included.*
