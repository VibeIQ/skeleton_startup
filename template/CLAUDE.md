# Project: [PROJECT NAME]

## Overview

[Brief description of what this app does]

## Tech Stack

- Framework: Next.js (App Router)
- UI: React, Tailwind CSS
- Auth: Clerk
- Database: Supabase (PostgreSQL + RLS)
- Payments: Stripe
- Hosting: Vercel
- AI: Claude API
- Voice: AssemblyAI (where applicable)

## Development Workflow

- No local dev environment — uses GitHub web editor + Vercel auto-deployment
- All code changes go through GitHub commits
- Vercel auto-deploys from main branch

## Code Conventions

- Always provide complete updated files, never partial snippets
- Include version comments (vX.X.X) in file headers, incrementing from the last version
- Do not break existing functionality when making changes
- Use TypeScript patterns consistent with existing codebase

## Skills References

When building or modifying frontend UI, apply design principles from:
- .claude/skills/frontend-design/SKILL.md — bold, distinctive UI design (no generic AI aesthetics)
- .claude/skills/react-best-practices/SKILL.md — React performance patterns
- .claude/skills/web-design-guidelines/SKILL.md — accessibility compliance
- .claude/skills/composition-patterns/SKILL.md — clean component architecture

When working with backend/data:
- .claude/skills/supabase-best-practices/SKILL.md — PostgreSQL, RLS, migrations
- .claude/skills/stripe-best-practices/SKILL.md — payment integration patterns

When working with Next.js specifically:
- .claude/skills/nextjs-skills/SKILL.md — Next.js best practices

## Context7 MCP

When writing code involving unfamiliar or version-sensitive APIs, use Context7 MCP to fetch current documentation before implementing. Do not rely on outdated knowledge.

## Design Workflow

When building or redesigning any UI page or component:
1. STOP and generate a design system recommendation first — present the style, colors, typography, layout pattern, and anti-patterns
2. WAIT for my approval before writing any code
3. If I request changes to the design direction, regenerate and present again
4. Only after I explicitly approve the design system, proceed to build
5. Never skip straight to code on UI work — always present the plan first

This also applies to major feature work:
1. Present your approach and what files you plan to create or modify
2. Wait for my approval
3. Then build

## Accessibility Standards (ADA / WCAG 2.1 AA — Non-Negotiable)

Every page, component, and feature must meet these standards from the first line of code. Accessibility is not a cleanup task — it is built in from the start.

### Every Element Must Have:
- Color contrast minimum 4.5:1 for normal text, 3:1 for large text
- Visible focus rings on all interactive elements — never remove outline without replacing it
- cursor-pointer on all clickable elements
- Smooth transitions between 150-300ms on all interactive states

### Every Page Must Have:
- Skip-to-content link as the first focusable element
- Proper heading hierarchy (h1 > h2 > h3, never skip levels)
- Semantic HTML structure (nav, main, section, article, aside — no div soup)
- Full keyboard navigation — every action achievable without a mouse
- Tab order that follows visual reading order
- prefers-reduced-motion respected on all animations

### Every Form Must Have:
- Labels visibly associated with every input (no placeholder-only labels)
- ARIA labels on all inputs and buttons
- Error messages linked to inputs via aria-describedby
- Focus moves to first error on failed submission

### Every Image and Icon Must Have:
- Descriptive alt text on meaningful images
- aria-hidden="true" on decorative images and icons
- SVG icons wrapped with proper role and aria-label

### Every Modal and Dropdown Must Have:
- Focus trapped inside when open
- Escape key closes it
- Focus returns to trigger element on close
- aria-modal="true" and proper role attributes

### Every Interactive Component Must Have:
- Minimum touch target 44x44px
- Hover, focus, and active states
- Screen reader announcement of state changes (aria-live for dynamic content)

### Pre-Delivery Accessibility Checklist:
Before presenting any completed UI work, verify:
- [ ] Tab through entire page — every element reachable and operable
- [ ] Screen reader passes — no unlabeled buttons, images, or inputs
- [ ] Contrast check — no text below 4.5:1 ratio
- [ ] Keyboard only — complete every user flow without a mouse
- [ ] Reduced motion — animations respect prefers-reduced-motion
- [ ] Mobile touch — all targets minimum 44x44px
- [ ] Semantic HTML — inspect for proper landmark elements

## Important Rules

- Always provide complete updated files — never partial snippets, never ask me to stitch code
- Include version comments (vX.X.X) in file headers, incrementing from the last version
- Do not break existing functionality when making changes
- Never remove or break existing features when adding new ones
- Ask clarifying questions when requirements are ambiguous
- Measure twice, cut once — plan before implementing
- When in doubt, ask before acting
- End every task with commit and push
