# Test strategy

The future implementation should begin with deterministic contract tests and a
fully simulated scheduler. Live checks should be separate and explicitly label
the exact source, runtime, infrastructure, and GPU shape they qualify.

Priority scenarios include stale inventory, occupied GPUs, budget exhaustion,
checkpoint incompatibility, telemetry disagreement, agent timeout, failed
repair, safe stop, and morning-report reconstruction.
