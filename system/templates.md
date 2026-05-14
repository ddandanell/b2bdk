# Templates Lock

Copy-paste templates per content type. Fill the `{slots}` with locks from
`keywords.md` and `personas.md`. Don't write from scratch.

---

## Meta title (≤60 chars)

**Pattern A — Crisis area (A1–A8):**
```
{Crisis} in Bali? {Outcome} in {Time}
```
Examples:
- `Scooter Accident in Bali? Help On Scene in 60 Minutes`
- `Locked Out of Your Villa in Bali? Locksmith in 45 Min`

**Pattern B — Brand / membership:**
```
{Brand or Service} — {Promise}
```
Examples:
- `Bali Fixer — Same-Day Emergency Help for Expats (24/7)`
- `Bali Expat Membership — Your Insurance That Shows Up`

---

## Meta description (≤155 chars)

**Formula:**
```
{Crisis hook}? {What we do in 3 nouns}. {Time}. From ${price}.
```

Example:
> Crashed in Bali? Bali Fixer dispatches a Bahasa speaker, handles hospital,
> police, insurance. On scene in 60 min. From $220.

Must contain: primary keyword · one secondary keyword · time signal · price signal.

---

## H1 patterns

| Persona target | Pattern |
| --- | --- |
| P1, P2 (crisis) | `{Problem statement}? We {fix verb} {time}.` |
| P3 (business) | `{Problem statement}? {Discretion or compliance word}, today.` |
| P4, P5 (pre-emptive) | `{Outcome statement}.` |

---

## Hero subhead (lede) pattern

```
{Comma-separated list of 4–5 fix scenarios in this area} — one call to Bali
Fixer {action verb} {who} to {outcome} in {time}.
```

Example:
> Scooter crash, visa overstay, landlord dispute, locked-out villa, KITAS
> panic — one call to Bali Fixer dispatches a real human to your problem in
> under an hour.

---

## 3-CTA pattern (every landing page)

Three buttons, in this order, on hero AND in sticky dock on mobile:

1. **Red (primary)** — `📞 Call the hotline now` → `tel:+62…`
2. **Dark (secondary)** — `💬 WhatsApp dispatch` → `https://wa.me/62…?text={prefilled}`
3. **Ghost (tertiary)** — `{See membership plans | Send me the brief | Get a quote}` → modal or `/membership`

**WhatsApp prefill template:**
```
Hi Bali Fixer, I need help with {area-name}. I'm in {area-modifier}.
```

---

## Trust line (under hero)

Three items, dot-separated, with green dots:
```
● {Quantitative proof}   ● {Quality proof}   ● {Authority proof}
```
Example:
> ● 1,400+ cases sorted   ● 4.9★ Google   ● Bali-licensed legal partners

---

## Standard 7-question FAQ

Every page uses these same 7 questions in this order. Answers swap by area:

1. Are you actually licensed?
2. How fast is "same day"?
3. Do I have to be a member to call?
4. What if I'm in trouble with police right now?
5. Can you actually {area-specific worst-case outcome}?
6. What's the difference vs. {area-specific alternative}?
7. How do I cancel my membership?

---

## Pricing display

Always show:
- Tier name (uppercase, emerald)
- Headline price in USD with `/month` or `from $X`
- 3–5 bullet benefits (checkmark green dot)
- "Billed in IDR at market rate. Cancel anytime."

Per-incident table always **under** the membership tiers, never above.

---

## Per-area landing page skeleton

```
1.  Top alert ribbon (24/7 line, pulsing red dot)
2.  Sticky nav (logo + Call button)
3.  Hero — H1 + lede + 3-CTA + trust line
4.  Crisis picker OR scenario card (hub page vs. area page)
5.  What we fix (single column mobile, two columns desktop)
6.  How it works — 3 numbered steps
7.  Comparison table — "vs the Bali default"
8.  Stats strip — 4 stats (response, cases, same-day %, rating)
9.  Pricing block — 3 tiers + per-incident table
10. Testimonials — 3, one per persona where possible
11. FAQ — the standard 7
12. Final CTA — dark emerald box, one CTA
13. Footer — legal entity, address, links
```

---

## Blog post skeleton (SEO + persona P4/P5)

```markdown
# {Question that persona literally types}
*By Bali Fixer · Updated {date} · {read time}*

## What happens if you {scenario}? (in plain language)
{60 words, no jargon}

## The actual procedure step-by-step
1. {…}
2. {…}
3. {…}

## What it costs (real numbers)
{Real numbers, IDR + USD}

## The 3 mistakes foreigners always make
1. {…}
2. {…}
3. {…}

## How Bali Fixer handles it (and why it's faster)
{50 words → link to /fix/{area}}

## FAQ (the standard 7, filtered to area)

## Don't wait until it happens
{Final CTA → /fix/{area} or /membership}
```

Every blog post ends with **one** internal link to its area page and **one**
link to membership. No "related posts" graveyard.

---

## Google Search ad

**Headlines** (≤30 chars each):
- `{Crisis} in Bali?`
- `Same-Day Fix · 24/7`
- `Bali Fixer — Real Human`

**Description** (≤90 chars):
> {Crisis} sorted today. Bahasa + English. On scene in 60 min. From ${price}. Call now.

---

## Meta / Instagram ad

**Hook** (first 3 words must shock):
- `Crashed in Bali?`
- `Visa expired today?`
- `Landlord scammed you?`

**Body** (≤90 words):
> Last Tuesday, Lukas wrecked his scooter in Pererenan at 11pm. He didn't
> speak Indonesian. He called us. 38 minutes later, our fixer was at the
> hospital with him. Bali Fixer is the 24/7 service that physically shows
> up. From ${price}. 1,400 cases sorted.

**CTA button:** `Get help now` → WhatsApp deep link.

---

## WhatsApp first-response auto-reply

```
Hi {name}, this is Bali Fixer — we received your message. A fixer is calling
you in <5 minutes. While you wait:

✓ Don't sign anything
✓ Don't pay anyone
✓ Don't leave the scene
✓ Send your live location if safe

You're not alone in this.
```

---

## Email signature (every team email)

```
{Name} — Bali Fixer
24/7 hotline: +62 810 0000 0000
WhatsApp: wa.me/6281000000000
Your Bali insurance policy that actually shows up.
```

---

## OG / social share card

- OG image: 1200×630, brand emerald background, BALI FIXER wordmark + red
  dot top-left, headline mirrors meta title, no stock photos
- Twitter card: `summary_large_image`
- Always set `og:title`, `og:description`, `og:url`, `og:image`
