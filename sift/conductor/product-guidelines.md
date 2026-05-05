# Sift — Product Guidelines

## Design Philosophy
Dark, precise, and cinematic. Think security operations centre meets
premium SaaS. Not a student hackathon project. Not crypto. Not neon chaos.

## Background Treatment
Apply a 3% opacity noise texture overlay on all page backgrounds using
an SVG filter. Add a barely visible radial gradient in #00D4FF emanating
from top-centre — opacity no higher than 8%.

## Cards and Surfaces
All cards use backdrop-blur-sm, a 1px border in #1E1E2E, rounded-xl,
and shadow-2xl with #00D4FF at 5% opacity. Never use grey shadows.

## Buttons
Primary CTA: bg-accent text-black font-semibold rounded-xl
Ghost button: transparent bg, accent border and text, rounded-xl
All buttons: transition-all duration-200 hover:scale-[1.02] active:scale-[0.98]

## Typography Rules
All UI copy uses Inter. All technical/data readouts use JetBrains Mono.
Never mix fonts within the same UI element.

## Animation Rules
All numbers and scores animate with Framer Motion useSpring — they
never jump. All page section transitions use AnimatePresence with
upward slide + fade, duration 0.6s, easeInOut.
The Tech Theater log is exactly 6 seconds regardless of real processing time.

## Platform Colour Rules
LinkedIn data: always #0A66C2
X data: always #E7E9EA
Cross-platform inference edges: animated glowing stroke in #00D4FF
Never use LinkedIn colour for X data or vice versa.

## Mobile Rules
The React Flow inference graph collapses to a vertical scrollable list
of connection cards on screens below md breakpoint.
All other layouts are responsive via Tailwind responsive prefixes.

## Accessibility
All interactive elements have focus-visible rings in the accent colour.
Minimum contrast ratio 4.5:1 for all body text against backgrounds.

## What NOT to Build
No server-side data storage of any kind.
No authentication or user accounts.
No backend API routes that persist data.
No CSS animations other than the trust badge pulse.
No icon libraries other than Lucide React.
No graph libraries other than React Flow.
