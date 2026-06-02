# Clase Modelo EternalBlue — Project Guide

## Project

Static GitHub Pages site for a 15-minute model class on EternalBlue / MS17-010.
Published at: `https://ollerenac.github.io/clase_modelo`
Repo: `ollerenac/clase_modelo`

## Stack

- Pure HTML + CSS (no frameworks, no build step)
- GitHub Pages serving `index.html` from `main` branch root
- No JavaScript required (optional syntax highlighting only)

## Content Source

The technical content comes from:
`/home/researcher/Teaching/inictel/clase_modelo/../../untels/ollerenacastro.github.io/_posts/2026-05-31-tema03.md`
Section: `## Kill Chain 3: EternalBlue / MS17-010`

Do NOT invent or extend technical content — extract from source only.

## Workflow

This project uses GSD (Get Shit Done) workflow.

- Planning docs in `.planning/`
- Mode: YOLO (auto-approve)
- Granularity: Coarse (2 phases)
- Config: `.planning/config.json`

## Phase Status

- Phase 1: Repo e Infraestructura → See `.planning/ROADMAP.md`
- Phase 2: Contenido y Publicación → See `.planning/ROADMAP.md`

## Key Constraints

- HTML/CSS static only — no Jekyll, no npm, no build pipeline
- Content in Spanish
- Site must load at the GitHub Pages URL (not just locally)
- `index.html` must be in repo root
