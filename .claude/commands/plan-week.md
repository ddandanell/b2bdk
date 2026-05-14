---
description: Run weekly planning with the project-manager agent
---

The user wants to plan the week.

1. Spawn the **project-manager** agent via Agent tool with `subagent_type: project-manager`.

2. The PM will:
   - Read `/system/plans/seo-roadmap.md` to see this week's roadmap slice
   - Read `/system/plans/backlog.md` for queued items
   - Read `/system/plans/current-sprint.md` (last week's, for carryover)
   - Propose this week's sprint with the cap (5 ship / 3 research / 3 review)

3. Return the proposed sprint to the user via AskUserQuestion:
   - Option 1: **Approve as-is** (PM overwrites `current-sprint.md`)
   - Option 2: **Edit before approving** (user dictates changes)
   - Option 3: **Re-do** (PM proposes a different theme)

4. Once approved:
   - PM overwrites `/system/plans/current-sprint.md`
   - PM updates `/system/plans/backlog.md` to remove committed items
   - Commit with message: `plan: sprint week of YYYY-MM-DD ({theme})`

5. Return the final sprint and the kill list + watch list to the user.
