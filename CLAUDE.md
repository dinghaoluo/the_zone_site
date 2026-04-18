# The Zone — Site Repo Instructions

This is the public site repo for **The Zone**, a visual companion to *Gravity's Rainbow* (1973).
Deployed at `dinghaoluo.github.io/the_zone_site` via GitHub Pages.

## Repo identity

- **Stack:** Astro 5, TypeScript, static output, GitHub Pages
- **Design system:** bespoke CSS in `src/styles/global.css`; no framework
- **Fonts:** Major Mono Display (display), JetBrains Mono (mono), Cormorant Garamond (headings), Inter (body) — all already imported
- **Routes:** `/`, `/episodes`, `/dissolution`, `/network`, `/strands`

## The analysis repo is read-only upstream

The private analysis repo lives at `L:/projects/the_zone` (Windows) / `/mnt/l/projects/the_zone` (WSL).

- **Never modify anything inside the analysis repo.**
- **Never commit, push, or write to the analysis repo from this side.**
- You may read files from the analysis repo for reference and copy approved assets from it.

## Asset copying rules

1. **Only assets listed in `docs/PUBLIC_ASSET_MANIFEST.md` may be copied.** That manifest derives from the analysis repo's `allowed_asset_manifest.md`.
2. **Assets listed in `docs/RIGHTS_BOUNDARY.md` must never enter this repo.** No source text, no normalised corpora, no snippet-bearing CSVs, no quotation packets, no archived external pages, no private diagnostics.
3. **Before copying any CSV**, check that no column header matches a forbidden token: `snippet`, `local_context`, `quote`, `quotation`, `evidence_note`, `short_evidence_note`, `brief_note`, `raw_text`, `source_text`, `context_window`, `first_sentence`, `longer_note`.
4. **Update `data/provenance.md` for every copied asset** using the existing entry format. Append only — never rewrite earlier entries.

## Integration discipline

- Integrate **one route at a time**. Do not try to fill multiple stub pages in a single pass.
- The current integration order is: `/network` first, then `/episodes`, `/strands`, `/dissolution`.
- See `docs/NEXT_SITE_INTEGRATION.md` for the current cycle.
- **Do not rebuild the existing site.** Augment existing components, layouts, and styles. New components are fine when existing ones do not fit.
- CSS variables defined in `global.css` are used first; add new ones only for genuinely new roles.
- Major changes to layout, hero, or navigation require a human decision.

## Tone and design

- Calm, literary, British English
- Dark palette, generous whitespace, restrained animation
- The site should read as a hand-built digital humanities project, not a product, platform, or dashboard
- No novel quotations on the public site unless a curated quotation layer is explicitly approved

## Provenance

`data/provenance.md` tracks every upstream import. Each copied asset gets a dated entry with source path, destination, supporting route, and public-safety justification. Passes that copy nothing get a boundary note.
