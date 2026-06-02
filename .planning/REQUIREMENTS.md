# Requirements: Clase Modelo EternalBlue / MS17-010

**Defined:** 2026-06-02
**Core Value:** Un alumno puede seguir esta clase de 15 minutos y ejecutar EternalBlue paso a paso.

## v1 Requirements

### Infraestructura (sitio)

- [ ] **SITE-01**: Repositorio público `ollerenac/clase_modelo` creado en GitHub
- [ ] **SITE-02**: Archivo `index.html` en raíz del repo que carga como página web válida
- [ ] **SITE-03**: GitHub Pages habilitado; sitio accesible en `ollerenac.github.io/clase_modelo`

### Contenido

- [ ] **CONT-01**: Sección de fases del ataque — reconocimiento, acceso inicial; cómo el adversario identifica servicio/puerto objetivo antes de explotar
- [ ] **CONT-02**: Mecánica de Metasploit — cómo construye un mensaje exploit en el protocolo del servicio, lo encapsula en TCP, y cómo el receptor lo ejecuta al desencapsular
- [ ] **CONT-03**: Contexto de la vulnerabilidad — qué es EternalBlue (CVE-2017-0143), SMBv1, por qué Metasploitable3 es vulnerable
- [ ] **CONT-04**: Lab Paso 1 — confirmación de vulnerabilidad con `nmap --script vuln -p 445 10.0.2.15`
- [ ] **CONT-05**: Lab Paso 2 — configuración del módulo Metasploit (`ms17_010_eternalblue`, RHOSTS, LHOST, payload, `run`)
- [ ] **CONT-06**: Lab Paso 3 — post-explotación con Meterpreter (`getuid`, `sysinfo`, `hashdump`)
- [ ] **CONT-07**: Tabla de mapeo MITRE ATT&CK (T1210 Lateral Movement, T1068 Privilege Escalation)

### Presentación

- [ ] **UX-01**: Bloques de código en fuente monospace, visualmente distinguibles del texto
- [ ] **UX-02**: Estructura de secciones clara — fases del ataque → mecánica del exploit → lab (3 pasos) → MITRE
- [ ] **UX-03**: Indicación de duración total (15 min) y tiempo sugerido por sección visible en la página
- [ ] **UX-04**: Preguntas interactivas (≥2) integradas en la página para dinamizar la clase — una al final del concepto teórico, otra al final del lab

## v2 Requirements

*(Deferred — not in current scope)*

- Diagrama de red del entorno de laboratorio (Kali → Metasploitable3)
- Sección de mitigaciones y parches
- Links internos / tabla de contenidos navegable
- Soporte de pantalla oscura

## Out of Scope

| Feature | Reason |
|---------|--------|
| Backend / servidor | Sitio 100% estático, GitHub Pages no admite código de servidor |
| Jekyll o generadores de sitio | Complejidad innecesaria para una sola página |
| Contenido en inglés | Clase dictada en español |
| Responsividad móvil | Uso en laboratorio de escritorio |
| Video embebido | Fuera del scope de esta clase modelo |
| Ejercicios interactivos | Solo material de referencia y exposición |

## Traceability

| Requirement | Phase | Status |
|-------------|-------|--------|
| SITE-01 | Phase 1 | Pending |
| SITE-02 | Phase 1 | Pending |
| SITE-03 | Phase 1 | Pending |
| CONT-01 | Phase 2 | Pending |
| CONT-02 | Phase 2 | Pending |
| CONT-03 | Phase 2 | Pending |
| CONT-04 | Phase 2 | Pending |
| CONT-05 | Phase 2 | Pending |
| CONT-06 | Phase 2 | Pending |
| CONT-07 | Phase 2 | Pending |
| UX-01 | Phase 2 | Pending |
| UX-02 | Phase 2 | Pending |
| UX-03 | Phase 2 | Pending |
| UX-04 | Phase 2 | Pending |

**Coverage:**
- v1 requirements: 14 total
- Mapped to phases: 14
- Unmapped: 0 ✓

---
*Requirements defined: 2026-06-02*
*Last updated: 2026-06-02 after initialization*
