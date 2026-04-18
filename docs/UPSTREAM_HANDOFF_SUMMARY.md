# Upstream Handoff Summary

Summary of the analysis-side handoff packet located at:
`L:/projects/the_zone/05_publication/site_handoff/`

Last reviewed: 2026-04-18.

---

## What the analysis repo supplies

The analysis repo (`the_zone`) provides:

- **Public-safe data exports** under `05_publication/public_safe/data/` — CSVs and JSON files stripped of all prose, quotation, and snippet fields.
- **Approved figures** from the `02_analysis/` figure directories — only specific figure IDs listed in the allowed manifest; archived, demo, and private-support figures are excluded.
- **Style documentation** under `05_publication/docs/` — plotting style regime, figure style audit, redesign brief and report. These are informational; they do not constrain the site's own design.
- **The handoff packet itself** — seven documents governing what is copyable, where it goes, and the rights boundary.

## What the analysis repo does not supply

- Site design system, component library, or CSS
- Copywriting, headings, or tone decisions
- Animation, interaction, or scrollytelling choices
- Build pipeline configuration
- Information architecture decisions

**Site design belongs to this repo.** The analysis repo supplies the evidence layer (data, figures, rights boundaries), not a site specification.

## Route integration order

The handoff packet recommends this sequence, one route per integration cycle:

1. **`/network`** — 2D assets (F05, F06, network layout data) are the most complete and rights-safe. Start here.
2. **`/episodes`** — episode metadata plus optional 2B companions (F10, F11).
3. **`/strands`** — 2H strand geometry and narrative architecture (F02, F04) once the public-safe export is stable.
4. **`/dissolution`** — 2E flagships (F11, F12) are copy-approved. The quote support panel (F10) remains forbidden until a curated quotation layer is separately approved.
5. **`/` landing** — touched only to update entry-link copy after a downstream section ships content.

## Handoff packet files

| File | Purpose |
| ---- | ------- |
| `README.md` | Orientation — hard rules, who this is for |
| `existing_site_integration_handoff.md` | Current site state, design vocabulary, integration principle |
| `allowed_asset_manifest.md` | Every copyable asset family with source paths and rationale |
| `forbidden_asset_manifest.md` | Explicit forbidden categories with examples |
| `page_asset_map_for_existing_site.md` | Per-route asset and argument map |
| `public_copy_plan.md` | Phased copy sequencing with exact source/destination tables |
| `claude_b_incremental_prompt.md` | The integration prompt and hard rules |

## Key constraints from the handoff

- Inspect the existing site before changing anything
- Copy only listed assets; never traverse the analysis repo opportunistically
- Update `data/provenance.md` for every import
- Augment, do not rebuild
- One route per cycle
- No source text, quotations, or snippet-bearing data on the public site
- No figures from `archive/`, `demos/`, or `private_support/` directories
