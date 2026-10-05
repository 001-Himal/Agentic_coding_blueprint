# incremental-development.md

# Incremental Engineering Principle

Build software in small, independently verifiable increments.

- Never generate a large implementation just because the model can.
- Prefer small changes, clear responsibilities, short feedback loops, frequent verification, reversible changes, understandable diffs, incremental commits.
- When a task is too large to understand or verify comfortably, stop and split it.

Loop: UNDERSTAND → PLAN SMALL STEP → IMPLEMENT → RUN CHECKS → REVIEW DIFF → UPDATE DOCS → CHECKPOINT → NEXT STEP

Never: PLAN → WRITE EVERYTHING → HOPE
