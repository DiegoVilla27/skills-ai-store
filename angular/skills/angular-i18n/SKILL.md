---
name: angular-i18n
description: Internationalization and Localization Best Practices
author: Diego Villanueva
trigger: When implementing multi-language support or localized formatting.
---

# Angular Internationalization (i18n)

Standardized implementation of multi-language support and cultural adaptation.

## ✅ ALWAYS
- Use the built-in `i18n` attributes for template translations.
- Use `provideLocaleData` and `LOCALE_ID` for date/number/currency formatting.
- Manage translation files (`.xlf`) using the Angular CLI `extract-i18n` command.
- Use the `translate` pipe or a service-based approach (like `ngx-translate` or `transloco`) if runtime language switching is required.
- Follow RTL (Right-to-Left) design best practices for applicable locales.

## ❌ NEVER
- Hardcode strings in templates or component logic.
- Concatenate strings for translation (breaks grammar rules); use placeholders.
- Manually format dates; use the `date` pipe with the appropriate locale.

## 🛠 Patterns
- **Runtime Switching**: Dynamic language loading without page refresh.
- **Language Guards**: Detecting and setting the user's preferred language on startup.
