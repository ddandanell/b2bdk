# Bali Fixer — Build System

This is the locked content/brand system for Bali Fixer. Every piece of content
you write — meta tags, landing pages, blog posts, ads, WhatsApp templates,
emails — references the files in this folder. The system is the source of
truth. If you find yourself making a decision twice, lock it here.

---

## The 5-step build loop

Before publishing **anything**, walk these five steps in order:

1. **Identify the AREA.** Open `keywords.md`. Which of the 10 areas (A0–A9)
   does this content belong to? Every piece belongs to exactly one.
2. **Identify the PERSONA.** Open `personas.md`. Which persona (P1–P5) is
   this for? Pick one. Don't write for two.
3. **Pull the LOCKED KEYWORDS.** From the area in step 1, copy the primary,
   2–3 secondary keywords, and the closest long-tail intent phrase.
4. **Open the matching TEMPLATE.** From `templates.md`, find the template
   for your content type (meta, landing, blog, ad). Fill it with the locks.
5. **Run the CHECKLIST.** Open `checklist.md`. Tick every line before publish.

If you ever feel "I'm not sure how to phrase this" — you skipped a step.

---

## File map

### The lock (strategy)
| File | What it locks |
| --- | --- |
| `brand.md` | Name, promise, position, voice rules, banned words, colors |
| `personas.md` | The 5 humans we write for (P1–P5) |
| `keywords.md` | 10 area-clusters of locked keywords (A0–A9) |
| `templates.md` | Copy-paste templates per content type |
| `checklist.md` | Pre-publish operational checklist |
| `connect.md` | How any new build wires into the existing site |

### The team (execution)
| Folder | What it holds |
| --- | --- |
| `team/` | Index of the 6 specialist agents |
| `plans/` | Roadmap, current sprint, backlog, cadence |
| `assets/` | Image/file storage rules + library |
| `research/` | Research outputs (competitors, keywords, market, pain, cases) |

Plus the wiring in `/.claude/`:
- `.claude/agents/` — 6 trained sub-agents (web-designer, seo-master, copywriter, researcher, project-manager, reviewer)
- `.claude/commands/` — slash commands: `/start`, `/new-page`, `/audit`, `/plan-week`

## How to start working

Type `/start` and the router reads the sprint, then offers a menu. See
`team/README.md` for the full team list.

---

## What's already built

- `/index.html` — homepage. Built using area **A0** + personas **P1** & **P2**.
  Proves the system works end-to-end.

## What's next to build (in priority order)

1. `/fix/scooter-accident` (A1, P1) — highest urgency, highest paid-search CPC
2. `/fix/visa-overstay` (A2, P1+P4) — highest evergreen search volume
3. `/fix/landlord-dispute` (A4, P2) — highest LTV per case
4. `/membership` (A9, P4+P5) — highest revenue per visitor
5. Remaining `/fix/*` pages
6. `/blog/*` SEO content per area
7. `/cases/*` real case studies

---

## How to add a new area

Found a new type of problem we fix? Don't write the page first. Add the new
area to `keywords.md` using the existing 11-row format. Lock its keywords.
THEN build the page using the 5-step loop.

---

## Rule of the lock

Once a keyword, persona, or template is locked, it doesn't change just because
you have a "better idea" mid-build. If it's actually wrong, update the lock
here first, then rebuild. **The lock changes deliberately, not in the moment.**

If a build feels like it's pulling away from the lock, stop. The build is
wrong, not the lock. Either:
- the area is wrong (re-pick from `keywords.md`)
- the persona is wrong (re-pick from `personas.md`)
- you're trying to write a page that doesn't belong on this brand at all.
