# NFS Trenching Tracker

Web-based performance tracker for the **Northfield South (NFS) — East Corridor Pipeline Trenching** project.

- **Client:** QatarEnergy LNG (QELNG)
- **Contractor:** McDermott International
- **Sub-Contractor:** Al Hassanain General Contracting
- **Document Ref:** NFS-MCD-MO-MST-00201 Rev. 01

Live site: **https://nfs-trench-tracker.com**

---

## What this app does

A single-page dashboard built from the project's Daily Progress Reports (DPRs). It contains:

- **Project Overview** — project summary, pipelines, trench zones, equipment fleet, and organization chart.
- **Dashboard** — KPI cards and charts (cumulative excavation, daily production, daily manpower, HSE safe manhours, weather downtime, permits status, % complete, reported vs surveyed).
- **Master Database** — the full DPR log, editable in-app.
- **Permits Register** — eCPW permit tracking with expiry alerts.
- **Look-Ahead** — upcoming events and milestones.
- **DPR Viewer** — print-ready single-day DPR.
- **Project Settings** — branding, team, surveyed quantities, scope, and data import/export.

All data lives in the browser (local storage). Real project data is loaded each time through the in-app **Import Excel** button — it is not embedded in the file.

---

## How the site is hosted

- Source lives in this repository as a single file: **`index.html`**.
- **Cloudflare Pages** watches this repo and automatically redeploys whenever `index.html` changes on the `main` branch.
- The site is protected by **Cloudflare Zero Trust Access** (authorized company emails only).

---

## How to update the site

1. Edit or replace **`index.html`** in this repository (`main` branch).
2. Commit the change.
3. Cloudflare Pages redeploys automatically within about one minute.

> **Tip:** When replacing the file on mobile, use **Add file -> Upload files** and upload the actual `index.html` file rather than copy-pasting its contents. Pasting on a phone can convert straight quotes into "smart quotes", which breaks the code.

---

## How to load real data

1. Open the live site and go to **Project Settings** (or use the **Import Excel** button in the top bar).
2. Select the Master Tracker Excel file.
3. The dashboard, charts, and tables update from the imported data.

Use **Export JSON** at any time to download a backup of the current data.

---

*Internal project tool — not for public distribution.*
