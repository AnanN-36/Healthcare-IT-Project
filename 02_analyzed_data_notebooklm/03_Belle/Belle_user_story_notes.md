# Belle_user_story_notes.md — Heat Risk Dashboard

Source: distilled from `Belle_literature_review.md` (IT Use Case, Product Requirements, and Frontend Dashboard Behavior).

## Users and Top Decisions (context for the stories below)

| User | Top decisions the dashboard should support |
|---|---|
| Public health officer | Which zones are at elevated risk today? Which teams/facilities have unresolved tasks? Where do I need to escalate coverage? |
| Community health worker (CHW) | Which residents on my list need a check today? What's the priority order? How do I mark a check complete or flag a problem? |
| Facility (clinic, shelter, cooling center) | Are we in an alert period that changes our protocol? Do we have capacity/status to report up? |
| Resident (at-risk individual) | Am I at risk today? What should I do? Has someone been assigned to check on me (if enrolled in a program)? |
| Caregiver | Is the person I care for at risk today? Do I need to act, or has a CHW/facility already been assigned? |

## User Stories with Acceptance Criteria

### US-1 — Officer sees today's risk picture
*As a public health officer, I want to see current risk level by zone on a map, so I can decide where coordinated action is needed.*
- AC: Map renders all configured zones with a color-coded risk level matching the ingested forecast data.
- AC: Each zone shows a "last updated" timestamp; if data is older than a configured threshold, the zone is visibly flagged as stale.
- AC: Clicking/tapping a zone opens a detail panel with task counts by status.

### US-2 — Officer assigns/reviews tasks
*As a public health officer, I want to see all tasks across zones with their status, so I can identify where coverage is falling behind.*
- AC: List/table view of all tasks, filterable by zone, status, and assignee.
- AC: Overdue tasks are visually distinct (e.g., color + icon) and sortable to the top.
- AC: Officer can reassign a task to a different CHW/facility.

### US-3 — CHW works their list
*As a community health worker, I want to see only my assigned tasks in priority order, so I know who to check on first.*
- AC: CHW view shows only tasks assigned to them, default-sorted by risk level then by time remaining before escalation.
- AC: CHW can mark a task done, add a short note, or flag an issue (e.g., "resident not home") in no more than two taps/clicks.
- AC: Status update reflects in the officer's view within a defined sync window.

### US-4 — Escalation on missed tasks
*As a public health officer, I want tasks that are not completed in time to escalate automatically, so nothing silently falls through.*
- AC: Each task has a configurable time threshold; when exceeded without a "done" status, the task state changes to "overdue" automatically (no manual step required).
- AC: Overdue tasks generate a visible alert in the officer's view (e.g., badge count, top-of-list placement).
- AC: Non-goal: the MVP does not need to auto-reassign overdue tasks; surfacing the overdue state is sufficient for this scope.

### US-5 — Facility reports status
*As a facility contact (e.g., cooling center), I want to report my current open/closed and capacity status, so the officer has an accurate operational picture.*
- AC: Facility can update a small, fixed set of status fields (open/closed, capacity indicator).
- AC: Facility view shows only their own record, not other facilities' internal data.

### US-6 — End-of-period summary
*As a public health officer, I want a summary of task completion by zone at the end of an alert period, so I can report on and improve coverage.*
- AC: Summary view shows completed vs. overdue task counts by zone for a selected date range.
- AC: Summary is exportable (e.g., CSV) for reporting outside the tool.

## Non-goals called out across the stories
- Auto-reassignment of overdue tasks (out of scope for MVP; only the overdue state needs to surface).
- Clinical protocol content, production build, and final visual/communication design remain out of scope for this research track (see `Belle_literature_review.md`, Section 4).

---
*File rule note: keep source files unchanged; do not add real personal or patient-identifiable data to this repository.*
