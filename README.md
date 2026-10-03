# App Privacy Policies & Terms of Service

A collection of privacy policies, terms of service, end-user license agreements,
and other legal documents for apps published by **Alston Albarado**.

## 🌐 Live Site

[https://alston808.github.io/app-privacy-policies/](https://alston808.github.io/app-privacy-policies/)

## 📋 Overview

This repository is a **GitHub Pages** project built with **[Jekyll](https://jekyllrb.com)**
(the static site generator natively supported by GitHub Pages). It renders
Markdown files into clean, readable HTML privacy policies, terms, and other
legal documents — organized per app.

## 📁 Project Structure

```
app-privacy-policies/
├── _config.yml                 # Jekyll configuration (collections, theme, etc.)
├── index.md                    # Landing page listing all apps & documents
├── README.md                   # This file
├── .gitignore
├── 404.md                    # Custom 404 page
├── _layouts/
│   └── document.html           # Layout for individual legal documents
├── _privacy/                   # Privacy policies (one file per app)
│   ├── beatvibrator.md      # → /privacy/beatvibrator/
│   └── .template.md         # Template for new privacy policies
├── _terms/                     # Terms of Service (one file per app)
│   └── .template.md         # Template for new ToS documents
└── _eula/                      # End-user license agreements
    └── .template.md         # Template for new EULAs
```

## 📝 How to Add a New App

Want to add a privacy policy for a new app? Just create a Markdown file in the
appropriate collection directory. No code changes needed.

### Example: Adding a Privacy Policy for "MyNewApp"

1. Create the file:

   ```bash
   touch _privacy/mynewapp.md
   ```

2. Add YAML front matter and content:

   ```markdown
   ---
   title: "MyNewApp — Privacy Policy"
   app: mynewapp
   app_display: MyNewApp
   doc_type: Privacy Policy
   effective_date: 2026-10-03
   layout: document
   ---

   **Privacy Policy**

   This privacy policy applies to the MyNewApp ...

   ### Information Collection

   ...
   ```

3. Commit and push:

   ```bash
   git add .privacy/
   git commit -m "docs: add privacy policy for MyNewApp"
   git push
   ```

The document will automatically appear at:
`https://alston808.github.io/app-privacy-policies/privacy/mynewapp/`

### Naming Convention

| Document Type   | File Location            | URL Pattern                         |
|-----------------|--------------------------|-------------------------------------|
| Privacy Policy  | `_privacy/<app>.md`      | `/privacy/<app>/`                   |
| Terms of Svc.   | `_terms/<app>.md`        | `/terms/<app>/`                     |
| EULA            | `_eula/<app>.md`         | `/eula/<app>/`                      |

### Front Matter Fields

| Field            | Required | Description                              |
|------------------|----------|------------------------------------------|
| `title`          | ✅       | Page title (shown in browser tab)        |
| `app`            | ✅       | Lowercase app identifier (used in URL)   |
| `app_display`    | ✅       | Human-readable app name                  |
| `doc_type`       | ✅       | "Privacy Policy", "Terms of Service", etc.|
| `effective_date` | ✅       | When the policy took effect (`YYYY-MM-DD`) |
| `last_updated`   | ⚪       | Last modification date (defaults to effective) |
| `version`        | ⚪       | Version string (e.g. `v1.0`)             |
| `layout`         | ✅       | Must be `document`                       |

## 🎨 Customization

### Changing the Theme

The site uses the [Minima](https://github.com/jekyll/minima) theme (Jekyll's
default). To change it, edit `_config.yml`:

```yaml
theme: minima
```

Replace `minima` with another [Jekyll theme](https://jekyllrb.com/docs/themes/).

### Custom Styling

Add CSS overrides to `_sass/custom.scss` and it will be picked up automatically
by the Minima theme.

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
