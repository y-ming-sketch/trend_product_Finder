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
```

No `npm install`, no dev server, no environment variables.

---

## How it works

### Scoring formula

```
overall = 0.24 * trendPotential
        + 0.22 * (100 - saturationRisk)
        + 0.20 * adPotential
        + 0.18 * profitPotential
        + 0.16 * creatorFit
```

Each category is computed from your inputs:

| Category | Driven by |
|---|---|
| Trend potential | Trend signals, urgency |
| Saturation risk | Competition level, trend stage |
| Ad potential | Creator skills (video, copy, paid ads weigh most), budget |
| Profit potential | Budget, competition, trend stage |
| Creator fit | Number of skills selected, bonus for video + paid ads combo |

### Recommendation logic

| Condition | Recommendation |
|---|---|
| `overall >= 70` and `saturationRisk < 60` | **Test now** |
| `overall >= 50` | **Research more** |
| Otherwise | **Avoid for now** |

### Ad angle templates

Pain-point hook · Before/after transformation · Social proof reaction · 5-second hack tutorial · Aesthetic unboxing · FOMO opener · Old way vs new way · Identity/status · Founder POV.

The app picks the 3 most relevant angles for your specific skill set and trend context.

---

## Data & privacy

- All data lives in your browser's `localStorage` under the key `trendProductFinder.v1`.
- Nothing is sent to a server. No analytics, no tracking.
- To wipe everything: clear site data in your browser, or delete each saved idea from the UI.

---

## File structure

```
.
├── index.html   # The entire app: HTML + CSS + JS
└── README.md
```

---

## Browser support

Tested in modern Chromium, Firefox, and Safari. Requires support for:

- CSS Grid and custom properties
- `localStorage`
- `navigator.clipboard` (with a `document.execCommand` fallback)

---

## License

MIT. Use it, fork it, ship it.
