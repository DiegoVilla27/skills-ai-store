---
description: 'TanStack Query for Angular - Server State Management'
author: 'Diego Villanueva'
trigger: 'When implementing caching, syncing, and updating server state.'
---

# Angular Query (TanStack Query)

Mastery of asynchronous server state management in Angular.

## ✅ ALWAYS
- Use `injectQuery` and `injectMutation` for data fetching and mutations.
- Define centralized `QueryKeys` factories to avoid string typos.
- Use `toSignal()` (implicit in `injectQuery`) for reactive template updates.
- Implement **Optimistic Updates** using `onMutate` for a snappy UX.
- Leverage `prefetchQuery` for improving navigation speed.

## ❌ NEVER
- Manually manage `isLoading` or `isError` flags for API calls.
- Duplicate data in local stores (NgRx/Signals) if it comes from the server; let Query be the source of truth.
- Use `useEffect` or complex RxJS logic to sync server data.

## 🛠 Patterns
- **Auto-Refetching**: Using `staleTime` and `gcTime` for efficient cache management.
- **Infinite Queries**: For handling paginated or infinite scroll data.
