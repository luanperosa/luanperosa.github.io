# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Overview

This is a static personal portfolio website for Luan Perosa Chitto, hosted on GitHub Pages. It is based on the "Massively" template by HTML5 UP. There is no build system or package manager — changes are made directly to HTML/CSS files and deployed by pushing to the `master` branch.

## Architecture

- **`index.html`** — Main portfolio page with bio, skills, and project experience entries
- **`contact-info.html`** — Contact information page
- **`elements.html`** — HTML5 UP elements reference (not linked in nav, kept for reference)
- **`assets/css/main.css`** — Compiled CSS (do not edit directly if using SASS)
- **`assets/sass/`** — SASS source files organized into `base/`, `components/`, `layout/`, and `libs/`
- **`assets/js/`** — jQuery and related plugins (minified third-party), plus `main.js` and `util.js`
- **`images/projects/`** — Project screenshot images referenced in `index.html`

## Previewing Locally

Since there's no build step, open `index.html` directly in a browser or serve with any static server:

```bash
python3 -m http.server 8000
```

## Styling

If modifying styles, edit the SASS source files in `assets/sass/` and compile to `assets/css/main.css`. If no SASS compiler is set up, `assets/css/main.css` can be edited directly.

## Adding Projects

Projects are listed in `index.html` as `<article>` elements inside `<section class="posts">` grids. The featured/most recent project sits outside the grid as `<article class="post featured">`. Each article includes:
- A `<span class="date">` for the time period
- A linked `<h2>` title
- An `<img>` referencing a file in `images/projects/`
- A `<ul>` of bullet-point contributions

New project images should be added to `images/projects/` and referenced from `index.html`.

## Deployment

Push to `master` — GitHub Pages serves the site automatically from the root of this branch.
