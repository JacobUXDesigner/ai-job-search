# Search Queries for Job Scraper

## Installed portal CLIs (primary for `/scrape`)

`/scrape` discovers every portal skill under `.agents/skills/*/SKILL.md` and runs its CLI first. Installed: `linkedin-search` and `freehire-search` (country-agnostic, primary for this profile), plus the four Danish demo CLIs (`jobbank-search`, `jobdanmark-search`, `jobindex-search`, `jobnet-search`) — **not relevant to this profile's markets (NL/remote/Israel/USA) and can be ignored**; they simply won't return useful results, not worth disabling.

The `site:` query templates below are the **WebSearch fallback** — for Dutch/Israeli/US boards without a CLI, company career pages, or when a CLI fails.

**Language scope:** English is the default query language (CV language is English). Add Dutch-language queries for on-site Netherlands roles specifically — see Priority 1b below — since some Dutch employers post primarily in Dutch even though the CV/cover letter stay English (Dutch is B1+, just below B2; not fluent enough to safely draft in, per the Language Gate in `04-job-evaluation.md`).

## Two tracks — run both

This profile covers two active tracks. Run search categories for both; do not assume one track supersedes the other.

- **Track A: UX/UI Design** (primary — the direction being built toward)
- **Track B: Sign Craft / Visual Production** (active — steady income, real decade-plus experience)

## Search Sites

Primary:
- **linkedin.com/jobs** — covered by `linkedin-search` CLI; filter Netherlands, remote, Israel, USA
- **freehire-search** CLI — tech-focused aggregator, useful for Track A, supports remote/multi-market facets
- **indeed.nl** — largest general Dutch job board (WebSearch fallback, no CLI)
- **nationalevacaturebank.nl** — general Dutch board (WebSearch fallback)

Secondary (company career pages via Google):
- Direct Google searches with `site:` filters for known target companies

## Query Categories

### Priority 1a: UX/UI Design roles (Track A)

**Run the `linkedin-search` CLI with `-l` set to a specific city — `"'s-Hertogenbosch, North Brabant, Netherlands"`, `"Eindhoven, North Brabant, Netherlands"`, `"Nijmegen, Gelderland, Netherlands"` — never a bare `-l "Netherlands"`.** Confirmed 2026-08-06: a country-wide location search floods results with Randstad (Amsterdam/Utrecht) postings by sheer volume, burying genuinely close matches. City-scoped queries still surface some Utrecht/Amsterdam results (the CLI location filter isn't a hard boundary), but they also surface real local ones — treat anything outside the acceptable tier as a location caution, not grounds to skip the search.

```
site:linkedin.com/jobs "UX Designer" OR "UX/UI Designer" OR "Product Designer" Netherlands
site:linkedin.com/jobs "UX Designer" OR "UX/UI Designer" remote
site:indeed.nl "UX Designer" OR "UX/UI Designer" Noord-Brabant OR Eindhoven OR "'s-Hertogenbosch"
site:linkedin.com/jobs "UX Researcher" OR "Product Designer" SaaS OR B2B Netherlands
```

### Priority 1b: UX/UI Design roles, Dutch-language postings

```
site:indeed.nl "UX ontwerper" OR "UX/UI designer" Nederland
site:linkedin.com/jobs "UX designer" 's-Hertogenbosch OR Eindhoven OR Nijmegen
```

### Priority 2: Sign Craft / Visual Production roles (Track B)

```
site:indeed.nl "sign specialist" OR "signage" OR "belettering" OR "visual merchandising" Noord-Brabant
site:linkedin.com/jobs "sign specialist" OR "signage designer" OR "visual merchandiser" Netherlands
site:nationalevacaturebank.nl reclame OR signing OR belettering Uden OR "'s-Hertogenbosch"
```

### Priority 3: Adjacent / AI-adjacent design roles

Roles combining the two tracks' underlying skills, or moving toward the stated AI-adjacent direction — worth surfacing even when not explicitly searched for.

```
site:linkedin.com/jobs "Design Systems" designer Netherlands OR remote
site:linkedin.com/jobs "AI product designer" OR "conversational design" remote
site:linkedin.com/jobs "brand designer" OR "environmental designer" Netherlands
```

### Priority 4: Israel and USA (remote-first, per stated eligibility)

Jacob is eligible to work in Israel and the USA (see `04-job-evaluation.md` Eligibility Gate) but is not actively relocating — these queries target remote roles at companies based in those countries, not on-site relocation. Confirm with Jacob before treating an on-site IL/US posting as in-scope.

```
site:linkedin.com/jobs "UX Designer" remote Israel
site:linkedin.com/jobs "UX Designer" OR "Product Designer" remote USA
```

## Location Filter

- **Ideal:** Uden and surrounding areas (commute)
- **Acceptable:** 's-Hertogenbosch, Eindhoven, Nijmegen (~30-40 min commute)
- **Borderline:** Amsterdam, Utrecht, Rotterdam (longer commute — flag for Jacob's judgment, especially if not remote-flexible)
- **Also in scope regardless of distance:** Remote roles (any location); on-site roles in Israel or the USA only if Jacob confirms relocation interest for that specific posting
- **Sign Craft track specifically, set by Jacob 2026-08-10 after a real drive-time miss (Mierlo estimated ~35-40 min, actually 45 min):** cap on-site roles at **~30-35 min drive from Uden**. Drive-time distances are not verified against a routing source in this workflow — state any distance as an estimate, never as checked, and tell Jacob to confirm the actual drive time himself before he invests time in a posting.

## Language Filter

Working languages and levels are in `01-candidate-profile.md`'s Languages table (English C2, Hebrew C2, Dutch B1+/just-below-B2). Apply `04-job-evaluation.md`'s Language Gate: a posting requiring a language not on this table is excluded; a posting requiring a higher level than declared in a language Jacob does work in is flagged, not excluded. A Dutch-language posting for a role that doesn't itself require fluent Dutch on the job is fine.

## Date Filter

Only include jobs posted within the last 14 days, or with an application deadline that has not yet passed. If a posting date cannot be determined, include it but flag as "date unknown".

## Adapting Queries

If Jacob specifies a focus area or a single track for a given `/scrape` run, select queries from the matching category and also generate 2-3 custom queries for that focus. For example: "/scrape sign craft only" → Priority 2 queries + custom focus-specific queries.
