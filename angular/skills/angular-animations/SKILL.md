---
description: 'Complex UI Transitions and Browser Animations API'
author: 'Diego Villanueva'
trigger: 'When implementing micro-interactions, page transitions, or state-based animations.'
---

# Angular Animations

Mastering the `@angular/animations` DSL for cinematic and performant UI.

## ✅ ALWAYS
- Define animations in separate files if they are complex and reusable.
- Use `trigger`, `state`, `transition`, and `animate` functions.
- Use `query` and `stagger` for coordinated multi-element animations.
- Use `params` to create dynamic and flexible animations.
- Prefer **CSS-based** animations for simple hover effects and standard browser transitions.

## ❌ NEVER
- Manually manipulate the DOM with JS for animations.
- Overload the browser with too many concurrent complex animations.
- Forget to handle the `void` state for entry/exit animations.

## 🛠 Patterns
- **Route Transitions**: Animating the switch between different pages.
- **List Animations**: Smooth entry/exit/reordering for `@for` blocks.
