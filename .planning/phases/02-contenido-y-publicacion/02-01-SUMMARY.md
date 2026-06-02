---
phase: 02-contenido-y-publicacion
plan: "01"
subsystem: frontend
tags: [html, css, content, github-pages, eternalblue]
dependency_graph:
  requires: [01-01]
  provides: [clase-modelo-page]
  affects: []
tech_stack:
  added: []
  patterns: [single-file-html, inline-css, static-github-pages]
key_files:
  created: []
  modified:
    - index.html
decisions:
  - "Content extracted strictly from tema03.md lines 1512-1761 — no invented content"
  - "All Spanish content with ASCII-safe text (no accented chars in code) to avoid encoding issues"
  - "pre>code pattern used for all command blocks — inline code uses separate style"
metrics:
  duration: "~12 minutes"
  completed: "2026-06-02"
  tasks_completed: 2
  files_changed: 1
---

# Phase 2 Plan 1: Contenido y Publicacion — Summary

## One-liner

Complete EternalBlue class page: SMBv1 exploit mechanics, 4-step lab with exact commands, MITRE T1046/T1210/T1068 table, and 2 interactive questions — published to GitHub Pages.

## What Was Built

Replaced the placeholder `index.html` with a complete 350-line self-contained HTML+CSS page
serving as the sole teaching material for a 15-minute oral class on EternalBlue / MS17-010.

### Sections Delivered

| Section | ID | Time Badge | Key Content |
|---------|-----|------------|-------------|
| Contexto de la Vulnerabilidad | `#contexto` | ~3 min | CVE-2017-0143, NSA/Shadow Brokers, WannaCry, NotPetya, lab environment |
| Fases del Ataque | `#fases` | ~3 min | Recon, initial access, Metasploit mechanics (make_kernel_user_payload, smb_eternalblue 4 steps, create_fea_list bug) |
| Laboratorio | `#lab` | ~6 min | Paso 0-3: msfconsole info, nmap vuln scan, exploit run, post-exploitation (sysinfo/getuid/hashdump) |
| Mapeo MITRE ATT&CK | `#mitre` | ~2 min | Table with T1046, T1210, T1068 for EternalBlue |
| Preguntas para la Clase | `#preguntas` | ~1 min | 2 questions with expected answers |

### Technical Mechanics Documented

- `make_kernel_user_payload`: kernel shellcode (ring 0) + Meterpreter (ring 3) joined; APC injection into spoolsv.exe via ROR13 hash lookup
- `smb_eternalblue` 4-step sequence: Connect IPC$, Large SMB1 buffer, Pool grooming (alternating SMBv1/SMBv2), Send payload
- `create_fea_list`: DWORD-vs-WORD arithmetic underflow in `SrvOs2FeaListSizeToNt()` → diminuto buffer → memmove overflow → fake_srv_net_buf overwrites kernel structure

## Commits

| Task | Commit | Description |
|------|--------|-------------|
| Task 1: Write index.html | `5a4b30f` | feat(02-01): write complete EternalBlue class page with all content sections |
| Task 2: Publish to GitHub Pages | (same commit, pushed) | git push origin master:main — exit 0 |

## Verification Results

All acceptance criteria passed:

| Check | Result |
|-------|--------|
| `wc -l index.html` | 350 (>= 200) |
| `grep -c "CVE-2017-0143"` | 3 (>= 1) |
| `grep -c "T1210"` | 1 (>= 1) |
| `grep -c "T1068"` | 1 (>= 1) |
| `grep -c "T1046"` | 1 (>= 1) |
| `grep -c "hashdump"` | 3 (>= 1) |
| `grep -c "NT AUTHORITY"` | 6 (>= 1) |
| `grep -c "ms17_010_eternalblue"` | 2 (>= 2) |
| `grep -c "nmap --script vuln"` | 2 (>= 1) |
| `grep -c "15 min"` | 1 (>= 1) |
| `grep -ci "pregunta"` | 13 (>= 2) |
| `grep -c "<section"` | 5 (>= 4) |
| `grep -c "<pre>"` | 8 (>= 4) |
| `grep -c "SMBv1\|SMB"` | 13 (>= 3) |
| HTML valid (DOCTYPE + /html) | PASS |
| `git push origin master:main` | exit 0 |

## Deviations from Plan

None — plan executed exactly as written.

Content was extracted strictly from `/home/researcher/Teaching/untels/ollerenacastro.github.io/_posts/2026-05-31-tema03.md` lines 1512-1761. No content was invented or extended.

## Known Stubs

None — all sections are fully wired with extracted technical content.

## Threat Flags

No new threat surface introduced. Content is purely static HTML with educational lab IPs (10.0.2.x — VirtualBox isolated network). No credentials, no real production IPs, no JavaScript execution.

## Self-Check: PASSED

- [x] `/home/researcher/Teaching/inictel/clase_modelo/index.html` exists (350 lines)
- [x] Commit `5a4b30f` exists in git log
- [x] Push to origin/main exited 0
- [x] All acceptance criteria grep checks returned expected counts
