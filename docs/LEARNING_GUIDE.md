# Learning guide: explain the tracker and reporting

## What the workbook does

Instructions holds the editable report date and definitions. Requests stores 36 fabricated records plus five formula columns. Summary counts requests by status, category and priority and highlights open, overdue, blocked and quality items. The CSV is the uncalculated source snapshot.

## Why the fields exist

ID prevents confusion between requests. Received date starts the age clock. Category and priority support triage and reporting. Description states the issue. Owner and next action support accountability. Status shows progress. Target date lets the team spot lateness. Last update tells readers whether the record is current. Closed date supports completion checks. Blocker records a dependency. Evidence note states what to verify before acting.

## How the key formulas work

- Open flag uses `IF(Status="Completed",0,1)` for a populated row. Summary adds those flags.
- Overdue uses `AND(Status<>"Completed", Target<AsOf, Target<>"")`. A completed item is excluded even if it finished after target.
- Age uses `AsOf-Received` while open and `Closed-Received` after completion. Invalid required dates leave a blank.
- Missing owner checks whether Assigned owner is blank.
- Data issue checks date order and whether Closed date agrees with Status.
- Summary uses `COUNTIFS` and `SUM` on the request rows. The as-of date is a visible cell, not the computer's changing TODAY value.

## How the recommendation follows from evidence

At the baseline, 22 of 36 requests are open, 9 are overdue, 6 are blocked, 2 have no owner and 2 contain a date/status inconsistency. That combination supports a short owner-led review of overdue and blocked work **and** correction of the flagged inputs before presenting trends as operational performance. The numbers do not prove staffing shortages or service failure.

## What remains uncertain

All records are synthetic. Targets are assumptions rather than official deadlines. Status conventions, prioritization, escalation rights, data retention and SharePoint permissions would require stakeholder confirmation. The static reports and slides must be regenerated or manually revised after workbook edits.

## Exercises for Aftab to complete and record

1. Add DS-037 with all fields. Check that the total and relevant category/status count each increase by one.
2. Change one open request to Completed and add a valid Closed date. Check that open and overdue counts change as expected.
3. Explain the Overdue formula aloud, including why a target due on the as-of date is not overdue.
4. Find DS-034, explain its inconsistent target date, then correct it after choosing a defensible hypothetical date.
5. Rewrite the recommendation paragraph of the decision briefing in your own words while preserving its evidence.
6. Give a three-minute explanation covering the problem, tracker, findings, recommendation and limitations.

## Questions for a project walkthrough

**Why did you include an as-of date?** It makes the overdue calculation reproducible. Changing the date gives a different snapshot, so reports must state which date they use.

**How is blocked different from overdue?** Blocked means a dependency prevents progress. Overdue means an open item passed its target date. An item can be both.

**Why separate missing-owner and data-issue flags?** They need different repairs. An owner assignment is a coordination task; an impossible date or status conflict requires source verification.

**What would you ask stakeholders first?** Confirm status meanings, completion evidence, ownership, target-date rules and escalation authority before production use.
