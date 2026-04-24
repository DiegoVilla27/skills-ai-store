---
name: nextjs-auth-js
description: Authentication and Session Management with Auth.js (NextAuth)
author: Diego Villanueva
trigger: When implementing login, oauth providers, or session protection in Next.js.
---

# Next.js Auth.js (NextAuth v5)

Modern authentication implementation for the App Router ecosystem.

## ✅ ALWAYS
- Use the `auth()` function in Server Components to access the session.
- Define a central `auth.ts` configuration file.
- Implement **Middleware** for global route protection.
- Use `signIn` and `signOut` actions for authentication flows.
- Leverage the `session` callback to inject custom user data (IDs, Roles).
- Use `AuthProvider` only if you need session access in Client Components.

## ❌ NEVER
- Store sensitive tokens in the client-side session.
- Manually manage cookies for authentication; let Auth.js handle security.
- Perform session checks inside every single page; use Middleware.

## 🛠 Patterns
- **Role-Based Access Control (RBAC)**: Using the session data to protect specific routes.
- **Adapter Pattern**: Integrating with Prisma, Drizzle, or external databases.
