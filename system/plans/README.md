# Plans — How We Run the Cadence

This folder holds the rolling plan and the weekly sprint. The
`project-manager` agent owns these files; everyone else reads them.

## Files

- `cadence.md` — daily / weekly / monthly / quarterly rhythm
- `seo-roadmap.md` — the rolling 12-week SEO build plan
- `current-sprint.md` — this week's commitments (rewritten every Monday)
- `backlog.md` — committed-to-do but not yet in a sprint

## How a task moves

```
idea → backlog.md → current-sprint.md → done (deleted) → archived in roadmap
```

If a task isn't in `current-sprint.md`, it doesn't get worked on this week.
**No shadow work. No "while I was in there" creep.**

## Sprint reset (every Monday)

1. Open `current-sprint.md` from last week.
2. Move incomplete items to "Carryover".
3. Pull new items from `seo-roadmap.md` (this week's slice).
4. Pull urgent items from `backlog.md` if any.
5. Cap: **5 ship, 3 research, 3 review.** Anything beyond goes back.

Run `/plan-week` and the project-manager agent walks this for you.
