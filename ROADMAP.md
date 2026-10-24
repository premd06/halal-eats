# Roadmap — Halal Eats

Built in small, daily commits. Each item is sized to land in one focused session, in order. Check items off as they ship.

## Phase 1 — App shell + map
- [ ] Replace the Vite template shell: header "Halal Eats", clean layout (map main view, list sidebar), mobile-friendly
- [ ] Leaflet map component centred on Brampton with Esri street tiles (same approach as davehomes.ca)

## Phase 2 — Seed data + list
- [ ] `src/data/spots.js`: ~20 well-known GTA halal spots (Brampton, Mississauga, Caledon first). Every entry: name, address, lat/lng (geocoded from the real address — verify, never guess), cuisine, trust level (`certified` / `full-menu` / `options`), basis + last-verified date. When certification can't be verified, the basis says so honestly.
- [ ] Results list rendering from the data file, sorted by city
- [ ] Map markers for each spot, popup with name, cuisine, trust label

## Phase 3 — The trust layer (the whole point)
- [ ] Trust label component with plain-English explanations of each level
- [ ] Filters: trust level, cuisine, city, open-now
- [ ] Details panel: address, hours, rating where known, directions link (Google Maps)

## Phase 4 — Grow the data
- [ ] Verification pass: cross-check certified listings against the HMA certified list; update basis/last-verified
- [ ] "Suggest a spot" and "Report an error" (simple form → mailto for v1)
- [ ] Search by city / neighbourhood

## Phase 5 — Ship it
- [ ] Loading/empty states and polish
- [ ] Deploy to Netlify, add the live link + screenshots to the README

## Later ideas
- Google Places API discovery layer: surface candidate spots, human-verify before listing
- Community submissions with moderation
- Prayer-friendly / no-alcohol-served filter
- More cities: Toronto, Scarborough, Vaughan, Markham
