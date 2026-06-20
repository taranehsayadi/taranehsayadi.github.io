# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this is

A personal academic website for Taraneh Sayadi (Professor at CNAM), served via **GitHub Pages**. It is a static [Jekyll](https://jekyllrb.com/) site using the remote `jekyll-theme-cayman` theme (configured in `_config.yml`). There is no local build tooling, Gemfile, or test suite — GitHub builds and deploys automatically on push to `master`.

## Local preview (optional)

GitHub renders the site on push. To preview locally you need a Ruby/Jekyll install with the github-pages gem:

```bash
gem install github-pages
jekyll serve   # serves at http://localhost:4000
```

Most edits are content (Markdown) and can be verified by inspecting the Markdown directly rather than building.

## Structure

- `index.md` — the homepage. It is the table of contents linking to every section. When adding a new teaching course, research topic, or opening, add its link here.
- Each top-level directory is a **section** with its own `index.md` (e.g. `PHD/`, `MU5MEF41/`, `Papers/`, `CV/`, `AIFM/`, `OFM/`, `CFD/`, `UQ/`, `STAGE/`, `POSTDOC/`, `DDMD/`, `MU4MEF01/`). Course/topic directories also hold their supporting assets (PDFs, notebooks, notes).
- `assets/` — shared images (`profile_photo.jpg`) and `assets/css/custom.css` for site-wide custom styling.
- Pages start with Jekyll front matter (`---\nlayout: default\n---`). The homepage links `assets/css/custom.css` and defines an inline `custom-header` block.

## Conventions

- Section pages link to each other and to files using **relative paths** (e.g. `MU5MEF41/index.md`, `PHD/FdP_2026-IFPen.pdf`). Keep links relative so they resolve both locally and on the published `taranehsayadi.github.io` site.
- Adding content = adding a Markdown file and/or PDF inside the relevant section directory, then linking to it from that section's `index.md` (and from the root `index.md` if it's a new top-level section).
- `.DS_Store` and `.ipynb_checkpoints/` are gitignored.
