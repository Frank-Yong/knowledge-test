---
id: workflows/rollback-ritual
title: Rollback Ritual (Also Known as Being Responsible)
tags: [workflow, incident, release]
owner: platform-team
last_reviewed: 2026-02-24
---

# Rollback Ritual (Also Known as Being Responsible)

## Goal
Restore service safely, quickly, and with minimal guesswork.

## Checklist
1. Declare intent: “Rolling back build/version X to Y”
2. Freeze new changes (pause deploy pipeline if applicable)
3. Execute rollback using the documented mechanism
4. Validate:
   - Key endpoints/health checks
   - Error rate and latency
   - Background jobs/queues if relevant
5. Communicate outcome and next update time

## Aftercare
- Capture timestamps and observations while they are fresh
- Create follow-ups for root cause and prevention
