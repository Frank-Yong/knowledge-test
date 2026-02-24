# Folder Structure and Tool Naming Standard

This standard is the contract that keeps tool names and descriptions stable and discoverable.

## 1) Knowledge Repo Structure (remote GitHub repo)

```text
knowledge-repo/
  README.md
  profiles/
    default/
      README.md
      architecture/
        README.md
        system-overview.md
        service-map.md
      standards/
        README.md
        coding-guidelines.md
        naming-conventions.md
      workflows/
        README.md
        release-process.md
        incident-response.md
      glossary/
        README.md
        terms.md
    platform/
      README.md
      ...
  _meta/
    schema-version.json
    aliases.json
```

## 2) README Contract (every folder)

Every folder-level `README.md` should include:

1. **Purpose** (1 paragraph)
2. **When to use** (bullets)
3. **Canonical documents** (ordered list with links)
4. **Do/Don’t** (short policy bullets)
5. **Tags** (`tags: ["architecture", "workflow"]` style line)

## 3) File Naming Rules

- Use kebab-case file names
- Prefix numbered workflow docs when order matters, e.g. `01-intake.md`
- Keep titles short and concrete
- One concept per file

## 4) Tool Naming Rules

Naming pattern:
- `knowledge_<verb>`

Allowed verbs (MVP):
- `bootstrap`
- `get`
- `search`
- `list`
- `refresh`
- `status`

Do not rename published tools without version bump.

## 5) Tool Description Style Guide

Descriptions must be:
- one sentence
- imperative and specific
- include scope and return shape hint

Examples:
- `knowledge_bootstrap`: "Return high-signal startup context from the configured knowledge profile."
- `knowledge_get`: "Return one canonical document or section by path/ID with source metadata."
- `knowledge_search`: "Search indexed knowledge chunks by keyword and optional filters."

## 6) Metadata Conventions

Document-level frontmatter (optional but recommended):

```yaml
id: architecture/system-overview
title: System Overview
tags: [architecture, overview]
owner: platform-team
last_reviewed: 2026-02-01
```

If frontmatter is absent, infer from path + heading.

## 7) Versioning

- Maintain `_meta/schema-version.json`
- Server checks compatibility at refresh time
- Incompatible schema triggers warning in `knowledge_status`
