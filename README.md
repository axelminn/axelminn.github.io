<div align="center">

# Axel Lárusson

**Infrastructure engineer** · OpenShift · Kubernetes · Linux · Automation

[![Live site](https://img.shields.io/badge/live-axelminn.github.io-2ea44f?style=for-the-badge&logo=github)](https://axelminn.github.io/)
[![Hosted on GitHub Pages](https://img.shields.io/badge/hosted%20on-GitHub%20Pages-222?style=for-the-badge&logo=githubpages)](https://pages.github.com/)
![No build step](https://img.shields.io/badge/build-none-blue?style=for-the-badge)
![Dependencies](https://img.shields.io/badge/dependencies-0-brightgreen?style=for-the-badge)

[About](#-about) · [Features](#-features) · [Sections](#-sections) · [Tech](#-tech) · [Structure](#-project-structure) · [Run locally](#-run-locally) · [Deployment](#-deployment)

</div>

---

## 👋 About

My personal website and CV: a single, fast, static page covering what I'm working on now, my experience, skills, education, interests and how to reach me.

> **🔗 [axelminn.github.io](https://axelminn.github.io/)**

---

## ✨ Features

<table>
  <tr>
    <td width="50%" valign="top">
      <h4>🌗 Light and dark theme</h4>
      Follows your system setting, with a toggle that remembers your choice.
    </td>
    <td width="50%" valign="top">
      <h4>📱 Responsive</h4>
      Designed for desktop and phone.
    </td>
  </tr>
  <tr>
    <td valign="top">
      <h4>🎞️ Subtle motion</h4>
      Animated skill and language bars, and sections that fade in as you scroll.
    </td>
    <td valign="top">
      <h4>🧭 Scroll-aware navigation</h4>
      Highlights the section in view, plus a back-to-top button.
    </td>
  </tr>
  <tr>
    <td colspan="2" valign="top">
      <h4>🪶 Featherweight</h4>
      One HTML file with no framework, no build and no dependencies.
    </td>
  </tr>
</table>

---

## 🗂️ Sections

| | Section | What's in it |
|:-:|---|---|
| 🏠 | **Hero** | Introduction |
| ⏱️ | **Now** | What I'm currently focused on |
| 💼 | **Experience** | Career timeline with the tools used in each role |
| 🛠️ | **Skills** | Skill bars and languages |
| 🎓 | **Education** | Degrees and studies |
| 🌱 | **Interests** | Interests and values |
| ✉️ | **Contact** | Ways to get in touch |

---

## 🧰 Tech

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![Google Fonts](https://img.shields.io/badge/Google%20Fonts-4285F4?style=flat-square&logo=googlefonts&logoColor=white)

Plain HTML, CSS and vanilla JavaScript in a single `index.html`. Colors are CSS custom properties, so theming is one override block.

| Role | Typeface |
|---|---|
| Headings | [DM Serif Display](https://fonts.google.com/specimen/DM+Serif+Display) |
| Body text | [DM Sans](https://fonts.google.com/specimen/DM+Sans) |
| Labels and metadata | [DM Mono](https://fonts.google.com/specimen/DM+Mono) |

---

## 📁 Project structure

```text
.
├── index.html    # the whole site: markup, styles and script
├── profile.jpg   # profile photo, referenced by relative path
├── CLAUDE.md     # notes for working on the site with Claude Code
└── README.md
```

---

## 🚀 Run locally

No install needed. Open `index.html` directly, or serve the folder:

```bash
python3 -m http.server 8000
```

Then visit <http://localhost:8000>.

---

## 🌍 Deployment

Hosted on **GitHub Pages** from the root of the `main` branch.

```text
git push  ──▶  GitHub Pages  ──▶  axelminn.github.io   (about a minute)
```

There is no build step or workflow file.

---

<div align="center">

Made with care in plain HTML · © Axel Lárusson

</div>
