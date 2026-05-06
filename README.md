# AI Research Reports

A static report archive generated from ChatGPT conversations.

## Site structure

- `index.html` — main navigation page for all reports
- `reports/<slug>/index.html` — individual HTML reports
- `reports.json` — machine-readable report registry used by the homepage
- `vercel.json` — Vercel static site configuration

## How to add a new report

1. Create a new folder under `reports/`, for example:

   ```text
   reports/2026-05-06-my-new-report/index.html
   ```

2. Add the report metadata to `reports.json`:

   ```json
   {
     "title": "My New Report",
     "slug": "2026-05-06-my-new-report",
     "path": "/reports/2026-05-06-my-new-report/",
     "date": "2026-05-06",
     "description": "Short summary shown on the homepage.",
     "tags": ["research", "strategy"]
   }
   ```

3. Commit and push to `main`. If the repository is connected to Vercel, deployment should run automatically.

## Vercel setup

Import this GitHub repository into Vercel as a static project.

Recommended settings:

- Framework Preset: `Other`
- Build Command: leave empty
- Output Directory: leave empty or `.`
- Install Command: leave empty
- Root Directory: repository root

After import, every push to `main` should update the production deployment.
