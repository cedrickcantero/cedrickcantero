# Cedrick Cantero

Full stack engineer working mostly in TypeScript, Next.js and Supabase/Postgres. I build web apps for clients on my own, from the database schema to deployment, and I keep them running after launch.

Most of my client code is private, so here is what two of the live apps do.

## Client work

### [Play4Serve](https://play4serve.thecedrickgroup.top/)

Court booking for a pickleball venue. Players book and pay without an account, and staff check payments and run the day from an admin console.

- Slot holds, a locking booking function and a unique index in Postgres stop double bookings, even when two people book the same slot at once.
- Screens update through Supabase Realtime instead of polling.
- I moved the server functions from Virginia to Tokyo, next to the database, since all the players are in the Philippines.
- Audit log, staff roles enforced with row-level security, and Sentry for errors.
- 120+ test files, CI on every push, and versioned releases through a staging branch.

Next.js, TypeScript, Supabase, Vercel, Sentry, Vitest, Playwright

### [River Dinks](https://riverdinks.thecedrickgroup.top/)

Booking for another pickleball venue, with e-wallet payment confirmation, staff management and automatic notifications.

- The production build checks the live database's migrations and stops if the code is ahead of the schema.
- Notifications go through an outbox table that a pg_cron job sends, plus a daily digest for staff.
- CI fails if the JavaScript bundle grows past its budget, and Lighthouse scores are compared against a baseline.
- 110+ app test files, plus SQL tests for the database functions and access policies.

Next.js 16, TypeScript, Tailwind 4, Supabase, TanStack Query, Zod, Vercel, Sentry

## Public code

- [Smart Spend](https://github.com/cedrickcantero/smart-spend): personal finance app with auth, about 30 API routes, SQL migrations and an admin area. [Live demo](https://smart-spend-unique.vercel.app)
- [Restaurant Finder](https://github.com/cedrickcantero/restaurant-finder): describe what you want to eat in plain English, and an LLM turns it into a Foursquare search. [Live demo](https://restaurant-finder-red.vercel.app)

## Tools

TypeScript, JavaScript, SQL, React, Next.js, Tailwind, TanStack Query, Node.js, Supabase, PostgreSQL, Vitest, Playwright, GitHub Actions, Sentry, Vercel

## Contact

[Portfolio](https://thecedrickgroup.top/) | [LinkedIn](https://linkedin.com/in/cedrick-cantero-755922161) | [Email](mailto:cmcantero28@gmail.com)
