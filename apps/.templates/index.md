# Template for new apps
#
# To add a new app, copy this directory and rename:
#   cp -r apps/.templates apps/NEWAPP_NAME
#
# Then edit each file, replacing placeholders:
#   APP_NAME       → lowercase app name (e.g. "mygame")
#   App Name       → human-readable name (e.g. "My Game")
#   APP_DESCRIPTION → short description
#   APP_VERSION    → app version string
#
# Naming convention for files:
#   apps/<app_name>/index.md   → app index page   (URL: /<app_name>/)
#   apps/<app_name>/privacy.md → privacy policy   (URL: /<app_name>/privacy)
#   apps/<app_name>/terms.md   → terms of service (URL: /<app_name>/terms)
#   apps/<app_name>/eula.md    → EULA             (URL: /<app_name>/eula)
#
# After creating the files:
#   git add -A && git commit -m "feat: add APP_NAME docs" && git push
#
# Then add a link card to the root index.md.
# ---------------------------------------------------------------------------

---
layout: app-index
title: "App Name — Legal Documents"
app: APP_NAME
app_display: App Name
description: APP_DESCRIPTION
version: APP_VERSION
permalink: /APP_NAME/
---

This page lists the legal documents for the **App Name** app.
