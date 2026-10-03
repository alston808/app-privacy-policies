# Template for new app landing pages
#
# To add a new app:
#   1. Copy this file to apps/NEWAPP_NAME/index.md
#   2. Update all front matter values (app, app_display, links, features, etc.)
#   3. Add a card to the root index.md
#   4. Commit and push
#
# URL will be: https://alston808.github.io/NEWAPP_NAME/
#
---
layout: app-page
title: "App Name — Legal Documents"
description: "Short description of your app."
permalink: /APP_NAME/

# App configuration
app: APP_NAME
app_display: App Name
app_icon: appicon.png
app_description: A short description of what your app does.
app_price: Free
playstore_link: https://play.google.com/store/apps/details?id=your.app.id
appstore_link:

# Cover image (optional)
cover_image: headerimage.png

# Feature list (FontAwesome 6 icons from https://fontawesome.com/icons)
features:
  - title: Feature 1
    description: Describe your first feature.
    fontawesome_icon_name: star
  - title: Feature 2
    description: Describe your second feature.
    fontawesome_icon_name: magic
---
