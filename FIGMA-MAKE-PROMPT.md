# MARVEAUX Digital Studio — Figma Make Build Prompt

Build a production-ready, fully responsive portfolio website for **MARVEAUX Digital Studio**, the personal portfolio of **Alo Emmanuel Marvellous (Kitan)**.

Reference portfolio/video/PDF: https://drive.google.com/file/d/15c0Sp4yaLrUM_Wz05iQHuY8G0_FHD0p_/view?usp=drivesdk

Use the reference for the exact visual direction, spacing, composition, copy pattern, and interaction style. Do not redesign the brand identity. Extend it into a complete, polished website.

## Brand direction

- Near-black/dark navy background throughout.
- Purple accent range: `#8B3FE8` to `#A855F7`.
- Large editorial serif headlines; use italic serif emphasis for selected words.
- Small-caps, letter-spaced eyebrow labels above headings.
- Rounded cards with subtle borders, glass/blur surfaces, and restrained gradients.
- Sticky navigation: Home, About, Services, Portfolio, Case Studies, Pricing, FAQ, Reviews, Contact.
- Solid purple `Let's Talk` button pinned at the right of the navigation.
- Use generous spacing, strong typography hierarchy, smooth but restrained motion, and excellent contrast.
- Respect `prefers-reduced-motion`.

## Required sections in this exact order

### 1. Hero

Eyebrow: `MARVEAUX DIGITAL STUDIO`
Headline: `We Build Digital Experiences That Elevate Brands.` Make `Digital` and `Elevate` italic and purple.
Description: `MARVEAUX Digital Studio helps businesses grow through modern websites, strategic branding, motion graphics, and high-converting digital experiences.`
Stats: `24+ Projects`, `10+ Industries`, `3 Years`, `100-Day Writing Streak — Completed`, `#2 Wattpad Purity`.
Buttons: `View Portfolio` and `Start Your Project`.

### 2. About

Heading: `One person. Every skill you need.`
Use a professional portrait placeholder if the supplied asset is unavailable, but make the image slot easy to replace.
Use this copy exactly:

“I architect and ship full-stack products — frontend, backend, database, deployment, brand, and copy — end to end, alone, at a level most people need a four-person team for. 24+ live, production-deployed builds across fintech, healthcare, real estate, hospitality, fashion, education, and beauty in three-plus years. Every one of them is running in production right now, not sitting in a design file.

The last stretch of work changed how I build. I moved from shipping fast to shipping engineered: structured technical briefs, accessibility passes, live third-party API integrations, and real production deployment on Vercel. I now direct AI coding agents the way a lead engineer directs a junior dev: detailed spec, generated output, audit, fix, ship.

Anthropic-certified in prompt engineering, among the first in Nigeria to hold the credential. Published fiction author ranked #2 on Wattpad. Final-year B.Tech student at FUTA.”

Add a credibility strip for the supplied certifications without inventing extra certifications.

### 3. Services

Create modular service cards for:
- Full-Stack Development
- UI/UX Design
- Brand Strategy
- Copywriting & Content Strategy
- Prompt Engineering & AI Workflow Integration
- No-Code/AI-Assisted Builds (Figma Make, Bolt.new, Base44)

Each card needs a short, clear description and an understated hover state.

### 4. Portfolio

Heading: `Selected work across ten industries.`
Create a responsive project grid. Every card has a screenshot/image slot, project name, category tag, stack, and opens a case-study detail view or modal. Use real supplied assets where available; never use stock images when a real project asset is available.

Include all 24 projects:
1. TrustFlow Bank — Fintech Web App — React, Node.js, PostgreSQL
2. PureLife+ Hospital — Healthcare Website — HTML, CSS, JS, React
3. Atlas International Airport — Institutional Platform — React, JS, Node.js
4. Hospital Management System — Healthcare Web App — React, Node.js, PostgreSQL
5. LagosHomes — Real Estate — React, JS, CSS
6. NaijaHomes — Real Estate (AI-assisted) — Base44, React
7. MARVEAUX Digital Studio — Agency Website — HTML, CSS, JS, React, 3D
8. Pinnacle University — Academic Platform — React, CSS, Node.js
9. Still Life Home — Furniture E-Commerce — React, Tailwind, JS
10. VYBN Fashion Store — Fashion E-Commerce — React, JS, CSS
11. Glows Beauty — Booking Site — React, JS, CSS
12. Kartify — E-Commerce — React, JS, Node.js
13. KITAN Digital Studio — Personal Brand Site — React, JS, Node.js
14. Glam by Mira — Booking Site — React, Bolt, JS
15. CleanPro — Booking Site — React, Bolt, CSS
16. FixIt — Booking Site — React, JS, CSS
17. EatWell — Subscription Site — React, JS, CSS
18. ZenSpace — Membership Platform — React, Bolt, JS
19. Velvet & Vine — Salon & Spa Booking — Bolt.new, React, Tailwind
20. EventCraft — Events Platform — React, JS, CSS
21. Leo Digital Studio — Art Studio Site — React, JS, CSS
22. SkyCast — Weather PWA — React, Vite, Tailwind, Open-Meteo, Vercel
23. Built By Naija — Tribute Page — HTML, CSS, JS, Scroll Animation
24. Etched in Stone — Editorial Site — HTML, CSS, JS, Scroll Animation

