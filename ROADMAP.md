# stuff I'm building, in order

I try to do one of these per session so the commits stay small and I actually understand everything in here.

## layout + map
- [ ] get rid of the default Vite page, put in a simple header + layout (started — header's in, layout still needs work)
- [ ] Leaflet map working, centred on Brampton (Esri tiles)

## backend
- [ ] express server in a `server/` folder, with a /api/health route so I know it's running
- [ ] sqlite database for the spots, plus a seed script that loads the starter list into it
- [ ] GET /api/spots route — sends spots to the frontend, handles the filters (city, cuisine, label) back here

## the spots themselves
- [ ] the starter list, ~20 spots around Brampton, Mississauga, Caledon — name, address, coordinates taken from the actual address (no guessing pins), cuisine, label, what the label is based on, date I checked it. this goes in through the seed script

## frontend using the api
- [ ] list of spots next to the map, loaded from the api (not hardcoded)
- [ ] markers on the map — click one and the name + label pops up
- [ ] label component, with a short explanation of what each label means
- [ ] filter controls that ask the api (label, cuisine, city)

## data cleanup
- [ ] re-check the certified ones against the HMA list
- [ ] "suggest a spot" / "this listing is wrong" link (just a mailto for now)
- [ ] search by city

## ship it
- [ ] fix the rough edges — empty states, mobile layout
- [ ] deploy (frontend on Netlify, backend somewhere free), add screenshots to the readme

## ideas for later
- filter for places that don't serve alcohol
- let restaurant owners claim their listing
- more cities: Toronto, Scarborough, Vaughan, Markham
- Places API to find new spots (still verified by hand before they go on the list)
