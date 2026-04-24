---
name: nextjs-safe-action
description: Typed and Validated Server Actions with next-safe-action
author: Diego Villanueva
trigger: When using the next-safe-action library to build robust server-side mutations.
---

# Next Safe Action

Standardized implementation of the `next-safe-action` library for secure and type-safe mutations.

## ✅ ALWAYS
- Define a base action client with global error handling and middleware.
- Use `actionClient.schema(zodSchema)` to define inputs.
- Use the `hook` returned by the client to access `status`, `result`, and `execute`.
- Implement `middleware` for authentication and authorization checks.
- Handle different result states: `onSuccess`, `onError`, `onExecute`.

## ❌ NEVER
- Define actions without a validation schema.
- Duplicate authorization logic; move it to the action client middleware.
- Ignore the `validationError` object returned by the library.

## 🛠 Patterns
- **Logged In Client**: A specialized client that automatically fails if the user is not authenticated.
- **Bind Pattern**: Using `.bind()` to pass extra arguments to the action securely.
