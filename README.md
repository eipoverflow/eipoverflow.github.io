# eipoverflow.github.io

Terminal-themed site powered by Jekyll (GitHub Pages' built-in engine).
The look is defined **once**; you publish by writing markdown.

## Deploy (one time)

1. Copy everything in this `site/` folder into the **root** of your
   `eipoverflow/eipoverflow.github.io` repo (the files must be at the top
   level, not inside a `site/` subfolder).
2. **Delete `.nojekyll` if it exists** — Jekyll must run for posts to work.
3. In `_config.yml`, remove any old `theme:` or `remote_theme:` line you had
   from before (this site ships its own layouts).
4. Commit & push to the default branch (`main`).
5. Wait ~1 minute, open https://eipoverflow.github.io/ (hard-refresh).

GitHub builds the site automatically on every push. No Settings to change for
a `username.github.io` repo.

## Write a post (every time after that)

Add a file to `_posts/` named `YYYY-MM-DD-title.md`:

```markdown
---
title: "My new finding"
category: research      # research | exploits | teaching
tags: [heap, glibc]     # optional
description: "One line shown in the terminal listing."
---

Your content in plain markdown...
```

Commit it. It automatically appears when someone types `cat research.md`
in the shell, and gets its own page at `/research/2025/my-new-finding/`.
That's it — no HTML.

## Edit the theme / identity

- Colors and CRT effects: `assets/css/terminal.css`
- Prompt name + site title: `_config.yml` (`shell.user`, `shell.host`, `title`)
- ASCII banner, `whoami`, and `contact`: top of `index.html` (marked `EDIT ME`)
- Page chrome shared by every page: `_layouts/default.html`
- How a post page renders: `_layouts/post.html`

## Preview locally (optional)

```bash
gem install bundler jekyll
jekyll serve     # then open http://localhost:4000
```
