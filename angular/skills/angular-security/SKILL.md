---
description: 'Authentication, Authorization, and Web Security'
author: 'Diego Villanueva'
trigger: 'When implementing login flows, route protection, or data sanitization.'
---

# Angular Security

Ensuring application integrity and user data protection.

## ✅ ALWAYS
- Use `DomSanitizer` for rendering dynamic HTML/URLs securely.
- Implement **Functional Guards** to protect routes.
- Use `HttpInterceptor` to attach JWT or CSRF tokens to outgoing requests.
- Validate all user inputs on the client (and ensure server validation exists).
- Follow the OWASP Top 10 guidelines for web security.

## ❌ NEVER
- Use `innerHTML` with untrusted data (use `[innerHtml]` and sanitize).
- Store sensitive tokens in `localStorage`; prefer `HttpOnly` cookies or secure memory storage.
- Disable Angular's built-in XSS protection.

## 🛠 Patterns
- **Auth Interceptor**: Centralized token management and 401 handling.
- **Permission Directive**: Conditionally showing UI elements based on user roles.
