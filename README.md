# FUzae.hub
Premium glassmorphism site — React + Vite + Framer Motion + Lucide. Plain CSS (no Tailwind); canvas particles + CSS 3D (no Three.js) for performance.

## Run
```bash
npm install
npm run dev      # local dev
npm run build    # production build in /dist
```

## Edit your links
Everything lives in **`src/config/links.js`**: Telegram (`TELEGRAM_CHANNEL_URL` placeholder), Editing News, ItzrchMethod, Payhip, TikTok, WhatsApp, notification email.

## Email notifications (FormSubmit) — IMPORTANT
Each username is POSTed (AJAX, no redirect) to `https://formsubmit.co/ajax/fuzaeeditor@gmail.com`.
**The first submission triggers an activation email from FormSubmit to fuzaeeditor@gmail.com. Open it (check spam) and click "Activate". Until you do, notifications will not arrive.**
To test: deploy, open the site in a private window, submit a username, then confirm the activation email.
If delivery fails, the visitor sees a discreet message and still enters. A honeypot field + timing check blocks basic bots.
Session: username saved in localStorage for 30 days (`SITE.sessionDays`); click the username in the navbar to change it.

## Deploy on Vercel
1. Push this folder to GitHub.
2. vercel.com → Add New Project → import the repo (Vite is auto-detected).
3. Deploy. `vercel.json` handles SPA routing so direct links like `/qualityboost/uploadmethod` work.
