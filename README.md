# 📊 AiNode QA — Live Test Reports Portal

This repository hosts the live **Test Execution Dashboards** and regression analytics for the **AiNode GUI Automation** suite.

Reports are automatically generated and deployed here by the `Ainode_GUI` GitHub Actions CI/CD workflows.

---

## 🌐 Live Report Links

| Environment | Report View | Link |
| :--- | :--- | :--- |
| **Portal Home** | Main Portal Index | [Open Portal Dashboard](./index.html) |
| **Staging (`gui_branch`)** | Service Test Dashboard & Failed Videos | [Open Staging Report](./playwright/) |
| **Staging (`gui_branch`)** | Raw JSON Results Data | [View Results JSON](./playwright/data/results.json) |
| **Production (`main`)** | Service Test Dashboard & Failed Videos | [Open Production Report](./playwright-prod/) |
| **Production (`main`)** | Raw JSON Results Data | [View Results JSON](./playwright-prod/data/results.json) |

---

## ✨ Features

- **📦 Service-wise Breakdown**: Displays total passed, failed, skipped, and pass-rate % for all core services (`Classroom IDP`, `AI Interview`, `IDP Core`, `Career Advisor`, `Resume Builder`, `Schedule Assessment`, `Mentorship`, etc.).
- **📹 Failed Test Video Recordings**: Automatically embeds Playwright `.webm` failure videos directly in the dashboard for instant debugging.
- **⏱️ Execution Metrics**: Tracks execution duration per test case and service suite.
- **⚡ Automated Deployment**: Updated automatically on every GitHub Actions test run via `peaceiris/actions-gh-pages`.

---

## 🛠️ Repository Setup & Maintenance

Refer to [SETUP_LIVE_REPORT_REPO.md](./SETUP_LIVE_REPORT_REPO.md) for full instructions on configuring GitHub Pages and linking this repository with the `Ainode_GUI` automation project.
