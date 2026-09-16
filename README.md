# 📊 AiNode QA — Unified Live Test Reports Portal

This repository serves as the central live **QA Test Reports Hub** for both **API Automation (Pytest + Allure)** and **Web GUI Automation (Playwright)**.

---

## 🌐 Live Dashboard Links

| Report Category | Environment | Dashboard View | Live Link |
| :--- | :--- | :--- | :--- |
| **Portal Hub** | Multi-Env | Central QA Portal Index | [Open Portal Home](https://ankithr564.github.io/Ainode-QA-Reports/) |
| **Backend API** | **Production** | Allure P0 Smoke Report | [Open Prod API Allure](https://ankithr564.github.io/Ainode-QA-Reports/pytest-prod/) |
| **Backend API** | **Staging** | Allure Full Test Suite | [Open Staging API Allure](https://ankithr564.github.io/Ainode-QA-Reports/pytest/) |
| **Web GUI** | **Production** | Playwright Web Report & Videos | [Open Prod GUI Dashboard](https://ankithr564.github.io/Ainode-QA-Reports/playwright-prod/) |
| **Web GUI** | **Staging** | Playwright Web Report & Videos | [Open Staging GUI Dashboard](https://ankithr564.github.io/Ainode-QA-Reports/playwright/) |

---

## ✨ Features

- **🚀 Backend API Analytics**: Interactive Allure reports generated directly from `test_prod.py` (97 P0 critical smoke tests across Auth, Billing, Courses, Interview, Jobs, Mentorship, Quiz, and Resumes).
- **📹 GUI Failure Recordings**: Embedded Playwright `.webm` failure videos for web automation issues.
- **⚡ Auto-Publishing**: Automatically published and updated via GitHub Actions after every pipeline execution.
