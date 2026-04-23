---
description: 'Performance Optimization with Caching and ISR'
author: 'Diego Villanueva'
trigger: 'When implementing Incremental Static Regeneration, caching strategies, or revalidation.'
---

# Next.js Caching & ISR

Professional management of the Next.js Cache and Data Lifecycle.

## ✅ ALWAYS
- Use `force-cache` for data that rarely changes.
- Implement **ISR** using `revalidate` property or `revalidatePath`.
- Use `unstable_cache` for caching non-fetch operations (e.g., direct DB queries).
- Use `requestTag` to group cache entries and invalidate them selectively.
- Monitor cache hits/misses in the production environment.

## ❌ NEVER
- Use `no-store` globally; identify what can be cached.
- Rely on automatic revalidation for critical business data.
- Forget that the cache is shared across requests in the Data Cache.

## 🛠 Patterns
- **On-Demand Revalidation**: Using Webhooks or Server Actions to purge the cache.
- **Dynamic Segment Config**: Controlling caching behavior at the page/layout level.
