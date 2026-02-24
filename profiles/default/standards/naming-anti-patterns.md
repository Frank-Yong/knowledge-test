---
id: standards/naming-anti-patterns
title: Naming Anti-Patterns (That We Promise Not to Repeat)
tags: [standards, naming]
owner: platform-team
last_reviewed: 2026-02-24
---

# Naming Anti-Patterns (That We Promise Not to Repeat)

## File names
- `final.md`, `final-final.md`, `final-final-2.md`
- `misc.md`, `stuff.md`, `temp.md`

Better:
- Use kebab-case and describe the concept: `incident-response.md`, `service-map.md`

## IDs
- Don’t use IDs that depend on a team’s internal slang
- Prefer stable, path-like IDs: `workflows/incident-response`
