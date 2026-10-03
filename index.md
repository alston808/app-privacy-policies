---
layout: home
title: App Legal Documents
permalink: /
---

<style>
  .app-grid {
    display: flex;
    flex-direction: column;
    gap: 1rem;
    margin: 1.5rem 0;
  }
  @media (min-width: 700px) {
    .app-grid {
      flex-direction: row;
      flex-wrap: wrap;
    }
  }
  .app-card {
    flex: 1 1 300px;
    padding: 1.5rem;
    background: #f6f8fa;
    border: 1px solid #d0d7de;
    border-radius: 8px;
  }
  .app-card h3 {
    margin-top: 0;
    color: #24292f;
  }
  .app-link {
    display: inline-block;
    margin-top: 0.5rem;
    color: #4688f0;
    text-decoration: none;
    font-weight: 600;
  }
  .app-link:hover {
    text-decoration: underline;
  }
</style>

# App Legal Documents

A collection of privacy policies, terms of service, end-user license
agreements, and other legal documents for apps published by
**Alston Albarado**.

---

## 📱 Apps

Click on an app below to view its legal documents.

<div class="app-grid">

{% comment %}
  Add new apps here — each entry links to the app's index page.
  The app's index page then links to its privacy policy, terms, and EULA.
{% endcomment %}

  <div class="app-card">
    <h3>BeatVibrator</h3>
    <p>A mobile app for haptic rhythm feedback.</p>
    <a href="{{ site.baseurl }}/beatvibrator/" class="app-link">View documents →</a>
  </div>

</div>

---

## 📄 Document Types

| Type | Description |
|------|-------------|
| **Privacy Policy** | How we collect, use, and protect your personal data. |
| **Terms of Service** | Rules and guidelines for using the app. |
| **EULA** | End-user license agreement for software use. |

---

## 📧 Contact

Questions about these policies? Contact:
**alston.albarado@gmail.com**

---

*This site is hosted on [GitHub Pages](https://pages.github.com) and built with
[Jekyll](https://jekyllrb.com).*
