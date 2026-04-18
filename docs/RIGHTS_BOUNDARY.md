# Rights Boundary

Assets and data categories that must **never** enter this public site repo.
Derived from the analysis repo's `05_publication/site_handoff/forbidden_asset_manifest.md`.

Last reviewed: 2026-04-18.

**General principle:** The public site ships structural analysis and approved figures. It does not ship the novel, and it does not ship prose that paraphrases or quotes the novel.

If in doubt, treat it as forbidden.

---

## Forbidden categories

### 1. Raw text, cleaned text, normalised text

No source text in any form:

- `01_text_extraction/outputs/raw_text/`
- `01_text_extraction/outputs/cleaned_text/`
- `01_text_extraction/outputs/normalised_text/`
- `02_analysis/step_2b_character_registry/outputs/source_texts_normalised/`
- Per-episode text files (`1_01.txt`, `3_32.txt`, etc.)

### 2. Snippet-bearing mention layers

- `character_mentions.csv` (raw, with `snippet`, `local_context`, `raw_text` columns)
- `character_mentions_visualisation_ready.csv` (contains full context windows)
- Any `*_snippet*.csv`, `*_context_windows*.csv`
- `slothrop_rocket_context_windows.csv`

### 3. Quotation packets, proofcheck packets, quote banks

- `00_reference_material/private_sources/derived_quotation_packets/*`
- `02_analysis/step_2b_character_registry/outputs/character_proofcheck_packet/*`
- Any `*_quotation_*.md`, `*_quote_*.csv`, `*_proofcheck*.md`
- 2E figure `F10_quote_support_panel` (embeds short quotations — forbidden unless separately approved via a new curated-quotation-layer entry)

### 4. Archived external pages

- `00_reference_material/private_sources/*` (Semley, Michael Bell, Weisenburger, source EPUB, archived wiki pages)
- Any `archived_*.html`, `archive/wiki_*`, `fandom_*` files

### 5. Private diagnostics with quotations or paraphrase

- `step_2h_narrative_strands/diagnostics/strand_profiles.md`
- `step_2h_narrative_strands/diagnostics/title_hypothesis_ledger.md`
- `step_2h_narrative_strands/diagnostics/motif_workbook.md`
- `step_2h_narrative_strands/diagnostics/theme_synthesis_note.md`
- `step_2h_narrative_strands/diagnostics/step_2h_interpretive_synthesis.md`
- Any diagnostics file containing quotation blocks from 2E or 2B

### 6. Forbidden CSV/JSON field names

Stop if any column header or JSON key matches:

`snippet`, `local_context`, `quote`, `quotation`, `evidence_note`, `short_evidence_note`, `brief_note`, `raw_text`, `source_text`, `context_window`, `first_sentence`, `longer_note`

Also `short_description` when it describes a plot event, and any `*_note` column containing prose about the novel's content rather than analytical metadata.

### 7. 2H registries with extended prose

- `strand_registry.csv`
- `motif_registry.csv`
- `strand_causal_links.csv`

Use the stripped public-safe exports under `05_publication/public_safe/data/step_2h/` instead.

### 8. 2B private mention and alias layers

- `alias_surface_registry.csv`
- Per-character audit/review files
- Proofcheck review spreadsheets

### 9. Figures from archive/, demos/, or private_support/

- All figures under any `figures/archive/` directory
- All figures under any `figures/demos/` directory
- `step_2e_slothrop_dissolution/figures/private_support/F10_quote_support_panel.{svg,png,pdf}`
- Legacy 2B figures: F01–F09 (all superseded)
- Archived 2E figures: F01–F06, F09 in archive
- Legacy mirror copies under `outputs/preview_visual_gallery/figures/`

### 10. Build artefacts that leak paths

- `.mplconfig/` cache directories
- `*.jsonl` logs that might include quoted text
- `__pycache__/`
- Anything inside `_archived/` unless explicitly whitelisted
