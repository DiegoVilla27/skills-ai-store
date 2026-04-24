---
name: angular-material-cdk
description: Official UI Components and Component Dev Kit (CDK)
author: Diego Villanueva
trigger: When using Angular Material components or building custom UI behaviors with CDK.
---

# Angular Material & CDK

Mastery of the official Angular UI ecosystem for accessible and professional interfaces.

## ✅ ALWAYS
- Use the **CDK** (`@angular/cdk`) for low-level behaviors like overlays, drag-and-drop, and accessibility.
- Follow Material Design 3 (M3) guidelines and theming system.
- Use `MatTable` with `MatTableDataSource` for complex data grids.
- Implement responsive layouts using `BreakpointObserver` from the Layout package.
- Use `Dialog` and `Overlay` for custom floating UI elements.

## ❌ NEVER
- Override Material styles with `!important` in global CSS; use proper CSS compounding or Mixins.
- Manually calculate element positioning for popups; use `CdkOverlay`.
- Ignore `Aria` labels provided by Material components.

## 🛠 Patterns
- **Custom Form Fields**: Implementing `MatFormFieldControl` for custom UI inputs.
- **Virtual Scrolling**: Using `CdkVirtualScrollViewport` for massive lists.
