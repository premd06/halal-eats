# Halal Eats

Find halal restaurants, cafés, and bakeries in the GTA — with the one thing Google Maps won't tell you: **how halal each place actually is.**

**Status:** in active development (started Oct 2026). Built in public, one small commit at a time — see [ROADMAP.md](ROADMAP.md).

## The problem

Search "halal" on Google Maps and you get whatever reviewers happened to mention in passing. A place can show up because one review says "not halal," another because the owner once replied "yes halal." There's no reliable way to tell:

- Is the **whole menu** halal, or just a few options?
- Is it **certified** (e.g. HMA — Halal Monitoring Authority), or self-declared by the restaurant?
- Is alcohol served on the premises?

For people who eat halal in the GTA — one of the largest Muslim populations in North America — this is a daily, practical problem with no good tool.

## What this does

- **Map + list** of halal spots across the GTA, starting with Brampton, Caledon, and Mississauga
- Every listing carries a **trust label**:
  - **Certified** — verified against a certifier's listing (e.g. HMA)
  - **Fully halal menu** — the restaurant states its full menu is halal
  - **Halal options** — some dishes are halal; the rest of the menu isn't
  - Each label shows **what it's based on** and a **last-verified date** — no claim without a source
- Filters: cuisine, trust level, city, open now
- Details per spot: address, hours, rating, and a directions link

## Data honesty

Halal status is a claim people make religious decisions on, so this project treats it like data, not decoration: every listing stores its basis (`certified`, `restaurant-stated`, `community-reported`) and when it was last checked. Listings never claim a certification that hasn't been verified against the certifier.

## Tech

React · Vite · Leaflet (Esri tiles) · Google Places API for discovery (verification data curated in-repo)

## Run it locally

```bash
npm install
npm run dev
```

---

Built by [Prem Dave](https://github.com/premd06) — also: [davehomes.ca](https://davehomes.ca) · [SEO & Performance Analytics Dashboard](https://github.com/premd06/seo-dashboard)
