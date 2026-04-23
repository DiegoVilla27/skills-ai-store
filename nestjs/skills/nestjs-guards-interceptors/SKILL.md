---
description: 'Request Lifecycle: Security Guards and Data Interceptors'
author: 'Diego Villanueva'
trigger: 'When implementing authorization logic, data transformation, or logging.'
---

# NestJS Guards & Interceptors

Mastery of the request-response lifecycle for security and consistency.

## ✅ ALWAYS
- Use **Guards** (`CanActivate`) for authorization and authentication logic.
- Use **Interceptors** (`NestInterceptor`) for response mapping, logging, and error transformation.
- Leverage `SetMetadata()` and `Reflector` to create custom decorators for guards.
- Apply guards at the controller or method level for fine-grained control.
- Use the `ExecutionContext` to access request/response data in a protocol-agnostic way.

## ❌ NEVER
- Perform authorization logic inside the Controller methods; use Guards.
- Modify the original request object directly; use Pipes for data transformation.
- Block the response stream in an interceptor without a good reason.

## 🛠 Patterns
- **Role Guard**: Authorizing users based on metadata roles.
- **Transform Interceptor**: Wrapping all responses in a standard `{ data, meta }` object.
