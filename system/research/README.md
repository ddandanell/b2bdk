# Research — Where Outputs Live

The `researcher` agent owns this folder. Other agents read from it. The
user reads it whenever they want to know what the world looks like.

## Folder structure

```
/system/research/
  competitors/{competitor-slug}.md       — one file per competitor
  keywords/{area-code}-{YYYY-MM}.md      — monthly keyword refresh per area
  market/{topic-slug}-{YYYY-MM}.md       — market trend briefs
  pain/{area-code}-{YYYY-MM}.md          — customer pain digest per area
  cases/{case-id}.md                     — real Bali Fixer case files
```

## File format (always this exact shape)

```markdown
# {Title}
*Researched by: researcher · Date: YYYY-MM-DD*

## TL;DR
- {3 bullets max}

## What I found
- {finding} — [source](URL)
- ...

## What this changes in our system
- `/system/keywords.md` → update area A{n}: ...
- `/system/plans/seo-roadmap.md` → add ...
- `/system/personas.md` → no change OR refine P{n}

## Sources
- [Title](URL)
```

## Cadence

| Type | Cadence | Owner |
| --- | --- | --- |
| Competitors | Quarterly + when a new one appears | researcher |
| Keywords | Monthly per area | researcher + seo-master |
| Market | Event-driven (policy change, news, raid) | researcher |
| Pain | Monthly per area | researcher |
| Cases | Within 48 hours of case closure | researcher |

## Rules

- **Cite every claim.** No "studies show" without a link.
- **5 sources minimum** for any market-trend brief.
- **Date every file** in the filename AND in the body.
- **Old research isn't deleted** — it's superseded by a newer dated file. Keep the history.
- If research contradicts a current lock in `/system/`, do **NOT** silently update the lock. Surface the contradiction to the user.

## How a research finding becomes a lock update

1. Researcher writes the file in `/system/research/`.
2. Researcher lists the proposed lock changes in the "What this changes" section.
3. User reviews.
4. If approved, the relevant specialist agent (seo-master for keywords, brand owner for brand.md) makes the lock change.
5. The research file stays as the audit trail for why the lock changed.

## Cross-references

Every research file should link to:
- The lock file(s) it informs (`/system/keywords.md`, etc.)
- The plan items it triggers (`/system/plans/seo-roadmap.md` week N)
- Any screenshots stored in `/system/assets/screenshots/`
