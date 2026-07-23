# 路牌 · HK Street Names

A mobile-first web app for looking up Hong Kong street names in English and Chinese — built for showing to taxi drivers.

- Search or browse all 4,543 officially named streets across Hong Kong's 18 districts
- Each entry shows the English name, Chinese name, and a plain-letter reading (tone-free) of the Chinese
- A hand-checked Jyutping reading (with tones) and a short history note is included for ~56 well-known streets
- Tap any street to open a large bilingual card designed to be held up and read by a driver

## Data sources

- Street names (English/Chinese, by district): [`hkstreetnames20`](https://github.com/Hong-Kong-Districts-Info/hkdatasets) dataset, derived from Hong Kong's public street name register
- Per-character Cantonese readings: [Unicode Unihan Database](https://www.unicode.org/charts/unihan.html) (`kCantonese` field)

## Running it

This is a single self-contained `index.html` — no build step, no dependencies. Open it directly in a browser, or serve the folder with GitHub Pages.
