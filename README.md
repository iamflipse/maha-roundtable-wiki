# MAHA Roundtable Wiki — American Health & Nutrition: A Second Opinion

A curated wiki distilling the MAHA roundtable hosted by **Sen. Ron Johnson** with **Robert F. Kennedy Jr.** and a panel of doctors, nutritionists, and food advocates (Dr. Casey Means, Dr. Jordan Peterson, Dr. Chris Palmer, Michaela Fuller, Courtney Swan, etc.).

**Public copy:** https://iamflipse.github.io/maha-roundtable-wiki/ (read-only; static build served from the `gh-pages` branch)

## Contents

- **9 concept pages**: US health-care crisis, ultra-processed foods, metabolic dysfunction, ketogenic/Lion diet, toxic chemicals & glyphosate, regulatory capture, mental health as metabolic, children's health & fertility, food as medicine.
- **Source of truth:** full timestamped transcript at `src/sources/maha-roundtable-transcript.md` (fetched from `http://100.65.70.20:8088/maha-roundtable/source/maha_roundtable_transcript.html`).

## Layout

- `src/` — markdown source pages
- `book/` — mdbook-generated static site (committed for GitHub Pages)
- `tools/mdbook` — mdbook v0.4.21 binary (aarch64 Linux, built from source)

## Rebuild + republish

```sh
./tools/mdbook build -d book
git add -A && git commit -m "update" && git push origin main
# republish: recreate orphan gh-pages branch with book files at root + tools/mdbook, force push
```
