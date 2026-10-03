# App Privacy Policies & Legal Documents

A multi-app landing page site for privacy policies, terms of service, and EULAs
for mobile apps published by **Alston Albarado** — built with Jekyll on GitHub Pages,
adapted from the [automatic-app-landing-page](https://github.com/emilbaehr/automatic-app-landing-page)
template.

**Live site:** https://alston808.github.io/

## 📱 URL Structure

| Page | URL |
|------|-----|
| Root index | `https://alston808.github.io/` |
| App index | `https://alston808.github.io/beatvibrator/` |
| Privacy policy | `https://alston808.github.io/beatvibrator/privacy` |
| Terms of service | `https://alston808.github.io/beatvibrator/terms` |
| EULA | `https://alston808.github.io/beatvibrator/eula` |

## 📁 Project Structure

```
.
├── _config.yml                    # Jekyll config
├── index.md                       # Root index — placeholder listing all apps
├── 404.md                         # Custom 404 page
├── main.scss                      # SCSS entry point (imports _sass/)
├── _sass/
│   ├── base.scss                  # Core styles (typography, layout, components)
│   ├── layout.scss                # Grid/layout styles
│   └── github-markdown.scss       # Markdown body styling
├── _layouts/
│   ├── default.html               # Base HTML wrapper
│   ├── app-page.html              # App landing page layout
│   ├── page.html                  # Legal document layout (privacy/terms/eula)
│   └── root-index.html            # Root index placeholder layout
├── _includes/
│   ├── head.html                  # <head> with meta tags, CSS, FontAwesome
│   ├── header.html                # Site header with navigation
│   ├── footer.html                # Footer with social links
│   ├── features.html              # Feature list rendering
│   └── appstoreimages.html        # Apple App Store image fetching (optional)
├── assets/
│   ├── css/main.scss              # Compiled stylesheet
│   └── img/                       # App icons, header images, buttons
└── apps/
    ├── .templates/                # Templates for new apps
    │   ├── index.md
    │   ├── privacy.md
    │   ├── terms.md
    │   └── eula.md
    └── beatvibrator/              # First app
        ├── index.md
        ├── privacy.md
        ├── terms.md
        └── eula.md
```

## 📝 How to Add a New App

### Step 1 — Copy the templates

```bash
cd apps/
cp -r .templates/newapp  # Replace "newapp" with your app's lowercase name
```

### Step 2 — Edit the app index page

Edit `apps/newapp/index.md` and update the front matter:

```yaml
app: newapp             # lowercase, no spaces (becomes URL path)
app_display: "My App"   # human-readable name
app_icon: appicon.png   # icon in assets/img/
app_description: "What your app does."
app_price: "Free"       # or "$2.99"
playstore_link: https://play.google.com/store/apps/details?id=your.app.id
features:
  - title: "Feature 1"
    description: "Description here."
    fontawesome_icon_name: "star"
```

### Step 3 — Edit the document templates

Update `apps/newapp/privacy.md`, `terms.md`, and `eula.md` — replace the
placeholder content with your actual legal text.

### Step 4 — Add to the root index

Edit `index.md` (which uses `layout: root-index`) and add a card for your new app:

```html
<div class="app-card">
  <h3>My App</h3>
  <p>Short description.</p>
  <a href="/my-app/" class="app-link">View documents →</a>
</div>
```

### Step 5 — Upload assets

Upload your app icon and header image to `assets/img/`.

### Step 6 — Commit and push

```bash
git add -A
git commit -m "feat: add My App legal documents"
git push
```

## 🎨 Customization

### Theme colors

All colors are configurable in `_sass/base.scss`:

| Variable | Default | Description |
|----------|---------|-------------|
| `$body-color` | `#ffffff` | Page background |
| `$accent-color` | `#1d63ea` | Links and accent elements |

### Header image

Replace `assets/img/headerimage.png` with your own cover image (recommended size: 1200×400px).

### App icon

Set `app_icon` in each app's `index.md` front matter to the filename in `assets/img/`.

## 🚀 Deployment

This is a **GitHub User Pages** site — it auto-deploys from the `main` branch of
the `alston808/alston808.github.io` repository. Changes go live within seconds
of pushing.

## 📄 License

The legal document content is © Alston Albarado.
The site template is based on [automatic-app-landing-page](https://github.com/emilbaehr/automatic-app-landing-page)
(licensed MIT).

## 📧 Contact

**Alston Albarado**  
Email: alston.albarado@gmail.com
