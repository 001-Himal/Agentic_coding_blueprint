# Blueprint README

> **This whole agentic coding blueprint folder is the best practice for vibe coding softwares.**
> - Everything here is optimized for AI agents.
> - This document is for 1st time pasting to an AI coder and starting to plan the software **before** actual coding.
> - Any files/folders can be appended, removed, or updated while planning; afterwards, the necessary and confirmed ones get carried into the main codebase directory.
> - This folder sits inside/alongside the project as a blueprint sub-folder; `src/`, `public/`, `scripts/` etc. here are just for showcase.
> - After planning is complete and confirmed, copy what you need into the real codebase directory, do the actual work there, and remove this blueprint folder.

---

## 0. START HERE

1. **Read `README.md` (this file) first.**
2. Then `.vibe/README.md`.
3. Then `.vibe/context/project.md` and `.vibe/config/protected.yaml`.
4. Only then start planning. No code before the plan is approved.
5. Use `START-PROMPT.md` — the exact text to paste to your AI coder each session.

## 1. What This Is

Copy this folder into every new project. Three layers:

| Layer | Purpose |
|---|---|
| `.vibe/` | AI's brain + project tracking |
| `docs/` | Human-readable documentation |
| `src/` | Actual product |

## 2. How To Use

1. Copy the blueprint into your new project root.
2. Fill in `.vibe/context/` (project, product, stack, architecture).
3. Prune what this project doesn't need; add/rename folders while planning if needed.
4. Write first spec (`.vibe/specs/features/`) + task IDs.
5. Paste this folder's path to the AI coder: "Read `README.md` first, then plan — no code yet."
6. After planning, carry the confirmed structure into the real codebase repo.

## 3. Tiers — don't create 150 empty files on day one

- 🟢 **Tier 1 (every project):** `AGENTS.md`, `.vibe/{context,rules,planning,specs,tasks,decisions,bugs,skills,checklists}`, `docs/`, `src/`, `tests/`
- 🟡 **Tier 2 (serious project):** add `reviews/`, `research/`, `releases/`, `security/`, `architecture/`, `dependencies/`, `operations/`, `agents/`, `quality/`, `design/`, `verification/`, `epistemic/`, `technology/`, `implementation/`, `documentation/`
- 🔴 **Tier 3 (production/autonomous):** add `gates/`, `mcp/`, `evals/`, audit logs, incident response

## 4. Lifecycle

```
IDEA → PRODUCT SPEC → RESEARCH → ARCHITECTURE → PLAN → HUMAN APPROVAL
     → IMPLEMENT → VERIFY (build/typecheck/lint/tests) → DIFF REVIEW
     → SECURITY REVIEW → DOCUMENTATION → COMMIT/PR → RELEASE → OBSERVABILITY
     → FEEDBACK → UPDATE KNOWLEDGE → NEXT ITERATION
```

## 5. Eight Pillars

CONTEXT (know the project) · PRODUCT (build the right thing) · ARCHITECTURE (keep it modular) · IMPLEMENTATION (small, minimal code) · DESIGN (avoid generic AI aesthetics) · VERIFICATION (prove it works) · SECURITY (control the agent) · KNOWLEDGE (document and learn)

## 6. The Anti-Slop Principle

> Don't optimize for producing more code. Optimize for the smallest amount of correct, understandable, maintainable software that solves the actual problem.

Details: `.vibe/quality/anti-slop.md`, `.vibe/quality/DEFINITION-OF-DONE.md`, `.vibe/design/anti-slop.md`, `.vibe/implementation/incremental-development.md`.

## 7. ID Convention

`FEAT-001` · `BUG-001` · `TASK-001` · `ADR-001` · `REVIEW-001` · `RELEASE-001` — link everything to its FEAT ID.

## 8. Folder Map

```
project/
├── AGENTS.md            # tiny universal entry point
├── README.md            # this Blueprint README (read first)
├── CLAUDE.md / GEMINI.md / .windsurfrules / .cursor/rules/  # tool adapters
├── .github/             # workflows, instructions, CODEOWNERS
├── .vibe/               # agent brain + tracking (see .vibe/README.md)
├── docs/                # human docs
├── src/  tests/  scripts/  public/
├── .env.example  .gitignore  package.json
```

## 9. First Session Checklist

- [ ] Read this Blueprint README
- [ ] `.vibe/context/` filled in
- [ ] Tier chosen; irrelevant parts pruned
- [ ] First spec + task created with IDs
- [ ] Create PRD
- [ ] Create phasewise detailed roadmap
- [ ] Plan reviewed by a human before code
