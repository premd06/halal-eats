# stuff I'm building, in order

I try to do one of these per session so the commits stay small and I actually understand everything in here.

## how I want it to look

green + warm off-white, basically. green because every halal sign you've ever seen is green. deep green (#177245) for the header/buttons, warm off-white background (#FAF6EF), dark text, and a bit of gold (#C19A2E) only on the "certified" badge so it stands out. clean cards, lots of space, has to look good on a phone first — that's where people will actually use it.

the labels: certified = filled green badge, full menu halal = green outline, halal options = grey/amber outline. colour tells you the level before you even read it.

## layout + map
- [ ] get rid of the default Vite page, put in a simple header + layout (started — header's in, layout still needs work)
- [ ] Leaflet map working, centred on Brampton (Esri tiles)
- [ ] make the map interactive properly — click a spot in the list and the map flies to it, click a marker and its card highlights

## backend
- [ ] express server in a `server/` folder, with a /api/health route so I know it's running
- [ ] sqlite database for the spots, plus a seed script that loads the starter list into it
- [ ] GET /api/spots route — sends spots to the frontend, handles the filters (city, cuisine, label) back here

## the spots themselves
- [ ] the starter list, ~20 spots across the GTA — Brampton, Mississauga, Caledon first, then wherever else I can verify. name, address, coordinates taken from the actual address (no guessing pins), cuisine, label, what the label is based on, date I checked it. this goes in through the seed script

## frontend using the api
- [ ] list of spots next to the map, loaded from the api (not hardcoded)
- [ ] markers on the map — click one and the name + label pops up
- [ ] label component, with a short explanation of what each label means
- [ ] filter controls that ask the api (label, cuisine, city)

## little things (the stuff that makes it feel finished)
- [ ] "open now" green dot on spots that are open, from their hours
- [ ] directions button on each spot (opens google maps)
- [ ] "last checked" date shown small on each spot — the trust thing only works if people can see it
- [ ] distance on each card, from the centre of the map
- [ ] a proper empty state when a filter finds nothing ("nothing here yet — know a spot?" instead of a blank page)
- [ ] footer with a "suggest a spot" mailto link
- [ ] favicon + the green theme colour in the browser bar (theme colour is already in)

## data cleanup
- [ ] re-check the certified ones against the HMA list
- [ ] search by city

## ship it
- [ ] fix the rough edges — loading state while the api answers, mobile layout pass
- [ ] deploy (frontend on Netlify, backend somewhere free), add screenshots to the readme

## ideas for later
- filter for places that don't serve alcohol
- let restaurant owners claim their listing
- more cities: Toronto, Scarborough, Vaughan, Markham (need spots I can actually verify)
- Places API to find new spots (still verified by hand before they go on the list)
