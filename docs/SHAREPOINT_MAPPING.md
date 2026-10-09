# Suggested SharePoint list mapping

This is a **design suggestion only**. No SharePoint list, Power Apps app, flow or Microsoft 365 integration was created for this project.

| Tracker field | Suggested SharePoint column type | Note |
|---|---|---|
| Request ID | Single line of text, unique | Generated ID or controlled numbering needed |
| Date received | Date and time | Date-only display for this exercise |
| Request category | Choice | Five simulation values |
| Short description | Multiple lines of text | Avoid sensitive details in public examples |
| Priority | Choice | Low, Medium, High |
| Assigned owner | Person or Group | Replace fictional role with an approved owner |
| Status | Choice | New, In Progress, Blocked, Completed |
| Target completion date | Date and time | Date only |
| Last update date | Date and time | Could be updated by process |
| Next action | Multiple lines of text | Short action statement |
| Closed date | Date and time | Required when Completed |
| Blocker or dependency | Multiple lines of text | Explain who/what is needed |
| Source or evidence note | Multiple lines of text or hyperlink | Link to controlled evidence, not a public copy |

Age, overdue and quality flags may be calculated in a reporting layer or Power Automate after agreement on definitions and permissions. SharePoint's Modified timestamp is not automatically equivalent to Last update date as defined here.
