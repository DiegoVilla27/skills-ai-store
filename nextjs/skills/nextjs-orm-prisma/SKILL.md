---
description: 'Database Integration and Type-Safe Queries with Prisma'
author: 'Diego Villanueva'
trigger: 'When implementing database schemas, migrations, or data access layers with Prisma.'
---

# Next.js + Prisma ORM

Mastery of the Prisma ORM for type-safe and performant database operations.

## ✅ ALWAYS
- Use a single instance of `PrismaClient` (Singleton pattern) to avoid connection exhaustion in dev.
- Define models with proper relations and indexes in `schema.prisma`.
- Run `npx prisma generate` after every schema change.
- Use `prisma.$transaction` for multi-step atomic operations.
- Map Prisma models to Domain Entities to keep the core logic decoupled.

## ❌ NEVER
- Expose the raw Prisma client to the UI components.
- Perform heavy filtering or joining in JS; let the database do it.
- Forget to run migrations in production.

## 🛠 Patterns
- **Repository Implementation**: Using Prisma within the `infrastructure/repositories` layer.
- **Typed Filters**: Building dynamic queries with strict TypeScript safety.
