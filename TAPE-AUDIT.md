# TAPE-AUDIT — hexa-farm

**Date:** 2026-05-14 · **Lens:** `.tape` (typed events).

## A. Audit-class ledgers

`state/markers/*.marker` — uniform dancinlab markers (5 checks × few timestamps), **CARGO**. No `.jsonl`, no `.hook-audit.jsonl`, no `verify/*_audit*` Python scripts.

## B. Identity surface

`hexa.toml` **has identity** (matched on `identity|agent_id|swarm_id` regex) — distinct vs the substrate-no-identity sibling default. Substrate-level identity (project-level brand identity) likely, not per-agent.

## C. Domain.md files

**Zero** UPPERCASE.md in repo root. Convention not adopted at root; per-verb dirs (`agriculture/`, `apiculture/`, `aquaculture/`, `baking/`, `coffee/`, `ecology/`, `entomology/`, `fermentation/`, `food-science/`, `horticulture/`, etc., ~20 verbs) carry their own internal docs.

## D. Per-run / per-event history

None — verify-marker touch only, no harvest/yield/run logs.

## E. Promotion candidates

- **`.tape` future fit**: per-season/per-harvest event streams (planting · yield · pest · weather event) are the obvious natural `@H` consumer per-verb. Today: pre-impl.
- **n6 atoms**: pollination-network, hive-fitness, fermentation-cohort cells — but again real-limits-first.
- **hxc / n12**: none.

## Verdict

**LIGHT** — ~20-verb agricultural-substrate roll-up (largest verb count in this audit set), all currently pre-implementation catalog. Marker-cargo only. Multi-verb structure means per-verb `<DOMAIN>.tape` would be a natural future surface, one per verb-dir.
