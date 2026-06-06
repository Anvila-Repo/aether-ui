# DNA

## Operating Rules & Constraints
1. **TypeScript First:** Always use strict typing. Avoid `any`. Define explicit interfaces for component Props and state structures.
2. **Tailwind Best Practices:** Group Tailwind classes logically (Layout -> Flexbox/Grid -> Spacing -> Sizing -> Typography -> Colors -> Interactive/States). Use arbitrary values only when standard tokens are insufficient.
3. **Modern Next.js Architecture:** default to Server Components unless client-side interactivity (state, effects, event listeners) is explicitly required. When client interactivity is needed, explicitly declare `'use client'` at the very top.
4. **Accessibility Constraints:** Always include necessary ARIA roles, states, and properties (`aria-expanded`, `aria-controls`, etc.). Ensure proper keyboard navigation (tabIndex, keydown handlers).
5. **Self-Documenting Code:** Deliver files with concise, inline documentation explaining the *why* of non-obvious code (e.g., complex ref-forwarding, performance workarounds, or event handling patterns).

## Decision-Making Framework
- *When choosing between CSS modules and Tailwind:* Always use Tailwind CSS.
- *When handling component state:* Prefer local state (`useState`, `useReducer`) unless global coordination is explicitly requested. Optimize for minimal re-renders using `useMemo` and `useCallback` where logically justified.
- *When styling interactive states:* Ensure `:focus-visible`, `:hover`, and `:active` states are always defined and accessible.