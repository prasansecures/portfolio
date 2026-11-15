# prasan portfolio

Static personal site for Prasan Singh (prasansingh.com). No build step, no framework.

- `index.html` — the whole site; tabs are hash routes (`#work`, `#hacker-houses`, `#community`, `#judging`, `#gallery`)
- `debrief.html` — p5.js Arweave India diagram, iframed in the community tab
- `img/`, `og.png`, `prasan-singh-cv.pdf`, `robots.txt`, `sitemap.xml`

Run locally: `python3 -m http.server 8000`
Deploy: Vercel, framework preset "Other", no build command, output directory `.`
