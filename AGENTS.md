# Repository guidance for coding agents

## Purpose

This repository is a non-operational public design skeleton for an agentic ML
research supervisor. Preserve the distinction between intended architecture
and verified behavior.

## Working rules

- Keep Slurm as the sole conceptual authority for GPU allocation.
- Keep agent interfaces capability-limited. Do not add raw shell, SSH,
  filesystem, credential, arbitrary network, or scheduler access.
- Use generic examples only. Never add real hostnames, addresses, GPU UUIDs,
  account names, tokens, private paths, traces, run IDs, or infrastructure
  configuration.
- Do not claim deployment, live operation, self-healing, reproducibility, or
  benchmark results unless matching evidence is added and independently
  reviewed.
- Treat unknown requirements and stale evidence as blocked.
- Model repair as a tested successor candidate, not an in-place mutation of a
  live experiment.

## Status vocabulary

- `proposed`: designed but not implemented or tested.
- `local-tested`: passed deterministic local or simulated tests only.
- `shape-qualified`: passed on one exact source/runtime/hardware shape.
- `live-admitted`: explicitly promoted for that exact signed combination.

The current repository status is `proposed`.
