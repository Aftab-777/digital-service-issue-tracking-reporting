# Data dictionary and calculation rules

The CSV holds input fields only. The workbook adds five calculated columns after Source or evidence note. Dates are calendar dates in ISO form in the CSV and Excel dates in the workbook. The as-of date is `Instructions!B4`.

| Field | Purpose |
|---|---|
| Request ID | Unique synthetic identifier |
| Date received | Start of the request age calculation |
| Request category | Access, Information, Reporting, Workflow or Document |
| Short description | Plain description of the issue |
| Priority | Low, Medium or High, set by the fictional team |
| Assigned owner | Fictional role responsible for follow-up; blank is flagged |
| Status | New, In Progress, Blocked or Completed |
| Target completion date | Working target for follow-up, not an SLA |
| Last update date | Date of latest recorded action |
| Next action | Concrete next step |
| Closed date | Required when status is Completed |
| Blocker or dependency | What prevents action, if any |
| Source or evidence note | Fictional note that identifies the supposed source |
| Age days | For Open records: as-of minus received; for Completed: closed minus received. Blank when dates needed for calculation are invalid. |
| Overdue | Yes when status is not Completed and target date is before the as-of date. Due today is not overdue. |
| Missing owner | Yes when Assigned owner is blank. |
| Data issue | Review for missing key dates, target before receipt, last update before receipt or after as-of, Completed without a valid closed date, or noncompleted with a closed date. |
| Open flag | 1 for New, In Progress or Blocked; 0 for Completed. |

**Open** means any status except Completed. **Blocked** is a distinct open status indicating a stated dependency. **Completed** is a status value and is excluded from open and overdue counts. These rules are internal assumptions for the portfolio simulation, not approved service standards. A missing owner is tracked separately from the Data issue flag so both problems are visible.
