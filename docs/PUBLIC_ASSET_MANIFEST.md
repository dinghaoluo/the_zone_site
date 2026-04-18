# Public Asset Manifest

Approved asset families that may be copied from the analysis repo into this site repo.
Derived from the analysis repo's `05_publication/site_handoff/allowed_asset_manifest.md`.

Last reviewed: 2026-04-18.

**Rule:** Only assets listed here may be copied. Anything not listed is private by default.
Every copy requires a corresponding entry in `data/provenance.md`.

---

## 1. Public-safe structural data

### 1.1 Base public-safe layer

| File | Source | Destination | Rationale |
| ---- | ------ | ----------- | --------- |
| `episode_metadata_public.csv` | `05_publication/public_safe/data/` | `public/data/base/` | IDs, part, word count — no prose |
| `character_registry_public.csv` | `05_publication/public_safe/data/` | `public/data/base/` | character IDs and tags — no prose |
| `character_mentions_public.csv` | `05_publication/public_safe/data/` | `public/data/base/` | mention counts only — stripped of snippets |
| `character_mentions_visualisation_public.csv` | `05_publication/public_safe/data/` | `public/data/base/` | visualisation-ready mention counts — stripped |
| `slothrop_dissolution_public.csv` | `05_publication/public_safe/data/` | `public/data/base/` | dissolution metrics — no prose fields |
| `slothrop_alias_by_episode_public.csv` | `05_publication/public_safe/data/` | `public/data/base/` | alias counts per episode — no prose |
| `slothrop_orbit_by_episode_public.csv` | `05_publication/public_safe/data/` | `public/data/base/` | orbit metrics per episode — no prose |

### 1.2 Step 2D — character network

| File | Source | Destination | Rationale |
| ---- | ------ | ----------- | --------- |
| `master_network_layout_nodes_public.csv` | `05_publication/public_safe/data/step_2d/` | `public/data/step_2d/` | node positions and metadata — no prose |
| `master_network_layout_edges_public.csv` | `05_publication/public_safe/data/step_2d/` | `public/data/step_2d/` | edge weights only |
| `master_network_layout_public.json` | `05_publication/public_safe/data/step_2d/` | `public/data/step_2d/` | combined layout metadata |

### 1.3 Step 2H — narrative strands

All files have the `_public.csv` suffix. Source: `05_publication/public_safe/data/step_2h/`. Destination: `public/data/step_2h/`.

**Geometry:** `strand_episode_segments`, `strand_similarity_by_episode`, `strand_global_similarity`, `strand_layout_coords`, `strand_handoffs`

**Stripped matrices:** `episode_strand_matrix`, `episode_motif_matrix`, `character_strand_roles`, `character_motif_roles`, `motif_strand_links`

**Event graph:** `plot_event_nodes`, `plot_event_edges`

Rationale: geometry, stripped matrices, and stripped event graph; `note`, `evidence_note`, `short_description`, and `short_evidence_note` columns removed during export.

---

## 2. Approved figures

All figures listed here contain no source text and draw only on public-safe structural data.
Source paths are relative to `L:/projects/the_zone/02_analysis/`.

### 2B — Character registry (post-redesign flagships only)

| Figure | Source path | Destination | Copy status |
| ------ | ----------- | ----------- | ----------- |
| F10 cast weather system | `step_2b_character_registry/figures/F10_cast_weather_system.{svg,png,pdf}` | `public/figures/step_2b/` | Approved — optional companion for `/episodes` or `/network` |
| F11 arrival cascade | `step_2b_character_registry/figures/F11_arrival_cascade.{svg,png,pdf}` | `public/figures/step_2b/` | Approved — optional companion for `/episodes` |

Do NOT copy any other 2B figure (F01–F09 are archived/superseded).

### 2D — Character network

| Figure | Source path | Destination | Copy status |
| ------ | ----------- | ----------- | ----------- |
| F05 network architecture flagship | `step_2d_character_network/figures/F05_network_architecture_flagship.{svg,png,pdf}` | `public/figures/step_2d/` | Approved — primary for `/network` |
| F06 master character network atlas | `step_2d_character_network/figures/F06_master_character_network_atlas.{svg,png,pdf}` | `public/figures/step_2d/` | Approved — primary for `/network` |

### 2E — Slothrop dissolution (post-redesign flagships only)

| Figure | Source path | Destination | Copy status |
| ------ | ----------- | ----------- | ----------- |
| F11 Slothrop dissolution field | `step_2e_slothrop_dissolution/figures/F11_slothrop_dissolution_field.{svg,png,pdf}` | `public/figures/step_2e/` | Approved — primary for `/dissolution` |
| F12 Slothrop-to-rocket transfer | `step_2e_slothrop_dissolution/figures/F12_slothrop_to_rocket_transfer.{svg,png,pdf}` | `public/figures/step_2e/` | Approved — primary for `/dissolution` |

### 2H — Narrative strands

| Figure | Source path | Destination | Copy status |
| ------ | ----------- | ----------- | ----------- |
| F02 strand geometry | `step_2h_narrative_strands/figures/F02_strand_geometry.{svg,png,pdf}` | `public/figures/step_2h/` | Approved — primary for `/strands` |
| F04 narrative architecture flagship | `step_2h_narrative_strands/figures/F04_2h_narrative_architecture_flagship.{svg,png,pdf}` | `public/figures/step_2h/` | Approved — primary for `/strands` |

---

## 3. Fonts

Already imported and logged in `data/provenance.md` (2026-04-17). No re-copy needed.

## 4. Style documentation (optional, informational)

| Item | Source | Status |
| ---- | ------ | ------ |
| Plotting style regime | `05_publication/docs/plotting_style_regime.md` | Copyable as reference to `site_notes/` |
| Figure style audit | `05_publication/docs/figure_style_audit.md` | Copyable as reference |
| Ground-up redesign brief | `05_publication/docs/ground_up_reader_figure_redesign_brief.md` | Copyable as reference |
| Ground-up redesign report | `05_publication/docs/ground_up_figure_redesign_report.md` | Copyable as reference |

## 5. Canonical style module (optional)

`05_publication/style/zone_style.py` — pure configuration. Only relevant if a Python build step is added. The site does not currently use Python at build time.
