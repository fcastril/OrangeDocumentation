# AGENTS.md — OrangeERP Documentation

## Project

Spanish-language end-user documentation for **OrangeERP** (cloud SaaS ERP). Pure Markdown + PNG images, no build system, no CI/CD.

## Language

All docs are in **Spanish**. Write content, headings, filenames, and alt text in Spanish.

## Navigation convention

Every page starts with a back-link and `---`:

```markdown
[Regresar al Inicio](../README.md)

---
```

Use relative paths for internal links (e.g., `../readme.md`, `../../Generales/maestros-tipoI.md`).

## Per-module structure

Each content module follows:

```
modulo/
  readme.md            ← Table of contents, back-link
  maestros/            ← Master data docs
  movimientos/         ← Transaction docs
  consultas-reportes/  ← Reports/queries
  procesos/            ← Processes
  recursos/
    img/               ← Screenshots (PNG, kebab-case, max 800 px, max 500 KB)
```

Stub modules (compras, gastos, cartera, tesoreria, talento-humano, calidad, documentacion) have only `readme.md` with a heading and back-link — preserve this pattern when adding content.

## Images

- Format: PNG, kebab-case filenames (e.g., `reporte-general.png`)
- Max width 800px, max size 500 KB
- Place in `recursos/img/<section>/` within the owning module

## Key cross-cutting references

- `Generales/maestros-tipoI.md` — simple coded masters
- `Generales/maestros-tipoII.md` — masters referencing a Type I
- `Generales/manejo-general-informacion.md` — standard index page, search, CRUD, export, pagination, favorites
- `Generales/documentacion.md` — OrangeLoading indicator system

## Releases

Release notes are consolidated in `releases/README.md`. The root README links to `releases/2026-03.md` but that file does not exist individually.
