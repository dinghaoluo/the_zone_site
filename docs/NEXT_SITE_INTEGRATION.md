# Next Site Integration Roadmap

This document records the current integration state after the April 2026
restart. It replaces the earlier `/network` handoff prompt, which described a
future static-figure pass that has already been completed and surpassed.

Do not treat the old `/network` static-figure instructions as active. The
current benchmark is the interactive `/network` route in `src/pages/network.astro`.

---

## Current Route Status

### `/network` - completed benchmark

Status: integrated as interactive D3 editorial plates.

- Uses `NetworkAtlas.astro` for the primary co-presence atlas.
- Uses `NetworkArchitecture.astro` for community, centrality, and dyad views.
- Fetches public-safe 2D data from `public/data/step_2d/`.
- Keeps the original F05/F06 SVG/PNG/PDF files as downloadable reference assets.
- Sets the visual standard for future routes: web-native plates, wide figure
  breakout, dark editorial field, restrained labels, and short prose bridges.

Do not rework `/network` as a static SVG embed. Future changes should be small
refinements or follow-on visual components that preserve the current plate
language.

### `/episodes` - first pass implemented

Status: first-pass implemented using the public-safe episode metadata export.

Current public-safe input:

- `05_publication/public_safe/data/episode_metadata_public.csv`
  to `public/data/base/episode_metadata_public.csv`

Current implementation:

- `EpisodeSequencePlate.astro` shows all seventy-three episodes as a horizontal
  reading score with length and density views.
- `EpisodePartStructure.astro` summarises the four parts with aligned
  statistical rows.
- No 2B figures were copied in the first pass.

Optional approved 2B figure assets remain available for a later, route-specific
copy/provenance pass only if the page needs them:

  - `F10_cast_weather_system.{svg,png,pdf}`
  - `F11_arrival_cascade.{svg,png,pdf}`

Before any future copy, verify against both:

- `docs/PUBLIC_ASSET_MANIFEST.md`
- `L:/projects/the_zone/05_publication/site_handoff/allowed_asset_manifest.md`

Then inspect CSV headers for forbidden fields and append provenance entries in
`data/provenance.md`.

Any later `/episodes` refinement should preserve the web-native plate structure
and avoid turning the route into a cast dashboard.

Next refinements for `/episodes`:

- visual review across desktop and mobile
- density-mode polish if the paragraph-density view needs further tuning
- optional 2B F10/F11 companion pass only after explicit approval

### `/dissolution` - later route

Status: scaffolded. This is the next likely major route after `/episodes`
stabilises.

Likely public-safe inputs are the base 2E data exports and the approved 2E
flagship figures listed in `docs/PUBLIC_ASSET_MANIFEST.md`:

- `slothrop_dissolution_public.csv`
- `slothrop_alias_by_episode_public.csv`
- `slothrop_orbit_by_episode_public.csv`
- `F11_slothrop_dissolution_field.{svg,png,pdf}`
- `F12_slothrop_to_rocket_transfer.{svg,png,pdf}`

The private 2E quote-support panel remains forbidden unless a separate curated
quotation layer is explicitly approved.

### `/strands` - scaffold only

Status: scaffolded. Keep as a marker until the 2H public-safe export contract
is stable enough for site integration.

The upstream public-safe manifest lists stripped 2H geometry, matrices, and
event graph exports, but the route should not be implemented opportunistically.
Wait for a route-specific pass that confirms the intended public argument,
field safety, and visual design.

---

## Standing Integration Rules

- Write only inside `L:/projects/the_zone_site`.
- Treat `L:/projects/the_zone` as read-only upstream.
- Copy only explicitly public-safe exports or separately approved curated short
  quotation material.
- Never copy corpora, normalized text corpora, snippet-bearing files, proof
  layers, notebooks, archived pages, or bulk quote banks.
- Update `data/provenance.md` for every imported asset.
- Integrate one route at a time.
- Preserve the figure-first editorial visual system established by `/network`.
- Prefer web-native Astro/D3 plates over embedded static analysis figures.
- Keep prose short, original, and free of novel quotations unless a curated
  quotation layer is separately approved.
