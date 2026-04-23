---
description: 'Advanced Internationalization with next-intl'
author: 'Diego Villanueva'
trigger: 'When implementing multi-language support, localized routes, or RTL.'
---

# Next.js i18n (next-intl)

Mastery of internationalization using the `next-intl` framework in the App Router.

## ✅ ALWAYS
- Use the `[locale]` dynamic segment for localized routing.
- Use `useTranslations` for accessing keys in components.
- Implement the `middleware` to handle locale detection and redirection.
- Define type-safe messages for autocomplete and validation.
- Use `unstable_setRequestLocale` for static rendering of localized pages.

## ❌ NEVER
- Hardcode strings in templates; always use a translation key.
- Store the locale in a client-side state only; keep it in the URL.
- Manually format dates; use the `t.dateTime` or `Intl` API.

## 🛠 Patterns
- **Localized Navigation**: Using shared navigation components that respect the current locale.
- **RTL Support**: Dynamically adjusting the `dir` attribute and CSS based on the locale.
