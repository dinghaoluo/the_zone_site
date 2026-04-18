# Next Site Integration — /network

The next implementation cycle targets the `/network` route only.

---

## Scope

- Copy Phase-A assets from the analysis repo (2D data + 2D figures)
- Fill the `/network` page with static figure references and short original prose
- Update `data/provenance.md` with each import
- Verify the build passes (`npm run build`)
- Stop after `/network`. Do not touch other routes in this cycle.

## Assets to copy (Phase A)

### Data

| File | Source | Destination |
| ---- | ------ | ----------- |
| `master_network_layout_nodes_public.csv` | `05_publication/public_safe/data/step_2d/` | `public/data/step_2d/` |
| `master_network_layout_edges_public.csv` | `05_publication/public_safe/data/step_2d/` | `public/data/step_2d/` |
| `master_network_layout_public.json` | `05_publication/public_safe/data/step_2d/` | `public/data/step_2d/` |

### Figures

| Figure | Source | Destination |
| ------ | ------ | ----------- |
| F05 network architecture flagship | `02_analysis/step_2d_character_network/figures/F05_network_architecture_flagship.{svg,png,pdf}` | `public/figures/step_2d/` |
| F06 master character network atlas | `02_analysis/step_2d_character_network/figures/F06_master_character_network_atlas.{svg,png,pdf}` | `public/figures/step_2d/` |

## Pre-copy verification

Before copying each file:

1. Confirm it appears in `docs/PUBLIC_ASSET_MANIFEST.md`
2. Confirm it does not match any pattern in `docs/RIGHTS_BOUNDARY.md`
3. For CSVs: check that no column header matches a forbidden token
4. Destination is inside this repo (`the_zone_site/`)
5. A new provenance entry will be appended to `data/provenance.md`

## Page integration

Update `src/pages/network.astro`:

- Keep the existing eyebrow / heading / lede convention
- Add one or both 2D figures as static `<img>` references from `/the_zone_site/figures/step_2d/`
- Add short bridging prose (no novel quotations)
- Do not introduce scrollytelling or interactivity in this cycle
- Do not rebuild the page scaffolding

## What not to do

- Do not touch `/`, `/episodes`, `/dissolution`, or `/strands`
- Do not copy assets from other phases (2B, 2E, 2H)
- Do not traverse `02_analysis/` for unlisted data
- Do not introduce a Python build step
- Do not symlink into the analysis repo
- Do not add interactive hovercards with narrative detail

## After this cycle

Once `/network` is stable and deployed, the next cycle will target `/episodes` with Phase-B assets (episode metadata CSV, optional 2B F10/F11 figures).
