# 🚀 Step-by-Step Guide: Setting Up a New Live Report Repository

This guide explains how to initialize this `ainode-qa-reports` folder into a **separate GitHub Repository** and enable **GitHub Pages** for your live test reports portal.

---

## 📌 Step 1: Initialize Git in this Folder

Open your terminal or command prompt and run:

```bash
cd "c:\Users\Ankith R\OneDrive\Documents\Sttarkel_Testing\Automation\ainode-qa-reports"
git init
git branch -M main
git add .
git commit -m "Initial commit: QA Live Reports Portal"
```

---

## 🌐 Step 2: Create a New GitHub Repository

1. Go to GitHub: [https://github.com/new](https://github.com/new)
2. Name the repository: `ainode-qa-reports` (or any custom name like `ainode-test-reports`).
3. Set Visibility: **Public** (required for free GitHub Pages hosting) or **Private** (if using GitHub Enterprise).
4. Do **NOT** initialize with README or `.gitignore` (we already have them here).
5. Click **Create repository**.

---

## 📤 Step 3: Link Local Folder & Push to GitHub

Copy your new repository's URL from GitHub and run:

```bash
# Replace <YOUR_GITHUB_USERNAME> with your actual GitHub username
git remote add origin https://github.com/<YOUR_GITHUB_USERNAME>/ainode-qa-reports.git
git push -u origin main
```

---

## ⚙️ Step 4: Enable GitHub Pages for Live URL

1. Open your repository on GitHub: `https://github.com/<YOUR_GITHUB_USERNAME>/ainode-qa-reports`
2. Go to **Settings** → **Pages** (on the left sidebar).
3. Under **Build and deployment**:
   - **Source**: Select `Deploy from a branch`
   - **Branch**: Select `main` (or `gh-pages` if publishing to gh-pages)
   - **Folder**: Select `/ (root)`
4. Click **Save**.

🎉 **Your Live Report URL is now LIVE!**
- **Main Portal URL**: `https://<YOUR_GITHUB_USERNAME>.github.io/ainode-qa-reports/`
- **Staging Dashboard URL**: `https://<YOUR_GITHUB_USERNAME>.github.io/ainode-qa-reports/playwright/`
- **Production Dashboard URL**: `https://<YOUR_GITHUB_USERNAME>.github.io/ainode-qa-reports/playwright-prod/`

---

## 🔗 Step 5: Link `Ainode_GUI` GitHub Workflows to this New Repo

To make `Ainode_GUI` automatically push test dashboards and failed testcase videos to your new repo:

1. Open `.github/workflows/playwright.yml` in `Ainode_GUI`:
   Change:
   ```yaml
         external_repository: prajwalcg99/qa-reports
   ```
   To:
   ```yaml
         external_repository: <YOUR_GITHUB_USERNAME>/ainode-qa-reports
   ```

2. Open `.github/workflows/playwright-prod.yml` in `Ainode_GUI`:
   Change:
   ```yaml
         external_repository: prajwalcg99/qa-reports
   ```
   To:
   ```yaml
         external_repository: <YOUR_GITHUB_USERNAME>/ainode-qa-reports
   ```

3. Ensure `GH_PAT` (GitHub Personal Access Token) in `Ainode_GUI` repo secrets (**Settings** → **Secrets and variables** → **Actions**) has `repo` permissions to write to `<YOUR_GITHUB_USERNAME>/ainode-qa-reports`.
