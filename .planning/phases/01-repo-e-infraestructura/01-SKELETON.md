# Walking Skeleton: Phase 1 — Repo e Infraestructura

## What This Phase Proves

A commit pushed to `ollerenac/clase_modelo` on the `main` branch is automatically
served as a live public web page at `https://ollerenac.github.io/clase_modelo`.

That single end-to-end path — **local file → GitHub repo → GitHub Pages → browser** —
is the skeleton. Once it is proven, Phase 2 can add all content with confidence that
every push will be visible immediately.

## Architectural Decisions (locked for all future phases)

| Decision | Choice | Rationale |
|----------|--------|-----------|
| Hosting | GitHub Pages (main branch root) | Zero infrastructure cost; satisfies SITE-03 |
| Markup | Pure HTML (`index.html` in repo root) | No Jekyll, no build step; satisfies SITE-02 |
| Styling | Inline `<style>` block in `index.html` | Single-file delivery; no separate CSS pipeline |
| JavaScript | None required | Static reference page; satisfies project constraint |
| Language | Spanish | Class is delivered in Spanish; satisfies project constraint |
| Branch | `main` | GitHub Pages default; Pages source = root of main |
| Repo visibility | Public | GitHub Pages free tier requires public repo |

## Skeleton Deliverable

A live page at `https://ollerenac.github.io/clase_modelo` that renders:

```
Clase Modelo: EternalBlue / MS17-010
[minimal placeholder — content added in Phase 2]
```

The page does not need to contain course content. It only needs to:
1. Return HTTP 200 (no 404)
2. Display the title "Clase Modelo: EternalBlue / MS17-010"
3. Be served from `index.html` at the repo root

## What Is NOT Part of the Skeleton

- Technical content (EternalBlue explanation, lab steps, MITRE table) → Phase 2
- Visual styling beyond bare legibility → Phase 2
- Code blocks, section structure, timing notes → Phase 2

## Directory Layout (established here, extended in Phase 2)

```
ollerenac/clase_modelo/        ← repo root = GitHub Pages source
└── index.html                 ← single deliverable for Phase 1
```

Phase 2 adds no new files — it only populates `index.html` with full content.
