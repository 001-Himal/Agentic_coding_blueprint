# principles.md — modularity

- Each module: one clear responsibility
- Intentional public interfaces; internals stay private
- No circular dependencies
- High-level modules must not depend on implementation details
- Shared code actually shared
- No abstractions before real need
- Composition over inheritance where appropriate
- Business logic independent from UI
- Infrastructure isolated from domain logic

## Key rule
Do not create a new abstraction until you can explain what concrete duplication or boundary it solves.
