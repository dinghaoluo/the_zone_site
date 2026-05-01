# Site State and Visual Standard

Last updated: 2026-05-01.

This site is the public Astro companion for *Gravity's Rainbow* analysis. The
private analysis repo supplies approved structural evidence; this repo owns the
reader-facing site, interaction, visual language, and provenance record.

---

## Current Site State

- Stack: Astro 5, TypeScript, static output, GitHub Pages.
- Deployment base: `astro.config.mjs` sets `base: "/the_zone_site"`.
- Base-path handling: routes and components should use
  `import.meta.env.BASE_URL` for internal links and fetches.
- Implemented routes:
  - `/`: editorial landing page with section links and a compact structural
    preview.
  - `/network`: completed interactive D3 route and current design benchmark.
  - `/episodes`: first-pass interactive/web-native route using
    `public/data/base/episode_metadata_public.csv`, with
    `EpisodeSequencePlate.astro` and `EpisodePartStructure.astro`.
- Scaffolded routes:
  - `/dissolution`: page head only; later 2E integration route.
  - `/strands`: intentional marker until 2H public-safe contract stabilizes.

Current public assets in this repo:

- `public/data/step_2d/master_network_layout_nodes_public.csv`
- `public/data/step_2d/master_network_layout_edges_public.csv`
- `public/data/step_2d/master_network_layout_public.json`
- `public/figures/step_2d/F05_network_architecture_flagship.{svg,png,pdf}`
- `public/figures/step_2d/F06_master_character_network_atlas.{svg,png,pdf}`
- `public/data/base/episode_metadata_public.csv`
- `public/fonts/MajorMonoDisplay-Regular.ttf`
- `public/fonts/JetBrainsMono-Regular.ttf`

## Public/Private Boundary

The only write target is `L:/projects/the_zone_site`.

The analysis repo at `L:/projects/the_zone` is read-only upstream. It may be
consulted for public-safe exports, manifests, and style references. It must not
be edited from this repo.

Never copy:

- full text, raw text, cleaned text, or normalized text corpora
- snippet-bearing mention files or context windows
- proof layers, proofcheck packets, notebooks, diagnostics with prose evidence,
  or bulk quote banks
- archived external pages or packaged helper corpora
- figures from `archive/`, `demos/`, or `private_support/`

Every copied public-safe asset must be recorded in `data/provenance.md` with
source, destination, route support, import date, and public-safety justification.

## Figure-First Design Rule

Figures are the centre of the site. Prose introduces, frames, and captions the
plates; it should not dominate the page.

Preserve these conventions:

- dark editorial space, thin rules, and restrained accent colour
- readable mono labels and quiet serif headings
- narrow prose columns with wide plate breakouts where the figure needs space
- plate numbering, short panel labels, and captioned analytical claims
- interaction that clarifies structure without becoming a generic dashboard

Avoid:

- static SVG embeds as the main experience when a web-native plate is feasible
- SaaS cards, chips, CTAs, or dashboard chrome
- generic D3 demos that ignore the site's literary/cartographic tone
- constraining visualisations to the main text width
- ornamental interaction that does not sharpen the reading of the figure

## `/network` Implementation Pattern

`/network` is the current benchmark route.

- `src/pages/network.astro` provides the route structure, prose, wide plate
  breakouts, captions, and notes.
- `src/components/NetworkAtlas.astro` builds the primary D3 network plate from
  public-safe CSVs and supports overview, Slothrop, community, and full modes.
- `src/components/NetworkArchitecture.astro` builds a secondary D3 plate from
  the same public-safe data, showing communities, centrality, and dyads.
- Components fetch data through the configured base path:
  `import.meta.env.BASE_URL`.
- The analysis SVG/PDF/PNG assets remain available as references/downloads, but
  the reader-facing route is web-native.

Future routes should copy this relationship between page and plate: the route
sets the editorial argument and spacing; dedicated components build the figure.

## Expectations for Future Visualisations

- Start with the public-safe data contract and provenance boundary.
- Design the figure as an editorial plate, not as a transplanted notebook chart.
- Recreate analysis figures for the web when the route depends on them.
- Let figures break out from the prose column when the reading task needs width.
- Use the existing CSS variables and typography before adding new design tokens.
- Keep interactions legible: a small number of named views usually beats a large
  control surface.
- Write original explanatory copy. Do not include novel quotations unless a
  curated quotation layer has been separately approved.

## Next Route Direction

The first `/episodes` pass is now implemented.

The next likely route-level work is either a refinement pass on `/episodes` or
the later `/dissolution` integration. Optional 2B F10/F11 assets are approved in
the upstream handoff manifest, but they have not been copied and should still be
used sparingly after a route-specific copy/provenance pass.
