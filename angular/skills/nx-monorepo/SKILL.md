---
name: nx-monorepo
description: Scaling Angular with Nx and Monorepo Architecture
author: Diego Villanueva
trigger: When working in monorepos, managing multiple apps/libs, or optimizing CI/CD.
---

# Nx & Monorepo Architecture

Enterprise-level scaling for complex Angular ecosystems.

## ✅ ALWAYS
- Organize code into **Libraries** (`libs/`) with a clear public API (`index.ts`).
- Follow the **Tags** system for dependency constraints (e.g., `scope:shared` can't depend on `scope:feature`).
- Use `nx affected` to run tasks only on changed projects.
- Use **Generators** to maintain code consistency across the workspace.
- Leverage the **Nx Cache** for local and remote build speed.

## ❌ NEVER
- Create giant, monolithic applications without library boundaries.
- Have circular dependencies between libraries.
- Import code from `apps/` into `libs/`.

## 🛠 Patterns
- **Library Types**: Feature, UI, Data-Access, and Utility libs.
- **Micro-Frontend Orchestration**: Using Nx with Module Federation.
