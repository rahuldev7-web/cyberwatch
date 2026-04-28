# 🌐 CyberWatch — Live Global Threat Intelligence

> Real-time cyber attack visualization. SOC-grade dashboard. Built with D3.js + Canvas API.

**[🚀 View Live →](https://rahuldev7-web.github.io/cyberwatch)**

---

![CyberWatch Dashboard](https://raw.githubusercontent.com/rahuldev7-web/cyberwatch/main/preview.png)

---

## What is CyberWatch?

CyberWatch is a real-time global cyber threat intelligence dashboard — inspired by professional Security Operations Center (SOC) displays used by Fortune 500 companies.

It visualizes simulated cyber attacks firing between countries in real time, complete with animated arc trajectories, pulse rings, severity alerts, and live intelligence feeds.

Built entirely with vanilla JavaScript, D3.js, and the Canvas API — no frameworks, no backend.

---

## Features

### 🗺️ Live Attack Map
- **Real world map** rendered with D3.js Natural Earth projection
- **Animated arc attacks** — curved bezier trajectories flying between countries
- **Dual pulse rings** — expanding ripple rings when attacks land at destination
- **Origin dots** — red glow markers on top attacker countries
- **Target dots** — green markers on primary target countries
- **Latitude/longitude graticule** grid overlay

### 🚨 Critical Alerts
- Full-screen **CRITICAL ALERT** popup triggers for high-severity attacks
- Ransomware detection triggers automatic alerts
- Auto-dismisses after 6 seconds with visual pulse animation

### 📊 SOC Dashboard Panels
- **Attack type breakdown** — DDoS, Brute Force, Ransomware, Phishing, Port Scan, Malware
- **Top source countries** — ranked leaderboard with attack bars
- **Live intelligence feed** — scrolling real-time attack log with severity tags
- **Severity gauge** — dynamic LOW → MEDIUM → HIGH → CRITICAL indicator
- **Country detail panel** — click any country for attack breakdown

### 📈 Live Statistics
- Attacks per second counter
- Total attacks today (starts at 600K–1.2M)
- Attacks blocked counter (73% block rate)
- Per-type counters in nav and bottom bar
- Scrolling ticker with active threat intelligence

### 🎨 Design
- **CRT scanline overlay** — government terminal aesthetic
- **Vignette effect** — cinematic map edges
- Deep space dark theme with green/red accent system
- Fully responsive layout

---

## Attack Types & Colors

| Attack | Color | Severity | Weight |
|--------|-------|----------|--------|
| ⚡ DDoS | `#ff2d4a` Red | HIGH | 28% |
| 🔑 Brute Force | `#ff6b2b` Orange | MEDIUM | 22% |
| 💀 Ransomware | `#8b5cf6` Purple | CRITICAL | 10% |
| 🎣 Phishing | `#ffd60a` Yellow | MEDIUM | 20% |
| 🔍 Port Scan | `#00b8ff` Blue | LOW | 14% |
| 🦠 Malware | `#00ff96` Green | HIGH | 6% |

---

## Countries Tracked

**Top Attack Sources:**
China · Russia · United States · Brazil · India · Germany · Netherlands · Ukraine · Iran · North Korea

**Primary Targets:**
United States · Germany · United Kingdom · Japan · France · Australia · Canada · India · South Korea · Brazil

---

## Tech Stack

| Tech | Usage |
|------|-------|
| **D3.js v7** | World map rendering, geo projection |
| **TopoJSON** | Country boundary data |
| **Canvas API** | Arc animations, pulse effects |
| **Vanilla JavaScript** | Zero framework, pure JS |
| **Inter + JetBrains Mono** | Typography |
| **GitHub Pages** | Free hosting |

---

## How the Simulation Works

### Attack Generation
```javascript
// Weighted random selection based on real-world attack frequency
const type = weightedRandom(ATTACK_TYPES);
const src  = weightedRandom(COUNTRIES);   // China 18%, Russia 15%, etc.
const tgt  = randomTarget(TARGETS);

// Quadratic bezier arc trajectory
x = (1-t)² × sx + 2(1-t)t × cx + t² × tx
y = (1-t)² × sy + 2(1-t)t × cy + t² × ty
```

### Severity System
```
Entropy fluctuates → LOW (0) → MEDIUM (1) → HIGH (2) → CRITICAL (3)
Ransomware attacks always trigger CRITICAL alerts
Alert cooldown: 35 seconds between alerts
```

### Statistics Model
- Attack rate: ~3–8 attacks/second
- Block rate: 73% (industry average)
- Background growth: +20–80 attacks/second simulated
- 20 source countries, 15 target countries

---

## Why I Built This

As a Cybersecurity M.S. student, I wanted to visualize what real Security Operations Centers monitor daily — global threat patterns, attack types, origin countries, and severity levels.

This project demonstrates:
- **D3.js** geospatial rendering and projections
- **Canvas API** real-time animation at 60fps
- **Data visualization** design and UX
- **Cybersecurity domain knowledge** — attack types, severity frameworks, threat intelligence concepts
- **Frontend engineering** — zero dependencies, pure performance

---

## Related Projects

| Project | Description |
|---------|-------------|
| 🔐 [PassGuard](https://rahuldev7-web.github.io/passguard) | Real-time password strength analyzer |
| 🛡️ [Network Security Monitor](https://github.com/rahuldev7-web/network-security-monitor) | Python ML anomaly detection |
| 📋 [Job Tracker API](https://github.com/rahuldev7-web/job-tracker-api) | Spring Boot REST API |
| 📄 [ATS Resume Scorer](https://github.com/rahuldev7-web/ATS-Resume-Scorer) | Python NLP resume analyzer |

---

## Run Locally

```bash
git clone https://github.com/rahuldev7-web/cyberwatch.git
cd cyberwatch
open index.html
```

No build step. No npm install. Just open and go.

---

## Author

**Kiran Rahul Pabboju** — Software Engineer · M.S. Cybersecurity

- 🌐 Portfolio: [rahuldev7-web.github.io](https://rahuldev7-web.github.io)
- 🔐 PassGuard: [rahuldev7-web.github.io/passguard](https://rahuldev7-web.github.io/passguard)
- 💼 LinkedIn: [pabboju-kiran-rahul](https://linkedin.com/in/pabboju-kiran-rahul)
- 🐙 GitHub: [@rahuldev7-web](https://github.com/rahuldev7-web)

---

## License

MIT — free to use, modify, and share.

---

*Built with D3.js · Canvas API · Vanilla JS · Zero dependencies · GitHub Pages*
