---
description: 'Mastery of Server-Side Mutations and Data Revalidation'
author: 'Diego Villanueva'
trigger: 'When implementing form submissions, data mutations, or server-side logic triggered by the client.'
---

# Next.js Server Actions

Professional implementation of the RPC-like mutation system in Next.js (App Router).

## ✅ ALWAYS
- Use the `"use server"` directive at the top of the file or function.
- Implement Zod validation at the beginning of every action.
- Use `revalidatePath` or `revalidateTag` after a successful mutation.
- Use `useActionState` (React 19) or `useFormState` to handle action results and pending states.
- Wrap action calls in a `try-catch` and return structured error objects.
- Ensure the action is authorized by checking the session inside the function.

## ❌ NEVER
- Leak sensitive data in action responses.
- Forget to handle the "pending" state in the UI.
- Use Server Actions for simple data fetching (use Server Components instead).

## 🛠 Patterns
- **Optimistic Updates**: Using `useOptimistic` to show immediate UI feedback.
- **Action Composition**: Grouping related actions in a `features/[name]/actions.ts` file.
