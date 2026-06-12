<div align="center">

# The Raw Studios

**Music Academy Website · Node.js + Express + EJS + Google Reviews**

[![Node.js](https://img.shields.io/badge/Node.js-18+-339933?style=flat-square&logo=node.js&logoColor=white)](https://nodejs.org)
[![Express](https://img.shields.io/badge/Express-4.x-000000?style=flat-square&logo=express&logoColor=white)](https://expressjs.com)
[![Vercel](https://img.shields.io/badge/Deployed%20on-Vercel-000000?style=flat-square&logo=vercel&logoColor=white)](https://vercel.com)
[![License](https://img.shields.io/badge/License-MIT-blue?style=flat-square)](LICENSE)

*Official website for The Raw Studios — a performing arts academy in Zirakpur, Punjab, offering singing, guitar, flute, and Kathak dance.*

</div>

---

## About The Raw Studios

**The Raw Studios** is a music and performing arts academy based in **Zirakpur, Punjab, India**. The website showcases courses, instructors, and real student testimonials pulled live from Google Reviews.

Built with a clean Node.js + EJS stack, deployed serverlessly on Vercel, with a Google Reviews integration that uses a 5-minute in-memory cache and gracefully falls back to curated mock reviews when the API is unavailable — so the site never shows an empty state.

---

## Pages

| Route | Description |
|---|---|
| `/` | Home — hero, featured courses, instructor highlights |
| `/courses` | Full course catalogue (Singing, Guitar, Flute, Kathak) |
| `/about` | Academy story, team, and philosophy |
| `/label` | Music label / original productions |
| `/contact` | Enquiry form and location |

---

## Features

- **Live Google Reviews** — Fetches real student reviews via Google Places API; 5-minute cache; automatic fallback to mock reviews if API is unavailable
- **Course Catalogue** — Detailed breakdown of all disciplines offered
- **Instructor Profiles** — Teaching staff and specialisations
- **Responsive Design** — Mobile-first layout across all pages
- **Serverless** — Zero-config Vercel deployment via `vercel.json`

---

## Tech Stack

| Layer | Technology |
|---|---|
| Runtime | Node.js 18+ |
| Framework | Express.js |
| Templating | EJS |
| Reviews API | Google Places API (axios) |
| Deployment | Vercel (Serverless) |

---

## Project Structure

```
raw-studios/
├── server.js           # Express server, routes, Google Reviews fetch + cache
├── vercel.json         # Vercel serverless config
├── package.json
├── views/
│   ├── index.ejs       # Home page
│   ├── courses.ejs     # Course catalogue
│   ├── about.ejs       # About the academy
│   ├── label.ejs       # Music label page
│   ├── contact.ejs     # Contact & enquiries
│   └── partials/       # Shared header, footer, nav
└── public/             # Static assets (CSS, images)
```

---

## Local Development

```bash
git clone https://github.com/CYBERSAREEN/raw-studios.git
cd raw-studios
npm install

# Optional: Google Places API key for live reviews
echo "GOOGLE_PLACES_API_KEY=your_key_here" > .env
echo "GOOGLE_PLACE_ID=your_place_id_here" >> .env

npm start
```

Open [http://localhost:3000](http://localhost:3000)

> Without the Google API key, the site serves polished mock reviews automatically — no crash, no empty state.

---

## Deploy to Vercel

```bash
npm install -g vercel
vercel --prod
```

Add `GOOGLE_PLACES_API_KEY` and `GOOGLE_PLACE_ID` as Vercel Environment Variables for live reviews in production.

---

## Author

**Vedant Sareen — CYBERSAREEN**
📧 securecybernetics@gmail.com · [GitHub](https://github.com/CYBERSAREEN)

---

<div align="center">

*Built for The Raw Studios, Zirakpur · Where music meets craft.*

</div>
