# Skeleton Startup

Personal starter kit for every new project. Pre-configured Claude Code skills, accessibility standards, design workflow rules, and GitHub templates — ready to copy into any new repo.

## Quick Start

1. Create a new GitHub repo for your project
2. Open it in Claude Code and paste:

> Copy everything from the template/ folder in my skeleton_startup repo into this project root. Commit and push.

3. Customize the CLAUDE.md:

> Update the CLAUDE.md — this project is called [APP NAME]. It does [DESCRIPTION]. Scan the codebase and update the Overview section. Keep all skills references, conventions, and rules exactly as they are. Commit and push.

4. Start a new session and build.

## What's in template/

| Path | Purpose |
|------|---------|
| .claude/skills/ | 8 curated skills (frontend-design, react-best-practices, web-design-guidelines, composition-patterns, supabase-best-practices, stripe-best-practices, nextjs-skills, ui-ux-pro-max) |
| .github/ | PR template, bug report, feature request, and UI improvement issue templates |
| CLAUDE.md | Master project instructions with design workflow, accessibility standards, skills references, and code conventions |
| .env.example | Standard environment variables for Next.js + Clerk + Supabase + Stripe |

## Reference Docs

All guides and prompts are in the docs/ folder:

| Doc | Purpose |
|-----|---------|
| SETUP_GUIDE.md | Full step-by-step reference for new projects |
| NEW_PROJECT_PROMPT.md | Copy-paste prompt for day-one setup |
| ADD_SKILLS_TO_EXISTING_PROJECT.md | Retrofit skills into existing projects |
| ADD_ACCESSIBILITY_TO_EXISTING_PROJECT.md | Add ADA compliance to existing projects |
| INSTALL_UI_UX_PRO_MAX.md | Design intelligence skill setup and usage |
| ELITE_PROMPTS.md | Library of copy-paste prompts for common tasks |

## Tech Stack This Supports

Next.js (App Router) | React | Tailwind CSS | Clerk | Supabase | Stripe | Vercel | Claude API

## Updating

When you add new skills or update templates, make changes in this repo first, then copy updated files to active projects.
