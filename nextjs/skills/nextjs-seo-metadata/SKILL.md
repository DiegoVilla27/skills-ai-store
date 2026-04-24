---
name: nextjs-seo-metadata
description: Search Engine Optimization and Dynamic Metadata
author: Diego Villanueva
trigger: When optimizing pages for SEO, social sharing, or dynamic metadata generation.
---

# Next.js SEO & Metadata

Standardized implementation of SEO best practices and the Metadata API.

## ✅ ALWAYS
- Define a base `metadata` object in the root `layout.tsx`.
- Use `generateMetadata` for dynamic pages (e.g., product detail).
- Include `openGraph` and `twitter` tags for social sharing optimization.
- Use the `<Image>` component with proper `alt` text and `priority` for LCP.
- Implement `robots.txt` and `sitemap.xml` using Next.js file-based generation.

## ❌ NEVER
- Use the legacy `<Head>` component in the App Router.
- Duplicate metadata across nested layouts without a merge strategy.
- Forget to set the `canonical` URL for duplicated content.

## 🛠 Patterns
- **Dynamic OG Images**: Using `@vercel/og` to generate sharing images on the fly.
- **Structured Data**: Injecting JSON-LD for rich search results.
