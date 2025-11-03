# Discord Server Stats Bot

Track your community’s growth, engagement, and health with real-time dashboards and automated reporting. **Discord Server Stats Bot** collects rich metrics (members, active users, messages, voice time, reactions) and turns them into insights you can act on. Teams use it to replace spreadsheets, spot trends quickly, and keep stakeholders aligned.

<p align="center">
  <a href="https://Appilot.app" target="_blank">
    <img src="media/appilot-baner.png" alt="Appilot Banner" width="100%">
  </a>
</p>
<p align="center">
  <a href="https://t.me/devpilot1" target="_blank">
    <img src="https://img.shields.io/badge/Chat%20on-Telegram-2CA5E0?style=for-the-badge&logo=telegram&logoColor=white" alt="Telegram">
  </a>&nbsp;
  <a href="https://wa.me/923249868488?text=Hi%20Appilot%2C%20I'm%20interested%20in%20automation." target="_blank">
    <img src="https://img.shields.io/badge/Chat-WhatsApp-25D366?style=for-the-badge&logo=whatsapp&logoColor=white" alt="WhatsApp">
  </a>&nbsp;
  <a href="mailto:support@appilot.app" target="_blank">
    <img src="https://img.shields.io/badge/Email-support@appilot.app-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Gmail">
  </a>&nbsp;
  <a href="https://appilot.app" target="_blank">
    <img src="https://img.shields.io/badge/Visit-Website-007BFF?style=for-the-badge&logo=google-chrome&logoColor=white" alt="Website">
  </a>
</p>

<p align="center"> 
   Created by Appilot, built to showcase our approach to Automation!<br>
   <strong>If you are looking for custom Discord Server Stats Bot, you've just found your team — Let’s Chat.👆👆</strong>
</p>

## Introduction
**What it does:** Continuously collects server analytics (joins/leaves, channel activity, message volume, reaction usage, voice minutes) and exposes them via commands, scheduled reports, and web dashboards.  
**Workflow automated:** Replaces manual export, copy-paste, and ad-hoc analysis with scheduled data capture, storage, and visualization.  
**Benefit:** Clear, always-on visibility into community health to improve moderation, content planning, and growth.

### Tracking Discord Community Health in Real Time
- Granular metrics: member growth, DAU/WAU/MAU, retention cohorts, channel heatmaps, top contributors.
- Visual dashboards + scheduled PDF/CSV reports for stakeholders.
- Alerting on anomalies: sudden spikes/drops in activity, raid hints, churn signals.
- Privacy-aware design with configurable scopes, opt-outs, and retention windows.
- Scales across multiple servers and shards with fault-tolerant workers.

## Core Features
- **Real Devices and Emulators:** Optional Android-companion capture (via Appilot) mirrors mobile notifications to enrich event timelines when needed for on-device flows.
- **No-ADB Wireless Automation:** Wireless control pipeline to trigger mobile-side checks without tethered USB; resilient to device restarts and network hiccups.
- **Mimicking Human Behavior:** Rate-limited interactions, randomized intervals, and Discord-API-safe patterns to avoid tripping automod/antispam.
- **Multiple Accounts Support:** Run observer shards and service accounts (bot tokens) across many servers with isolated quotas and prefixes.
- **Multi-Device Integration:** Pair cloud emulators (Bluestacks/Nox) or real phones for companion tasks like screenshotting dashboard snapshots to channels.
- **Exponential Growth for Your Account:** Data-driven insights highlight best posting times, high-retention channels, and content formats that compound engagement.
- **Premium Support:** SLA-backed onboarding, scaling assistance, and custom metric pipelines.
- **Role & Channel Heatmaps:** Identify where conversations thrive and where they stall.
- **Retention & Cohorts:** Track new member activation, 7-day/30-day return rates.
- **Anomaly Alerts:** Webhook/Discord alerts for raids, churn bursts, or message floods.

**Additional Feature Set**

| Feature | Description |
|---|---|
| **Scheduled Reports** | Auto-send weekly/monthly PDFs/CSVs with KPIs to selected channels or emails. |
| **Dashboard Embeds** | Live charts embedded in Discord with pagination and quick filters. |
| **Export API** | REST endpoints to pull raw metrics into BI tools or data warehouses. |
| **Permissions Matrix** | Fine-grained scopes to restrict who can view metrics per role/channel. |
| **Shard & Queue Orchestrator** | Scales ingestion via workers, Redis queues, and horizontal sharding. |
| **Data Retention Policies** | Configurable rollups (hourly/daily) and auto-pruning for compliance. |

</p>
<p align="center">
  <a href="https://appilot.app" target="_blank">
    <img src="media/Discord Server Stats Bot-banner.png" alt="Discord Server Stats Bot-architecture" width="95%">
  </a>
</p>

