# Project checks

This page explains the sample report figures. It is supporting documentation; you do not need to run code to understand the tracker.

## Why the date is 7 October 2026

The workbook uses **7 October 2026** as its example report date (`Instructions!B4`). It compares each open request's target date with that date to decide whether the request is overdue. It is a fixed example date, not a record of live work.

## What the numbers represent

The register contains **36 fictional practice requests** received between 1 September and 6 October 2026. The role names and source notes are fictional too. The status counts are **7 New, 9 In Progress, 6 Blocked and 14 Completed**. That leaves **22 open**; **9** are flagged overdue and **6** are blocked. The groups can overlap.

Two requests lack owners (DS-021 and DS-032). Two need a data check (DS-033 and DS-034). DS-034 has a target date earlier than its received date, yet that target is included in the nine overdue requests. The overdue figure should be treated as provisional until that input is corrected.

## How to check the project

1. Open the workbook. Check the report date on Instructions and the status reconciliation on Summary; it should say **PASS**.
2. Filter Requests by **Missing owner = Yes** and **Data issue = Review** to find the four IDs above. Compare the counts with `data/metrics.json`.
3. Compare the fixed-date figures in the status report, decision brief and slides with Summary. After editing the workbook, update those static files for a new report date.

For an automated file check, install `validation/requirements.txt` and run `python validation/check_project.py` from the project root. The check also reads internal Office package themes and properties, which may contain text that is not visible on sheets or slides. The workbook and presentation were also inspected through rendered file views. This project does not claim a live deployment or measured operational results.
