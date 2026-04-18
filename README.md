# The Zone

Companion site for visualising the structure, networks, and dissolution patterns of Thomas Pynchon's *Gravity's Rainbow* (1973).

## Development

Requires [Node.js](https://nodejs.org/) 22+.

```bash
npm install
npm run dev        # local dev server at localhost:4321
npm run build      # static build to dist/
npm run preview    # preview the build
```

## Deployment

Pushes to `main` trigger automatic deployment to GitHub Pages via the workflow in `.github/workflows/deploy.yml`.

To enable: go to **Settings > Pages** in the GitHub repo, set source to **GitHub Actions**.

## Structure

```text
src/
  layouts/       base HTML layout
  components/    shared components (nav, etc.)
  pages/         route pages (index, episodes, dissolution, network, strands)
  styles/        global CSS
  data/          imported public-safe data (consumed at build time)
data/
  provenance.md  provenance log for imported assets
public/          static assets served as-is
```

## License

MIT
