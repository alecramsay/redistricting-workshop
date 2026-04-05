# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a GitHub Pages site (Jekyll) hosted from the `docs/` folder of the `main` branch. The project is building an interactive redistricting game/puzzle — see `docs/specs/` for design specifications.

## Site Structure

- `docs/` — all GitHub Pages content; Jekyll builds from here
- `docs/_config.yml` — Jekyll site configuration (`title: Redistricting Workshop`)
- `docs/specs/` — design specifications written before implementation
- `docs/index.md` — site home page

The site uses the default Jekyll theme with `layout: default` front matter.

## Development Conventions

Design specs are written in `docs/specs/` before any code is written. Ask before taking on new dependencies or doing more than explicitly requested.

The `.gitignore` covers Jekyll (`_site/`, `.jekyll-cache/`), Node/TypeScript (`node_modules/`, `dist/`), and common OS/editor artifacts.
