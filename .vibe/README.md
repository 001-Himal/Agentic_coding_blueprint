# .vibe — The Control Center

Canonical source of truth for how AI agents work on this project + project tracking.

## Read order

1. `../README.md` (Blueprint README — read first)
2. `../AGENTS.md`
3. `.vibe/README.md` (this file)
4. `context/project.md` → `stack.md` → `architecture.md`
5. `config/protected.yaml` + `config/permissions.yaml`
6. `rules/core.md`
7. The matching skill in `skills/` for the task

## Map

```
.vibe/
├── config/          # project.yaml, commands.yaml, paths.yaml, permissions.yaml, protected.yaml
├── context/         # project, product, stack, architecture, structure, conventions, glossary, dependencies, health
├── rules/           # core, coding, architecture, frontend, backend, database, testing, security, performance, accessibility, git, documentation
├── product/         # vision, requirements, personas, user-flows, acceptance-criteria, design-system
├── specs/           # features, APIs, database, components, integrations
├── planning/        # roadmap, milestones, backlog, current, blockers, completed/
├── tasks/           # active, queued, blocked, completed
├── decisions/       # ADRs + index
├── bugs/            # open, investigating, resolved, wont-fix
├── research/        # technical, product, dependencies, decisions
├── reviews/         # code, architecture, security, performance, UX
├── releases/        # changelog, release-notes/, deployment-log, checklists/
├── sessions/        # current, history/
├── skills/          # planning, implementation, debugging, testing, code-review, security-review, migration, refactoring, ui-polish, performance, documentation, release
├── agents/          # researcher, planner, implementer, tester, reviewer, security-reviewer
├── prompts/         # feature, bug, research, refactor, review, release
├── checklists/      # feature, bug, migration, security, production, release
├── gates/           # pre-task, pre-implementation, post-implementation, pre-commit, pre-merge, pre-release
├── security/        # threat-model, trust-boundaries, sensitive-data, allowed-tools, allowed-network, dependency-policy, prompt-injection, agent-security
├── mcp/             # allowlist, tool-permissions, servers, security
├── evals/           # coding, planning, review, security, regression
├── architecture/    # principles, boundaries, invariants, forbidden-patterns, scalability, evolution, modularity, coupling, dependencies
├── dependencies/    # policy, approved, rejected, audit, decisions/
├── operations/      # health-checks, runbooks/, incident-log/
├── quality/         # anti-slop, code-quality, complexity, duplication, technical-debt, DEFINITION-OF-DONE
├── design/          # principles, design-system, visual-language, component-rules, layout, typography, color, spacing, motion, responsive, accessibility, anti-slop
├── verification/    # functional, regression, visual, performance, accessibility, security, production-readiness
├── epistemic/       # assumptions, unknowns, verified-facts, external-research
├── technology/      # approved-stack, dependency-policy, version-policy, upgrade-policy, prohibited-technologies
├── implementation/  # incremental-development, change-sizing, checkpoints, definition-of-done
├── documentation/   # map, ownership, freshness, drift
└── logs/            # changes, agent-actions, lessons
```

## Agent tracking duties (automatic)

- `planning/current.md` + `sessions/current.md` while working
- move tasks between `tasks/` folders
- `releases/changelog.md` every change
- `decisions/` every architectural call (ADR)
- `bugs/` lifecycle
- `logs/agent-actions.md` meaningful agent actions
- docs/ updated when behavior changes

## PASS definition

```
PASS = tests passed + expected behavior verified + scope respected
     + no suspicious changes + documentation updated
```

A passing test rate alone is NOT proof of correctness or security.
