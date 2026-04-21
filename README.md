# TrueTrace

A mobile-web wireframe for a product transparency app — *The Living Ledger* of origin, ethics, and sustainability for every item in your cart.

On desktop the app is rendered inside a centered phone frame (420 × 900) so the
experience is always presented at mobile proportions, not stretched to the window.
On a phone browser it fills the viewport edge-to-edge.

## The narrative

Every screen threads the same product through the flow so the experience feels
coherent, not like a gallery of unrelated mocks:

> **Altura Organic Coffee** — a 340 g single-origin bag grown at 1,820 m by the
> Finca La Esperanza co-op in Huila, Colombia. Scanned by **Anju Sharma** in
> Hackney, London, two minutes ago.

- **Scan** → finds Altura Organic Coffee
- **Product** → shows its score (A), footprint, and story
- **Supply chain** → traces the 5 stops from farm to shelf
- **Certifications** → lists the 4 audits backing the score
- **Impact** → Anju's cumulative monthly footprint and milestones
- **Profile** → Anju's account, library, and settings

## Structure

```
.
├── index.html             # Welcome splash
├── home.html              # Anju's dashboard
├── scan.html              # Live scanner
├── product.html           # Altura Organic Coffee detail
├── supply-chain.html      # 5-stop journey, farm → shelf
├── certifications.html    # Fair Trade, Organic, RA, B Corp
├── impact.html            # Monthly footprint + milestones
├── profile.html           # Anju's account
├── styles.css             # Shared tokens + phone-frame layout
├── DESIGN.md              # The Ethical Editorial design system
└── assets/                # (legacy screenshots, not referenced by app)
```

Stack: **Plus Jakarta Sans** + **Fraunces** (Google Fonts), **Material Symbols Outlined**,
and a small hand-written `styles.css`. No build step, no framework.

## Run locally

```sh
cd truetrace-app
python3 -m http.server 8000
# visit http://localhost:8000
```

Opening `index.html` directly in a browser also works.

## Deploy to GitHub Pages

```sh
git init
git add .
git commit -m "Initial commit: TrueTrace wireframe"
git branch -M main
git remote add origin https://github.com/<you>/truetrace.git
git push -u origin main
```

Then in GitHub → **Settings → Pages** → source: `main` / `(root)`. The site goes live at
`https://<you>.github.io/truetrace/` in under a minute.

## Design language

Deep forest greens on paper-white surfaces, no 1px borders, tonal layering instead
of shadows, a small terracotta accent for warmth, and **Fraunces** italics used sparingly
on display headlines for an editorial-broadsheet feel. Full spec in
[`DESIGN.md`](./DESIGN.md).
