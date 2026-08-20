# Source 02: Frontend Requirements

Source-summary notes — screen-level requirements and frontend feasibility considerations for the Heat Risk Dashboard project.

## Problem Gap (frontend angle)

Existing heat-risk tools (NWS HeatRisk, CDC HeatRisk Dashboard, CDC Heat & Health Tracker, Harris County Heat and Health Dashboard, UKHSA alerts) are read-only: they show a risk level or historical burden, but their screens have no concept of an assigned task, its owner, or its completion state. A frontend built for this project needs a second state system — task status — layered on top of the familiar risk-level display, without the two being visually confused.

## Screens and Behavior

- **Map/Overview (officer default view):** zone polygons/markers colored by current 5-level risk (consistent with HeatRisk-style conventions to reduce training burden); toggle to list view; filters (risk level, task status, vulnerability category); data-freshness indicator, global and per-zone; explicit "no active alerts" empty state instead of a blank map.
- **Task List:** table with zone, task type, assignee, status, time remaining/overdue; status filter chips; default sort is overdue-first then soonest deadline; empty state ("no tasks yet for this alert") with a prompt to generate tasks, officer view only.
- **My Tasks (CHW/facility view):** simplified list, no map required; mobile-first, single-column, large tap targets; one-tap status update; empty state ("no tasks assigned to you today").
- **Zone Detail:** current risk level plus trend (rising/falling/steady); task counts by status for that zone; list of active facilities/CHWs in the zone.
- **Summary/Report:** date-range selector; completion-rate chart by zone; export control (e.g., CSV).

## Alert/Task State System

Two state systems must stay visually distinct so users don't conflate "how hot is it" with "is the work done":
- **Risk states:** No alert (neutral) → Low → Moderate → High → Extreme, shown as map/background color.
- **Task states:** Not started → In progress → Done → Overdue, shown as icon/badge rather than background color.

## Frontend Feasibility Notes

- **Mock states needed:** one zone per risk level; one task per status including overdue; one zone with stale data; one facility per open/closed status.
- **Empty states needed (must be explicitly designed, not blank):** no active alerts (map view), no tasks yet (task list), no tasks assigned (CHW view).
- **Responsive requirement:** CHW/facility views are mobile-first for field use; officer map/summary views can assume a larger screen but should not break below tablet width.
- **Component boundaries:** Risk-level badge, Task-status badge, Zone card, Task row, and Summary chart should be independent, reusable components so state representation stays consistent across map, list, and detail screens.

## Implementation Constraints

- The frontend consumes an existing risk index/forecast feed; it does not calculate heat risk itself.
- Data-freshness must be visible per zone, since source forecast data may update on different cadences than task data.
- Role-based view logic (officer / CHW / facility / resident-caregiver) is a frontend requirement, not just a backend permission — each role should see a purpose-built screen rather than a single screen with hidden fields.

Full source list and citations are provided in `literature_review.md`.
