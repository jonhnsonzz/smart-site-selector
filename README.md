# Smart Site Selector

### Turn Location Selection from Gambling into Calculation

> **Pain Point:** 30% of new retail stores fail due to poor location choices, with average losses of $20K-55K USD.
> Smart Site Selector quantifies location risk with AI, giving every store decision data-backed support.

**[Live Demo](https://jonhnsonzz.github.io/smart-site-selector/)**

---

## Problem It Solves

| Traditional Approach | Smart Site Selector |
|:---|:---|
| "This street looks busy" | Huff Gravity Model quantifies foot traffic attraction |
| "Several competitors nearby but unclear if oversaturated" | 2SFCA supply-demand ratio measures market saturation |
| "Breakeven calculation takes 3 hours of spreadsheets" | 30-second automatic 3-line breakeven report |
| "Competitor analysis requires manual counting" | Amap POI data auto-fetches nearby competitors |
| "Location decisions based on intuition" | AI composite score + explainable recommendations |

---

## Core Features

### 📊 AI Location Scoring
Combines Huff Gravity Model + 2SFCA spatial accessibility + competitive analysis into a single 100-point score that directly answers "Should I open here?"

### 💰 Breakeven Analysis
Input area/rent/average order value → 30-second complete breakeven report:
- Monthly fixed cost breakdown
- Breakeven point (revenue + customer count)
- 3-line analysis (Pessimistic / Neutral / Optimistic)
- Estimated payback period

### 🗺️ Competitor Intelligence
Auto-fetches same-category competitors within 1km radius:
- Competitor count + average rating
- Distance distribution
- Competitive intensity radar

### 🎯 AI Recommendations
Natural language output with quantitative backing — not just a conclusion, but why.

---

## Quick Start

### Option 1: Live Demo (Recommended)
👉 **[https://jonhnsonzz.github.io/smart-site-selector/](https://jonhnsonzz.github.io/smart-site-selector/)**

> Demo runs on simulated data. Works out of the box. Configure Amap key for real POI data.

### Option 2: Local Run

```bash
git clone https://github.com/jonhnsonzz/smart-site-selector.git
cd smart-site-selector
# Open index.html directly in browser, or:
python -m http.server 8080
# Visit http://localhost:8080
```

### Option 3: Enable Real POI Data

```javascript
// In index.html, replace YOUR_AMAP_KEY with your own key
// Get free key at: https://lbs.amap.com/
<script src="https://webapi.amap.com/maps?v=2.0&key=YOUR_AMAP_KEY"></script>
```

---

## Methodology

This project integrates globally-validated site selection frameworks:

- **Huff Gravity Model (1963)** — Quantifies probability of consumer choosing a venue, core of ESRI/McDonald's methodology
- **MCI Multi-factor Competition Model** — Huff generalization, distinguishes strong/weak competition
- **2SFCA Supply-Demand Accessibility** — Regional saturation assessment
- **XGBoost Revenue Prediction** — 40+ dimension synthetic prediction (v1.2)

> Reference: [Full Site Selection Methodology Research](https://feishu.cn/docx/BfkndZ0Rmo9C1uxBx87cfjmGnhd) (Chinese)

---

## Data Sources

| Source | Purpose | Status |
|:---|:---|:---:|
| Amap POI | Competitor location/rating | Requires key |
| National Stats Bureau | Regional population density | Built-in |
| Simulated Data | Feature demo | ✅ Available |

> **Amap free tier:** 1,000 POI queries/day — sufficient for small-scale use and demos.

---

## Comparison with Alternatives

| Product | Target User | Price | China Coverage | AI Prediction |
|:---|:---|:---|:---|:---|
| **Smart Site Selector** | Independent small retailers | Free/Low | ✅ Focused | ✅ Built-in |
| ESRI BAO | Enterprise | $100K+/yr | ⚠️ Expensive | ✅ |
| Placer.ai | Mid-size chain | $30K-100K/yr | ❌ | ✅ |
| WinShang/氪星 | Commercial real estate | Negotiable | ✅ | ⚠️ |

---

## Tech Stack

| Layer | Technology | Note |
|:---|:---|:---|
| Frontend | Vanilla HTML/CSS/JS | Zero dependencies, single file |
| Maps | Amap JS API | POI search + routing |
| Model Layer | Huff / MCI / 2SFCA | Classic spatial analysis |
| Prediction | XGBoost | Revenue forecast (v1.2+) |
| Hosting | GitHub Pages | Free, instant deploy |

---

## File Structure

```
smart-site-selector/
├── index.html    # Complete MVP (single file, works standalone)
└── README.md     # This file
```

---

## License

MIT License - Star ⭐ welcome

---

**Smart Site Selector** | Every location decision, backed by data.
