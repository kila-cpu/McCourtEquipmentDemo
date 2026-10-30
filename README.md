# McCourt Equipment — Sales Quoting App wireframes

Interactive wireframe of the **McCourt Equipment sales app**, mobile first,
prepared by DMC Consultancy Ltd. One self-contained page, no build, no
dependencies, no backend — everything runs in the browser tab.

Built from the Vincent's quoting wireframes and re-cut for McCourt: US dollars
and **sales tax** instead of VAT, **sale and rental** quotes, **freight**, and
the crushing / screening / washing / organics range off mccourtequipment.com.

## Running it

```bash
python3 -m http.server 8812 --directory public
```

Then open http://localhost:8812. With Node installed, `npm start` does the same
through `server.js` (that is what Railway runs).

On a desktop the phone sits in a frame with a **screen map** on the left and
**notes for the current screen** on the right. On a phone it fills the screen.

## What's in it

Screen layout follows the client's existing sales app wireframes; colours are
the McCourt green and yellow.

- **Home** — greeting and weather, six tiles: Quotes, Stock, Sales Leads, Site
  Visits, Parts & Services, Requested Equipment. Tab bar: Home, **+**, Account.
- **+ Create New** — Quote, Sales Order, Sales Lead, Site Visit.
- **Quotes** — search; each card shows customer, model • total • rep, status and
  number, with View / Edit / Send (drafts) / Convert. Quote view and a **PDF**
  on McCourt letterhead.
- **New / edit quote** — Sale or Rental. Customer from the list, or **+ Customer**
  adds one without losing the quote; company optional. Items: **Select product**
  from the McCourt range (fills brand, spec, price), **Enter Custom Product**, or
  pick a serial-numbered machine from stock. Optional **Custom items / parts**
  and **Trade-in** sections. Quote validity date, freight, sales tax (8.25% or
  exempt). **Save Quote** or **→ Order**.
- **Sales orders** — raised from a quote; Draft → Sent to office → Completed.
- **Stock** — search, brand and New / Used / Rental fleet filters; months in
  stock with amber/red edge; Quote and Allocate.
- **Sales leads / Show leads** — search and status filter; View / Edit / Quote.
  Lead form: customer from list or Enter Custom Customer, machine from list or
  Enter Custom Product, status, 1–4 priority, follow-up. Show leads pick the show.
- **Customers** — list and Add Customer (name, phone, email, company, address,
  ZIP, sales tax exemption certificate in place of a VAT number).
- **Requested Equipment** — what customers have asked for; Match stock, Quote.
- **Site visits** — three-field log; the revisit date becomes the lead's follow-up.
- **Parts & Services** — parts or service request, "machine down" flag.
- **My Account** — counts for draft/sent quotes, draft/sent/completed orders,
  sales leads, show leads, site visits, customers, each with a quick Add. Switch
  rep and reset the demo here too.

## Where the content came from

- **Equipment, brands, yards, phone numbers, terms** — mccourtequipment.com
  (new/used listings, rentals page, contact page). Used prices that the site
  lists (ST100TLA $118k, S130 $128k, LS622 $297k) are used as-is; the rest of
  the prices and rental rates are **illustrative**.
- **Sales reps** are names from their contact page. **Customers, contacts and
  phone numbers are invented.**
- Serial numbers are placeholders.

## Known limits

- Nothing is saved; data reseeds on reload, dates shift to today.
- Tax is a single rate field, not a by-county lookup.
- The logo is the white version supplied, so it only sits on the dark green.
