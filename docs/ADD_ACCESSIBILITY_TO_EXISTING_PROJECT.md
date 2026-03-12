# Add Accessibility Standards to an Existing Project

Use this when you have a project that already has a CLAUDE.md and you want to bake in ADA/WCAG 2.1 AA compliance from the ground up.

## Step 1: Add Standards to CLAUDE.md

Open your existing project in Claude Code and paste this prompt:

> Read the CLAUDE.md in this project. Add the following as a new section — find the most logical placement after any design or workflow sections and before any rules sections. Do not remove or change anything already there. If there is no obvious placement, append it before the last section.
>
> ## Accessibility Standards (ADA / WCAG 2.1 AA — Non-Negotiable)
> Every page, component, and feature must meet these standards from the first line of code. Accessibility is not a cleanup task — it is built in from the start.
>
> ### Every Element Must Have:
> - Color contrast minimum 4.5:1 for normal text, 3:1 for large text
> - Visible focus rings on all interactive elements — never remove outline without replacing it
> - cursor-pointer on all clickable elements
> - Smooth transitions between 150-300ms on all interactive states
>
> ### Every Page Must Have:
> - Skip-to-content link as the first focusable element
> - Proper heading hierarchy (h1 > h2 > h3, never skip levels)
> - Semantic HTML structure (nav, main, section, article, aside — no div soup)
> - Full keyboard navigation — every action achievable without a mouse
> - Tab order that follows visual reading order
> - prefers-reduced-motion respected on all animations
>
> ### Every Form Must Have:
> - Labels visibly associated with every input (no placeholder-only labels)
> - ARIA labels on all inputs and buttons
> - Error messages linked to inputs via aria-describedby
> - Focus moves to first error on failed submission
>
> ### Every Image and Icon Must Have:
> - Descriptive alt text on meaningful images
> - aria-hidden="true" on decorative images and icons
> - SVG icons wrapped with proper role and aria-label
>
> ### Every Modal and Dropdown Must Have:
> - Focus trapped inside when open
> - Escape key closes it
> - Focus returns to trigger element on close
> - aria-modal="true" and proper role attributes
>
> ### Every Interactive Component Must Have:
> - Minimum touch target 44x44px
> - Hover, focus, and active states
> - Screen reader announcement of state changes (aria-live for dynamic content)
>
> ### Pre-Delivery Accessibility Checklist:
> Before presenting any completed UI work, verify:
> - [ ] Tab through entire page — every element reachable and operable
> - [ ] Screen reader passes — no unlabeled buttons, images, or inputs
> - [ ] Contrast check — no text below 4.5:1 ratio
> - [ ] Keyboard only — complete every user flow without a mouse
> - [ ] Reduced motion — animations respect prefers-reduced-motion
> - [ ] Mobile touch — all targets minimum 44x44px
> - [ ] Semantic HTML — inspect for proper landmark elements
>
> Commit and push.

## Step 2: Start a New Session

Close your current session and start a new one so Claude Code picks up the updated CLAUDE.md.

## Step 3: Audit Existing Pages (Optional but Recommended)

After adding the standards, run an audit on what's already built. Paste this prompt:

> Run a full accessibility audit on every page and component in this project. Before making any changes, present me with a list of every accessibility issue found organized by severity (critical, major, minor), your recommended fixes for each issue, and which files will be modified. Do NOT change any functionality, layout, design direction, colors, or typography. This is accessibility compliance only — visual appearance stays the same. Wait for my approval before making any changes.

## What This Does

- Adds WCAG 2.1 AA standards to your project's CLAUDE.md
- Every future page, component, and feature Claude Code builds will be accessible from the start
- Does not change any existing code — only adds rules for future work
- The optional audit in Step 3 identifies issues in existing code for you to approve fixes

## What This Does NOT Do

- Does not modify any existing files or code
- Does not change your design system or visual styling
- Does not remove or alter any existing CLAUDE.md content
