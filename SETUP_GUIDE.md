# Skeleton Startup — New Project Setup Guide

## What This Is

This is your personal starter kit for every new project. It includes pre-configured Claude Code skills, a CLAUDE.md template, and environment variable templates so you skip setup and go straight to building.

## What's Included

- `.claude/skills/` — 7 curated skills for your tech stack
  - frontend-design — bold, distinctive UI (no generic AI aesthetics)
  - react-best-practices — React performance patterns (Vercel)
  - web-design-guidelines — accessibility compliance (Vercel)
  - composition-patterns — clean component architecture (Vercel)
  - supabase-best-practices — PostgreSQL, RLS, migrations (Official Supabase)
  - stripe-best-practices — payment integration patterns (Official Stripe)
  - nextjs-skills — Next.js specific best practices
- `CLAUDE.md` — master project instructions template for Claude Code
- `.env.example` — standard environment variables for the full stack

## Tech Stack This Supports

Next.js (App Router) | React | Tailwind CSS | Clerk | Supabase | Stripe | Vercel | Claude API | AssemblyAI

## New Project Setup Steps

### Step 1: Create Your New Repo

Create a new repository on GitHub for your project.

### Step 2: Copy Starter Files

Open your new repo in Claude Code and paste this prompt:

> Copy the .claude/ folder, CLAUDE.md, and .env.example from my skeleton_startup repo into this project. Then commit and push.

Or manually copy these from the skeleton_startup repo into your new project:

- `.claude/` folder (entire folder with all skills)
- `CLAUDE.md`
- `.env.example`

### Step 3: Customize CLAUDE.md

In Claude Code, paste this prompt:

> Update the CLAUDE.md — this project is called [YOUR APP NAME]. It does [brief description]. Scan the codebase and update the Overview section and any project-specific details. Keep all skills references, conventions, and rules the same.

### Step 4: Set Up Environment Variables

- Copy `.env.example` to `.env.local`
- Fill in your keys for Clerk, Supabase, Stripe, etc.

### Step 5: Context7 MCP (One-Time Setup)

If you haven't already set up Context7 globally, run this once:

> claude mcp add context7 -- npx -y @upstash/context7-mcp@latest

This gives Claude access to live, up-to-date documentation for your entire stack. To use it, add "use context7" to any prompt where you need current API docs.

### Step 6: Start Building

Start a new Claude Code session on your project. Your skills, rules, and conventions are now active from the first message.

## Tips

- Always start a new session after adding or updating CLAUDE.md or skills
- Skills auto-activate — you don't need to invoke them manually
- Add "use context7" to prompts when working with version-sensitive APIs
- Keep skeleton_startup clean — never build directly in this repo
- When you find new skills worth adding, add them to skeleton_startup first, then copy to active projects

## Updating Your Starter Kit

When you want to add new skills or update your CLAUDE.md template:

1. Make changes in the skeleton_startup repo
2. For active projects, copy over the updated files
3. Start a new session to pick up changes
