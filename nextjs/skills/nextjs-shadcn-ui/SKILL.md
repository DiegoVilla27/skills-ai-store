---
description: 'Premium UI Construction with Shadcn/UI and Tailwind'
author: 'Diego Villanueva'
trigger: 'When building modern, accessible, and themeable UI components in Next.js.'
---

# Next.js + Shadcn/UI

The modern standard for building high-quality, copy-pasteable UI components.

## ✅ ALWAYS
- Use the `npx shadcn@latest add` command to integrate components.
- Use `lucide-react` for consistent iconography.
- Leverage the `cn()` utility for conditional Tailwind classes.
- Theme components using CSS Variables in `globals.css`.
- Ensure all components maintain high accessibility (Radix UI primitives).

## ❌ NEVER
- Modify the base component code in a way that breaks its accessibility or core logic.
- Overuse "Mega-Components"; keep them atomic and reusable.

## 🛠 Patterns
- **Form Integration**: Combining Shadcn `Form` with `react-hook-form` and `zod`.
- **Custom Themes**: Creating brand-specific color palettes using the shadcn theme generator.
