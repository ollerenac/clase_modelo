# Roadmap: Clase Modelo EternalBlue / MS17-010

**2 phases** | **12 requirements mapped** | All v1 requirements covered ✓

| # | Phase | Goal | Requirements | Success Criteria |
|---|-------|------|--------------|-----------------|
| 1 | Repo e Infraestructura | Repositorio GitHub creado, GitHub Pages activo, página base visible | SITE-01, SITE-02, SITE-03 | 3 |
| 2 | Contenido y Publicación | Todo el contenido técnico de EternalBlue incorporado, listo para presentar | CONT-01–07, UX-01–04 | 5 |

---

### Phase 1: Repo e Infraestructura

**Goal:** Repositorio `ollerenac/clase_modelo` creado en GitHub, GitHub Pages habilitado, y una página HTML base accesible públicamente en `ollerenac.github.io/clase_modelo`.

**Mode:** mvp

**Requirements:** SITE-01, SITE-02, SITE-03

**Plans:** 1 plan

Plans:
- [x] 01-01-PLAN.md — Create repo, push index.html skeleton, enable GitHub Pages, verify live URL (complete — user confirmed live URL 2026-06-02)

**Success Criteria:**
1. `https://ollerenac.github.io/clase_modelo` carga sin error 404 en un navegador
2. El repositorio `ollerenac/clase_modelo` aparece como público en `github.com/ollerenac`
3. El `index.html` incluye el título "Clase Modelo: EternalBlue / MS17-010" visible en la página

---

### Phase 2: Contenido y Publicación

**Goal:** La página publicada contiene todo el contenido de la clase — fases del ataque, mecánica de Metasploit, 3 pasos del lab, tabla MITRE ATT&CK, preguntas interactivas — estructurado para entrega oral de 15 minutos.

**Mode:** mvp

**Requirements:** CONT-01, CONT-02, CONT-03, CONT-04, CONT-05, CONT-06, CONT-07, UX-01, UX-02, UX-03, UX-04

**Plans:** 1 plan

Plans:
- [x] 02-01-PLAN.md — Rewrite index.html with full EternalBlue content, styles, MITRE table, interactive questions; commit and publish to GitHub Pages (complete — commit 5a4b30f, pushed to main 2026-06-02)

**Success Criteria:**
1. La página tiene 4 secciones: Contexto (CVE-2017-0143), Fases del Ataque (reconocimiento → acceso inicial + mecánica Metasploit), Lab (3 pasos), Mapeo MITRE
2. La explicación de cómo Metasploit encapsula el exploit en TCP y cómo el receptor lo ejecuta está presente
3. Todos los comandos de shell/Metasploit están en bloques monospace visualmente distinguibles
4. La indicación "15 minutos" y tiempos sugeridos por sección son visibles en la página
5. Al menos 2 preguntas interactivas están integradas en la página (post-concepto y post-lab)

---

## Phase Dependency

```
Phase 1 → Phase 2
```

Phase 2 requires Phase 1 complete (repo + Pages live before adding content).

---
*Roadmap created: 2026-06-02*
*Updated: 2026-06-02 — Phase 1 plan created (01-01-PLAN.md)*
*Updated: 2026-06-02 — Phase 2 plan created (02-01-PLAN.md)*
*Updated: 2026-06-02 — Phase 2 plan 02-01 complete — site live at https://ollerenac.github.io/clase_modelo*
