[README.md](https://github.com/user-attachments/files/29750427/README.md)# The Margin — Public Research Catalogue

This repository is both the **data source and the public website** for The Margin. It's published as a webpage via GitHub Pages (`index.html`), and that same page reads directly from `proyectos.csv`. Uwazi remains the internal working archive, not the public face.

## Structure

```
the-margin-data/
├── index.html               # The public site (GitHub Pages serves this)
├── proyectos.csv             # Master index with all projects (one row per project)
├── proyectos/                 # One Markdown file per project, with full detail
│   ├── right-wing-litigation-ecthr.md
│   └── municipalities-social-rights.md
├── SCHEMA.md                  # Description of each column/field
└── CONTRIBUTING.md            # How to add or update a project
```

## How the public site is enabled (GitHub Pages)

1. In GitHub, go to the repository → **Settings** → **Pages** (left sidebar).
2. Under "Build and deployment" → "Source", choose **"Deploy from a branch"**.
3. Under "Branch", select `main` and the `/ (root)` folder.
4. Click **Save**.
5. GitHub will give you the site's URL, in the format:
   ```
   https://your-username-or-org.github.io/repository-name/
   ```

## How the site gets updated

You don't need to touch `index.html` to add a project. It's enough to:
1. Add a new row to `proyectos.csv` (following `SCHEMA.md`).
2. Add the matching Markdown file in `/proyectos/`.
3. Push the changes (see `CONTRIBUTING.md`).

GitHub Pages updates itself automatically, usually within 1–2 minutes of each change.

## Uwazi's role now

Uwazi is the internal working tool: submission management, validation, non-public internal fields. Once a project is validated, its public-facing data moves into `proyectos.csv` to appear on the site.

