# Snapshot boundary

This repository starts from a clean public history and contains an architecture
skeleton only. It is not a deployment bundle.

Deliberately excluded:

- Prior source history and private development metadata
- Runtime state, caches, virtual environments, build output, and model files
- Credentials, environment files, certificates, keys, tokens, and SSH material
- Hostnames, addresses, hardware identities, storage layouts, and fleet routes
- Slurm, service-manager, container, network, and machine deployment manifests
- Raw logs, operator traces, incident bundles, W&B run IDs, and run results
- Admission receipts and any claim of operational readiness
- Executable implementation source

Before every release, review the complete tree, run secret and license scans,
verify third-party attribution, and confirm that every example is synthetic.
