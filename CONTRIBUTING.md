# How to add or update a project

Step-by-step guide for two people working without stepping on each other.

## Adding a new project

1. **Pull the latest version** of the repository (`git pull` if you already have it cloned).
2. **Create a new branch** with a descriptive name, e.g.:
   ```
   git checkout -b new-project-border-migration
   ```
3. **Copy an existing file** in `proyectos/` as a starting template, rename it with the project's `id` (e.g. `2026-border-migration.md`), and fill in all the fields.
4. **Add a row to `proyectos.csv`** with the same data, following `SCHEMA.md` (controlled vocabulary, date format, etc.).
5. **Push your changes**:
   ```
   git add .
   git commit -m "Add project: border migration"
   git push origin new-project-border-migration
   ```
6. **Open a Pull Request** on GitHub. This lets the other person review before it merges into the main repository — especially useful while you're both getting the hang of things.
7. Once reviewed, **merge** into the main branch.

## Updating an existing project (e.g. status changes to "completed")

1. Edit the file in `/proyectos/` and the matching row in `proyectos.csv` directly.
2. Same flow: branch → commit → push → Pull Request.
3. **Never change the `id`** of a project when updating it, even if the title or status changes.

## Avoiding conflicts between the two of you

- Always work on a separate branch per project or change, never directly on the main branch.
- If you're both about to edit `proyectos.csv` at the same time, give each other a heads-up: it's the file most likely to cause conflicts because everyone edits the same file.
- An alternative if this becomes frequent: split `proyectos.csv` into several files (by year or country) to reduce the chance of both of you editing the same line at once. No need to do this now, but keep it in mind if the repository grows a lot.

## Before merging, check

- [ ] The `id` follows the `YYYY-slug` format and isn't reused.
- [ ] Dates are in `YYYY-MM` format.
- [ ] `discipline` uses exactly one term from the controlled vocabulary in `SCHEMA.md`.
- [ ] The `contact` field only includes information the researcher has authorized to be public.
