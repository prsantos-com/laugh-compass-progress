# Week 3 Progress Report - Laugh Compass

> **Dates:** Monday, September 29 - Sunday, October 5, 2025  
> **Active Days:** 7 of 7 planned  
> **Active Hours:** 15.5 of 14 planned

## 🛠️ Built

- Completely migrated from Firebase to a new flexible stack (Neon Postgres, Drizzle ORM, etc.).
- Enabled PostGIS extension in Neon and created events table with geospatial coordinate support.
- Built Server Action for event insertion with Zod validation to be in sync with database schema.
- Set up Drizzle code-first migrations workflow.
- Created functional admin page for adding comedy events.
- Built initial event listing page that successfully displays data from database in a card format.

## ✅ Decided

- Made a stack pivot after researching with Claude and ChatGPT. The main reason is that the components are easier to swap out and won't have me locked into the Firebase way of doing things. New stack: Vercel (hosting), Neon Postgres + Drizzle (DB). I would list more components I might use, but I may not get to that point if my first small bet doesn't pay off.
- Decided to make a much smaller feature set for my initial launch in order to ship sooner, which is why I didn't list of a bunch other tools I was going to use. Claude talked me out of it, when I told it to evaluate my idea based on the Small Bets approach talked about by [Daniel Vasello](https://dvassallo.com/).

## 💭 Stuck/Learned

- Claude baited me into actually shipping a working product quickly instead of over-planning, which turned out to be great advice. The weird part of that conversation was that it started being a jerk to me, when I kept asking it more questions. It just wanted me to ship.
- Hit a weird issue where Claude insisted on using the wrong Zod method (flatten() instead of flattenError()), claiming the correct method didn't exist even though I pointed it directly at the documentation. This was a good showcase of the limitations of strictly relying on LLMs.
- Migration setup required trial and error to understand the proper naming conventions and workflow.
- Discovered that Neon Postgres was surprisingly fast to set up and much smoother to work with than Firebase. Switching over was easier than expected.
- Learned about PostGIS and storing geospatial coordinates in Postgres for location-based queries.

## 👉 Next

- Finish all the admin functionality to smoothly add, edit, and delete events
- Style the main listings page properly, as well as past shows
- Add a map to place location of listings if time permits

## 📱 Screenshots

### Admin Page for Adding Comedy Events

![Admin page to add comedy event](https://github.com/prsantos-com/laugh-compass-progress/raw/main/screenshots/week-3-admin-add-comedy-event-page.png)

### Home Page (still humble and needs some love)

![Home page at week 3](https://github.com/prsantos-com/laugh-compass-progress/raw/main/screenshots/week-3-home-page.png)
