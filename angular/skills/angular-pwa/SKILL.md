---
name: angular-pwa
description: Progressive Web Apps and Service Workers
author: Diego Villanueva
trigger: When implementing offline support, push notifications, or app-like experiences.
---

# Angular PWA

Transforming web applications into reliable, installable mobile experiences.

## ✅ ALWAYS
- Use `@angular/pwa` to scaffold the Service Worker and manifest.
- Configure the `ngsw-config.json` for fine-grained asset caching.
- Use `SwUpdate` to detect and notify users about app updates.
- Optimize the `manifest.webmanifest` for cross-platform app status.
- Test offline behavior using the browser DevTools.

## ❌ NEVER
- Cache sensitive user data in the Service Worker.
- Ignore lighthouse performance scores for PWA compliance.
- Forget to provide a fallback UI for offline mode.

## 🛠 Patterns
- **Data Caching**: Caching API responses using the `dataGroups` configuration.
- **Push Notifications**: Integrating `SwPush` with a VAPID key backend.
