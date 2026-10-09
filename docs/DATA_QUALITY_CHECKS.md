# Data Quality Checks

Use these checks before a status pack is discussed as a reliable snapshot. The date below is the delivered baseline, not a live feed.

1. Confirm `Instructions!B4` is **2026-10-07**. The baseline CSV has **36 unique IDs** and a received-date span of 1 September to 6 October 2026.
2. In Summary, confirm the four statuses add to 36 and Reconciliation says **PASS**. The expected values are 7 New, 9 In Progress, 6 Blocked and 14 Completed.
3. Check **Open 22**, **Blocked 6**, **High priority open 6**, **Missing owner 2**, **Data issue 2** and **Overdue 9**. Blocked and overdue can overlap.
4. Filter Missing owner = Yes. Confirm **DS-021** and **DS-032**. Filter Data issue = Review. Confirm **DS-033** and **DS-034**.
5. Inspect **DS-033**: Completed with no closed date. Inspect **DS-034**: target date 2 October precedes received date 4 October. Its target also precedes the as-of date, so it is in the overdue count. Do not simply remove it from the count without checking and correcting the source record.
6. For a disposable-copy change check, complete overdue DS-003 with a valid closed date and recalculate. Open should become **21**, overdue **8** and Completed **15**. Restore the original before any other check. Then add a new open DS-037 within the table and supported range; Total and Open should each rise by one. Keep the delivered workbook at its original baseline.

The [project checks](../validation/VALIDATION.md) give a short way to verify the figures. A real team would also decide how to record source corrections and who can approve target changes.
