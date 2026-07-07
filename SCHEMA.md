# Data schema — proyectos.csv

Each row represents one research project. Here are the fields and what they mean.

| Column | Type | Required | Description |
|---|---|---|---|
| `id` | text | Yes | Stable unique identifier for the project, format `YYYY-slug` (e.g. `2026-border-migration`). Never changes even if other fields do. |
| `title` | text | Yes | Project title as it should appear publicly. |
| `researcher` | text | Yes | Name of the lead researcher. |
| `institution` | text | Yes | Affiliated institution. |
| `country` | text | Yes | Country or region where the research takes place (use "Europe" for cross-country/regional projects, not a country code). |
| `discipline` | text | Yes | Subject area (use the same controlled vocabulary across all projects — see list below). |
| `status` | text | Yes | One of: `ongoing`, `completed`, `suspended`. |
| `start_date` | date (YYYY-MM) | Yes | Project start date. |
| `end_date` | date (YYYY-MM) | No | Completion date (leave blank if ongoing). |
| `summary` | text | Yes | 1–2 sentences, accessible language (not the technical abstract). |
| `file` | text | Yes | Name of the matching Markdown file in `/proyectos/` (e.g. `2026-border-migration.md`). |
| `contact` | text | No | Email or authorized contact link the public can use to reach the researcher. |
| `external_link` | text | No | URL to an external record of the project (thesis repository, publication, Uwazi profile, etc.), if one exists. |

## Suggested controlled vocabulary for `discipline`

Keeping this list fixed avoids the same discipline being written differently by different people (e.g. "Law" vs "law" vs "Legal"). Add new ones here as needed, and always use exactly these terms:

- Law
- International and Comparative Human Rights Law
- Sociology
- Political Science
- History
- Anthropology
- Economics
- Gender Studies
- Communication
- Other (specify in summary)

## Consistency rules

- Don't leave required fields blank.
- Dates always in `YYYY-MM` format (e.g. `2026-03`), never `03/2026` or `March 2026`.
- The `id` is never reused or edited once created, even if the project's status changes.
