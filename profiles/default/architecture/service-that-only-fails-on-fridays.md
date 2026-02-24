---
id: architecture/service-that-only-fails-on-fridays
title: The Service That Only Fails on Fridays
tags: [architecture, reliability]
owner: platform-team
last_reviewed: 2026-02-24
---

# The Service That Only Fails on Fridays

This is a pattern catalog entry: a funny label for a real class of problems.

## Usual causes
- Weekly cron/reporting spikes
- Certificate or token rotation schedules
- Cache expiration aligned to a weekly TTL
- Batch jobs that collide with peak traffic

## What to document
- The weekly schedule (jobs, rotations, deploy windows)
- Known load inflection points and thresholds
- Runbook links and dashboards

## Suggested mitigations
- Stagger scheduled tasks
- Add capacity ahead of predictable spikes
- Add synthetic checks before the “Friday window”
