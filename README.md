# SURAKKHA Document Templates

A hub page (`index.html`) listing fill-in-browser report templates for the SURAKKHA project. Each template opens on its own, lets staff fill it in, and exports a print-ready PDF or Word file — no installation needed.

## What's in this package

```
/
├── index.html                        ← the hub / registry page
├── surakkha-event-report.html        ← Event / Activity Report (Reporting)
├── fivdb-attendance-sheet.html       ← Attendance Sheet (Reporting)
├── fivdb-attendance-sheet-camp.html  ← Attendance Sheet — Camp (Reporting)
├── event-agenda.html                 ← Event Agenda (Planning)
└── README.md
```

All files sit flat at the same level — this matches how GitHub's web uploader publishes files, so there's no folder structure to keep in sync.

## Publish with GitHub Pages

1. Upload all five `.html` files (and this README, optional) to your repository, overwriting any existing versions.
2. In the repo, go to **Settings → Pages**.
3. Under **Build and deployment**, set **Source** to "Deploy from a branch."
4. Pick the branch (usually `main`) and the root folder.
5. Save. GitHub will give you a URL like `https://<your-username>.github.io/<repo-name>/` — that's your template hub.

No build step is required — everything is static HTML/CSS/JS. After pushing, allow 1–2 minutes for the deploy, then hard-refresh (Ctrl/Cmd+Shift+R) if a page still looks old.

## Current template registry

| Code | Template | Category |
|---|---|---|
| SRK-RPT-01 | Event / Activity Report | Reporting |
| SRK-ATT-01 | Attendance Sheet | Reporting |
| SRK-ATT-02 | Attendance Sheet — Camp | Reporting |
| SRK-AGD-01 | Event Agenda | Planning |
| — | *(MEAL drawer is live and empty, ready for future templates)* | MEAL |

## Annexes list (Event / Activity Report)

The Event Report's annex checklist is numbered in this order:

1. Concept Note (Mandatory)
2. Safeguarding & PSHEA Risk Assessment (Mandatory)
3. Schedule (Mandatory)
4. Participants list (Mandatory)
5. Invitation / Approval / Notification Letter
6. Email communication with stakeholder / technical partner
7. Photo (Mandatory)
8. Attendance / Muster Roll (Mandatory)
9. Assessment / Pre-Post Test / Evaluation
10. Resolution
11. Documents / PPT (Mandatory)
12. Budget Breakdown (Optional)

Both attendance sheets carry the label "Annexes (8): Attendance Sheet" to match their position in this list. If the order changes again, update the checklist in `surakkha-event-report.html`, the "Photo Documentation" section header in the same file, and the annex label in both attendance sheet files together — they're meant to stay in sync.

## Adding a new template later

1. Add the new template's `.html` file at the repo root, next to the others.
2. Open `index.html` and add one entry to the `TEMPLATES` array near the bottom of the file, for example:

```js
{
  code: "SRK-MEAL-01",
  title: "Post-Distribution Monitoring",
  category: "MEAL",
  description: "One sentence on when to use this template.",
  badges: ["Beneficiary feedback", "Sampling"],
  file: "pdm-report.html",
  updated: "2026"
}
```

3. Save and re-publish (or push — GitHub Pages redeploys automatically). The `category` value must match one of the three drawer names already in the `CATEGORIES` list (`Reporting`, `Planning`, `MEAL`) — or add a new category there too.

## Notes

- Each template includes its own toolbar with Print Preview, PDF export, and Word export.
- The hub's drawer colors carry over from each category: teal for Reporting, blue for Planning, amber for MEAL — so the transition from hub to template feels continuous.
- Accessibility basics are built in: a skip link, visible keyboard focus outlines, semantic headings, full keyboard operation of the drawers, and `prefers-reduced-motion` support.
- Support contact on every template and the hub: mohasan.uddin@fivdb.org
