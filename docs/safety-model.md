# Safety model

## Protected assets

- Credentials and private infrastructure identity
- GPU availability and unrelated workloads
- Experiment source, parameters, checkpoints, and results
- Scheduler, storage, network, and service configuration
- The evidence used to decide whether a run is safe to admit

## Trust boundaries

Agent reasoning is advisory. Deterministic code should validate contracts,
enforce budgets, bind exact identities, and reject stale or incomplete evidence.
Slurm remains authoritative for GPU allocations and job state.

Cloud-assisted repair should receive only the minimum redacted case material
needed to reason about a failure. It should return a candidate change for
isolated validation, never an instruction that directly mutates production.

## Failure behavior

The supervisor should stop or remain idle when requirements are unknown,
identity is ambiguous, telemetry is inconsistent, a budget is exhausted, or a
repair cannot be qualified. Unattended progress is less important than a clear,
recoverable boundary.
