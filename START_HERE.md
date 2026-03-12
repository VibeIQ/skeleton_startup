# START HERE

You built a starter kit. Now use it to launch real projects — fast.

This repo (`skeleton_startup`) is your reusable foundation. It contains no app code. It contains the **knowledge layer** — skills, conventions, and templates — that makes Claude Code build your projects the right way from the first prompt.

---

## What's Inside

```
skeleton_startup/
├── README.md
├── docs/
│   ├── SETUP_GUIDE.md              # Full step-by-step reference
│   ├── NEW_PROJECT_PROMPT.md        # Copy-paste prompt for day-one setup
│   ├── ADD_SKILLS_TO_EXISTING_PROJECT.md
│   ├── ADD_ACCESSIBILITY_TO_EXISTING_PROJECT.md
│   ├── INSTALL_UI_UX_PRO_MAX.md
│   └── ELITE_PROMPTS.md            # Library of copy-paste prompts
└── template/                        # Everything that gets copied into new projects
    ├── .claude/skills/              # 8 best-practice skills Claude Code uses automatically
    │   ├── frontend-design/         # Bold, distinctive UI — no generic AI aesthetics
    │   ├── react-best-practices/    # React performance patterns (from Vercel)
    │   ├── web-design-guidelines/   # Accessibility & UX compliance
    │   ├── composition-patterns/    # Clean component architecture
    │   ├── supabase-best-practices/ # PostgreSQL, RLS, migrations
    │   ├── stripe-best-practices/   # Payment integration patterns
    │   ├── nextjs-skills/           # Next.js App Router best practices
    │   └── ui-ux-pro-max/           # Design intelligence skill
    ├── .github/
    │   ├── pull_request_template.md
    │   └── ISSUE_TEMPLATE/
    │       ├── bug_report.md
    │       ├── feature_request.md
    │       └── ui_improvement.md
    ├── CLAUDE.md                    # Project instructions template (Claude reads this first)
    └── .env.example                 # Every env var you'll need, pre-organized
```

**Your tech stack:** Next.js (App Router) · React · Tailwind CSS · Clerk · Supabase · Stripe · Vercel · Claude API · AssemblyAI

---

## Launch a New Project (5 Steps)

### Step 1: Create a new GitHub repo

Go to GitHub and create a new empty repository for your project. Name it whatever you want.

### Step 2: Copy the starter files

Open Claude Code in your **new project repo** and paste this:

```
Copy everything from the template/ folder in my skeleton_startup repo into this project root. Commit and push.
```

That's it — Claude Code copies the skills, GitHub templates, CLAUDE.md, and .env.example for you.

### Step 3: Customize CLAUDE.md

In Claude Code, paste this (replace the bracketed parts):

```
Update the CLAUDE.md — this project is called [YOUR APP NAME].
It does [one sentence about what your app does].
Update the project name and Overview section. Keep everything else the same.
```

### Step 4: Set up your services and env vars

You need accounts with these services. Sign up and grab your API keys:

| Service | What it does | Get keys at |
|---------|-------------|-------------|
| **Clerk** | Authentication | clerk.com |
| **Supabase** | Database (Postgres) | supabase.com |
| **Stripe** | Payments | stripe.com |
| **Anthropic** | AI (Claude API) | console.anthropic.com |
| **AssemblyAI** | Voice (optional) | assemblyai.com |
| **Vercel** | Hosting | vercel.com |

Then set your environment variables:
- **On Vercel**: Go to your project → Settings → Environment Variables → add each key from `.env.example`
- **Locally** (if developing locally): Copy `.env.example` to `.env.local` and fill in the values

### Step 5: Start building

Open a new Claude Code session on your project and start prompting. All skills and conventions are active automatically — you don't need to do anything special.

**Example first prompt:**

```
Initialize a Next.js App Router project with TypeScript and Tailwind CSS.
Set up Clerk authentication, a Supabase client utility, and a Stripe
webhook handler. Follow the CLAUDE.md conventions.
```

---

## One-Time Setup: Context7 MCP

Run this once (ever, not per project) to give Claude Code access to live documentation for your entire stack:

```bash
claude mcp add context7 -- npx -y @upstash/context7-mcp@latest
```

After that, add **"use context7"** to any prompt where you want Claude to pull up-to-date API docs instead of relying on its training data. Useful for version-sensitive code.

---

## How the Skills Work

You don't invoke skills manually. Claude Code reads them automatically and applies them when relevant:

| When you're doing... | Claude uses... |
|---------------------|---------------|
| Building UI components | `frontend-design` + `composition-patterns` |
| Writing React code | `react-best-practices` |
| Reviewing accessibility/UX | `web-design-guidelines` |
| Writing database queries or schema | `supabase-best-practices` |
| Adding payments | `stripe-best-practices` |
| Working with Next.js routing, layouts, metadata | `nextjs-skills` |

**The frontend-design skill is especially important** — it prevents Claude from generating the same generic purple-gradient, Inter-font UI that every AI tool produces. Your app will look distinctive.

---

## Rules to Follow

1. **Never build directly in `skeleton_startup`** — always copy template files to a new repo first
2. **Start a new Claude Code session** after adding or updating CLAUDE.md or skills
3. **Keep `skeleton_startup` as your single source of truth** — when you discover a new best practice or skill, add it here first, then copy to active projects
4. **Don't delete the template placeholders** in this repo's CLAUDE.md — they're meant to be replaced per-project

---

## Updating Your Starter Kit

As you build projects, you'll learn what works. Improve the skeleton over time:

1. **New skill?** Add a new `SKILL.md` under `template/.claude/skills/your-skill-name/` in this repo
2. **Better conventions?** Update the `template/CLAUDE.md` template here
3. **New env vars?** Add them to `template/.env.example` here
4. **New GitHub templates?** Add them to `template/.github/` here
5. **Active projects need updates?** Copy the changed files from `template/` into those projects and start a new session

---

## Quick Reference

| I want to... | Do this |
|--------------|---------|
| Start a new project | Follow the 5 steps above |
| Add a skill to all future projects | Add it to `template/.claude/skills/` |
| Update a skill on an active project | Copy the updated skill file from template, restart session |
| Use live API docs in a prompt | Add "use context7" to your prompt |
| See the copy-paste bootstrap prompt | Open `docs/NEW_PROJECT_PROMPT.md` |
| See what env vars are needed | Open `template/.env.example` |
| See all reference guides | Browse the `docs/` folder |

---

**That's it. Create a repo, copy the template files, customize CLAUDE.md, add your keys, and start building.**
