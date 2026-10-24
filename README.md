# Halal Eats

A small app I'm building to find halal restaurants in the GTA — and actually tell you how halal a place is, not just that the word "halal" showed up in a review somewhere.

Still early. I'm building it in small pieces and pushing as I go.

## why

If you search "halal" on Google Maps you get any place where a reviewer mentioned the word once. Sometimes the review literally says "not halal" and the place still shows up. What I actually want to know before picking a spot:

- is the whole menu halal, or just a couple of dishes?
- is it certified by somebody (like HMA), or does the restaurant just say it is?
- when was that last checked?

No app really shows that, so I'm making one.

## how it works

Every spot gets a label:

- **certified** — checked against a certifier's list
- **full menu halal** — the restaurant says its whole menu is halal
- **halal options** — only some dishes are halal

Each listing also says what the label is based on and when it was last verified. If I can't verify something, the listing says that instead of guessing. I'd rather have fewer spots that are right than a big list that's half wrong.

The app itself is a frontend + backend: the spots live in a database on the backend, and the frontend asks the backend for them through an API. Filtering (by city, cuisine, label) happens on the backend too.

## status

Right now it's just the scaffold. The plan, in order: basic layout, a Leaflet map centred on Brampton, the backend with the spots database, the frontend showing spots from the API, then labels and filters, then put it live. Full checklist is in ROADMAP.md.

## tech

React + Vite for the frontend, Leaflet for the map (Esri tiles — same setup I used on davehomes.ca). Backend is Node + Express with SQLite holding the spots. Same stack as my seo dashboard, on purpose — I'd rather know one stack properly. Maybe the Google Places API later to find new spots, but every listing still gets checked by hand.

## run it

frontend:

```
npm install
npm run dev
```

backend (once it exists):

```
cd server
npm install
npm start
```

---

I'm Prem — realtor in Brampton/Caledon and a CS student. Other stuff: [davehomes.ca](https://davehomes.ca) · [seo-dashboard](https://github.com/premd06/seo-dashboard)
