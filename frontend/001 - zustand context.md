## 001 - Zustand Context

**Status:** Accepted

**Date:** 23 / 07 / 2025

---

## Context

On deployment at Vercel (not local build): in cart parallel routes useEffect which is depending on authStore initializing doesn't re-rended on initializing auth store

---

## Decision

Use custom components to initialize Zustand stores that work on layout instead of parallerl routes

---

## Consequences

- Cannot access params and searchParams directly as in routes
- More clean code due to not having much folders at (app) directory
