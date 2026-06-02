# Project State: Clase Modelo EternalBlue / MS17-010

## Project Reference

See: .planning/PROJECT.md (updated 2026-06-02)

**Core value:** Un alumno puede seguir esta clase de 15 minutos y ejecutar EternalBlue paso a paso.
**Current focus:** Phase 1 — Repo e Infraestructura

## Current Status

- **Phase:** 1 of 2
- **Plan:** 01 of 01 — awaiting human verification (Task 2 checkpoint)
- **Status:** Checkpoint — human verify live URL
- **Last action:** Task 1 complete — repo created, index.html pushed, GitHub Pages enabled (2026-06-02)
- **Stopped at:** Task 2 checkpoint:human-verify — confirm https://ollerenac.github.io/clase_modelo loads in browser

## Phase Progress

| Phase | Name | Status | Notes |
|-------|------|--------|-------|
| 1 | Repo e Infraestructura | 🔄 In Progress | Plan 01 at checkpoint |
| 2 | Contenido y Publicación | 🔲 Not started | Depends on Phase 1 |

## Decisions Log

- GitHub Pages API: use `--input -` pipe for JSON body (not `--field` which mis-quotes objects as strings)
- Push strategy: `git push -u origin master:main` to publish local master as remote main without renaming local branch

## Blockers

*(none)*

---
*State initialized: 2026-06-02*
