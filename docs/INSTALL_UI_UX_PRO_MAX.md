# Install UI/UX Pro Max — Design Intelligence Skill

This skill eliminates design decision paralysis by generating complete design systems before you write a single line of code. It includes 67 UI styles, 96 color palettes, 57 font pairings, 99 UX guidelines, and 100 industry-specific reasoning rules.

## What It Does

You describe what you're building, and it automatically generates:

- Color palette matched to your industry/product type
- Font pairings with Google Fonts imports
- Layout patterns and page structure
- UI style recommendation (glassmorphism, minimalism, brutalism, etc.)
- Animation and interaction effects
- Anti-patterns to avoid
- Pre-delivery accessibility checklist

## Prerequisites

Python 3.x is required for the design system generator script.

Check if installed:

    python3 --version

If not installed:
- macOS: `brew install python3`
- Ubuntu/Debian: `sudo apt update && sudo apt install python3`
- Windows: `winget install Python.Python.3.12`

## Install in a New Project (from skeleton_startup)

Open your project in Claude Code and paste:

> Install the UI/UX Pro Max skill:
> npm install -g uipro-cli
> uipro init --ai claude
>
> Verify the install created .claude/skills/ui-ux-pro-max/ with SKILL.md, scripts/ folder, and data/ folder.
>
> Then append this to the Skills References section of CLAUDE.md — do not remove anything already there:
>
> When starting any new page or UI feature, generate a design system first:
> - .claude/skills/ui-ux-pro-max/SKILL.md — design intelligence with 67 styles, 96 color palettes, 57 font pairings, and 99 UX guidelines
> - Before writing UI code, run the design system generator to get tailored colors, typography, layout patterns, and anti-patterns for the specific product type
>
> Commit and push.

## Install in an Existing Project

Open your existing project in Claude Code and paste:

> Install the UI/UX Pro Max skill:
> npm install -g uipro-cli
> uipro init --ai claude
>
> Then append this to the Skills References section of the existing CLAUDE.md — do not remove anything already there:
>
> When starting any new page or UI feature, generate a design system first:
> - .claude/skills/ui-ux-pro-max/SKILL.md — design intelligence with 67 styles, 96 color palettes, 57 font pairings, and 99 UX guidelines
> - Before writing UI code, run the design system generator to get tailored colors, typography, layout patterns, and anti-patterns for the specific product type
>
> Commit and push.

## Verify Installation

Run this to test the design system generator:

    python3 .claude/skills/ui-ux-pro-max/scripts/search.py "SaaS dashboard" --design-system -p "Test"

You should see a complete design system output with colors, typography, style, and layout recommendations.

## Day-to-Day Usage

### Auto-Activate (Just Build Naturally)

The skill activates automatically when you ask Claude Code to build UI. Just describe what you need:

- "Build a landing page for my SaaS product"
- "Create a dashboard for healthcare analytics"
- "Design a settings page with dark mode"

### Generate a Full Design System First (Recommended for New Projects)

Before building any UI, ask Claude Code:

> Generate a design system for a relationship conversation platform targeting couples. use context7

This hands you the complete palette, fonts, layout patterns, effects, and anti-patterns before writing a single line of code. No more staring at a blank screen.

### Persist Your Design System Across Sessions

For consistency across your entire project, ask Claude Code:

> Run the design system generator with --persist flag to save to design-system/MASTER.md

This creates a design-system/ folder:
- design-system/MASTER.md — your global design source of truth
- design-system/pages/ — page-specific overrides when needed

### Search Specific Design Domains

You can also search specific areas directly:

- Styles: `python3 .claude/skills/ui-ux-pro-max/scripts/search.py "glassmorphism" --domain style`
- Typography: `python3 .claude/skills/ui-ux-pro-max/scripts/search.py "elegant serif" --domain typography`
- Colors: `python3 .claude/skills/ui-ux-pro-max/scripts/search.py "wellness spa" --domain color`
- Charts: `python3 .claude/skills/ui-ux-pro-max/scripts/search.py "dashboard" --domain chart`
- Stack-specific: `python3 .claude/skills/ui-ux-pro-max/scripts/search.py "form validation" --stack react`

## Example Prompts That Work Great

"Build a landing page for my relationship conversation platform. Warm, inviting, trust-building aesthetic for couples."

"Design the pricing page for my operations knowledge portal. Clean, professional, targeting manufacturing SMBs."

"Create an onboarding flow for a subscription wellness app. Calming, accessible, mobile-first."

"Redesign my dashboard with a cohesive design system. Generate the system first, then implement."

## Tips

- Always generate a design system BEFORE building UI on a new project
- Use --persist to save your design system so every page stays consistent
- Add "use context7" to prompts when you need current API docs alongside design
- The skill works alongside frontend-design — they complement each other
- Start a new session after installing so Claude Code picks up the skill

## Notes

- This skill requires Python 3.x for the search/generator scripts
- The data/ folder contains CSV databases — do not modify these manually
- UI/UX Pro Max is MIT licensed and free to use
- Updates: run `uipro update` to get the latest version
