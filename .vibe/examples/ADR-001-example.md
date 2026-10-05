# Filled Example — ADR-001

# ADR-001 — Use Prisma for database access

## Status
Accepted

## Context
Need type-safe DB access with migrations and a small team.

## Decision
Use Prisma with PostgreSQL. Schema in prisma/schema.prisma; migrations via prisma migrate.

## Alternatives considered
- Drizzle — good, but team already knows Prisma
- Raw SQL — too error-prone for this speed

## Consequences
- +Type safety, easy migrations
- -Bundle overhead, some raw SQL still needed for complex queries
