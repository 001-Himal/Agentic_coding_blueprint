# dependencies.md (architecture)

- Dependency direction: UI → application/service → domain ← infrastructure.
- Never invert real dependency flow for convenience.
- Shared logic lives in shared modules.
