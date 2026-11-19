---
description: Susan Social's weekly report. The analyst reviews the last 7 days against your goals and writes rules for next week's plan. Report-only, no tasks for you on report day. Usage /susan-review [yyyy-mm-dd]
argument-hint: "[yyyy-mm-dd report date]"
---

# /susan-review: Weekly report (report-only)

Start the `susan-analyst` agent with the Agent tool for the 7 days ending the day before `$ARGUMENTS` (default: today). Report day and time come from `.claude/skills/susan-social/brand/rhythm.md` (default Friday 09:00).

Report day is report-only: no tasks or questions for the owner. Anything needed goes on the "For next work day" list.

Relay the short summary: best and worst post, new rules, progress on each KPI, a suggested change for next week, and the "For next work day" list.

To run this automatically, ask Claude to create a scheduled task for your report day and time. Scheduled tasks run while the Claude app is open on your computer.
