# React Style Guide

## Component Definitions
- Use functional components with hooks.
- Prefer arrow functions for component definitions.
- Use PascalCase for component names and filenames.

## Props
- Use TypeScript interfaces/types for prop definitions.
- Destructure props in the component signature.
- Provide default values using destructuring defaults.

## State Management
- Use `useState` for local component state.
- Use `useReducer` for complex state logic.
- Keep state as close as possible to where it is used.

## Hooks
- Follow the Rules of Hooks.
- Extract complex logic into custom hooks.
- Use `useMemo` and `useCallback` only when necessary for performance.

## Styling
- Use Tailwind CSS utility classes.
- Avoid inline styles.
- Maintain a consistent ordering of Tailwind classes (e.g., layout, spacing, typography, colors).
