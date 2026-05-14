# Connect — How New Builds Plug In

Every new piece of content connects to the existing site via four mechanisms:
**URL structure**, **internal linking**, **ad campaign mapping**, **tracking**.
Don't invent a fifth.

---

## 1. URL structure

```
/                          → homepage (A0)
/fix/scooter-accident      → A1
/fix/visa-overstay         → A2
/fix/villa-lockout         → A3
/fix/landlord-dispute      → A4
/fix/kitas-business        → A5
/fix/theft-fraud           → A6
/fix/police-stop           → A7
/fix/hospital-medical      → A8
/membership                → A9
/blog/{slug}               → SEO content
/cases/{slug}              → real case studies
/about                     → trust + team
/contact                   → fallback
```

**Rules:**
- Lowercase, hyphen-separated, no trailing slash.
- `/fix/{area}` is reserved — only one URL per A1–A8.
- New area? Add it to `keywords.md` first, then claim its `/fix/{slug}` URL.

---

## 2. Internal linking map

Every page MUST link out as follows:

| Page type | Required outbound links |
| --- | --- |
| Homepage (A0) | Top 3 fix pages + `/membership` |
| Fix page (A1–A8) | `/membership` + 2 sibling fix pages (matrix below) + 1 case study from same area |
| Membership (A9) | All 8 fix pages (covered grid) + 1 case per persona |
| Blog post | 1 fix page (its area) + `/membership` + 1 sibling blog post |
| Case study | The corresponding fix page + `/membership` |

### Sibling matrix (which fix pages link to which)

| From | Link to (2 siblings) |
| --- | --- |
| A1 Scooter | A7 Police · A8 Hospital |
| A2 Visa | A5 KITAS · A7 Police |
| A3 Lockout | A6 Theft · A0 Brand |
| A4 Landlord | A6 Theft · A2 Visa |
| A5 KITAS | A2 Visa · A6 Theft |
| A6 Theft | A5 KITAS · A4 Landlord |
| A7 Police | A1 Scooter · A8 Hospital |
| A8 Hospital | A1 Scooter · A2 Visa |

---

## 3. Ad campaign mapping

One campaign owns one area-cluster. **Never** run a single campaign across
two areas — it dilutes the keyword lock and ruins quality scores.

| Ad campaign | Owned area | Landing page | Persona |
| --- | --- | --- | --- |
| "Scooter Help" | A1 | /fix/scooter-accident | P1 |
| "Visa Same-Day" | A2 | /fix/visa-overstay | P1 or P4 |
| "Villa Locksmith" | A3 | /fix/villa-lockout | P1 or P5 |
| "Deposit Mediator" | A4 | /fix/landlord-dispute | P2 |
| "KITAS Help" | A5 | /fix/kitas-business | P4 or P3 |
| "Quiet Investigator" | A6 | /fix/theft-fraud | P3 |
| "Police Translator" | A7 | /fix/police-stop | P1 |
| "Hospital Liaison" | A8 | /fix/hospital-medical | P1 or P5 |
| "Membership" | A9 | /membership | P4 or P5 |

Each campaign uses ONLY the keywords from its locked area. No keyword
borrowing across campaigns.

---

## 4. Tracking & lock

- One GA4 event per area: `area:A{n}_lead`.
- Phone-call source attribution via dynamic number per area (placeholder
  until real numbers issued).
- WhatsApp inbound: `?text=` prefill includes the area name so the
  dispatcher knows what's coming before the conversation starts.
- Every form submit POSTs to `/api/lead` with a `source_area` field
  (placeholder endpoint).
- UTM convention: `utm_source={channel}&utm_medium={paid|organic|email}&utm_campaign={areacode}-{persona}`.
  Example: `utm_campaign=A1-P1` = scooter-area ad targeting Lukas.

---

## 5. Adding a new build (any content type)

1. Open `README.md`. Walk the 5-step loop.
2. Confirm the URL slot is free (per section 1 above).
3. Confirm the internal link map (section 2) — what links in, what links out.
4. Confirm an ad campaign (section 3) — or note "no paid traffic for this page".
5. Run `checklist.md` end-to-end.
6. Ship. Add the new page to the live site map in section 6 below.

---

## 6. Live site map

| URL | Area | Status |
| --- | --- | --- |
| `/` (`/index.html`) | A0 | ✅ built |
| `/fix/scooter-accident` | A1 | ⏳ TODO |
| `/fix/visa-overstay` | A2 | ⏳ TODO |
| `/fix/villa-lockout` | A3 | ⏳ TODO |
| `/fix/landlord-dispute` | A4 | ⏳ TODO |
| `/fix/kitas-business` | A5 | ⏳ TODO |
| `/fix/theft-fraud` | A6 | ⏳ TODO |
| `/fix/police-stop` | A7 | ⏳ TODO |
| `/fix/hospital-medical` | A8 | ⏳ TODO |
| `/membership` | A9 | ⏳ TODO (currently a modal on homepage) |
| `/blog/*` | — | none yet |
| `/cases/*` | — | none yet |

Update this table every time a page ships.
