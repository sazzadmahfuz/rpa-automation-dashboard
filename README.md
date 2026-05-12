# 🤖 RPA Process Automation Dashboard

<div align="center">

[![Live Demo](https://img.shields.io/badge/▶_Live_Demo-00C7B7?style=for-the-badge)](https://sazzadmahfuz.github.io/rpa-automation-dashboard)
[![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)](.)
[![Robocorp](https://img.shields.io/badge/Robocorp-00C7B7?style=for-the-badge)](.)
[![Chart.js](https://img.shields.io/badge/Chart.js-FF6384?style=for-the-badge&logo=chartdotjs&logoColor=white)](.)
[![Course](https://img.shields.io/badge/HAMK-Software_Development-003087?style=for-the-badge)](.)

> **Project for Software Application Development & RPA — HAMK University of Applied Sciences**  
> Monitoring dashboard for Robotic Process Automation workflows — tracking task success rates, throughput, exceptions, and time saved across multiple automation bots.

</div>

---

## 📸 Screenshot

```
┌─────────────────────────────────────────────────────────────────┐
│  RPA MONITOR                    ● 4 bots active                 │
├──────────┬──────────┬──────────┬──────────┬─────────────────────┤
│  929     │  94.0%   │  26h     │  55      │  4                  │
│  Tasks   │  Success │  Saved   │  Errors  │  Active Bots        │
│  ↑ +111  │  target  │  ↑ +2h   │  ↓ low   │  of 6 configured    │
├──────────┴──────────┴──────────┴──────────┴─────────────────────┤
│  Hourly Throughput (24h)        │  Outcome Breakdown (Donut)    │
│  ▇▇▅▇▇▅▆▇▅▇▇▆▆▇▇▅▆▇▅▅▆▇▇▆     │   ◉ Success  ◉ Error  ◉ Run  │
├─────────────────────────────────┴───────────────────────────────┤
│  Workflow Status                │  Success Rate by Workflow      │
│  Web Scraper  320/340  ██ 94% 🟢│  ▇ ▅ ▇ ▆ ▄ ▇                │
│  Form Filler  183/210  ██ 87% ✅│  94 87 100 78 94 100          │
│  Report Gen   95/95   ██ 100%🟢 │                               │
├─────────────────────────────────┴───────────────────────────────┤
│  Live Event Log                                    [Clear]      │
│  12:34:05  Web Scraper   Scraped 48 listings successfully       │
│  12:34:02  Invoice Parser  Warning: low OCR confidence p.3      │
└─────────────────────────────────────────────────────────────────┘
```

---

## ✨ Features

| Feature | Description |
|---|---|
| **5 KPI Cards** | Tasks completed, success rate, time saved, exceptions, active bots |
| **Hourly Throughput** | 24-hour line chart with completed vs. error breakdown |
| **Outcome Donut** | Success / exception / running proportions at a glance |
| **Workflow Status Table** | Per-bot: run count, success count, rate bar, avg time, live status |
| **Success Rate Bar Chart** | Colour-coded (green ≥90%, amber ≥75%, red <75%) |
| **Live Event Log** | Auto-streaming timestamped log with OK / WARN / ERROR / INFO levels |
| **Refresh Button** | Randomise all metrics to simulate a new data pull |

---

## 🧠 RPA Concepts Demonstrated

### What is RPA?
Robotic Process Automation (RPA) uses software bots to automate repetitive, rule-based digital tasks — exactly what **Robocorp** and its Python-based `rpaframework` library enable.

### Workflow Architecture (Robocorp style)
A production Robocorp robot follows this structure:

```
robot.yaml                    # Robot metadata and entry points
conda.yaml                    # Python dependency environment
tasks/
└── tasks.py                  # Main task definitions
```

A typical task in `rpaframework`:

```python
from robocorp.tasks import task
from robocorp import browser, log

@task
def fill_web_form():
    """Automate web form submission."""
    log.info("Starting form filler bot")
    browser.configure(headless=True)
    page = browser.page()
    
    page.goto("https://target-site.com/form")
    page.fill("#name",    "Sazzad Mahfuz")
    page.fill("#email",   "sazzadibnamahfuz@gmail.com")
    page.click("#submit")
    
    log.info("Form submitted successfully")
```

### Metrics Tracked in This Dashboard

| Metric | Formula | Why It Matters |
|---|---|---|
| Success Rate | `success / total_runs × 100` | Core bot health KPI |
| Time Saved | `runs × avg_manual_time - runs × avg_bot_time` | Business value of automation |
| Exceptions | `total_runs - successful_runs` | Bot stability indicator |
| Throughput | `completions per hour` | Capacity planning |

---

## 🔄 Data Flow

```
[Physical Bots] → [Robocorp Cloud / Control Room]
                         ↓
               [REST API / Webhook push]
                         ↓
               [Dashboard fetch() call]
                         ↓
               [Chart.js visualisation]
```

In this demo, `fetch()` calls are replaced by in-browser simulation. In production, the `refreshData()` function would call the Robocorp Control Room API:

```javascript
async function fetchRobocopMetrics() {
    const res = await fetch('https://cloud.robocorp.com/api/v1/runs', {
        headers: { 'Authorization': `RC-WSKEY ${API_KEY}` }
    });
    const data = await res.json();
    // map data.results → workflows array, update charts
}
```

---

## 🗂️ File Structure

```
rpa-automation-dashboard/
└── index.html        # Complete dashboard — Chart.js via CDN, all state in memory
```

---

## 🎓 Academic Context

**Course**: Software Application Development / Robotic Process Automation  
**Programme**: BEng ICT & Robotics, HAMK University of Applied Sciences  
**Certification**: Robocorp Python Automation Certificate (Nov 2024, ID: d38fbb43)  
**Topics covered**: RPA workflow design, Robocorp `rpaframework`, bot monitoring, KPI metrics, exception handling in automation.

---

## 👤 Author

**Sazzad Ibna Mahfuz** — BEng ICT & Robotics, HAMK · Robocorp Certified  
[Portfolio](https://sazzadmahfuz.github.io) · [LinkedIn](https://www.linkedin.com/in/sazzad-mahfuz) · [GitHub](https://github.com/sazzadmahfuz)
