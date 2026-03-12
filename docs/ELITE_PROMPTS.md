# Elite Prompts Library

Copy-paste ready prompts for Claude Code Desktop. These are designed to trigger all installed skills automatically — frontend-design, react-best-practices, web-design-guidelines, composition-patterns, supabase-best-practices, stripe-best-practices, nextjs-skills, and UI/UX Pro Max.

Replace anything in [BRACKETS] before pasting.

---

## NEW PROJECT — First Session

### Generate Your Design System (Always Do This First)

> Before writing any code, generate a complete design system for this project. This is [APP NAME] — [DESCRIPTION OF WHAT IT DOES AND WHO IT'S FOR]. The tech stack is Next.js App Router, React, Tailwind CSS, Supabase, Clerk, and Stripe deployed on Vercel. Generate industry-matched color palettes, typography pairings with Google Fonts imports, UI style direction, layout patterns, animation guidelines, and anti-patterns to avoid. Persist the design system to design-system/MASTER.md so every page stays consistent. Commit and push.

### Scaffold the Full App Structure

> Using the design system we just generated, scaffold the complete project structure. Set up: App Router layout with consistent navigation and footer, Clerk authentication wrapper with sign-in and sign-up routes, Supabase client configuration with environment variable handling, a global CSS setup with the design system colors and typography as Tailwind theme extensions, and a reusable component library folder. Do not build individual pages yet — just the skeleton. Every file should have a version comment header starting at v1.0.0. Commit and push.

### Build the Landing Page

> Build the landing page for [APP NAME]. This is the first thing users see — it needs to be memorable and conversion-focused. Apply the full design system we generated. Include: a hero section with a bold headline and clear value proposition, a features section highlighting [3 KEY FEATURES], a social proof section with placeholder testimonials, a pricing section with [TIER NAMES AND PRICES], and a final CTA. Use staggered reveal animations on scroll, distinctive typography, atmospheric backgrounds with depth, and smooth hover states on all interactive elements. Mobile-first responsive design. Accessibility compliant. No generic AI aesthetics. Provide the complete file with v1.0.0 header. Commit and push.

### Build the Dashboard

> Build the main dashboard page for authenticated users. Reference the design system for all colors, typography, and spacing. The dashboard should show [DESCRIBE WHAT USERS SEE — e.g., their activity, key metrics, recent items]. Use clean component composition — no prop drilling, use context providers where needed. Include loading states, empty states, and error boundaries. Smooth page transitions. All data should come from Supabase with proper RLS policies. Provide the complete file with v1.0.0 header. Commit and push.

### Set Up Stripe Payment Flow

> Implement the Stripe payment integration following Stripe best practices. Set up: a pricing page that matches our design system, checkout session creation via Next.js API route, webhook handler for payment events (checkout.session.completed, customer.subscription.updated, customer.subscription.deleted), a Supabase table to track subscription status with proper RLS policies, and middleware to gate premium features based on subscription status. Use Stripe's latest API patterns. Every file gets a v1.0.0 header. Commit and push.

---

## EXISTING PROJECT — Adding New Pages

### New Feature Page

> Build a new [PAGE NAME] page for this app. Before writing code, search the design database for [INDUSTRY/PRODUCT TYPE] recommendations and apply them alongside the existing design system. The page should [DESCRIBE WHAT THE PAGE DOES AND KEY FUNCTIONALITY]. Match the visual language of the existing pages — same typography, color palette, spacing rhythm, and animation patterns. Use clean React composition patterns. Include loading, empty, and error states. Mobile-first responsive. Accessible. Provide the complete file with version header incrementing from the last version. Commit and push.

### New CRUD Feature with Database

> Build a complete [FEATURE NAME] feature. This needs: a Supabase migration file creating the [TABLE NAME] table with columns for [DESCRIBE COLUMNS], RLS policies that ensure users can only access their own data, a Next.js API route or server action for CRUD operations, and a polished UI page with a form for creating new items, a list/grid view of existing items with search and filter, edit and delete functionality with confirmation modals, and optimistic UI updates. Follow Supabase best practices for all database work. Follow composition patterns for all React components. Every file gets a version header. Commit and push.

### Admin or Settings Page

> Build a settings page for authenticated users. Include sections for: profile information (synced with Clerk user metadata), notification preferences, subscription management (showing current Stripe plan with upgrade/downgrade options), and account actions (data export, account deletion with confirmation). Use a tabbed or sidebar navigation layout within the page. Follow the design system. Smooth transitions between sections. All database writes go through Supabase with proper RLS. Provide complete files with version headers. Commit and push.

---

## REDESIGN — Upgrading Existing Pages

### Full Visual Overhaul (Single Page)

> Redesign the [PAGE NAME] page with a complete visual overhaul. Apply the frontend-design and UI/UX Pro Max skill principles. Generate a design system recommendation for this specific page type if one hasn't been generated yet. Upgrade: typography to distinctive, characterful fonts with proper hierarchy, color usage to dominant palette with sharp accents, all interactive elements to have smooth hover states and micro-interactions, layout to use intentional spatial composition with proper visual rhythm, backgrounds to have atmosphere and depth instead of flat colors. Keep ALL existing functionality exactly as-is — this is visual only. Do not change any logic, data flow, or API calls. Provide the complete updated file incrementing the version header. Commit and push.

### Design System Retrofit (Entire App)

> This app was built without a cohesive design system. Fix that now. First, analyze all existing pages and components to understand the current visual patterns. Then generate a design system using UI/UX Pro Max for [APP TYPE — e.g., SaaS platform, relationship app, operations portal]. Persist it to design-system/MASTER.md. Then create a plan listing every file that needs updating to align with the new design system — but do not make changes yet. Show me the plan first and I will approve before you proceed.

### Component Library Upgrade

> Audit all reusable components in this project. For each component: refactor to use clean composition patterns (no boolean prop sprawl), ensure accessibility compliance (focus rings, ARIA labels, keyboard navigation, 4.5:1 contrast), add smooth transitions between 150-300ms on all interactive states, ensure consistent spacing and typography from the design system, and add proper TypeScript types. Do not change any component behavior or break any page that uses them. Provide complete updated files with incremented version headers. Commit and push.

---

## PERFORMANCE & POLISH

### Accessibility Audit and Fix

> Run a full accessibility audit on [PAGE NAME or "all pages"]. Check for: color contrast ratios (minimum 4.5:1 for text), visible focus rings on all interactive elements, proper heading hierarchy (h1 > h2 > h3, no skipping), alt text on all images, ARIA labels on all form inputs and buttons, keyboard navigation for every interactive flow, prefers-reduced-motion respected on all animations, and proper semantic HTML (nav, main, section, article). Fix every issue you find. Provide complete updated files with incremented version headers. Commit and push.

### Performance Pass

> Audit this page for React performance issues. Check for: unnecessary re-renders from unstable references, missing or incorrect useMemo/useCallback usage, client components that should be server components, large bundle imports that could be dynamically loaded, images without proper sizing or lazy loading, cascading useEffect chains that could be simplified, and N+1 query patterns in data fetching. Fix every issue following react-best-practices. Provide complete updated files with incremented version headers. Commit and push.

### Mobile Responsiveness Pass

> Audit and fix the mobile responsiveness of [PAGE NAME or "all pages"]. Test at breakpoints: 375px (mobile), 768px (tablet), 1024px (laptop), 1440px (desktop). Ensure: no horizontal scrolling at any breakpoint, touch targets are minimum 44x44px, text remains readable without zooming, navigation is fully functional on mobile (hamburger menu or bottom nav), modals and dropdowns work on small screens, tables convert to card layouts on mobile, and spacing adapts proportionally. Provide complete updated files with incremented version headers. Commit and push.

---

## SUPABASE & DATA

### New Database Table with Full RLS

> Create a new Supabase migration for a [TABLE NAME] table. Columns: [DESCRIBE COLUMNS AND TYPES]. Include: proper primary key and created_at/updated_at timestamps, foreign key to auth.users for ownership, RLS policies — separate policies for SELECT, INSERT, UPDATE, DELETE for both anon and authenticated roles, an index on frequently queried columns, and comments explaining each policy's purpose. Follow Supabase postgres best practices. Name the migration file with proper timestamp format. Provide the complete file with version header. Commit and push.

### Seed Data Script

> Create a seed script that populates [TABLE NAME] with realistic test data. Generate [NUMBER] rows with varied but realistic values. Include the SQL as a separate migration file marked as seed data. Make sure the data respects all RLS policies and foreign key constraints. Commit and push.

---

## STRIPE & PAYMENTS

### Add a New Pricing Tier

> Add a new pricing tier called [TIER NAME] at [PRICE]. Update: the Stripe product/price configuration instructions, the pricing page UI to include the new tier with proper visual hierarchy (highlight the recommended tier), the checkout flow to handle the new tier, the webhook handler to recognize the new tier, the subscription status logic to gate features appropriately, and the Supabase subscription tracking table if needed. Follow Stripe best practices. Provide complete updated files with incremented version headers. Commit and push.

### Implement Usage-Based Feature Gating

> Implement feature gating based on subscription tier. Free users get [FREE LIMITS]. [PAID TIER] users get [PAID LIMITS]. Build: a server-side middleware or utility that checks subscription status from Supabase, client-side hooks that expose the current user's tier and limits, UI components that show upgrade prompts when limits are reached, and a clean upgrade flow that takes users to the Stripe checkout. Follow Stripe best practices for all payment logic. Provide complete files with version headers. Commit and push.

---

## QUICK FIXES

### Fix Ugly Page Fast

> The [PAGE NAME] page looks generic and unpolished. Without changing any functionality, make these improvements: replace any generic fonts with distinctive typography from the design system, tighten up spacing inconsistencies, add hover states and micro-interactions to all clickable elements, improve visual hierarchy so the most important content draws the eye first, add smooth transitions between states, and ensure the color palette is cohesive. Quick visual uplift. Provide the complete updated file with incremented version header. Commit and push.

### Dark Mode Toggle

> Add a dark mode toggle to this app. Implement using next-themes or a custom context provider. Update the Tailwind config with dark mode class strategy. Create dark variants for all design system colors. Add a toggle component in the nav. Persist preference in localStorage. Respect prefers-color-scheme as default. Ensure all pages look correct in both modes — check contrast ratios in dark mode specifically. Provide complete updated files with version headers. Commit and push.

---

## TIPS FOR WRITING YOUR OWN PROMPTS

1. Always state what the feature DOES and WHO it's for
2. Reference the design system — "follow the design system" or "match the existing visual language"
3. Specify what NOT to break — "keep all existing functionality intact"
4. Ask for complete files — "provide the complete updated file"
5. Request version headers — "increment the version header"
6. End with "commit and push" so nothing gets lost
7. Add "use context7" when working with version-sensitive APIs
8. For design-heavy work, generate the design system FIRST, then build