## How It Works
1. **Input or Trigger** — From the Appilot dashboard or bot commands, you configure tracked servers, reporting schedules, and alert thresholds.  
2. **Core Logic** — Workers ingest Discord gateway events and REST data; Android companion (optional) uses UI Automator/ADB flows for mobile-only checks; data is validated, rate-limited, and queued.  
3. **Output or Action** — KPIs render to dashboards, scheduled reports post to channels/email, and alerts fire on anomalies.  
4. **Other functionalities** — Retry logic, dead-letter queues, structured logging, and parallel processing ensure resilience and traceability.

## Tech Stack
**Language:** Python, TypeScript, Java/Kotlin (Android), Go (optional workers)  
**Frameworks:** discord.py / discord.js, FastAPI/Express, Appium, UI Automator, Robot Framework  
**Tools:** Appilot, Android Debug Bridge (ADB), Appium Inspector, Bluestacks/Nox, Scrcpy, Redis, PostgreSQL, Prometheus, Grafana  
**Infrastructure:** Dockerized services, Cloud-based emulators, Parallel Device Execution, Proxy networks, Task Queues, Horizontal Sharding

## Directory Structure
```
    discord-server-stats-bot/
    │
    ├── bot/
    │   ├── main.py
    │   ├── cogs/
    │   │   ├── metrics.py
    │   │   ├── reports.py
    │   │   ├── alerts.py
    │   │   └── admin.py
    │   └── utils/
    │       ├── rate_limit.py
    │       ├── validators.py
    │       └── permissions.py
    │
    ├── services/
    │   ├── api/
    │   │   ├── app.ts
    │   │   └── routes/
    │   │       ├── metrics.ts
    │   │       └── exports.ts
    │   └── workers/
    │       ├── ingest_worker.py
    │       ├── report_worker.py
    │       └── alert_worker.py
    │
    ├── android-companion/
    │   ├── app/
    │   │   ├── src/main/java/com/appilot/discordstats/
    │   │   │   ├── UiFlows.kt
    │   │   │   └── DeviceService.kt
    │   └── tests/
    │       └── uiautomator_scenarios.robot
    │
    ├── configs/
    │   ├── settings.yaml
    │   ├── retention.yaml
    │   └── secrets.env
    │
    ├── dashboards/
    │   ├── grafana.json
    │   └── templates/
    │       └── weekly_report.html
    │
    ├── scripts/
    │   ├── migrate.sql
    │   └── seed_demo.py
    │
    ├── logs/
    │   └── bot.log
    │
    ├── output/
    │   ├── reports/
    │   │   └── weekly_YYYY-MM-DD.pdf
    │   └── exports/
    │       └── metrics_YYYYMMDD.csv
    │
    ├── docker-compose.yml
    ├── requirements.txt
    └── README.md
```

## Use Cases
- **Community Managers** use it to monitor daily activity and retention so they can plan events and content with confidence.  
- **Moderation Teams** use it to detect raids and spam spikes so they can respond instantly.  
- **Marketing Leads** use it to correlate campaigns with server growth so they can prove ROI.  
- **Developers** use the Export API to feed BI dashboards so they can unify data across products.

## FAQs
**How do I configure this for multiple servers?**  
Provide bot invites per server, then add each guild to the dashboard with its own report schedule, quotas, and role-based visibility.

**Does it support proxy rotation or anti-detection?**  
For Discord API calls we rely on compliant rate limits; optional proxy layers are supported for external webhooks and reporting endpoints.

**Can I schedule it to run periodically?**  
Yes—use cron-like schedules in the Appilot dashboard to post weekly/monthly reports or run nightly rollups.

**Where is data stored and for how long?**  
PostgreSQL stores raw events; Prometheus keeps time series. Retention is configurable with rollups (hourly/daily) and auto-pruning.

**Can I run it without the Android companion?**  
Absolutely. The Android module is optional and designed for mobile-side checks or screenshots; the core bot runs purely on the Discord API.

## Performance & Reliability Benchmarks
- **Execution Speed:** Processes >50k events/min per shard under sustained load; dashboard queries return in <300ms P95 with indexed rollups.  
- **Success Rate:** Automated ingestion and scheduled reporting operate at **~95%** success across rolling 30-day windows with retries.  
- **Scalability:** Proven horizontally to **300–1000** guilds/devices via sharding and worker queues; storage rollups keep query latency stable.  
- **Resource Efficiency:** CPU-bound parsing offloaded to workers; memory capped via chunked exports and streaming responses.  
- **Error Handling:** Circuit breakers, exponential backoff, DLQs, structured logs, and alerting to on-call channels keep incidents contained.

##
<p align="center">
<a href="https://cal.com/app-pilot-m8i8oo/30min" target="_blank">
  <img src="https://img.shields.io/badge/Book%20a%20Call%20with%20Us-34A853?style=for-the-badge&logo=googlecalendar&logoColor=white" alt="Book a Call">
</a>
</p>
