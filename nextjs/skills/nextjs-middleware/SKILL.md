---
name: nextjs-middleware
description: Edge Logic, Security, and Routing with Middleware
author: Diego Villanueva
trigger: When implementing global route protection, redirects, or header manipulation.
---

# Next.js Middleware

Leveraging the Edge Runtime for global request interception.

## ✅ ALWAYS
- Keep the `middleware.ts` file in the root or `src` directory.
- Use a `matcher` to limit the middleware execution to relevant paths.
- Perform high-speed checks (Auth, Geo, Cookies) without blocking the response.
- Use `NextResponse.redirect` or `NextResponse.rewrite` for routing logic.
- Ensure the middleware logic is compatible with the Edge Runtime.

## ❌ NEVER
- Perform heavy database operations in the middleware.
- Use libraries that are not supported by the Edge Runtime (e.g., standard Node.js FS).
- Create infinite redirect loops.

## 🛠 Patterns
- **Auth Guard**: Centrally protecting the `/dashboard` or `/admin` routes.
- **A/B Testing**: Randomly assigning users to different versions of a page at the edge.
