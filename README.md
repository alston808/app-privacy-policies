# App Privacy Policies & Terms of Service

A collection of privacy policies, terms of service, end-user license agreements,
and other legal documents for apps published by **Alston Albarado**.

## 🌐 Live Site

**Root index (lists all apps):**
https://alston808.github.io/app-privacy-policies/

**BeatVibrator app index:**
https://alston808.github.io/app-privacy-policies/beatvibrator/

**BeatVibrator privacy policy:**
https://alston808.github.io/app-privacy-policies/beatvibrator/privacy

**BeatVibrator terms of service:**
https://alston808.github.io/app-privacy-policies/beatvibrator/terms

**BeatVibrator EULA:**
https://alston808.github.io/app-privacy-policies/beatvibrator/eula

## 📋 Overview

This repository is a **GitHub Pages** project built with **[Jekyll](https://jekyllrb.com)**
(the static site generator natively supported by GitHub Pages). It renders
Markdown files into clean, readable HTML privacy policies, terms, and other
legal documents — organized **per app**.

## 📁 Project Structure

```
app-privacy-policies/
├── _config.yml                 # Jekyll configuration (theme, markdown, etc.)
├── index.md                    # Root index — placeholder listing all apps
├── README.md                   # This file
├── 404.md                      # Custom 404 page
├── _layouts/
│   ├── app-index.html          # Layout for per-app index pages
│   └── document.html           # Layout for legal documents (privacy, terms, eula)
├── apps/
│   ├── .templates/             # Templates for adding new apps
│   │   ├── index.md
│   │   ├── privacy.md
│   │   ├── terms.md
│   │   └── eula.md
│   └── beatvibrator/           # The first app
│       ├── index.md            # → /beatvibrator/
│       ├── privacy.md          # → /beatvibrator/privacy
│       ├── terms.md            # → /beatvibrator/terms
│       └── eula.md             # → /beatvibrator/eula
└── .gitignore
```

## 📝 How to Add a New App

### Step 1 — Copy the template directory

```bash
cp -r apps/.templates apps/NEWAPP_NAME
```

Replace `NEWAPP_NAME` with the lowercase app name (e.g., `mygame`).

### Step 2 — Edit each file

Replace the placeholders in each file:

| Placeholder | Replace with |
|-------------|-------------|
| `APP_NAME` | lowercase app name (e.g., `mygame`) |
| `App Name` | human-readable name (e.g., `My Game`) |
| `APP_DESCRIPTION` | short description |
| `APP_VERSION` | app version string |

Each template file has a `permalink` that determines the URL:
- `apps/<app_name>/index.md` → `https://alston808.github.io/<app_name>/`
- `apps/<app_name>/privacy.md` → `https://alston808.github.io/<app_name>/privacy`
- `apps/<app_name>/terms.md` → `https://alston808.github.io/<app_name>/terms`
- `apps/<app_name>/eula.md` → `https://alston808.github.io/<app_name>/eula`

### Step 3 — Add to the root index

Edit `index.md` and add a new app card in the `app-grid` div:

```html
<div class="app-card">
  <h3>Your New App</h3>
  <p>Short description.</p>
  <a href="{{ site.baseurl }}/your-new-app/" class="app-link">View documents →</a>
</div>
```

### Step 4 — Commit and push

```bash
git add -A
git commit -m "docs: add legal documents for YourNewApp"
git push
```

The site will auto-deploy via GitHub Pages within a few seconds.

## 📄 Document Front Matter

Each legal document (`.md` file) uses YAML front matter. Here are the required fields:

```yaml
---
title: "AppName — Privacy Policy"       # Page title (browser tab)
app: appname                             # Lowercase ID (used in URL and back-link)
app_display: AppName                     # Human-readable name
doc_type: Privacy Policy                 # "Privacy Policy", "Terms of Service", "EULA"
effective_date: 2026-10-03              # When the document took effect (YYYY-MM-DD)
last_updated: 2026-10-03                # Last modification (YYYY-MM-DD)
version: v1.0                           # Optional version string
layout: document                         # Must be "document"
permalink: /appname/privacy              # Explicit URL path
---
```

## 🎨 Customization

### Root index page

Edit `index.md` to:
- Add/remove app cards in the `.app-grid` div
- Update the site title and description in `_config.yml`
- Change the contact email in the layouts

### Theme

The site uses the [Minima](https://github.com/jekyll/minima) theme (Jekyll's
default). Custom styles are inlined in the layouts for reliability.

## 🚀 Deployment

This site auto-deploys to GitHub Pages on every push to `main`:

1. Go to **Settings → Pages** in the GitHub repo.
2. Set **Source** to `Deploy from a branch` → `main` → `/ (root)`.
3. Save. GitHub Pages will build and publish automatically.

## 📄 License

The content of these legal documents is © Alston Albarado.
The site template and structure are provided as-is for reuse.

## 📧 Contact

**Alston Albarado**  
Email: alston.albarado@gmail.com
