# Data Provenance Log

This directory holds data assets imported from the upstream analysis repository.
Each entry records the source, destination, and justification for the import.

## Candidate Import Manifest

### Candidate: `MajorMonoDisplay-Regular.ttf`

- **Source**: `L:/projects/the_zone/05_publication/fonts/MajorMonoDisplay-Regular.ttf`
- **Destination**: `L:/projects/the_zone_site/public/fonts/MajorMonoDisplay-Regular.ttf`
- **Supports**: homepage display typography, navigation branding, footer branding
- **Why allowed**: publication-stage font asset stored under `05_publication/fonts/`; non-prose, release-safe asset

### Candidate: `JetBrainsMono-Regular.ttf`

- **Source**: `L:/projects/the_zone/05_publication/fonts/JetBrainsMono-Regular.ttf`
- **Destination**: `L:/projects/the_zone_site/public/fonts/JetBrainsMono-Regular.ttf`
- **Supports**: mono labels, microtypography, structural annotations
- **Why allowed**: publication-stage font asset stored under `05_publication/fonts/`; non-prose, release-safe asset

## Imports

### Imported: `MajorMonoDisplay-Regular.ttf`

- **Source**: `L:/projects/the_zone/05_publication/fonts/MajorMonoDisplay-Regular.ttf`
- **Imported**: 2026-04-17
- **Supports**: homepage hero wordmark and site branding
- **Justification**: approved publication asset copied as a local static font with no runtime dependency

### Imported: `JetBrainsMono-Regular.ttf`

- **Source**: `L:/projects/the_zone/05_publication/fonts/JetBrainsMono-Regular.ttf`
- **Imported**: 2026-04-17
- **Supports**: structural labels, section eyebrows, and metric typography
- **Justification**: approved publication asset copied as a local static font with no runtime dependency

## Boundary Notes

- No data exports were copied for this homepage pass.
- The structural preview uses manually encoded aggregate episode word-count values derived from inspection of `episode_metadata_public.csv`, not a copied dataset.
- No quotations were copied or used.
