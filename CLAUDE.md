# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this is

A single-file static portfolio website for Milo McDonald (ballet dancer / musical theatre performer), built for college and conservatory applications. There is no build system, package manager, or framework — `index.html` contains all HTML, CSS (in a `<style>` block), and JS (in a `<script>` block) inline.

## Development

No install or build step. To preview changes, open `index.html` directly in a browser, or serve it locally:

```
python3 -m http.server 8000
```

There is no linter, formatter, or test suite configured for this project.

## Architecture

Everything lives in one file: `index.html`.

- **CSS custom properties** (`:root` in the `<style>` block) define the color palette (`--cream`, `--charcoal`, `--blush`, `--gold`, etc.) and are reused throughout — change the theme by editing these variables rather than individual rules.
- **Sections** are laid out in reading order and match the nav anchors: `#about`, `#ballet`, `#musical-theatre`, `#training`, `#gallery`, `#contact`. The `#ballet` section is the primary/featured section (dark charcoal background, distinct styling) since ballet is the subject's main discipline.
- **`.placeholder` elements** mark spots awaiting real content (photos, video embeds) — they render as a dashed-border striped box with bracketed instructional text (e.g. `[ Add full-length ballet photo here ]`). When replacing one with a real image, keep the same class name (e.g. `hero-photo`, `about-photo`) since layout/aspect-ratio CSS is keyed off those classes.
- **Repeatable content blocks** use a template pattern meant to be duplicated: `.timeline-item` (training/intensives entries), `.rep-list li` (repertoire roles), `.comp-list li` (competition results). Duplicate the existing block and edit its contents rather than inventing new markup.
- **Responsive behavior** is handled by a single `@media (max-width:860px)` block near the end of the `<style>` section, which collapses grid layouts to one column and switches the nav to a slide-in mobile menu (toggled via the small inline `<script>` at the bottom).

## Content editing

`CUSTOMIZE-GUIDE.md` is the authoritative walkthrough for filling in placeholder content (name, bio, photos, videos, resume link, etc.) — consult it before making structural changes so edits stay consistent with the intended fill-in points. Bracketed text like `[ Add photo here ]` or `[ Role ]` marks a placeholder to be replaced with real content, not a literal value to preserve.
