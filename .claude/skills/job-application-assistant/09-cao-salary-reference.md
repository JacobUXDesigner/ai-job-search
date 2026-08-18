---
framework_version: 1.0.0
---

# CAO Salary Reference (Sign Craft track)

## Why this file exists, and why `salary_lookup.py` doesn't apply here

`salary_lookup.py` / `salary_data.json` (see `04-job-evaluation.md` Step 6) were built for a
Danish-style model: real per-company salary index data from union surveys. The Netherlands
doesn't have an equivalent — what exists is the **CAO** (Collectieve Arbeidsovereenkomst), a
sector-wide **legal minimum wage floor**, not a per-employer index. There is no honest
"company X's salary index" number to look up here; a specific employer may pay above the
CAO floor, but that figure isn't published anywhere. Forcing CAO data into the per-company
tool would mean presenting an invented number as if it were verified — do not do that. This
file is the Sign Craft track's actual salary reference instead.

## Source

**CAO voor Signbedrijven ("Sign-cao")** — CAO-nummer 2165, agreed by VSBN (werkgevers) and
LBV (werknemers), covering **1 maart 2026 – 31 december 2027**. Registered with the
Ministerie van Sociale Zaken en Werkgelegenheid.

- Archived locally: `documents/references/CAO-Signbedrijven-2026-2027.pdf` (fetched
  2026-08-14, so a broken source URL later doesn't lose it).
- Source URL: https://m.vsbn.nl/content/7821/download/clnt/112694_CAO_boekje_2026_-_2027_-_Webversie.pdf

## Function groups (functiegroepen) — safe to trust, verified 2026-08-14

Classification is based on aard van het werk, vereiste kennis/vaardigheid/ervaring, and mate
van zelfstandigheid (Artikel 15, decision tree in Bijlage 3). Example titles for the
"Signing, DTP en Ontwerp" discipline (Bijlage 4 + 5):

| FG | Level | Work-and-think level | Example titles |
|---|---|---|---|
| 1 | Junior medewerker — repetitive work, direct supervision | Geen of geringe beroepsopleiding | Junior signmaker, junior creatief productiemedewerker |
| 2 | Vakman — repetitive work, some variation, limited supervision | VMBO basis | **Signmaker**, beletteraar, junior DTP-er |
| 3 | Zelfstandig vakman — standard/varied work, partly independent | VMBO | Senior signmaker/creatief productiemedewerker, DTP-er |
| 4 | Volleerd vakman — independent, own initiative in planning | MBO/HAVO | **Specialist signmaker**, senior DTP-er, ontwerper |
| 5 | Teamleider/vakspecialist — coordinating, may require leadership | MBO/HAVO | Senior ontwerper, hoofd (fullcolour) productie |
| 6 | Afdelingshoofd/specialist — organisational | MBO4/HAVO + gespecialiseerde vervolgopleiding | Hoofd afdeling decoratie en belettering |
| 7 | Manager/specialist — organising and controlling | HAVO+vervolgopleiding / HBO | Hoofd afdeling DTP en ontwerp |
| 8 | Management — initiating within a specialism | HBO | (no Signing-specific title listed; general management) |
| 9 | Directie/management — organisation-wide | HBO/Academisch | (no Signing-specific title listed) |

**Job-title detail (Bijlage 5 profiles), verified:**
- **Junior signmaker**: onder direct toezicht, aanbrengen/verwerken van zelfklevende folie op verschillende ondergronden; samenstellen/assembleren van signgerelateerde producten. Geen of geringe beroepsopleiding.
- **Signmaker**: hetzelfde werk maar onder *beperkt* toezicht; daarnaast instellen/onderhouden van machines en gereedschappen, en het **instrueren en begeleiden van junior medewerkers, stagiairs en afstudeerders**. VMBO basis. — *This is the FG2 "Signmaker" profile. Note it already includes junior-mentoring as a stated task at FG2, not just FG3+ — worth knowing before assuming "Senior" is required to mentor at all.*
- **Beletteraar**: belettering van reclameborden, lichtbakken, reclamezuilen en voertuigen; aanbrengen van (complexere) belettering op vlakke ondergronden én op 3D-vormen; aansturen van snijplotters/snijmachines. VMBO basis (FG2).

## Wage table — do NOT hand-copy numbers from memory

The monthly and hourly wage tables (Bijlage 2, per functiegroep-schaal 11–46 × trede 1–9)
are real and complete in the source PDF, but **the crosswalk from functiegroep (1–9, used for
job classification) to the specific schaal-row (11–46, used for pay) is not stated in plain
text anywhere in this booklet** — it likely depends on a separate ORBA
functiewaarderingshandboek that isn't published here. Two attempts to transcribe the grid by
reading the page produced inconsistent results between attempts, so **no numbers are copied
into this file** — a wrong number here is worse than no number.

**When an exact monthly/hourly figure is actually needed:**
1. Read `documents/references/CAO-Signbedrijven-2026-2027.pdf`, pages 15 (hourly, per 1 April
   2026) or 16 (monthly, per 1 April 2026) fresh, at that moment — never from a cached
   transcription.
2. Cross-check the read against the row/column header before quoting it to Jacob.
3. **Better than guessing the crosswalk: ask the employer directly which schaal the role is
   classified at.** This is standard, expected practice in a Dutch salary conversation, not
   an admission of not knowing something you should — "in welke schaal is deze functie
   ingedeeld, en wat is het bijbehorende maandloon?" is a normal, professional question.

## Other CAOs relevant to this track

**Grafimedia-cao** (print/DTP-adjacent roles, e.g. PromoXL-style DTP work) is going through a
2026-2027 renegotiation with a new ORBA-based function classification handbook — not yet
pulled into this file. Fetch and verify before citing, same standard as above, if a posting
in that CAO comes up.
