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

## status

Right now it's just the scaffold. The plan, in order: basic layout, a Leaflet map centred on Brampton, a starter list of spots added by hand, the labels and filters, then put it live. Full checklist is in ROADMAP.md.

## tech

React + Vite, Leaflet for the map (Esri tiles — same setup I used on davehomes.ca). Maybe the Google Places API later to find new spots, but every listing still gets checked by hand.

## run it

```
npm install
npm run dev
```

---

I'm Prem — realtor in Brampton/Caledon and a CS student. Other stuff: [davehomes.ca](https://davehomes.ca) · [seo-dashboard](https://github.com/premd06/seo-dashboard)
