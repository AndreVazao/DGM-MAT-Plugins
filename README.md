# DGM-MAT-Plugins — Optional Extensions

## Purpose
Optional, isolated extensions that add a clearly scoped capability to DGM-MAT through a documented interface.

## Allowed contents
Plugin manifests, adapters, capability declarations, configuration schemas, sandbox policies and plugin-specific tests.

## Boundaries
- The DGM-MAT core owns authority, policy, task state, memory and execution decisions.
- Plugins must not create a competing brain, bypass approvals or modify the core implicitly.
- Keep plugins disabled until explicitly enabled and validated.
- Never store secrets in source control; use the approved local credential mechanism.
- No automatic cloning/import of other repositories.

## Contract and validation
Every plugin documents its API/version compatibility, permissions, inputs/outputs, failure modes, dependencies and tests. Test isolation, permission denial, malformed input and safe shutdown before enabling it.
