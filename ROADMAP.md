# stuff I'm building, in order

I try to do one of these per session so the commits stay small and I actually understand everything in here.

## layout + map
- [ ] get rid of the default Vite page, put in a simple header + layout
- [ ] Leaflet map working, centred on Brampton (Esri tiles)

## the list of spots
- [ ] data file with ~20 spots around Brampton, Mississauga, Caledon — name, address, coordinates taken from the actual address (no guessing pins), cuisine, label, what the label is based on, date I checked it
- [ ] show the list on the page next to the map
- [ ] markers on the map — click one and the name + label pops up

## labels + filters
- [ ] label component, with a short explanation of what each label means
- [ ] filters: label, cuisine, city

## data cleanup
- [ ] re-check the certified ones against the HMA list
- [ ] "suggest a spot" / "this listing is wrong" link (just a mailto for now)
- [ ] search by city

## ship it
- [ ] fix the rough edges — empty states, mobile layout
- [ ] deploy to Netlify, add screenshots to the readme

## ideas for later
- filter for places that don't serve alcohol
- let restaurant owners claim their listing
- more cities: Toronto, Scarborough, Vaughan, Markham
- Places API to find new spots (still verified by hand before they go on the list)
