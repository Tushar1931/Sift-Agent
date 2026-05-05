# Next.js Style Guide

## Routing
- Use the App Router (`app/` directory).
- Use `page.tsx` for route segments.
- Use `layout.tsx` for shared UI across segments.

## Server and Client Components
- Use Server Components by default for better performance and SEO.
- Use `'use client'` only when necessary for interactivity (hooks, event listeners).
- Keep Client Components as small as possible at the leaves of the component tree.

## Data Fetching
- Use `fetch` with appropriate caching and revalidation options.
- Fetch data in Server Components whenever possible.
- Use `loading.tsx` for streaming and instant loading states.

## Metadata
- Use the Metadata API for SEO (static or dynamic metadata).
- Define base metadata in the root layout.

## Optimisation
- Use `next/image` for image optimisation.
- Use `next/font` for font optimisation.
- Use `next/link` for client-side navigation.
