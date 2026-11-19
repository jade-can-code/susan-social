# Susan Social

**A specialist social media team for Claude Code.** Susan Social interviews you about your business, sets itself up around your brand, and then runs a weekly content pipeline with one specialist agent per job: research, planning, writing, design, video, scheduling, reporting and community engagement.

Built by [The Vine System](https://thevinesystem.com). MIT licensed.

---

## What you get

| Agent | Job |
|---|---|
| `susan-researcher` | Finds what's working in your niche this week: hooks, formats, trends, competitor ads |
| `susan-strategist` | Turns research and your real results into a weekly content calendar |
| `susan-copywriter` | Writes every caption, script, carousel and thread in your voice |
| `susan-designer` | Builds graphics in Canva from your own templates and photos |
| `susan-video-creator` | Turns scripts into shot lists and edit notes you (or an editor) can follow |
| `susan-publisher` | Builds your approval pack, then schedules only what you approve |
| `susan-analyst` | Weekly report on what worked, and rules the strategist learns from |
| `susan-engager` | Finds fresh posts from creators your audience follows and drafts comments for you to post |

| Command | When |
|---|---|
| `/susan-setup` | Once, at the start. The interview (quick or full). Re-run or deepen any section later |
| `/susan-week` | Your approval day. Builds next week and stops for your approval |
| `/susan-week approve` | After you approve. Schedules the approved posts |
| `/susan-review` | Your report day. Report-only |
| `/susan-engage` | Your engagement days. Comment drafts for you to post |

Plus nine skills: `susan-paid-ads-plan`, `susan-ad-math`, `susan-competitor-ads`, `susan-ad-creative-brief`, `susan-landing-page-review`, `susan-ab-test`, `susan-performance-report`, `susan-reel-edit-plan` and `susan-canva-production`.

## Safety by design

- **Nothing is posted, scheduled, commented, liked, followed or messaged without your explicit approval, item by item.** The engager never posts at all: you post your own comments.
- **No invented numbers.** Results, stats and testimonials come only from your proof file.
- **No AI images of real people,** and no AI version of your face or voice.
- **Your brand stays private.** Everything the interview learns is written to files in *your* copy. Keep that copy private (see below).

## Install

You need [Claude Code](https://claude.com/claude-code) (desktop app or terminal) on a paid Claude plan.

1. **Make your own private copy.** On GitHub, click **Use this template → Create a new repository**, and set it to **Private**. Your brand files will live there, so don't make your filled-in copy public.
2. **Download it** to your computer (GitHub Desktop, or `git clone`).
3. **Open that folder in Claude Code.**
4. **Type `/susan-setup`** and answer the interview. Choose quick setup (about 15 minutes, with sensible defaults you can change later) or full setup (about 45 minutes). It saves as you go, and you can stop and pick up later.

When the interview finishes, Susan writes your brand files, gives you a personal guide for connecting your channels, and suggests a weekly rhythm.

## How a week works (default rhythm, yours to change in setup)

| Day | What happens | Your part |
|---|---|---|
| Mon, Tue, Thu | `/susan-engage` | Post the comments you like (about 2 minutes each) |
| Wed | `/susan-week`, then `/susan-week approve` | Approve, change or drop each post for next week |
| Fri 09:00 | `/susan-review` | Read the report. No tasks |

Once posts are on a scheduler (Buffer, Meta Business Suite, TikTok Studio and so on), they go out from that service's servers. Your computer can be asleep.

## What it costs

Susan Social is free. You may choose to use paid services alongside it (a paid Claude plan is required; a scheduler or Canva plan is optional). The setup interview asks your budget and only suggests paid tools you say yes to.

## Folder map

```
.claude/
  agents/            the eight specialist agents
  commands/          /susan-setup, /susan-week, /susan-review, /susan-engage
  skills/
    susan-social/    the operating manual, guardrails and your brand files
      brand/         filled in by /susan-setup
      lessons.md     your corrections (always win)
      learnings.md   what your real results say works
    susan-*/         the specialist skills
content/             created as you go: research, weekly posts, reports, engagement
```

## Credits and licence

Created by The Vine System. Released under the MIT licence (see `LICENSE`). Use it, adapt it, build on it.
