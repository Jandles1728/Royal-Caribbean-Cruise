# Cruise Fare Watch

A one-page tracker for Royal Caribbean's **Symphony of the Seas, Dec 4, 2027** (8-night Perfect Day CocoCay & Eastern Caribbean from Fort Lauderdale), watching ocean-view balcony fares.

## What it does

- Rates the latest balcony fare against comparable 8-night Symphony sailings (Great / Good / Typical / Above normal)
- Lets you log fares you find, with source, taxes, and perks
- Charts balcony fares over time
- Counts down to the reprice deadline (final payment, about Sep 5, 2027)

Fares come from two places:

- `fares.json` in this repo. A weekly scheduled check adds the latest prices from Royal Caribbean, Expedia, iCruise and other sites here, so everyone who opens the page sees them.
- Fares you log on the page, saved in that browser's local storage.

Each entry in `fares.json` looks like:

```json
{"date": "2026-10-23", "source": "Expedia", "cabin": "Balcony", "price": 1211, "tax": "incl", "perks": "60% off 2nd guest"}
```

`price` is per person in USD. `tax` is `incl`, `excl` or `unknown`.

## Run it

Open `index.html` in a browser, or turn on GitHub Pages (Settings → Pages → deploy from the `main` branch) to get a link.

Benchmark fares were sampled from iCruise, Cruise Web and CruiseTimetables on Oct 23, 2026.
