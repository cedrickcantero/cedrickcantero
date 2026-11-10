# Cedrick Cantero

**Full Stack Engineer · TypeScript · React / Next.js · Node.js · Supabase/Postgres**

I build and run production web apps end to end: schema, API, UI, CI, deployment, and what happens after launch. Most of my client work is private, so below are short write-ups of two live systems, followed by public code you can read.

---

### Production work (client projects · private repos)

**[Play4Serve](https://play4serve.thecedrickgroup.top/)** — court booking & operations platform<br>
Players book and pay for courts without an account; staff verify payments and run the venue from an admin console.<br>
`Next.js` `TypeScript` `Supabase (Postgres, Auth, Storage, pg_cron, Realtime)` `Vercel` `Sentry` `Vitest` `Playwright`
- **No double bookings:** 10-minute slot holds, a locking booking RPC, and a database-level unique index on active slots, so correctness doesn't depend on the client
- **Live updates without polling:** booking and admin screens refresh from Supabase Realtime change signals, with a slow safety poll as a fallback
- **Latency:** moved server functions from Virginia to Tokyo to sit beside the database, cutting a cross-Pacific round trip from every query
- **Trust & ops:** hash-chained audit log, role-based staff access with RLS, payment-proof verification queue, Sentry error tracking
- **Delivery:** 120+ test files including accessibility checks, CI on every push, staging → production promotion, semver releases with a changelog

**[River Dinks](https://riverdinks.thecedrickgroup.top/)** — court booking for a pickleball venue<br>
Account-free booking with e-wallet payment confirmation, staff management, and automated notifications.<br>
`Next.js 16` `TypeScript` `Tailwind CSS 4` `Supabase` `TanStack Query` `Zod` `Vercel` `Sentry`
- **Safe deploys:** the production build checks the live database's migration history and refuses to ship code ahead of its schema
- **Background work in the database:** notification outbox drained by a `pg_cron` worker, daily staff digests, automatic sweep of lapsed holds
- **Performance as a gate:** JS bundle budgets enforced in CI, plus Lighthouse runs compared against a stored baseline
- **Tested at both layers:** 110+ app test files and SQL test suites for database functions and policies, all in CI

---

### Code you can read

**[Smart Spend](https://github.com/cedrickcantero/smart-spend)** — personal finance app · [live demo](https://smart-spend-unique.vercel.app)<br>
`Next.js App Router` `TypeScript` `Supabase` `SQL migrations` `Recharts`<br>
~30 route handlers behind Supabase auth, versioned schema with generated types, admin area.

**[Restaurant Finder](https://github.com/cedrickcantero/restaurant-finder)** — LLM-powered search · [live demo](https://restaurant-finder-red.vercel.app)<br>
`Next.js 14` `TypeScript` `OpenRouter` `Foursquare API`<br>
Turns a natural-language request into a structured Places API query through a server-side route.

---

### Toolbox

**Languages** TypeScript, JavaScript, SQL<br>
**Frontend** React, Next.js, Tailwind CSS, TanStack Query, Radix / shadcn/ui<br>
**Backend & data** Node.js, Supabase, PostgreSQL (RLS, RPCs, pg_cron, Realtime), REST APIs<br>
**Quality & ops** Vitest, Playwright, GitHub Actions, Lighthouse CI, Sentry, Vercel

### Contact

[Portfolio](https://thecedrickgroup.top/) · [LinkedIn](https://linkedin.com/in/cedrick-cantero-755922161) · [Email](mailto:cmcantero28@gmail.com)
