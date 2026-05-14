# The Bali Fixer Team

Six specialist agents. Each is trained against the locks in `/system/`.
Each has its own tools and model. **Never invoke them all at once** — pick
the right one for the task.

## The team

| Agent | Use it for | Definition file | Model |
| --- | --- | --- | --- |
| **web-designer** | UI, HTML/CSS, mobile-first builds | `.claude/agents/web-designer.md` | sonnet |
| **seo-master** | Keyword research, on-page SEO, content strategy | `.claude/agents/seo-master.md` | opus |
| **copywriter** | All written copy — meta, hero, body, ads, blog | `.claude/agents/copywriter.md` | sonnet |
| **researcher** | Competitor / market / regulatory / pain research | `.claude/agents/researcher.md` | opus |
| **project-manager** | Weekly planning, sprint, status, priorities | `.claude/agents/project-manager.md` | sonnet |
| **reviewer** | Pre-publish audit, persona walk-throughs | `.claude/agents/reviewer.md` | opus |

## How to start a session

Easiest: type `/start`. The router reads the sprint and offers a menu.

Specific flows:
- `/new-page` — full page build (designer + copy + SEO + review)
- `/audit` — runs reviewer
- `/plan-week` — runs project-manager

Or call any agent directly via the Agent tool when working freestyle.

## What each agent reads (the lock)

All agents read these before doing anything:
- `/system/brand.md`
- `/system/personas.md`
- `/system/keywords.md`
- `/system/templates.md`
- `/system/checklist.md`
- `/system/connect.md`

Plus their specialist files:

| Agent | Extra files |
| --- | --- |
| web-designer | `templates.md` skeleton + `brand.md` tokens + `assets/README.md` |
| seo-master | `keywords.md` + `plans/seo-roadmap.md` |
| copywriter | `templates.md` + `brand.md` voice |
| researcher | `research/README.md` + `research/*` history |
| project-manager | `plans/*` |
| reviewer | `checklist.md` + `personas.md` |

## How they hand off

```
new page  →  seo-master + copywriter  →  web-designer  →  reviewer  →  SHIP
research  →  researcher  →  proposes lock update  →  user approves  →  seo-master updates lock
plan week →  project-manager  →  user approves  →  current-sprint.md rewritten
audit     →  reviewer  →  punch list  →  copywriter + web-designer fix  →  reviewer re-runs
```

## Hard rules

- **Only the user updates the locks** in `/system/`. Agents propose changes; they don't push them silently.
- **One specialist owns each domain.** Don't ask the copywriter for SEO advice or the SEO master for visual decisions.
- **The reviewer is independent.** Never let a builder review their own work.
- **The router never freelances.** When you type `/start`, the main Claude is the router that dispatches — it shouldn't start writing copy or HTML directly.
