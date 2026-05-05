# Tailwind CSS Style Guide

## Class Ordering
- Follow a consistent order: Positioning -> Box Model (Layout) -> Typography -> Visuals -> Misc.
- Use the Prettier plugin for Tailwind CSS to automatically sort classes.

## Utility-First Approach
- Avoid creating custom CSS classes unless absolutely necessary.
- Use arbitrary values (e.g., `top-[117px]`) sparingly; prefer theme values.

## Responsive Design
- Use responsive prefixes (`sm:`, `md:`, `lg:`, `xl:`, `2xl:`) for mobile-first development.
- Ensure all layouts are functional at every breakpoint.

## Design Tokens
- Reference theme values (colors, spacing, etc.) defined in `tailwind.config.ts`.
- Use the custom color tokens defined in the tech stack (e.g., `text-accent`, `bg-base`).

## Interactivity
- Use hover, focus, and active states (`hover:`, `focus:`, `active:`) consistently.
- Use `transition` and `duration` classes for smooth UI interactions.
