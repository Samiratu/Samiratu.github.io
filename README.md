Personal website for graduate school applications

This is a minimal single-page static site intended to be deployed with GitHub Pages.

Quick start

1. Preview locally with a simple HTTP server (Python 3):

```bash
# from the project root
python3 -m http.server 8000
# open http://localhost:8000 in your browser
```

2. Deploy to GitHub Pages (recommended: `main` branch):

- Create a repository on GitHub and push this folder to the repository's `main` branch.
- If you add the included workflow at `.github/workflows/pages.yml`, GitHub Actions will deploy automatically on push to `main`.
- Alternatively, enable Pages in GitHub Settings and point it at the `main` branch and folder `/`.

Files

- `index.html` — single-page content
- `styles.css` — styling
- `cv.pdf` — add your CV here if you want a downloadable link

Notes

- Edit `index.html` to add your real name, links, project repos, and CV.
- This is intentionally simple so it's easy for admissions committees to view.

Images

- `images/limbum.svg`, `images/ncd-detection.svg`: small illustrative SVGs added for project thumbnails (created/optimized for this site).
