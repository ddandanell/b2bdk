---
description: Build a new landing page using the 5-step loop and the specialist agents
---

The user wants to build a new page. Walk this exact flow. **Don't skip steps.**

## Step 1 — Identify AREA + PERSONA

If not obvious from the user's request, ask via AskUserQuestion:
- Which AREA (A0–A9 from `/system/keywords.md`)?
- Which PERSONA (P1–P5 from `/system/personas.md`)?

Confirm the URL slot is free per `/system/connect.md` section 1.

## Step 2 — Spawn seo-master (parallel with step 3)

Use the Agent tool with `subagent_type: seo-master`:
- Re-read the locked keywords for the chosen area
- Verify they're still current with 1–2 web searches
- Return: confirmed primary + 3 secondary + 2 long-tail + 2 pain queries
- Identify schema.org types needed (LocalBusiness, Service, FAQPage, etc.)

## Step 3 — Spawn copywriter (parallel with step 2)

Use the Agent tool with `subagent_type: copywriter`:
- Pass the AREA + PERSONA + the SEO master's confirmed keywords
- Draft: meta title, meta description, H1, hero subhead, body sections, FAQ answers, CTA labels
- Return ready-to-ship copy in the locked output shape

## Step 4 — Spawn web-designer

Use the Agent tool with `subagent_type: web-designer`:
- Pass the copy from step 3 + the SEO outputs from step 2
- Build the actual HTML page at the right URL slot per `/system/connect.md`
- Apply brand tokens from `/system/brand.md`
- Use the landing-page skeleton from `/system/templates.md`
- Wire internal links per `/system/connect.md` sibling matrix

## Step 5 — Spawn reviewer

Use the Agent tool with `subagent_type: reviewer`:
- Pass the new page path
- Run the 3-pass review method (checklist, persona walk-through, adversarial)
- Return SHIP / FIX BEFORE SHIP / REBUILD verdict

## Step 6 — Loop or commit

- If **FIX BEFORE SHIP**: re-spawn copywriter and/or web-designer to address the punch list. Re-run reviewer. Repeat until SHIP.
- If **REBUILD**: surface to the user. Don't just rebuild — the lock or the persona match may be wrong.
- If **SHIP**:
  1. Update `/system/connect.md` section 6 site map (mark ✅ built)
  2. Commit with message format: `feat: ship /fix/{slug} (area A{n}, persona P{n})`
  3. Confirm to user

## Important

You are the **router**, not the builder. All actual work happens in the
specialist agents. If you find yourself writing copy or HTML directly,
you've gone off-flow — back up and spawn the right agent.
