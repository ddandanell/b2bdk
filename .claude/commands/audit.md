---
description: Run a full review on an existing page using the reviewer agent
---

The user wants a page audited.

1. Ask which file/URL to audit if not specified. If they say "the homepage" → `/index.html`.

2. Spawn the **reviewer** agent via Agent tool with `subagent_type: reviewer`. Pass the target file path. The agent will:
   - Walk `/system/checklist.md` against the file
   - Conduct persona walk-throughs (target persona + 1 adjacent)
   - Run an adversarial pass
   - Return a structured punch list with verdict SHIP / FIX BEFORE SHIP / REBUILD

3. Return the reviewer's report verbatim to the user.

4. If verdict is **FIX BEFORE SHIP**:
   - Offer to dispatch **copywriter** for copy issues
   - Offer to dispatch **web-designer** for layout/markup issues
   - Wait for user approval before dispatching

5. If verdict is **REBUILD**:
   - Surface the persona/area mismatch
   - Ask the user whether to re-plan or update the lock

Do not edit the file directly. The reviewer is read-only; the fixers are
separate.
