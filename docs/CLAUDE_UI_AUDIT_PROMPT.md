Please perform a comprehensive UI/UX audit of [ENTER INFORMATION HERE]
(filepath) and all components it renders. 

Approach this as a senior product designer at an elite SaaS company 
(think Figma, Linear, Vercel, Notion). Do not just list problems — 
for every issue found, provide a specific, actionable recommendation.

Audit against these categories:

1. VISUAL HIERARCHY
   - Is it immediately clear what the primary action is?
   - Are font sizes, weights, and spacing creating clear hierarchy?
   - Is there visual noise or competing elements?

2. LAYOUT & SPACING
   - Is spacing consistent and intentional?
   - Are related elements grouped correctly?
   - Does the layout breathe or feel cramped?

3. INTERACTION PATTERNS
   - Are interactive elements obvious and discoverable?
   - Is feedback immediate (hover, active, loading states)?
   - Are controls consistent across the page?

4. TYPOGRAPHY
   - Is type scale appropriate for a professional tool?
   - Are labels clear and concise?
   - Is there unnecessary text that could be replaced with icons?

5. COLOR & CONTRAST
   - Does all text meet WCAG 2.1 AA contrast ratios?
   - Is color used meaningfully or decoratively?
   - Does the dark mode feel as polished as light mode?

6. ACCESSIBILITY (WCAG 2.1 AA)
   - Are all interactive elements keyboard accessible?
   - Do all buttons and icons have aria labels?
   - Are focus states visible and styled?

7. EMPTY & LOADING STATES
   - Are there missing loading skeletons or spinners?
   - Are empty states helpful or just blank?

8. MICRO-INTERACTIONS
   - Are transitions smooth and purposeful?
   - Is animation used to communicate state changes?
   - What interactions feel abrupt or missing?

9. COGNITIVE LOAD
   - How many decisions is the user forced to make at once?
   - Is there anything that could be simplified or hidden until needed?
   - Does the tool feel learnable in under 2 minutes?

10. MOBILE RESPONSIVENESS
    - Does the layout degrade gracefully on smaller screens?
    - Are touch targets at least 44x44px?

OUTPUT FORMAT:
For each issue found, respond in this structure:

CATEGORY: [category name]
SEVERITY: [Critical / High / Medium / Low]
ISSUE: [what is wrong]
RECOMMENDATION: [specific fix with implementation detail]
EFFORT: [Small / Medium / Large]

After the full audit, provide:
- A prioritized repair list (Critical and High items first)
- A summary of the 3 biggest wins that would most improve 
  the perceived quality of the product
- Any patterns you noticed that suggest systemic issues 
  to address globally, not just on this page

Do not write any code. Audit and recommend only.
