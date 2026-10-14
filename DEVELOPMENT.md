# PICHONIA LLC — Engineering & Operations Master Guide

**Last Updated:** October 11, 2026  
**Repository:** `PICHONIA/pichonia-website`  
**Current Phase:** Phase 1 — Pre-Formation & Digital Foundation  

---

## 📌 MASTER OPERATIONS & BUILD TRACKER

### PHASE 1: Pre-Formation & Digital Foundation (CURRENT)
- [x] Secure Domain: `pichonia.com`
- [x] Set up Company Email via Cloudflare (`contact@pichonia.com`)
- [x] Create Official PICHONIA GitHub Organization
- [x] Verify `pichonia.com` domain in GitHub Settings
- [x] Update Site Branding & HQ: Sheridan, Wyoming (`contact@pichonia.com`)
- [x] Re-establish Cloudflare Pages CI/CD pipeline under `PICHONIA` GitHub Org
- [x] Create Official LinkedIn Company Page (COMPLETED)
- [x] Set up Google Voice / Business Phone Routing (`+1 (307) 228-0774`)
- [ ] Prepare IP Assignment Record (reclaiming personal code/AI models)

### PHASE 2: State Formation & Privacy Shield (Target: Next)
- [x] Formation Documents & EIN Verified in Legal Vault
- [ ] Submit Northwest Registered Agent order ($142 - Wyoming LLC + Privacy Shield)
- [ ] File Wyoming Articles of Organization ($100 state fee included)
- [ ] Draft Internal LLC Operating Agreement (Wyoming Single-Member)

---

## 🛠️ LOCAL DEVELOPMENT WORKFLOW

### Prerequisites
- Node.js (v18 or higher)
- Git & GitHub CLI (`gh`)

### Commands
```bash
# Install dependencies
npm install

# Start local development server
npm run dev

# Build production bundle static output (/dist)
npm run build

# Preview production build locally
npm run preview
---

## 📜 INFRASTRUCTURE INCIDENT LOG

### Post-Mortem: Cloudflare-GitHub Integration Loop
* **Date:** October 11, 2026
* **Symptom:** Git pushes to `PICHONIA/pichonia-website` (`main` branch) were not triggering automated Cloudflare Pages builds.
* **Root Cause:** Re-hosting from personal user scope (`DerBesJC`) to GitHub Organization scope (`PICHONIA`) severed the OAuth token loop, causing an authorization lock state in the GitHub App permission interface.
* **Resolution Steps:**
  1. Unlinked legacy repository inside Cloudflare Pages Settings.
  2. Forced a permission refresh in GitHub by toggling repository selection to `Only select repositories` → `pichonia-website` and saving.
  3. Re-established Git connection under `PICHONIA/pichonia-website` with `npm run build` static output (`dist/`).
  4. Verified deployment `66e9e46` built cleanly and published live to production (`pichonia.com/about`).

---

## 🔒 LEGAL & OPERATIONS VAULT INDEX

* **Target Legal Name:** PICHONIA LLC
* **Target Jurisdiction:** Wyoming (Domestic LLC)
* **HQ Address:** Sheridan, Wyoming
* **Contact Email:** `contact@pichonia.com`
* **Technical Asset Inventory:**
  1. **Predictive AI System for Options Trading:** Proprietary algorithms, trained models, datasets.
  2. **Pichonia Logistics App:** Source code, UI designs, databases, documentation.

---

## 🚀 CACHE INVALIDATION & SEO PROTOCOL
- **Favicon Cache Busting:** All favicons and apple-touch-icons include version parameters (`?v=2`) in `src/layouts/Layout.astro` to bypass aggressive browser caching.
- **Social Previews (Open Graph / Twitter):** Configured in `<head>` to explicitly point to `https://pichonia.com/brand/pichonia_source.png` with `summary_large_image` cards.