Only SkyCast has a live link/badge:
https://skycast-weather-neon.vercel.app/
Do not add live links to any other project.

### 5. Case studies CTA

Eyebrow: `CASE STUDIES`
Heading: `Want to see the full body of work?`
Copy: `Twenty-four shipped projects, written up with context, decisions and outcomes.`
Button: `View Full Portfolio ↗`.
Open the supplied `Kitan_Portfolio_FULL_Updated.pdf` in an embedded Google-Docs-style viewer or modal. Do not regenerate the PDF or fabricate its contents.

### 6. Pricing

Heading: `Three ways to work together.`
Create three cards:
- Starter (Foundation): `A sharp, fast marketing site that earns trust on first load.` Up to 5 responsive pages, custom UI, performance and SEO setup, 2 weeks delivery.
- Growth (Momentum): `Site, identity and messaging built as one coherent system.` Up to 10 pages, CMS and analytics integration, motion and interaction design. Mark as `RECOMMENDED`.
- Full-Service (Everything): `A complete product build with AI woven into the workflow.` Unlimited scope, design system, ongoing iteration and performance tuning.

Use `Contact for pricing` for all figures. Do not fabricate prices. Include a Brand + Copy item in every tier.

### 7. CVs & résumés

Heading: `CVs & résumés, ready to download.`
Create cards and real download links for:
- Full-Stack Developer
- UX/UI Designer + Prompt Engineer
- Marveaux — Full-Stack Developer
- Marveaux — Prompt Engineer
- CV — Writer

Use `/assets/resumes/<slug>.pdf` paths. Until separate files are supplied, point every card to the same master `Kitan_Portfolio_FULL_Updated.pdf` rather than using dead buttons.

### 8. Project Brief Generator

Eyebrow: `PROJECT BRIEF`
Heading: `Not sure where to start?`
Copy: `Describe what you need in plain words. You'll get a tailored project brief and the package that fits best — in seconds.`
Fields: project description textarea, optional budget, optional timeline.
Button: `✦ Generate my brief`.

Build a real submission flow. Submit to a secure server-side endpoint such as `/api/brief`. The server must call Claude or another configured LLM without exposing API keys in the browser, return a structured brief and recommended pricing tier, and email the visitor input plus generated result to `aloemmanuel369@gmail.com` through Resend or SendGrid. Use environment variables only: `CLAUDE_API_KEY`, `RESEND_API_KEY` or `SENDGRID_API_KEY`.

### 9. Reviews

Heading: `What clients say — and what you think.`
Display existing supplied testimonials only; do not invent testimonials. Add a `Post Review` form with name, rating, and review text. On submit, save the review for public display and POST to `/api/reviews`, which emails the review to `aloemmanuel369@gmail.com`.

### 10. FAQ

Collapsed accordion, keyboard accessible, with:
- What services does MARVEAUX Digital Studio offer?
- Do you offer branding strategy or do you only design UI?
- How does the process work from initial idea to final delivery?
- Do you offer support after the project goes live?
- What's your turnaround time?
- Do you work with international clients?

### 11. Contact

Heading: `Tell me what you're building.`
Copy: `Remote-first, working with clients worldwide. Every enquiry gets a direct reply — no account managers in between.`
Fields: Name, Email, Project Type dropdown, Budget, Message.
Button: `Send Message`.
Contact cards: LinkedIn (`linkedin.com/in/aloemmanuel`), GitHub (`github.com/aloemmanuel369-hue`), Vercel (`vercel.com/marveaux-digital-studio`), Email.
POST to `/api/contact`; validate client-side and server-side; email all details to `aloemmanuel369@gmail.com`.

### 12. Footer

Logo and `MARVEAUX — DESIGN. DEVELOP. ELEVATE.`
Social links for GitHub, LinkedIn, and email.
Copyright: `© 2026 MARVEAUX Digital Studio. All rights reserved.`

## Functional requirements

- Build with React + Vite + Tailwind CSS.
- Use modular components, one component per major section.
- Fully responsive for mobile, tablet, and desktop.
- Semantic HTML, keyboard navigation, visible focus states, ARIA labels, and strong color contrast.
- Add loading, success, and error states to all forms.
- Never silently lose submissions: if email delivery fails, log/store the submission and show a clear error state.
- Use Vercel serverless functions under `/api/*` for contact, review, and brief flows.
- Never expose API keys client-side and never commit secrets.
- Use `prefers-reduced-motion` to disable or reduce animation.
- Add an accessible embedded PDF viewer/modal for the full portfolio.
- Use real `<a href="..." download>` links for résumé downloads.
- Do not fabricate metrics, pricing, testimonials, project links, screenshots, or certification details.

## Deployment checklist

- Generate a complete runnable project, not a static mockup.
- Add `.env.example` documenting `CLAUDE_API_KEY`, `RESEND_API_KEY` or `SENDGRID_API_KEY`, and any storage/database variables.
- Run `npm install` and `npm run build` with zero errors.
- Explain any missing assets or environment variables.
- Before production, configure the variables in Vercel and test all three email flows to `aloemmanuel369@gmail.com`.
- Do not claim email delivery works until the real provider credentials are configured and tested.
