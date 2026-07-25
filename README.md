# 路牌 · HK Street Names

A mobile-first web app for looking up Hong Kong streets, transit stops, attractions, and hotels in English and Chinese — built for showing to taxi drivers.

- **Streets** — all 4,543 officially named streets across Hong Kong's 18 districts, most with a neighbourhood name (e.g. Mid-Levels, Causeway Bay) assigned by nearest-match against OpenStreetMap place data. Streets that genuinely cross more than one named area (e.g. Nathan Road spanning Tsim Sha Tsui, Yau Ma Tei, and Mong Kok) show as separate rows, one per area
- **Transport** — 172 MTR stations, Light Rail stops, and major ferry piers
- **Sightseeing** — 11 major tourist attractions
- **Hotels** — 1,815 licensed hotels and guesthouses
- Every street shows a tone-marked Jyutping reading, built character-by-character from Unicode's public Cantonese pronunciation data; Transport/Sightseeing/Hotels show the same reading with the tone dropped. ~55 well-known streets additionally get a short history note, matched by name *and* Chinese characters together so streets that share an English name (e.g. two unrelated "Tai Yuen Street"s) never inherit the wrong note
- One unified Search tab covers all four categories at once, with category chips (All/Streets/Transport/Sights/Hotels) and a second tier of filter chips: region → district for Streets (HK Island/Kowloon/New Territories, each expanding to its own districts), or MTR/Light Rail/Ferry for Transport
- Search results across categories are tagged with colour-coded badges (Street/MTR/Light Rail/Ferry/Sight/Hotel) so it's clear what kind of place each one is
- Tap any result to open a Detail view with the reading, history, and address, plus actions: save as favorite, open in Maps, share, and (for streets) add a specific street number
- From Detail, "Show taxi card" opens a separate, full-screen dark view — just the giant bilingual sign, meant to be held up and read by a driver
- Favourites is its own bottom-nav tab, saved locally (no account, no server)
- Installable as a PWA (manifest + service worker); "Add to Home Screen" gives a full-screen app-like experience on Android and iOS

## Data sources

- Street names (English/Chinese, by district): [`hkstreetnames20`](https://github.com/Hong-Kong-Districts-Info/hkdatasets) dataset, derived from Hong Kong's public street name register
- Neighbourhood names: © [OpenStreetMap](https://www.openstreetmap.org/copyright) contributors, available under the [Open Database Licence (ODbL)](https://opendatacommons.org/licenses/odbl/)
- Per-character Cantonese readings: [Unicode Unihan Database](https://www.unicode.org/charts/unihan.html) (`kCantonese` field)
- Transport: [MTR Open Data](https://opendata.mtr.com.hk/) (stations, Light Rail); ferry piers are a small hand-compiled list of well-known termini
- Attractions: Culture, Sports and Tourism Bureau, via [data.gov.hk](https://data.gov.hk/en-data/dataset/hk-cstb-cstb_tc-tc-hk-major-attractions-general-info)
- Hotels: Home Affairs Department, [licensed hotels & guesthouses register](https://data.gov.hk/en-data/dataset/hk-had-json1-licensed-hotels-and-guesthouses)

## Running it

This is a single self-contained `index.html` — no build step, no dependencies. Open it directly in a browser, or serve the folder with GitHub Pages.
