---
description: Susan Social's engagement run. Finds fresh posts from creators you chose and drafts value-adding comments for you to post yourself. Usage /susan-engage [creators]
argument-hint: "[creators]"
---

# /susan-engage: Comment opportunities

Check `.claude/skills/susan-social/brand/engagement.md` and `rhythm.md`. If engagement is off, or today isn't an engagement day, say so and name the next one.

Start the `susan-engager` agent with the Agent tool, passing today's date and `content/engagement/`.

- *(no argument)*: a normal run, output to `content/engagement/<today>-engage.md`.
- `creators`: build or refresh the creator watchlist (`content/engagement/creators.md`) for the owner to approve. Run this once first.

Then tell the owner: the file, posts per platform, minutes needed (about 2 per comment), creators waiting for approval, and any paid lookup cost.

The owner posts every comment themselves. When they say which ones they posted, have the agent update `creators.md`.
