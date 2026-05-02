# Data Provenance Log

This directory holds data assets imported from the upstream analysis repository.
Each entry records the source, destination, and justification for the import.

## Candidate Import Manifest

### Candidate: `MajorMonoDisplay-Regular.ttf`

- **Source**: `L:/projects/the_zone/05_publication/fonts/MajorMonoDisplay-Regular.ttf`
- **Destination**: `L:/projects/the_zone_site/public/fonts/MajorMonoDisplay-Regular.ttf`
- **Supports**: site display typography and branding
- **Why allowed**: publication-stage font asset stored under `05_publication/fonts/`; non-prose, release-safe asset

### Candidate: `JetBrainsMono-Regular.ttf`

- **Source**: `L:/projects/the_zone/05_publication/fonts/JetBrainsMono-Regular.ttf`
- **Destination**: `L:/projects/the_zone_site/public/fonts/JetBrainsMono-Regular.ttf`
- **Supports**: mono labels, footnotes, and data annotations
- **Why allowed**: publication-stage font asset stored under `05_publication/fonts/`; non-prose, release-safe asset

## Imports

### Imported: `MajorMonoDisplay-Regular.ttf`

- **Source**: `L:/projects/the_zone/05_publication/fonts/MajorMonoDisplay-Regular.ttf`
- **Imported**: 2026-04-17
- **Supports**: hero wordmark and site branding
- **Justification**: approved publication asset copied as a local static font with no runtime dependency

### Imported: `JetBrainsMono-Regular.ttf`

- **Source**: `L:/projects/the_zone/05_publication/fonts/JetBrainsMono-Regular.ttf`
- **Imported**: 2026-04-17
- **Supports**: section numbering, footnotes, and structural labels
- **Justification**: approved publication asset copied as a local static font with no runtime dependency

## Phase A — /network integration (2026-04-18)

### Imported: `master_network_layout_nodes_public.csv`

- **Source**: `L:/projects/the_zone/05_publication/public_safe/data/step_2d/master_network_layout_nodes_public.csv`
- **Destination**: `L:/projects/the_zone_site/public/data/step_2d/master_network_layout_nodes_public.csv`
- **Imported**: 2026-04-18
- **Supports**: /network route — node positions, community assignments, centrality metrics for 130 named characters
- **Justification**: public-safe export; contains only IDs, coordinates, community labels, and graph metrics; no prose, snippets, or quotations

### Imported: `master_network_layout_edges_public.csv`

- **Source**: `L:/projects/the_zone/05_publication/public_safe/data/step_2d/master_network_layout_edges_public.csv`
- **Destination**: `L:/projects/the_zone_site/public/data/step_2d/master_network_layout_edges_public.csv`
- **Imported**: 2026-04-18
- **Supports**: /network route — 1,959 co-presence edges with weights and association strengths
- **Justification**: public-safe export; contains only source/target IDs, edge weights, and display widths; no prose fields

### Imported: `master_network_layout_public.json`

- **Source**: `L:/projects/the_zone/05_publication/public_safe/data/step_2d/master_network_layout_public.json`
- **Destination**: `L:/projects/the_zone_site/public/data/step_2d/master_network_layout_public.json`
- **Imported**: 2026-04-18
- **Supports**: /network route — combined layout metadata, community definitions, label tiers, and recommended highlight sets
- **Justification**: public-safe export; structural metadata only; no forbidden field names present

### Imported: `F05_network_architecture_flagship.svg` / `.png` / `.pdf`

- **Source**: `L:/projects/the_zone/02_analysis/step_2d_character_network/figures/F05_network_architecture_flagship.{svg,png,pdf}`
- **Destination**: `L:/projects/the_zone_site/public/figures/step_2d/`
- **Imported**: 2026-04-18
- **Supports**: /network route — three-panel composite figure arguing distributed network architecture
- **Justification**: approved reader-facing figure; draws only on public-safe structural data; no source text

### Imported: `F06_master_character_network_atlas.svg` / `.png` / `.pdf`

- **Source**: `L:/projects/the_zone/02_analysis/step_2d_character_network/figures/F06_master_character_network_atlas.{svg,png,pdf}`
- **Destination**: `L:/projects/the_zone_site/public/figures/step_2d/`
- **Imported**: 2026-04-18
- **Supports**: /network route — full 130-node character atlas with community colouring, sized by weighted degree
- **Justification**: approved reader-facing figure; draws only on public-safe structural data; no source text

## Phase B — /episodes integration (2026-05-01)

### Imported: `episode_metadata_public.csv`

- Source: `L:/projects/the_zone/05_publication/public_safe/data/episode_metadata_public.csv`
- Destination: `L:/projects/the_zone_site/public/data/base/episode_metadata_public.csv`
- Imported: 2026-05-01
- Supports: /episodes route — 73 episode units with part, order, word count, and paragraph count
- Justification: public-safe export; contains only episode IDs, part labels, order, word counts, and paragraph counts; no source text, snippets, quotations, descriptions, evidence fields, or notes

### Imported: `episode_anchors_public.csv`

- Source: `C:/Users/Dinghao Luo/Downloads/episode_anchors_public_draft.csv`
- Destination: `L:/projects/the_zone_site/public/data/base/episode_anchors_public.csv`
- Imported: 2026-05-01
- Supports: /episodes route — selected episode anchors with labels, anchor types, original interpretive summaries, motif tags, display priority, and quote status
- Justification: curated public layer; contains original interpretive summaries and labels only; no source text, quotations, snippets, excerpts, context windows, evidence fields, or raw/normalised corpus material

### Imported: `episode_anchor_quotes_public.csv`

- Source: `L:/projects/the_zone/05_publication/site_handoff/episode_anchor_quotes_APPROVED_PUBLIC.csv`
- Destination: `L:/projects/the_zone_site/public/data/base/episode_anchor_quotes_public.csv`
- Imported: 2026-05-01
- Supports: /episodes route — sparse manually approved short quotes for selected episode anchors
- Justification: curated public quotation layer; contains eight short manually approved quotes, maximum 19 words; no context windows, source-line context, raw paragraph text, rejected candidates, or bulk quote bank; quotes are tied to /episodes commentary and visualisation

## Boundary Notes

- No new upstream assets were copied in this editorial refinement pass (2026-04-17).
- No new upstream assets were copied in the design/content polish pass (2026-04-17).
- The compact sparkline still uses manually encoded episode word-count values derived earlier from inspection of `episode_metadata_public.csv`, not a copied dataset.
- No quotations were copied or used before the approved `/episodes` anchor quote layer. The current quote layer is intentionally sparse, short, manually approved, and logged above.
