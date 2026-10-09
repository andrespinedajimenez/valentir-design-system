# Valentir Green Tech — Design System

![Valentir Green Tech](assets/Logos/valentir-logo-horizontal.svg)

Valentir Green Tech sells fleet video, tracking, and protection to owner-operators and growing carriers in Canada and the United States. The brand is **clear, practical, and understated**: deep forest green, plenty of white, thin-bordered cards, and a single warm accent. Everything here comes from the production site (valentirtech.com) and the official logo files.

## Content and tone

- **Product language: North American English.** Interface copy is written in Canadian/US English unless the channel calls for another language.
- **Talk to the operator, not the enterprise.** Implied second person, short concrete sentences that name the real problem on the truck: *“Protect tools and trailers stored at home — alerts to your phone, not a security desk.”*
- **Benefit + qualifier with an em dash (—).** The brand's signature pattern is a claim followed by a dash that states the limit or the differentiator: *“Same-day visibility for owner-operators and small fleets — without enterprise minimums.”* Use a spaced em dash.
- **No hype.** No “revolutionary”, no exclamation marks. Numbers only when verifiable (*“200 trucks in Brazil for two years”*). Never invent discounts or legal dates; on compliance topics (B.C. Bill M-217), point readers to confirm with legal counsel.
- **Casing:** headlines and buttons in *Sentence case* (“Contact an expert”, “Solutions by industry”). Product names are always CamelCase with the **Valen** prefix: ValenCam, ValenTrack, ValenInsights, ValenLock, ValenGuard; plus **SolarTrack Pro**. Only the eyebrow and footer headings are UPPERCASE.
- **Verb-led CTAs:** “Talk to a Fleet Expert”, “Calculate your ROI”, “Explore solution →”, “Learn more →”. Action links carry an arrow (`arrow-forward`).
- **No emoji.** Icons are Material glyphs, never emoji.
- Site campaign line: **“Clarity for every mile.”** Logo tagline: **“Smarter fleets. Safer operations. Greener future.”**

## Color

