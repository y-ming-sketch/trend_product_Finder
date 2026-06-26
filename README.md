# tinder_web

# Trend Product Finder

A single-file browser app that helps creators evaluate e-commerce product ideas **before** the niche becomes saturated. Score an idea, get a category breakdown, pick ad angles, draft a brand outreach email, and compare saved ideas side-by-side.

No backend. No build step. No API keys. No external libraries. Just one HTML file.

---

## Features

- **Modern dark dashboard** — glassy cards, animated score ring, color-coded progress bars
- **Idea inputs** — product idea, target audience, budget, trend signals, competition level, urgency, creator skills
- **0–100 overall score** — weighted across five categories
- **Category breakdown** — trend potential, saturation risk, ad potential, profit potential, creator fit
- **Clear recommendation** — `Test now`, `Research more`, or `Avoid for now`
- **Three ad angle suggestions** — picked from 9 templates based on your skills, trend signals, and saturation
- **Brand outreach email draft** — personalized, ready to copy into your inbox
- **Saved ideas** — persisted in `localStorage` (key: `trendProductFinder.v1`)
- **Comparison table** — saved ideas ranked by overall score
- **Copy buttons** — one click to copy the final plan or the outreach email
- **Responsive** — works on desktop and mobile (breakpoints at 960px and 560px)

---

## Quick start

1. Clone the repo or download `index.html`.
2. Open `index.html` directly in any modern browser. That's it.

```bash
git clone https://github.com/y-ming-sketch/tinder_web.git
cd tinder_web
# macOS
open index.html
# Linux
xdg-open index.html
# Windows
start index.html
