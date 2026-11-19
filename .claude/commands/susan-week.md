---
description: Susan Social's approval-day pipeline. Researches, plans, writes, designs and packs next week's posts, stops for your approval, then schedules only what you approve. Usage /susan-week [yyyy-mm-dd Monday] [skip-research] | /susan-week approve
argument-hint: "[yyyy-mm-dd Monday] [skip-research] | approve"
---

# /susan-week: Weekly specialist pipeline

Read `.claude/skills/susan-social/brand/rhythm.md` first. If brand files still contain `[fill in]`, stop and suggest `/susan-setup`.

`$ARGUMENTS`:
- *(empty or a date)*: build the week starting that Monday (default: the next Monday at least 5 days away, in the owner's timezone). Runs stages 1 to 5, then stops for approval.
- `skip-research`: reuse a research brief less than 7 days old.
- `approve`: run stage 6 only, for the newest week folder with a `posting-pack.md`.

Week folder: `content/weekly/<monday>/` (create it if missing).

## Stages

Start each stage with the Agent tool and the matching `subagent_type`, giving it the week folder and Monday date. Wait for each to finish; they hand off through files. Stage 4's two agents run in parallel.

| Stage | Agent | Writes |
|---|---|---|
| 0. Latest report | *(no agent)* | Find the newest `content/reports/*-report.md`; pass its path on. Its rules are already in `learnings.md` |
| 1. Research | `susan-researcher` | `content/research/<monday>-brief.md` |
| 2. Plan | `susan-strategist` | `calendar.md` |
| 3. Write | `susan-copywriter` | `posts/day-NN-<slug>.md` |
| 4a. Design | `susan-designer` | Canva designs, `images/` |
| 4b. Video | `susan-video-creator` | `## Production` in each video post |
| 5. Approval pack | `susan-publisher` | `posting-pack.md` |
| *Stop for approval* | | |
| 6. Schedule | `susan-publisher` | scheduled posts or `upload-list.md`, `schedule-report.md` |

If a stage fails (a connector is down, Canva isn't connected), continue with what you have and list it. Never fake a result.

## The approval stop

Show the owner: the week folder, how many posts are ready, what's blocked (missing proof, open decisions, failed designs), and their one action: mark each post **approve / change / drop** (a reply like "approve all except 3 and 6" works). Re-run only the needed agent for "change" posts, then show them again. When every post has a decision, run stage 6 with exactly the approved post numbers.

## After stage 6

Report what's scheduled (with times), what's on the upload list, and what must be posted natively. Everything is finished on approval day; nothing lands on the owner's free days.
