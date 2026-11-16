# EQC Hub — Intake 25J

> A big-screen classroom hub and live dashboard for Equinim College's Intake 25J (Diploma of IT — Back End Web Development).

**Live demo:** [eqc-hub-25j.vercel.app](https://eqc-hub-25j.vercel.app)

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat-square) ![Tailwind CSS](https://img.shields.io/badge/Tailwind%20CSS-06B6D4?style=flat-square) ![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square) ![Chart.js](https://img.shields.io/badge/Chart.js-FF6384?style=flat-square) ![Firebase](https://img.shields.io/badge/Firebase-FFCA28?style=flat-square) ![Vercel](https://img.shields.io/badge/Vercel-000000?style=flat-square)

## Features

- Six-tile classroom display: intake, trainer, today's topics, attendance, Riz Quiz leaderboard and course progress
- Live clock, class-day counter and course progress bar calculated from the intake's start/end dates and class days
- Today's topics, notes and attendance pulled from a published Google Sheet (CSV) on a timer
- **Riz Quiz** (`play.html`) — real-time trivia leaderboard backed by Firebase Realtime Database
- **Live dashboard** (`dashboard.html`) — animated KPI counters, Chart.js line/doughnut/bar charts and a recent-activity feed driven by mock data that refreshes every few seconds
- Responsive layout: full-screen grid on a classroom TV, stacked cards on phones
- All per-intake settings live in one `CONFIG` object at the top of `index.html`

## Tech stack

- Plain HTML + vanilla JavaScript (no build step)
- Tailwind CSS (Play CDN), Inter + JetBrains Mono, Bootstrap Icons
- Chart.js 4 for the dashboard charts
- Firebase Realtime Database (compat SDK) for the quiz leaderboard
- Hosted on Vercel as a static site

## Run it locally

```bash
git clone https://github.com/thedalycreative/eqc-hub-25J.git
cd eqc-hub-25J
python3 -m http.server 8000   # or: npx serve .
# open http://localhost:8000  (dashboard: /dashboard.html)
```

## Deployment (Vercel)

Static site — no build command, output directory is the repo root. The Vercel project **eqc-hub-25j** is linked to this repo and deploys `main` to production at **https://eqc-hub-25j.vercel.app**. Every push to `main` redeploys; other branches get preview URLs.

To reuse for a new intake, edit `CONFIG` in `index.html` (intake code, dates, class days, Google Sheet CSV URL, Firebase config).

## Screenshots

![EQC Hub — Intake 25J demo](docs/screenshots/demo.gif)

<p align="center">
  <img src="docs/screenshots/desktop.jpg" alt="Classroom hub on a 1440px screen" width="560">
  <img src="docs/screenshots/dashboard.jpg" alt="Live dashboard with charts and activity feed" width="560">
  <img src="docs/screenshots/mobile.jpg" alt="Hub on a phone" width="260">
</p>

_Captured from the live site (https://eqc-hub-25j.vercel.app). Regenerate with any headless browser; files live in `docs/screenshots/`._

---

Built by [The Daly Creative](https://www.thedalycreative.com) · Perth, WA
