# Cedrick Cantero

Full stack engineer working mostly with TypeScript, Next.js and Supabase. I build web apps for clients on my own, from the database to the live site, and I keep them running after launch.

Most of my client code is private, so here is what two of the live apps do.

## Client work

### [Play4Serve](https://play4serve.thecedrickgroup.top/)

Court booking for a pickleball venue. Players book and pay without signing up, and staff check payments and manage the day from an admin page.

- Two people can never book the same court at the same time. The database itself blocks it, not just the app.
- Booking screens update live the moment anything changes.
- I moved the servers to Tokyo, next to the database, so pages load faster for players in the Philippines.
- Every staff action is logged, and each staff member only sees what their role allows.
- Over 120 automated test files run on every change, and new versions go through a test site before going live.

Built with Next.js, TypeScript and Supabase, hosted on Vercel.

### [River Dinks](https://riverdinks.thecedrickgroup.top/)

Booking for another pickleball venue, with e-wallet payments, staff management and automatic notifications.

- A safety check stops a release from going live if the database isn't ready for it.
- Booking updates and daily staff summaries are sent automatically.
- Automated checks block any change that would make the site noticeably slower.
- Over 110 automated test files, covering both the app and the database.

Built with Next.js, TypeScript and Supabase, hosted on Vercel.

## Public code

- [Smart Spend](https://github.com/cedrickcantero/smart-spend): a personal finance app for tracking spending, budgets and subscriptions, with user accounts and an admin area. [Live demo](https://smart-spend-unique.vercel.app)
- [Restaurant Finder](https://github.com/cedrickcantero/restaurant-finder): describe what you want to eat in plain English, and it uses AI to find matching restaurants. [Live demo](https://restaurant-finder-red.vercel.app)

## Tools

TypeScript, JavaScript, React, Next.js, Node.js, Supabase, PostgreSQL, Tailwind, Playwright, Vercel

## Contact

[Portfolio](https://thecedrickgroup.top/) | [LinkedIn](https://linkedin.com/in/cedrick-cantero-755922161) | [Email](mailto:cmcantero28@gmail.com)
