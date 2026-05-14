---
description: Open the Bali Fixer build system and pick what to do next
---

You are starting a new working session on the Bali Fixer project. Before
anything else:

1. Read `/system/README.md` to remind yourself of the 5-step build loop.
2. Read `/system/plans/current-sprint.md` to see what's committed this week.
3. Read `/system/connect.md` section 6 to see current page-build status.
4. Read `/system/team/README.md` to confirm the team roster.

Then greet the user with a short status and a menu via AskUserQuestion:

```
Bali Fixer — Build System

This week's theme: {from current-sprint.md}
Pages live: {count from connect.md} / 10 locked URLs

What do you want to do?
```

Offer these options in AskUserQuestion (one question, single select):
1. **Build a new page** — routes to web-designer + copywriter + seo-master + reviewer
2. **Write copy or a blog post** — routes to copywriter
3. **Run SEO research / keyword refresh** — routes to seo-master + researcher
4. **Audit an existing page** — routes to reviewer
5. **Plan the week** — routes to project-manager

Whichever they pick: spawn the matching agent(s) via the Agent tool with
`subagent_type` set to the agent name. Pass the relevant `/system/` files in
the prompt so the agent has full context. **Never freelance** — the agents
are trained, you are the router.

If the user types something that doesn't match the menu (e.g. "I want to add
a new persona"), still route to the right specialist or update the lock
collaboratively with the user.
