# Add Skills to an Existing Project

Use this guide when you have a project that already has a CLAUDE.md and GitHub rules in place, and you want to add the skeleton_startup skills to it.

## Step 1: Copy Skills Into Your Project

Open your existing project in Claude Code and paste this prompt:

> Copy the entire .claude/skills/ folder from my skeleton_startup repo into this project. If a .claude/ folder already exists, merge the skills/ subfolder into it — do not overwrite anything else in .claude/. Do not touch CLAUDE.md or any other existing files. Commit and push.

## Step 2: Add Skills References to Your Existing CLAUDE.md

Paste this prompt next:

> Add the following section to the existing CLAUDE.md — do not remove or change anything that's already there. Just append this new section to the end:
>
> ## Skills References
> When building or modifying frontend UI, apply design principles from:
> - .claude/skills/frontend-design/SKILL.md — bold, distinctive UI design
> - .claude/skills/react-best-practices/SKILL.md — React performance patterns
> - .claude/skills/web-design-guidelines/SKILL.md — accessibility compliance
> - .claude/skills/composition-patterns/SKILL.md — clean component architecture
>
> When working with backend/data:
> - .claude/skills/supabase-best-practices/SKILL.md — PostgreSQL, RLS, migrations
> - .claude/skills/stripe-best-practices/SKILL.md — payment integration patterns
>
> When working with Next.js:
> - .claude/skills/nextjs-skills/SKILL.md — Next.js best practices
>
> When writing code involving unfamiliar or version-sensitive APIs, use Context7 MCP to fetch current documentation before implementing.
>
> Commit and push.

## Step 3: Start a New Session

Close your current session and start a new one so Claude Code picks up the new skills and updated CLAUDE.md.

## What This Does NOT Touch

- Your existing CLAUDE.md content (only appends to it)
- Your existing .claude/ settings or configs
- Your GitHub rules or workflows
- Any project files or code

## What This Adds

- 7 skill files in .claude/skills/
- A Skills References section in your CLAUDE.md

## Notes

- Skills are additive — they never conflict with existing configs
- Skills only activate when relevant to what you're asking Claude to do
- If you later add new skills to skeleton_startup, repeat Step 1 to sync them over
- Always start a new session after adding skills
