# Sift — Tech Stack

## Framework
Next.js 14 with App Router

## Languages
TypeScript throughout — no plain JS files

## Styling
Tailwind CSS — utility classes only, no custom CSS files unless
unavoidable. No CSS modules.

## Animation
Framer Motion — all transitions, counters, micro-animations, and
phase changes use Framer Motion. No CSS animations except for the
pulsing green dot on the trust badge (animate-ping).

## Graph Visualisation
React Flow — used exclusively for the inference node graph in Phase 4.
Do not use D3 or any other graph library.

## PDF Generation
jsPDF — for the Privacy Receipt in Phase 6.

## Share Card Capture
html2canvas — for generating the viral share card image in Phase 6.

## Icons
Lucide React — no other icon library.

## Fonts
Inter — all UI text (loaded via next/font/google)
JetBrains Mono — all terminal log lines, confidence scores, 
technical readouts, and code blocks (loaded via next/font/google)

## Colour Tokens (use these exact values everywhere)
--bg-base: #0A0A0F
--bg-surface: #12121A
--bg-border: #1E1E2E
--accent: #00D4FF
--linkedin: #0A66C2
--x-platform: #E7E9EA
--success: #00FF88
--danger: #FF4444
--warning: #FFB800
--text-primary: #F0F0F0
--text-secondary: #888899

## Key Dependencies to Install
npm install framer-motion @xyflow/react jspdf html2canvas lucide-react

## Routes
/ — Landing page (Phase 1)
/scanning — Tech theater (Phases 2 and 3)
/reveal — Identity reveal and inference graph (Phase 4)
/audit — Audit and remediation workspace (Phase 5)
/exit — Exit loop (Phase 6)
