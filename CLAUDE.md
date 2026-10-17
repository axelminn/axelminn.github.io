# Personal page

Axel Lárusson's personal website and CV (infrastructure engineer). It is a static, single-page site with no build step, no framework and no dependencies.

## Files

- `index.html` — the whole site: markup, a `<style>` block in the head, and a `<script>` block at the end of the body.
- `profile.jpg` — the profile photo, referenced by a relative path (`src="profile.jpg"`). Keep it next to `index.html`.

## Running it

Open `index.html` in a browser, or serve the folder with `python3 -m http.server 8000` and visit http://localhost:8000.

## Page structure

The sections, in order, are `#hero`, `#currently`, `#experience`, `#skills`, `#education`, `#interests` and `#contact`. The fixed nav links point at these ids, and the scroll handler highlights the active one, so when you add, rename or remove a section, update the nav links to match.

## Styling conventions

- All colors are CSS custom properties on `:root`, overridden under `[data-theme="dark"]`. Use the tokens (`--bg`, `--surface`, `--ink`, `--muted`, `--accent`, `--accent-light`, `--border`, `--card`, `--shadow`) rather than hard-coded colors, so dark mode keeps working.
- Fonts: `--serif` (DM Serif Display) for headings, `--sans` (DM Sans) for body text and `--mono` (DM Mono) for labels and metadata. They load from Google Fonts.
- The content column is `.container` (max-width 760px). Mobile breakpoints are at 600px and 640px. Check layout at phone width after changes.

## Script behavior

- Theme: the toggle sets `data-theme` on `<html>` and saves it to `localStorage` under `theme`. With no saved value, the page follows `prefers-color-scheme`.
- Skill and language bars animate to their `data-width` value when scrolled into view (`.skill-fill`, `.lang-fill`).
- `.exp-item` and `.edu-item` fade in via IntersectionObserver by gaining a `.visible` class.
- A back-to-top button (`#backToTop`) appears after 400px of scrolling.

## Working on this site

- Keep it a single, dependency-free HTML file unless asked otherwise.
- Match the existing tone: concise, first-person and professional.
- This folder is not a git repository yet, so back up before large rewrites.
