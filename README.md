# 🤖 RPA Process Automation Dashboard

<div align="center">

[![Live Demo](https://img.shields.io/badge/▶_Live_Demo-00C7B7?style=for-the-badge)](https://sazzadmahfuz.github.io/rpa-automation-dashboard)
[![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)](.)
[![Robocorp](https://img.shields.io/badge/Robocorp-00C7B7?style=for-the-badge)](.)
[![Chart.js](https://img.shields.io/badge/Chart.js-FF6384?style=for-the-badge&logo=chartdotjs&logoColor=white)](.)
[![Automation](https://img.shields.io/badge/RPA-Workflow_Monitoring-7B61FF?style=for-the-badge)](.)
[![Course](https://img.shields.io/badge/HAMK-Software_Development-003087?style=for-the-badge)](.)

> **Project for Software Application Development & RPA — HAMK University of Applied Sciences**  
> Advanced monitoring dashboard for Robotic Process Automation workflows — visualising task execution analytics, workflow stability, automation throughput, operational KPIs, and exception monitoring across multiple software bots using Robocorp-inspired automation architecture.

---

### Developed by

# Sazzad Ibna Mahfuz

Bachelor of Engineering — ICT Robotics  
Häme University of Applied Sciences (HAMK), Finland

</div>

---
---

## Project Overview

This project demonstrates a complete **RPA monitoring and analytics dashboard** inspired by real industrial Robotic Process Automation systems used in enterprise environments.

The dashboard simulates the monitoring layer commonly found in:

- Robocorp Control Room
- UiPath Orchestrator
- Automation Anywhere Control Center
- Blue Prism monitoring systems

The application visualises:

- Bot execution metrics
- Workflow performance
- Success and failure rates
- Exception monitoring
- Automation throughput
- Estimated business time savings
- Real-time process logs
- Operational status of multiple bots


using:

- HTML5
- CSS3
- JavaScript
- Chart.js
- Robocorp automation concepts
- Python RPA workflow architecture

The system simulates a real enterprise automation monitoring environment where multiple bots continuously execute workflows and stream operational data into a central dashboard.

---

## System Dashboard Preview

```text
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

## Features

| Feature | Description |
|---|---|
| **5 KPI Monitoring Cards** | Real-time tracking of tasks completed, success rate, automation time savings, exceptions, and active bots |
| **24-Hour Throughput Analytics** | Dynamic line chart showing completed tasks vs errors over time |
| **Outcome Distribution Donut Chart** | Success / Exception / Running workflow visualisation |
| **Workflow Performance Table** | Per-bot statistics including runs, success count, processing time, and operational state |
| **Success Rate Analytics** | Colour-coded workflow comparison using bar charts |
| **Live Event Streaming Log** | Timestamped real-time process events with INFO / WARN / ERROR levels |
| **Interactive Refresh System** | Simulated API refresh to emulate live production monitoring |
| **Real-Time Data Simulation** | Dynamic randomised execution metrics and workflow updates |
| **Responsive UI Design** | Works across desktop and mobile displays |
| **Modern Enterprise Dashboard UI** | Inspired by industrial automation monitoring systems |

---

## RPA Concepts Demonstrated

### What is Robotic Process Automation?

Robotic Process Automation (RPA) refers to the use of software bots that automate repetitive, rule-based digital tasks normally performed by humans.

Examples include:

- Form submission
- Invoice processing
- Email automation
- Web scraping
- Data extraction
- ERP system interaction
- Database synchronisation
- Report generation

The project demonstrates the operational monitoring side of RPA systems, where automation engineers supervise:

- bot performance
- task execution
- workflow reliability
- business efficiency
- runtime analytics

---

## Enterprise RPA Architecture

A production-grade RPA system generally consists of:

```text
┌────────────────────┐
│   Human Operator   │
└─────────┬──────────┘
          │
          ▼
┌────────────────────┐
│  Control Room UI   │
│  (Monitoring)      │
└─────────┬──────────┘
          │
          ▼
┌────────────────────┐
│  RPA Orchestrator  │
└─────────┬──────────┘
          │
 ┌────────┴────────┐
 ▼                 ▼
Bot A            Bot B
(Web)            (Email)

 ▼                 ▼
ERP Systems      Databases
```

This project focuses on the:

### Monitoring + Analytics Layer

which is responsible for:

- collecting bot metrics
- displaying execution states
- visualising exceptions
- identifying failed workflows
- estimating automation ROI
- improving operational efficiency

---

## Dashboard Analytics Architecture

The dashboard continuously monitors:

```text
Bot Runs
   │
   ▼
Task Metrics
   │
   ▼
KPI Calculations
   │
   ▼
Chart.js Visualisation
   │
   ▼
Operational Dashboard
```

Key analytics generated include:

- task throughput
- hourly execution trends
- average success rate
- workflow reliability
- automation productivity
- exception frequency
- time saved estimation

---

## Workflow Monitoring System

The dashboard tracks multiple simulated enterprise workflows:

| Workflow | Purpose |
|---|---|
| Web Scraper | Extracts product and pricing information |
| Form Filler | Automates repetitive online submissions |
| Report Generator | Creates automated PDF reports |
| Email Bot | Sends automated notification emails |
| Invoice Parser | OCR-based invoice processing workflow |
| DB Sync | Synchronises records between databases |

Each workflow maintains:

- execution count
- success count
- runtime duration
- operational status
- exception rate

---

## Workflow Status Types

The monitoring system supports multiple workflow states:

| Status | Meaning |
|---|---|
| Running | Bot currently executing |
| Success | Workflow completed successfully |
| Failed | Workflow exception detected |
| Idle | Bot waiting for next trigger |

The dashboard visualises each state using:

- colour indicators
- status badges
- live updates
- performance metrics

---

## KPI Monitoring System

The dashboard calculates operational KPIs dynamically.

### Tasks Completed

```text
Total Executed Tasks
```

Measures:

- automation productivity
- overall workload
- system utilisation

---

### Success Rate

```text
successful_runs / total_runs × 100
```

Used to determine:

- bot reliability
- automation stability
- workflow quality

---

### Time Saved

```text
(manual_time − bot_time) × runs
```

Represents:

- business value
- operational efficiency
- labour reduction

---

### Exceptions

```text
total_runs − successful_runs
```

Tracks:

- failed processes
- runtime issues
- automation instability

---

## Real-Time Event Logging

The dashboard contains a simulated streaming event log similar to:

- Robocorp Control Room
- Splunk
- Elastic Stack
- Grafana logs

Example log events:

```text
12:34:05  Web Scraper     Scraped 48 listings successfully
12:34:07  Form Filler     Login successful
12:34:11  Invoice Parser  Warning: OCR confidence low
12:34:15  Email Bot       SMTP retry initiated
```

Supported log levels:

| Level | Purpose |
|---|---|
| INFO | General execution messages |
| OK | Successful workflow events |
| WARN | Recoverable issues |
| ERROR | Critical failures |

---

## Charts and Visual Analytics

### Line Chart — Hourly Throughput

Displays:

- completed tasks
- error count
- workload spikes
- operational patterns

Updated dynamically every refresh cycle.

---

### Donut Chart — Workflow Outcomes

Visualises:

- successful executions
- exceptions
- currently running tasks

Provides instant operational overview.

---

### Bar Chart — Workflow Reliability

Shows comparative success rates across workflows:

| Colour | Meaning |
|---|---|
| Green | ≥ 90% success |
| Amber | 75–89% success |
| Red | < 75% success |

---

## Robocorp Workflow Architecture

A standard Robocorp automation project follows:

```text
robot.yaml
conda.yaml
tasks/
└── tasks.py
```

### Example Robocorp Task

```python
from robocorp.tasks import task
from robocorp import browser, log

@task
def fill_web_form():

    log.info("Starting automation bot")

    browser.configure(headless=True)

    page = browser.page()

    page.goto("https://target-site.com")

    page.fill("#username", "operator")

    page.click("#submit")

    log.info("Workflow completed")
```

The dashboard simulates monitoring data generated from workflows like these.

---

## Data Flow Architecture

```text
[Software Bots]
        │
        ▼
[Robocorp Control Room]
        │
        ▼
[REST API / Webhooks]
        │
        ▼
[Dashboard JavaScript Layer]
        │
        ▼
[Chart.js Visualisation]
        │
        ▼
[Real-Time Monitoring UI]
```

---

## Production API Integration

In a real deployment, metrics would be fetched using APIs:

```javascript
async function fetchMetrics() {

    const res = await fetch(
        'https://cloud.robocorp.com/api/v1/runs',
        {
            headers: {
                'Authorization': `RC-WSKEY ${API_KEY}`
            }
        }
    );

    const data = await res.json();

    updateDashboard(data);
}
```

This project simulates live updates entirely in-browser.

---

## Front-End Architecture

The application is implemented as a fully self-contained dashboard using:

| Technology | Purpose |
|---|---|
| HTML5 | Dashboard structure |
| CSS3 | Enterprise UI styling |
| JavaScript | State management and logic |
| Chart.js | Data visualisation |
| Robocorp Concepts | Workflow simulation |

---

## Dashboard Components

### KPI Cards

Displays:

- total tasks
- success percentage
- exceptions
- active bots
- time savings

---

### Workflow Table

Shows:

- execution count
- success count
- average processing time
- runtime state

---

### Event Log

Streams:

- execution updates
- workflow events
- retry attempts
- warnings
- failures

---

### Refresh Engine

The dashboard dynamically generates:

- new execution counts
- updated success rates
- refreshed charts
- simulated workflow behaviour

to emulate production RPA environments.

---

## Industrial Relevance

This project reflects real enterprise automation scenarios used in:

- banking
- logistics
- healthcare
- manufacturing
- finance
- insurance
- customer support

where hundreds of bots may operate simultaneously.

The dashboard demonstrates practical concepts used by:

- RPA Developers
- Automation Engineers
- Process Analysts
- Operations Teams
- DevOps Monitoring Teams

---

## Educational Objectives

The project was designed to develop understanding of:

- RPA architecture
- bot orchestration
- workflow analytics
- monitoring systems
- automation KPIs
- operational dashboards
- enterprise UI design
- process reliability
- exception handling
- automation lifecycle management

---

## Learning Outcomes

This project helped develop practical skills in:

- Robocorp workflow concepts
- automation monitoring
- JavaScript dashboard engineering
- Chart.js visualisation
- KPI system design
- enterprise interface development
- operational analytics
- software architecture
- event-driven UI updates
- process automation analytics

---

## Future Improvements

Potential future extensions include:

- Real Robocorp API integration
- PostgreSQL logging backend
- Authentication system
- User roles and permissions
- Real bot deployment monitoring
- AI anomaly detection
- OCR pipeline monitoring
- Email notification system
- Grafana integration
- Prometheus metrics support
- Docker deployment
- Kubernetes orchestration monitoring
- Multi-user dashboards
- Cloud deployment
- Historical analytics database

---

### Academic Context

**Course**: Software Application Development / Robotic Process Automation  
**Programme**: BEng ICT & Robotics, HAMK University of Applied Sciences  

### Topics Covered

- Robotic Process Automation
- Robocorp Framework
- Python Automation
- Workflow Monitoring
- KPI Analytics
- Dashboard Engineering
- Process Automation
- Enterprise UI Systems
- Exception Monitoring
- Automation Lifecycle Design

### Certification

**Robocorp Python Automation Certificate**  
Issued: November 2024  
Credential ID: d38fbb43

---

## Performance Characteristics

| Component | Performance |
|---|---|
| Dashboard Refresh | < 50 ms |
| Chart Update | Real-time |
| Event Log Capacity | 60 live entries |
| Supported Workflows | Multiple concurrent bots |
| UI Rendering | Responsive |
| Simulation Interval | 3–4 seconds |

---

## Real Enterprise Mapping

| Dashboard Feature | Real Industry Equivalent |
|---|---|
| KPI Cards | Business Operations Metrics |
| Workflow Table | Bot Orchestration View |
| Event Logs | SIEM / Monitoring Logs |
| Throughput Graphs | Operational Analytics |
| Status Badges | Workflow State Monitoring |
| Error Metrics | Incident Detection |

---

## Conclusion

This project demonstrates how modern RPA systems are monitored and analysed in enterprise environments.

Beyond simple automation scripting, the project focuses on:

- workflow observability
- operational analytics
- automation reliability
- KPI-driven monitoring
- enterprise dashboard engineering

The system combines concepts from:

- software engineering
- enterprise automation
- operational analytics
- real-time monitoring
- UI/UX dashboard systems
- process automation engineering

while reflecting real industrial RPA monitoring workflows used in modern automation operations.

---

## 👤 Author

**Sazzad Ibna Mahfuz** — BEng ICT & Robotics, HAMK · Robocorp Certified  
[Portfolio](https://sazzadmahfuz.github.io) · [LinkedIn](https://www.linkedin.com/in/sazzad-mahfuz) · [GitHub](https://github.com/sazzadmahfuz)



<div align="center">

# ⭐ If you found this project interesting, consider starring the repository!

</div>
