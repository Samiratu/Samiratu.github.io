This repository is a minimal, single-page static website intended for graduate school applications. The goal of an AI assistant working in this repo is to help produce, polish, and deploy a compact, accessible, and easily-maintained personal website.

Key facts
- Single-page static site: `index.html` + `styles.css` (+ optional `cv.pdf`). No build step or JS frameworks.
- Deployment: GitHub Pages is the target. A Pages workflow is included at `.github/workflows/pages.yml` which deploys the repository root on pushes to `main`.

What to prioritize
- Keep the site small, fast, and readable by humans (admissions committee). Avoid heavy client-side frameworks or large assets.
- Focus on content: About, Education, Research Interests, Projects (link to repos), CV link, and contact information.
- Ensure accessibility: use semantic HTML (landmarks, headings), visible focus states, and reasonable color contrast.

Conventions and patterns in this repo
- Styling: `styles.css` uses CSS variables at the top (`:root`) and simple utility classes (`container`, `card`). Follow the same lightweight approach.
- Links to external repos should include `rel="noopener"` and `target="_blank"` when opening new tabs (see examples in `index.html`).
- CV file (if present) is `cv.pdf` at repo root and is referenced from `index.html` as a download link.

Examples to follow (drawn from codebase)
- Project entry: Add a short description, one-line tech summary, and a repo link. Prefer linking to README or specific notebook paths (e.g., `notebooks/`) when available.
- Accessibility: `header` uses `role="banner"`, `main` uses `role="main"`, and project section uses `aria-labelledby`. Use these patterns when adding sections.

Notes and constraints
- Keep total site size small (prefer <1 MB). If adding images, optimize them and put them in an `images/` directory and provide `alt` text.
- Avoid adding build tooling (Node, Webpack) unless explicitly requested.

Developer workflows (how to run and verify)
- Local preview (no build required):
  python3 -m http.server 8000
  then open http://localhost:8000
- Deploy: push to `main`. The included GitHub Actions workflow will deploy to Pages automatically. Alternatively enable Pages manually in repo Settings and point at the `main` branch.

When editing content
- Edit `index.html` for structural/content changes. Keep styles in `styles.css` and minimize adding new selectors; reuse `card` and `container`.
- Use relative links for local assets (e.g., `cv.pdf`, images in `images/`). If adding images, add `alt` text and optimize file size.

If unsure
- Ask the user whether they prefer a color scheme, fonts, or a multi-page layout (e.g., separate publications page) before adding larger changes.

After making changes, run the local preview to validate layout and accessibility before pushing.
