# Ilaria Rossi — Portfolio (Static HTML + CSS + Bootstrap + Sass)

Static portfolio site, pure HTML/CSS, ready for GitHub Pages.

## Stack
- **Framework front-end:** Bootstrap 5.3 (loaded via CDN — `navbar`, `grid`, `collapse`, `row/col`, utilities).
- **Sass:** `scss/styles.scss` (variables, mixins, nesting, `@media`, `@extend`) compiled to `css/styles.css`.
- **Fonts:** Google Fonts (Fraunces + Inter).
- **Favicon:** `favicon.svg` linked in every page.

## Pages
- `index.html` — Home (hero, stats, testimonial, CTA)
- `portfolio.html` — CV / Portfolio (case studies + experience)
- `contact.html` — Contact form

## Flexbox + Grid
- **CSS Grid** → `.ir-stats` (impact metrics), `.cv-header`, `.cv-body` (two-column CV layout on desktop), `.case-card .metrics`.
- **Flexbox** → `.ir-footer`, `.cv-header .meta`, `.cv-block .entry .top`, navbar items, button rows (`d-flex` Bootstrap utilities).
- **Bootstrap grid** (`.row` / `.col-md-6` / `.col-lg-7`) on hero + case study + contact layouts.

The portfolio page (`portfolio.html`) uses **all three**: Bootstrap's grid for case study cards, CSS Grid for the CV body, and Flexbox inside individual blocks.

## Sass usage (`scss/styles.scss`)
- **Variables**: `$brand-ink`, `$brand-cream`, `$brand-coral`, `$brand-sage`, `$radius-pill`, `$ease`.
- **Mixins**: `@mixin gradient-text`, `@mixin card-hover` (reused on `.stat` and `.case-card`).
- **Nesting**: `.ir-navbar { .nav-link { &.active {...} } }`, `.case-card { &:hover img {...} }`.
- **@extend**: headings extend `.font-display`.
- **Color functions**: `darken()`, `rgba()`.
- **@media** queries inside selectors for responsive Grid layouts.

## Build the CSS
```bash
npm i -g sass
sass scss/styles.scss css/styles.css
```
The compiled `css/styles.css` is included so you can deploy without rebuilding.

## Deploy to GitHub Pages
1. Push this folder to a GitHub repo.
2. Settings → Pages → Branch: `main`, folder: `/ (root)`.
3. Site goes live at `https://<user>.github.io/<repo>/`.
