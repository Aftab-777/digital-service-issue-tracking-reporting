# Tracker User Guide

This guide is for a fictional service coordinator or analyst using the Excel tracker. The delivered reports reflect **7 October 2026**. Editing the workbook does not update the PDFs or presentation.

## Record and update a request

1. On **Requests**, add a new row at the bottom of the blue table. Enter a unique Request ID and the input fields in columns A-M. Choose Priority and Status from the dropdowns. Use real Excel dates, not text that looks like a date. If columns N-R do not fill into the new table row, copy their formulas from the row above.
2. Assign a role in **Assigned owner** and record a specific **Next action**. Update **Last update date** when the record changes, so someone reviewing the queue can tell how recent the information is.
3. Select New, In Progress, Blocked or Completed. For Completed, add a valid **Closed date** and describe the final action. A completed row leaves the open and overdue counts.

## Review the queue

1. Check the report date at `Instructions!B4`. A target date earlier than this date is overdue only when the request remains open. A target due today is not overdue.
2. Filter **Overdue** to Yes and **Status** to Blocked to find exceptions; the groups can overlap. Confirm the owner and next action before changing a target date. Record the reason for a revised target in the source note rather than changing it silently.
3. Filter **Missing owner** to Yes. DS-021 and DS-032 are examples for assignment review.
4. Filter **Data issue** to Review. DS-033 lacks a valid close date, and DS-034 has a target before receipt. Check the source note and a credible source before correction. DS-034 is currently counted overdue, making that headline number provisional.
5. Recalculate with **Formulas > Calculate Now** or F9 if Summary looks stale. Confirm the status reconciliation says PASS and compare counts with the checked baseline. Summary formulas cover rows 7-200; extend those ranges if needed.

## Manager review and reporting

Use the [weekly status report](../reports/Status_Report.md) to see the fixed snapshot and the [prioritization brief](../reports/Decision_Briefing.md) to decide whether to trial a regular exception review. Recheck flagged data before presenting the overdue count as settled. Update the static reports and slides after changing the workbook. Preserve an untouched copy before practice edits.

This is a synthetic portfolio tool, not a production ticketing system.
