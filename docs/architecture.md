# Architecture

## Separation of responsibilities

The intended design separates research intent, agent reasoning, execution
authority, and evidence:

| Boundary | Responsibility | Explicitly not responsible for |
| --- | --- | --- |
| Control tower | Compile goals into contracts and evaluate evidence | Direct GPU allocation |
| OpenClaw gateway | Expose a narrow local-agent interface | General machine access |
| Local LLM operator | Propose bounded campaign actions | Infrastructure mutation |
| Slurm adapter | Translate approved contracts into scheduler requests | Choosing undeclared substitutions |
| Training harness | Execute one declared program contract | Fleet-wide policy |
| W&B adapter | Read and reconcile structured run telemetry | Acting as execution authority |
| ChatGPT repair boundary | Propose a repair from a sanitized bundle | Editing or restarting live jobs |

## Intended evidence flow

1. Research intent becomes a versioned experiment contract.
2. Read-only discovery produces a time-bounded capability snapshot.
3. Admission binds the contract to an exact eligible resource shape.
4. Slurm produces scheduler-owned job and allocation state.
5. The training harness emits structured results and checkpoint metadata.
6. Telemetry is reconciled into a report without becoming scheduler truth.
7. Failures become redacted repair cases. Accepted repairs create successors.

Every transition should be deterministic, auditable, and safe to reject.
