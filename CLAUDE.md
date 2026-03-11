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

## Important Rules

- Measure twice, cut once — plan before implementing
- Never remove or break existing features when adding new ones
- Ask clarifying questions when requirements are ambiguous

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

## Important Rules

- Always provide complete updated files — never partial snippets, never ask me to stitch code
- Include version comments (vX.X.X) in file headers, incrementing from the last version
- Do not break existing functionality when making changes
- Ask clarifying questions when requirements are ambiguous
- Measure twice, cut once — plan before implementing
- When in doubt, ask before acting
- End every task with commit and push
