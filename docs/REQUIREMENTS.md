# Requirements and acceptance criteria

**Project:** Operations Request Tracker and Reporting  
**Context:** Personal portfolio simulation using fabricated operations requests. The scenario is intended to be understandable in any team that coordinates incoming work.

## Users and needs

| Fictional user | Need | Project response |
|---|---|---|
| Service coordinator | Record requests consistently and see the next action | Filterable Requests table with owner, status, dates and next action |
| Assigned team member | Understand what is due and what is blocked | Target, blocker, last-update and evidence fields |
| Reporting analyst | Produce reconciled counts and find weak inputs | Formula-driven Summary and separate quality flags |
| Operations manager | Decide where to focus follow-up | One-page status report, prioritization brief and five-slide presentation |

## Acceptance criteria

1. The workbook contains 36 labelled synthetic requests and the documented input fields.
2. Status and priority inputs offer dropdowns; the as-of date is visible and editable.
3. Open, blocked, overdue and completed rules are documented and results reconcile to the request rows.
4. Missing-owner and inconsistent-record flags remain visible in the tracker and report.
5. The reports and slides use the workbook's 2026-10-07 baseline figures and state that the overdue count is provisional.
6. A user can edit a request or add one within the supported range and refresh Summary by recalculating Excel.
7. Any SharePoint mapping is clearly a proposal; no deployment is claimed.

## Scope boundary

The files demonstrate tracking and management communication with fabricated records. They do not demonstrate a live service desk, production workflow, stakeholder interviews or measured improvements.
