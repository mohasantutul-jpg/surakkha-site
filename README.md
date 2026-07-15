# SURAKKHA Document Templates

A small hub page (`index.html`) that lists fill-in-browser report templates for the SURAKKHA project. Each template opens on its own, lets staff fill it in, and exports a print-ready PDF or Word file — no installation needed.

## Folder structure

```
/
├── index.html              ← the hub / gallery page
├── templates/
│   ├── surakkha-event-report.html
│   └── event-agenda.html
└── README.md
```

## Publish with GitHub Pages

1. Push this folder to a GitHub repository (as the repo root, or inside a `docs/` folder — your choice).
2. In the repo, go to **Settings → Pages**.
3. Under **Build and deployment**, set **Source** to "Deploy from a branch."
4. Pick the branch (usually `main`) and the folder this content lives in (`/root` or `/docs`).
5. Save. GitHub will give you a URL like `https://<your-username>.github.io/<repo-name>/` — that's your template hub.

No build step is required — everything is static HTML/CSS/JS.

## Adding a new template later

1. Drop the new template's `.html` file into `/templates`.
2. Open `index.html` and add one entry to the `TEMPLATES` array near the bottom of the file, for example:

```js
{
  code: "SRK-XXX-01",
  title: "New Template Name",
  category: "Reporting",       // reuses an existing filter chip, or creates a new one
  accent: "var(--teal)",       // var(--navy), var(--teal), or var(--blue)
  description: "One sentence on when to use this template.",
  badges: ["Short feature tag", "Another tag"],
  file: "templates/new-template.html",
  updated: "2026"
}
```

3. Save and re-publish (or just push — GitHub Pages redeploys automatically). No other code changes are needed; the filter chips and cards build themselves from this list.

## Notes

- Each template already includes its own toolbar with Print Preview, PDF export, and Word export — that's unchanged from the original files.
- The hub page keeps colour-coding consistent with each template's own accent colour (teal for the Event Report, blue for the Agenda) so the transition from hub → template feels continuous.
- Accessibility basics are built in: a skip link, visible keyboard focus outlines, semantic headings, and `prefers-reduced-motion` support.