- Page background `surface-page`; cards, header and fields on `surface`. Closing bands (testimonial, newsletter, footer) on `surface-inverse` with `ink-inverse` text.
- **`green-900` is the brand color in the interface**: primary button, action links, icons and the footer rule. `green-700` is the action green over photography (hero CTA) and the border of outlined buttons.
- `teal-600` is the signal color: eyebrow, quote marks, newsletter rule and focus ring. On light backgrounds use it only for borders, icons or text ≥24px (3.7:1).
- `rust-700` appears **once per view** (Subscribe). Don't use it for errors or decoration.
- Text: `ink` for headlines and body, `ink-muted` for intros and descriptions. On dark, `ink-inverse`, `ink-inverse-secondary` and `ink-inverse-tertiary` (the site's 1 / 0.85 / 0.65 opacities).
- `logo-teal`, `logo-orange`, `logo-ink` and `logo-slate` belong to the logo; keep them out of the UI.
- No decorative gradients. The one exception is the hero scrim (`scrim`, 90°, 0.84 to 0), which exists so the headline reads over the photo.

## Typography

- One family: variable **Inter** (`sans`), with a metric-matched Arial fallback. The bundled file covers Latin.
- Hierarchy through weight, not color: headlines at 800 with negative tracking (`hero-title`, `section-title`), card titles at 700 (`card-title`), body at 400 (`body`, `body-sm`).
- `hero-title` once per page. Each section opens with `section-title` + a `body` intro in `ink-muted`, max ~560px wide.
- Buttons at 600–700 (`button`, `button-lg`, `button-sm`), never uppercase.
- `eyebrow` and `footer-heading` are the only UPPERCASE styles.
- Quotes use `quote` (500 italic) on `surface-inverse`.

## Space, shape and elevation

- 4/8px grid inherited from MUI. Content at `container-max` (1200px) with a `space-lg` (mobile) / `space-2xl` (≥600px) gutter.
- Card grids use a `space-xl` gap. Product card: `product-image-height` image on top, content padded `space-lg space-lg space-2xl`. Industry card: `space-xl space-xl space-2xl`.
- **Default radius `radius-md` (12px)** for buttons, cards, fields and panels. `radius-sm` only for the large hero buttons; `radius-lg` for the icon tile.
- **Borders before shadows.** Cards are flat with a 1px `divider`. Shadows are reserved for contained buttons (`elevation-2`) and floating surfaces (`elevation-8`).
- 3px top rules accent dark blocks: `teal-600` on the newsletter, `green-900` on the footer.

## States and interaction

- Visible focus: solid 3px `teal-600` outline with 2px offset (2px `green-700` on the logo). Never remove it.
- Sticky header: on scroll it switches to `header-scrolled` with a 10px blur and `header-scrolled-shadow`; 0.28s ease transition.
- Touch targets at least `icon-tile` (44px).

## Imagery

- Cinematic photography of real fleets: trucks and trailers on the road at sunset or night, western-Canada mountains and coastline, with overlaid data layers (location pins, teal connection lines). See the **Images** asset group.
- In cards, crop with `object-fit: cover` at 168px tall over a `surface-inverse` placeholder while loading.
- People only in an operational context (driver in the cab, dispatcher at screens). No generic office stock.

## Iconography

- **Material Icons** (*Outlined* for industry illustrations, *Filled* for utilities), 24px viewBox, rendered at 16–20px. The SVGs in the **Icons** group were copied from the site and use `green-900` ink; change the fill in your copy on dark backgrounds (`ink-inverse`).
- Industry icons sit in a `green-50` tile with `radius-lg`; `arrow-forward` at 16px follows action links.
- Social icons (LinkedIn, Facebook, Instagram) in white inside 40px round buttons in the footer.

## Logo

- **Primary lockup: `valentir-logo-horizontal.svg`** (original PNG as backup). The shutter mark (`logo-teal` with a `logo-orange` dot) + “Valentir” in `logo-ink` and letter-spaced “Green Tech” in `logo-slate`. Use it for any new piece on a light background.
- **Stacked lockup with tagline: `valentir-logo-stacked-tagline.svg`** — the official tagline “Smarter fleets. Safer operations. Greener future.” in spaced capitals under a teal rule. For covers and vertical formats.
- **Mark only: `valentir-mark.webp`** (show at 36–40px) for small spaces, avatars and the favicon.
- Header and footer use the SVGs (see the Logo, SiteHeader and SiteFooter components). The live site still sets the name in Inter text (`logo-name`, `logo-suffix`, `navy-800`); that version is kept only as a record of what's published today.
- Never redraw, recolor or stretch the logo, or place it on photos. Clear space: the height of the orange dot on every side.
- On dark backgrounds: the negative versions `valentir-logo-horizontal-white.svg` / `valentir-logo-stacked-tagline-white.svg` (white with the `logo-orange` dot).

## Components

Components are CSS classes in `components/bundle.css` (prefix `vg-`) that read the tokens; each has its own card with guidelines and a live preview: Logo, Button, Hero, ProductCard, IndustryCard, ResourceCard, Testimonial, NewsletterPanel, SiteHeader, SiteFooter, CookieBanner.

## Repository layout

| Path | What |
|---|---|
| `tokens.json` | Source of truth: colors, type, spacing, radius, shadow and size tokens, each with a usage note. |
| `tokens.css` | The same tokens as CSS custom properties, `@font-face` and one class per type style. Generated from `tokens.json`. |
| `fonts/` | Inter variable (Latin subset, woff2). |
| `components/bundle.css` | Component styles (prefix `vg-`), built on `tokens.css`. |
| `components/<Name>/` | `README.md` guidelines and a `preview.html` you can open in a browser. |
| `assets/Logos/` | Official logos: traced SVGs (color and white) plus the original PNG/JPG files. |
| `assets/Icons/` | Material Icons SVGs used on the site. |
| `assets/Images/` | Product and hero photography. |

### Using it

```html
<link rel="stylesheet" href="tokens.css">
<link rel="stylesheet" href="components/bundle.css">

<div class="vg-root">
  <a class="vg-btn vg-btn--primary" href="/roi">Calculate your ROI</a>
</div>
```

Open any `components/<Name>/preview.html` locally to see the component rendered with the real tokens.
