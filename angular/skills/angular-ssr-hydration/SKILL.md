---
name: angular-ssr-hydration
description: Server-Side Rendering (SSR) and Performance Hydration
author: Diego Villanueva
trigger: When implementing SSR, SSG, or optimizing initial load performance.
---

# Angular SSR & Hydration

Mastering Server-Side Rendering and the new **Eventual Hydration** model.

## ✅ ALWAYS
- Use `provideClientHydration()` to enable non-destructive hydration.
- Use `isPlatformBrowser` and `isPlatformServer` to handle environment-specific logic.
- Optimize LCP by pre-fetching critical data during SSR.
- Use `TransferState` to share data between server and client and avoid duplicate requests.
- Leverage **Deferrable Views** (`@defer`) to lazy-load non-critical parts of the page.

## ❌ NEVER
- Access `window`, `document`, or `localStorage` directly without checking the platform.
- Block the server-side rendering process with long-running tasks.
- Use `afterRender` for logic that must run on the server.

## 🛠 Patterns
- **Server Actions**: Handling form submissions and mutations in a SSR context.
- **Pre-rendering**: Generating static pages during the build process.
