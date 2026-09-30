# AEROSENSE

**Pantau Udara, Lindungi Warga.**

AEROSENSE is an interface for understanding air quality around industrial buffer areas in Indonesia. The goal is to make sensor readings useful to residents, operators, and ESG reviewers without turning every decision into a spreadsheet exercise.

This repository is the **UI prototype**. It is meant to show the product flow and visual direction while the sensor network, accounts, and APIs are being connected.

## What you can explore

- **Beranda** — the area AQI at a glance, active nodes, alerts, and a small daily recommendation from AERO-BOT.
- **Peta sensor** — ten example nodes with filters and per-node detail.
- **Analitik AI** — raw readings next to corrected estimates, plus model metrics.
- **Audit ESG** — a report preview, traceable sample log, and export controls.
- **Peringatan** — plain-language alerts with practical next steps.
- **Tanya AERO-BOT** — a chat flow for explaining air-quality terms and conditions.

The interface is in Indonesian, uses Inter for the wordmark and UI, and follows the blue and white AEROSENSE identity. The logo and AERO-BOT character are based on the project's supplied artwork.

## Screenshots

| Dashboard | Sensor map |
| --- | --- |
| ![AEROSENSE dashboard](screenshots/overview.svg) | ![Sensor map](screenshots/peta.svg) |

| ESG audit | AERO-BOT chat |
| --- | --- |
| ![ESG audit view](screenshots/audit.svg) | ![AERO-BOT chat view](screenshots/aerobot.svg) |

## Run it locally

No install step is needed. From the repository folder:

```bash
python -m http.server 4173 --directory dist
```

Open [http://localhost:4173](http://localhost:4173).

## Current state

All readings, locations, scores, recommendations, and reports are **sample data**. The map is intentionally schematic and does not show actual sensor coordinates. The chat uses prepared replies to demonstrate the conversation; it does not call Gemini yet. Exports contain sample audit records and are not official ESG evidence. There is no account system or live alert delivery in this version.

The next implementation step is to connect real telemetry and timestamps, then add role-based access and a server-side Gemini integration. API keys should stay on the server, never in the browser.

## Project files

```text
dist/
  index.html          Dashboard and application views
  styles.css          Responsive UI and motion
  dashboard-refinement.css  AQI hero and recommendation card
  app.js              Prototype interactions and exports
  assets/             Supplied brand mark and AERO-BOT artwork
```

The layout was designed to stay usable on desktop and mobile, with keyboard focus states, text labels alongside status colors, and reduced-motion support.
