# Clase Modelo: EternalBlue / MS17-010

## What This Is

Una clase modelo de 15 minutos sobre la vulnerabilidad EternalBlue (CVE-2017-0143), publicada como sitio web en GitHub Pages en el repositorio `ollerenac/clase_modelo`. La clase resume el Kill Chain 3 del laboratorio de ciberseguridad del curso, cubriendo detección y explotación de SMBv1 vulnerable usando Kali Linux y Metasploitable3.

## Core Value

Un alumno que no asistió al laboratorio completo puede seguir esta clase de 15 minutos y ejecutar el ataque EternalBlue paso a paso en su entorno VirtualBox.

## Requirements

### Validated

(None yet — ship to validate)

### Active

- [ ] Sitio web estático publicado en GitHub Pages accesible en `ollerenac.github.io/clase_modelo`
- [ ] Repositorio público en GitHub: `ollerenac/clase_modelo`
- [ ] Sección de contexto histórico: qué es EternalBlue, NSA/Shadow Brokers, WannaCry/NotPetya
- [ ] Explicación técnica: vulnerabilidad en SMBv1, FEA buffer overflow, CVE-2017-0143
- [ ] Lab paso a paso: detección con `nmap --script vuln -p 445`
- [ ] Lab paso a paso: explotación con Metasploit `ms17_010_eternalblue` + payload Meterpreter
- [ ] Comandos post-explotación con Meterpreter (`getuid`, `hashdump`, `sysinfo`)
- [ ] Tabla de mapeo MITRE ATT&CK (T1210, T1068)
- [ ] Diseño legible en navegador de escritorio con bloques de código resaltados
- [ ] Contenido estructurado para entrega oral de 15 minutos

### Out of Scope

- Video grabado de la clase — el sitio es soporte escrito, no reemplaza grabación
- Ejercicios interactivos o quizzes — solo lectura/referencia
- Soporte móvil responsivo — uso en laboratorio de escritorio únicamente
- Backend o servidor — sitio completamente estático
- Contenido en inglés — clase en español

## Context

- **Fuente de contenido**: Sección `## Kill Chain 3: EternalBlue / MS17-010` del post `2026-05-31-tema03.md` en `ollerenacastro.github.io`. Todo el contenido técnico (comandos, salidas de terminal, explicaciones) ya existe ahí.
- **Entorno de laboratorio**: Kali Linux (10.0.2.9) como atacante, Metasploitable3/Windows Server 2008 R2 (10.0.2.15) como víctima, VirtualBox NAT Network.
- **Cuenta GitHub**: username `ollerenac`, repositorio a crear: `clase_modelo`.
- **Audiencia**: Alumnos del curso INICTEL de ciberseguridad que ya conocen el contexto general del laboratorio.
- **Restricción de tiempo**: 15 minutos de exposición oral — el contenido debe poder presentarse en ese tiempo sin apresurar.

## Constraints

- **Stack**: HTML/CSS estático puro — no Jekyll, no frameworks — para máxima simplicidad de despliegue en GitHub Pages
- **Contenido**: Extraído directamente de `tema03.md` (sección Kill Chain 3) — no inventar ni extender el contenido técnico
- **GitHub Pages**: Servir desde `main` branch, archivo `index.html` en raíz
- **Tiempo de entrega**: Clase modelo lista para presentar — no es un proyecto de largo aliento

## Key Decisions

| Decision | Rationale | Outcome |
|----------|-----------|---------|
| HTML estático en vez de Jekyll | Sin pipeline de build, deploy inmediato, sin dependencias | — Pending |
| Contenido extraído de tema03.md | Reutilizar material ya validado en clase, consistencia pedagógica | — Pending |
| GitHub Pages desde rama `main` | Configuración más simple, rama por defecto | — Pending |

## Evolution

This document evolves at phase transitions and milestone boundaries.

**After each phase transition** (via `/gsd-transition`):
1. Requirements invalidated? → Move to Out of Scope with reason
2. Requirements validated? → Move to Validated with phase reference
3. New requirements emerged? → Add to Active
4. Decisions to log? → Add to Key Decisions
5. "What This Is" still accurate? → Update if drifted

**After each milestone** (via `/gsd:complete-milestone`):
1. Full review of all sections
2. Core Value check — still the right priority?
3. Audit Out of Scope — reasons still valid?
4. Update Context with current state

---
*Last updated: 2026-06-02 after initialization*
