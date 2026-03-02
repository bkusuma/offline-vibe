# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

A Jekyll-based documentation site for Mistral Vibe (a CLI coding agent), deployed to GitHub Pages at https://bkusuma.github.io.

## Build & Development Commands

```bash
bundle install                          # Install Ruby dependencies
bundle exec jekyll serve                # Local dev server with live reload
bundle exec jekyll build                # Build site to _site/
bundle exec jekyll build --incremental  # Faster incremental builds
bundle exec jekyll build --profile      # Build with profiling output
```

## Architecture

- **Static site generator**: Jekyll 4.3 with the minima theme
- **Markdown processor**: kramdown with GitHub Flavored Markdown
- **Syntax highlighting**: Rouge
- **Deployment**: GitHub Pages (auto-builds on push to `main`)

### Content Structure

Four main pages defined as root-level Markdown files:
- `index.md` — Homepage with feature overview and quick navigation
- `about.md` — Product overview, architecture, use cases, getting started
- `docs.md` — Technical documentation (components, usage patterns, advanced features)
- `performance.md` — MacBook Pro optimization guide

### Key Config Files

- `_config.yml` — Site metadata, theme, navigation links, build settings
- `Gemfile` — Ruby dependencies (only `jekyll ~> 4.3`)

### Jekyll Directories

- `_site/` — Generated build output (gitignored)
- `_includes/`, `_layouts/`, `_posts/` — Standard Jekyll dirs (currently empty, using theme defaults)
- `assets/css/`, `assets/js/` — Asset dirs (currently empty, using theme defaults)
