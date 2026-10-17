# Personal page

Axel Lárusson's personal website and CV (infrastructure engineer). It is a static, single-page site with no build step, no framework and no dependencies.

## Files

- `index.html` — the whole site: markup, a `<style>` block in the head, and a `<script>` block at the end of the body.
- `profile.jpg` — the profile photo, referenced by a relative path (`src="profile.jpg"`). Keep it next to `index.html`.

## Page structure

The sections, in order, are `#hero`, `#currently`, `#experience`, `#skills`, `#education`, `#interests` and `#contact`, followed by a `<footer>`. The fixed `<nav>` has the "AL." logo (links to `#hero`), the links Now (`#currently`), Experience, Skills, Education and Contact, and the theme toggle. `#interests` is a section but has no nav link at the moment. The scroll handler highlights the nav link for the section in view, so when you add, rename or remove a section, update the nav links to match.

## Styling conventions

- All colors are CSS custom properties on `:root`, overridden under `[data-theme="dark"]` (the `<html>` tag starts with `data-theme="light"`). Use the tokens (`--bg`, `--surface`, `--ink`, `--muted`, `--accent`, `--accent-light`, `--border`, `--card`, `--shadow`) rather than hard-coded colors, so dark mode keeps working.
- Fonts: `--serif` (DM Serif Display) for headings, `--sans` (DM Sans) for body text and `--mono` (DM Mono) for labels and metadata. They load from Google Fonts.
- The content column is `.container` (max-width 760px, 32px side padding, 20px on phones). Mobile breakpoints are `max-width: 600px` and `max-width: 640px`. Check layout at phone width after changes.
- The favicon is an inline ⚡ emoji SVG data URI in the head, so there is no favicon file.

## Script behavior

- Theme: the toggle (`#themeToggle`, with `#themeIcon` and `#themeLabel`) sets `data-theme` on `<html>` and saves it to `localStorage` under `theme`. With no saved value, the page follows `prefers-color-scheme`.
- Skill and language bars animate to their `data-width` value when their container (`.skills-grid`, `.lang-list`) scrolls into view (`.skill-fill`, `.lang-fill`).
- `.exp-item` and `.edu-item` fade in via IntersectionObserver by gaining a `.visible` class.
- The scroll handler loops over `section[id]` and `.nav-links a` to set the active nav link.
- A back-to-top button (`#backToTop`) appears after 400px of scrolling.

## Working on this site

- Keep it a single, dependency-free HTML file unless asked otherwise.
- Match the existing tone: concise, first-person and professional.
- Before large rewrites, make sure the work is committed so it can be restored with git.

## Git and deployment

- This folder is its own git repository (branch `main`), with `origin` at https://github.com/axelminn/axelminn.github.io (public, HTTPS, authenticated through `gh`).
- The site is deployed with GitHub Pages from `main` at the repo root, live at https://axelminn.github.io/. Every push to `main` redeploys it in about a minute. There is no build step or workflow file.
- Commit and push only when asked. Commit messages are short and imperative, and end with the Co-Authored-By line given in the session.
- Everything committed is public, including this file. Keep secrets and private details out of it.
- The `/push` skill (`.claude/skills/push/SKILL.md`) reviews this file against the changes, updates it if needed, then commits and pushes.
