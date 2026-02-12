# NYC Category Theory Reading Club

Static website for the NYC Beginners-friendly Category Theory Reading Club, built with [Hugo](https://gohugo.io/) and deployed via GitHub Pages.

## Links

- **Meetup:** https://www.meetup.com/nyc-beginners-friendly-category-theory-reading-club-awodey/
- **Discord:** https://discord.gg/NWGdjJ6nJJ

## Local development

```sh
hugo server --buildDrafts
```

Then open http://localhost:1313/nyc-category-theory-website/

## Adding a new meeting

Create a new markdown file in `content/meetings/`:

```sh
hugo new content meetings/meeting-N.md
```

Then edit the file with front matter:

```yaml
---
title: "Meeting N: Topic"
date: 2025-03-01
summary: "Brief description of what was covered."
---

Your meeting notes here in markdown.
```

## Deploying

Push to `main` — the GitHub Actions workflow in `.github/workflows/hugo.yml` builds and deploys to GitHub Pages automatically.

## Project structure

```
content/          # Markdown content
  _index.md       # Home page content
  meetings/       # Meeting log entries
layouts/          # HTML templates
  index.html      # Home page template
  _default/       # Default templates (list, single, baseof)
  partials/       # Reusable template fragments
static/           # Static assets (CSS, images)
hugo.toml         # Site configuration
```
