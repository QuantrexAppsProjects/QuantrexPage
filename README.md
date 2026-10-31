# QuanTrexApps website

The public website for **QuanTrexApps** (www.quantrexapps.com). Blue Edition, English and Spanish.

## Files

| File | What it is |
|---|---|
| `index.html` | The whole site in one file: all pages, styles, scripts, logos and both languages |
| `assets/portfolio/` | Screenshots for the Portfolio page (WebP) |
| `CNAME` | Custom domain for GitHub Pages (`www.quantrexapps.com`). Don't delete it. |
| `README.md` | This file |

The only things loaded from outside are Google Fonts, three.js (for the 3D logo) and FormSubmit (for the contact form). If three.js can't load, the flat logo is shown instead.

## Deploying

1. Commit your changes on `develop`.
2. Merge `develop` into the branch GitHub Pages publishes from (usually `main`) and push.
3. GitHub Pages updates www.quantrexapps.com within a minute or two.

## Pages

Home, Services, Work, Portfolio, Method, Engage, Notes, About and Contact are separate pages inside `index.html`. Each has its own link, for example `https://www.quantrexapps.com/#services`.

## Languages (English / Spanish)

- Visitors switch with the ENG / ESP buttons in the header. The choice is remembered, and first-time visitors whose browser is set to Spanish see Spanish.
- Link straight to a language with `?lang=es` or `?lang=en`, for example `https://www.quantrexapps.com/?lang=es#contact`.
- **When you change any English text, change the Spanish too.** Spanish lives in two places in `index.html`:
  - `ES_TEXT`, a dictionary keyed by the original English HTML. If you edit an English sentence, update its key and its Spanish value, or that sentence will stay in English on the Spanish site.
  - The Spanish arrays in the script: `WORDS` (scrolling strip), `LOGS` (build log), `STMT` (Home statement), `scopesEs` (scope dial), `casesEs` (Work page), `SPEC_EX` (spec compiler examples).
- Spanish style: Mexican Spanish, informal "tú". Budgets are marked USD.

## Portfolio

The Portfolio page is built from the `PROJECTS` list in the script, so every project uses the same layout: a browser-window frame with the screenshot, a project number, category, description, features, tags and two buttons. Projects alternate sides automatically.

To add a project:

1. Save a desktop screenshot (about 1200px wide) as WebP in `assets/portfolio/`, for example `assets/portfolio/myproject-home.webp`.
2. Copy the TraduceDoc entry in `PROJECTS` and fill in `name`, `domain`, `url`, `img`, `w` and `h` (the image's width and height in pixels), plus the English and Spanish `alt`, `cat`, `summary`, `feats`, `tags` and `chips`.
3. Newest or most important project first.

## Contact form

- "Send my brief" emails the brief to quantrexapps@gmail.com through FormSubmit. Briefs sent in Spanish arrive with Spanish field names and an "Idioma: Español" line.
- **First time only:** after the site is live, send a test brief. FormSubmit emails an activation link to quantrexapps@gmail.com. Click it, and from then on every brief is delivered.
- Optional: once activated, FormSubmit gives you a random code. Replace the email address in the line starting `const FORM_ENDPOINT=` with that code, so the address isn't visible in the page source.
- If sending fails, visitors get a **Send email** button (opens their email app) and **Copy brief**, so nothing is lost.

## Brand rules

- Always write the company name in full: **QuanTrexApps**. Never "Quantrex" or "QuanTrex".
- Logo colours: dark purple `#320D6B`, violet `#6627E7`. Don't recolour the Q mark; on dark backgrounds it gets a white outline.
- Site palette: navy `#050A24`, blue `#2D5BFF`, violet `#8456FF`, cyan `#2EE6F6`. Fonts: Sora, Manrope, JetBrains Mono.

## Before launch

- Replace the Instagram and Facebook links in the footer (they point to the platforms' home pages) with the real QuanTrexApps pages.
- The Work page shows example project blueprints, not real clients. Swap in real projects when you can share them.
- Keep only the commitments you'll honour (2-week sprints, day-1 repo access, code ownership, written change control).
- Have a native Mexican Spanish speaker read the Spanish once.
