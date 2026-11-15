# prasansingh.com — production handoff

Static personal site for Prasan Singh. No build step, no framework. Deploy as-is to Vercel and point prasansingh.com at it.

## What's here

| Path | What it is |
|---|---|
| `index.html` | The whole site. Tabs (home, work, hacker houses, community design, mentorship & judging, gallery) are hash routes inside this one file. |
| `debrief.html` | The stippled Arweave India system diagram (p5.js), embedded in the community design tab via an iframe. |
| `img/` | 21 gallery photos (`g-p1…21.webp`) and the hover photo (`me.webp`). |
| `og.png` | 1200×630 link-preview image. `index.html` points to it at `https://prasansingh.com/og.png`. |
| `prasan-singh-cv.pdf` | CV. The top "cv" link opens it in a new tab. |
| `robots.txt`, `sitemap.xml` | Basic SEO. |

Fonts: Newsreader and JetBrains Mono are self-hosted in `fonts/` (copied from Google Fonts, SIL OFL) and declared inline in `index.html`. External loads are only in `debrief.html`: Google Fonts (Space Mono) and p5.js from cdnjs.

## Task

1. `git init`, commit everything, and push to a new **private** GitHub repo named `prasansingh.com` under the user's account (`gh repo create prasansingh.com --private --source=. --push`).
2. Deploy to Vercel as a static site (framework preset: Other, no build command, output directory `.`):
   - Either `npx vercel --prod` from this folder, or import the GitHub repo in the Vercel dashboard.
3. Add the domain: `npx vercel domains add prasansingh.com` (and `www.prasansingh.com` redirecting to the apex). If the domain is already on the user's Vercel account, just attach it to this project.
4. Verify after deploy:
   - `https://prasansingh.com` loads; every tab works (`#work`, `#hacker-houses`, `#community`, `#judging`, `#gallery`).
   - Gallery images and `img/me.webp` load (hover the name on desktop).
   - The debrief diagram renders inside the community design tab.
   - The "cv" link opens the PDF in a new tab.
   - Link preview works: check with https://www.opengraph.xyz/url/https%3A%2F%2Fprasansingh.com or paste into X/LinkedIn.

## Rules

- Don't change copy, numbers or layout. The content was finalised line by line with the user.
- Don't add a framework, bundler or analytics without asking.
- Ask the user before buying anything, changing DNS records at a registrar outside Vercel, or making the repo public.
