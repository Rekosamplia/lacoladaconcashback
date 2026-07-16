# Samplia Design System

> _Turning tryers into buyers._

Samplia is a **phygital sampling & brand experience agency**. They run sampling
campaigns for big FMCG, fashion and cosmetics brands across their own pop-up
stores, vending-style sampling machines, brand events and retail partners. The
**Samplia app** is how consumers ("tryers") discover campaigns, reclaim their
free product or experience, and get measured into the data-feedback loop that
the brand-side of the business sells.

The brand wants to be perceived as **creative, data-centric, innovative** — and
this design system is built to feel **clean, minimal and confident**, with
deliberate white space so colourful campaign imagery from each client can sit
on top without competing.

---

## Source materials

| Asset | Where it lives | Notes |
|---|---|---|
| Manual de Identidad Corporativa (WIP 6) | `reference/Manual_Identidad_Samplia.pdf` | The brand-book PDF supplied by the user. All colors, typography, motifs and tone notes below are derived from it. |
| _(no codebase attached)_ | — | UI kit screens are inferred. See **Caveats** below. |
| _(no Figma attached)_ | — | — |

---

## Repo index

```
Samplia Design System/
├── README.md                       ← you are here
├── SKILL.md                        ← cross-compatible Agent Skill manifest
├── colors_and_type.css             ← CSS custom-property tokens (drop-in)
├── assets/                         ← logos (placeholder wordmarks — see caveats)
├── reference/                      ← original brand-manual PDF
├── preview/                        ← Design-System-tab cards (19 cards)
└── ui_kits/
    └── samplia_app/                ← iOS consumer-app UI kit (interactive)
```

Open `ui_kits/samplia_app/index.html` for the live UI kit. Browse the **Design
System** tab for foundation cards (colors, type, spacing, components).

---

## Content fundamentals

Samplia's brand voice is **creative, innovative, transgressive and
professional**. The Spanish-language brand manual frames this tightly — copy
should feel _personalized, agile, sensorial-innovative_ and never generic.

| Dimension | Choice | Example |
|---|---|---|
| **Language** | Spanish-first (es-ES). Spanish for ES product surfaces, English-equivalent only on internal / global comms. | "Reclamar", "Cerca de ti", "Mías" |
| **Person** | _Tú_ — direct, second-person, no "usted". | "Descarga la aplicación y empieza a disfrutar." |
| **Tone** | Confident but warm. Imperative + invitation, never sales-y. | "Reserva tu muestra." · "Vive una experiencia sensorial." |
| **Length** | Short. Two clauses max in a CTA. Body copy is informative, no fluff. | — |
| **Casing** | Sentence case for headlines and body. **ALL CAPS only on the app-download lockup** ("DESCARGA LA APLICACIÓN Y EMPIEZA A DISFRUTAR CON SAMPLIA") and on textile/vehicle wayfinding. | — |
| **Punctuation** | Italic full-stop on the claim — _Turning tryers into buyers**.**_ — is the brand's signature flourish. Keep the period. | — |
| **Emoji** | **Avoid.** The brand-book never uses them; minimalist visual identity. Use Lucide icons or a small red dot for emphasis instead. | — |
| **Numbers / data** | Lean into them — Samplia is a data-centric brand. "172 / 500 muestras disponibles", "+14 marcas". | — |
| **Words to favour** | _disruptivo, experiencia, sensorial, sampler, phygital, a medida, accionable, insight_. | — |
| **Words to avoid** | _users, customers_ when speaking to consumers (use _tryers_), _free trial_ (use _muestra gratis_), generic marketing tropes. | — |
| **Claim usage** | "Turning tryers into buyers." — italic, lowercase, paired with the wordmark or used alone in product pages. Translation lives intact, never localized. | — |

Sample lines drawn directly from the manual:

- "Conectar de forma innovadora marcas y consumidores a través de experiencias disruptivas."
- "Somos sastres: creamos campañas a medida."
- "Innovación sensorial."
- "Descarga la aplicación y empieza a disfrutar con Samplia."

---

## Visual foundations

### Type

- **Primary:** [Raleway](https://fonts.google.com/specimen/Raleway) — weights
  used across the system: 200 (ExtraLight), 300 (Light), 400 (Regular),
  500 (Medium), 600 (SemiBold), 700 (Bold), 900 (Black). Italic 300 is reserved
  for the brand claim. Loaded from Google Fonts in `colors_and_type.css`.
- **Secondary (per manual):** Myriad Pro, "for web and technical applications
  where Raleway is not available." Myriad Pro is **not free / web-licensed**, so
  this system substitutes **Inter** as the UI fallback (`--font-ui`). 🚩
  **Substitution flagged** — if you have a licensed Myriad Pro webfont, drop the
  files into `fonts/` and point `--font-ui` at it.
- **Tracking:** display sizes get negative tracking (`-0.02em` to `-0.03em`).
  Eyebrows and uppercase labels open up to `+0.08em` to `+0.18em`.
- **Hierarchy:** see `preview/type-scale.html` — strict 1.250 (Major Third) ramp
  from 12px to 72px.

### Colour

- **Brand red — `#C73346` (Pantone 198 C, "Rojo Intenso").** The hero colour.
  Used for primary CTAs, live indicators, accent dots, the wordmark accent
  punctuation, and full-bleed brand backgrounds.
- **Supporting reds:** `#CB4A5F` (190 C), `#DC97AD` (197 C), `#F1D8DE` (196 C).
  Soft pink (`#F1D8DE`) is the workhorse tint for backgrounds and "Próximo" badges.
- **Neutrals:** `#000000` (Black 6 C), `#FFFFFF`, `#F2F2F2` (7% black). The
  manual stops there; we've added derived greys (`#FAFAFA`, `#E6E6E6`, `#CCCCCC`,
  `#999999`, `#666666`, `#444444`, `#2A2A2A`) for UI surfaces. These are
  **derived**, not manual-mandated — easy to retune if the brand standardizes them.
- **No invented accents.** The brand has _no_ secondary accent color outside the
  red family. Status colours (success/warning/info) live only on UI signals,
  never in marketing surfaces.

### Backgrounds

- **Default surfaces are white or `#F2F2F2`.** Heavy use of negative space.
- **Brand red full-bleed** appears on hero CTAs, app-download lockups and the
  redeem ticket. Always paired with a white wordmark.
- **Trama (network) pattern** — a dotted-grid network mask used as a subtle
  background fill on red panels. See `preview/motif-trama.html`. Use _sparingly_
  to fill empty space; never as a hero background.
- **Esquineros (corner brackets)** — diagonal L-shaped corner marks that frame
  a "window". The Samplia wordmark anchors one corner of the diagonal. Used to
  frame editorial copy or hero photography. See `preview/motif-esquineros.html`.
- **No** gradients in marketing imagery. Within the app, soft brand-to-dark
  gradients are acceptable for placeholder campaign art _until_ real photos
  replace them.

### Photography / imagery

Per the manual:
- **Realistic, not over-retouched.** Real consumers, real sampling moments,
  real product hero shots.
- **Coherent with the palette.** Red, white, grey. Brand-red accents in detail
  (product packaging, a logo, an interaction).
- **High resolution, well-lit, single focal point.** Avoid clutter.
- **Background imagery is subtle** — desaturated, or blurred so text/graphics
  stay primary.

### Spacing & layout

- 4-pt base. Scale: 4 · 8 · 12 · 16 · 20 · 24 · 32 · 40 · 48 · 64 · 80 · 96.
- Generous padding around content blocks (16–32px on mobile, 48–96px on web).
- **Logo safety area** = the height of the wordmark, on all sides. Manual
  spec: don't print below 20mm wide (full lockup), 10mm (symbol).
- Max content width: **1240px** (`--maxw-page`), 68ch for prose.

### Radii

- **8 / 12 / 16 / 20** for cards and modals.
- **999px (pill)** for buttons, badges, tags, search fields, segmented controls.
  Pills are the dominant interactive shape across the system.

### Shadows / elevation

Four levels (`--shadow-xs/sm/md/lg`), all near-black neutral. No coloured glows
in chrome — except `--shadow-brand` (red drop) which is reserved for the
floating "Reclamar" FAB on the bottom nav.

### Borders

- Hairline `1px` borders use `#E6E6E6`.
- Strong borders (used on ghost buttons) are `1.5px` solid black.
- Dashed perforation lines (`1.5px dashed #EEE`) are used on the redeem ticket.

### Motion

- Easing: standard `cubic-bezier(0.22, 1, 0.36, 1)` — punchy out-back without
  bounce.
- Durations: `120ms` micro, `220ms` standard, `400ms` page transitions.
- **Hover** = brand-darken (`--primary-hover: #B32A3C`); never opacity changes
  on brand red.
- **Press** = subtle `scale(0.97)` on primary buttons.
- **Live indicators** pulse the dot opacity 0.3 → 1 at 1.4s.
- **Entry animations** are 8px upward rise + fade (`.s-rise`) or 0.94 → 1 scale
  (`.s-pop`).

### Cards

White background, `16px` radius, hairline border `#F0F0F0` _or_ `shadow-sm`
(not both), 14–18px interior padding. Campaign cards add a 16:10 art tile at the
top with the campaign tag overlaid top-left.

### Transparency & blur

- **Backdrop blur** is used on overlay chrome (the back button on the campaign
  detail) — `rgba(255,255,255,0.92)` with `backdrop-filter: blur(8px)`.
- **No glassy UI everywhere** — the look is opaque and crisp by default.

### Layout rules (fixed)

- Bottom nav is always 5 items, with the centre slot a raised red FAB.
- Sticky CTA bars on detail pages: white background, 1px top border, 14px /
  20px / 28px padding (the extra bottom-padding clears the iOS home indicator).
- App header pattern: greeting + name (left), notification + avatar (right).

---

## Iconography

- **Library: [Lucide](https://lucide.dev) at 1.6 stroke weight.** Minimal,
  geometric, fully open-source. Loaded from a CDN (`unpkg.com/lucide@0.453`).
- **Sizing:** 14 (inline meta), 18 (nav, list rows), 22 (bottom nav), 24 (primary
  FAB).
- **Colour:** icons inherit `currentColor`. Red (`#C73346`) when they accompany
  a red label or live signal; otherwise black or grey.
- **No filled icons.** No emoji. No Unicode symbols as iconography (except `→`
  in CTAs, which is allowed as it scans as type).
- **Custom icons:** none in the brand book. If a Samplia-specific glyph is
  needed (e.g. the sampling-machine pictogram on Aéreos signage), draft it in
  the Lucide style: 24×24 viewbox, 1.6 stroke, round line-cap/join.

🚩 **Substitution flag:** The Samplia brand book references illustrative
iconography in §06.B (the "Trama" graphic + custom motifs for digitalisation
and connection) but did not include the source files. We've represented the
**trama** as a CSS dot-grid pattern. If real Illustrator/SVG assets are shared
later, drop them into `assets/` and reference from `motif-trama.html`.

---

## Caveats — please help us iterate

1. 🚩 **Logo files were not extractable from the supplied PDF.** The wordmarks
   in `assets/logo-samplia-*.svg` are **placeholders** typeset in the brand
   font (Raleway 800 + a red accent dot). The real Samplia imagotype likely has
   custom letterforms or a distinct symbol — **please share the original SVG /
   AI / PNG logo files** so we can swap them in.
2. 🚩 **Myriad Pro substituted with Inter** for UI/web type. If you have a
   licensed Myriad Pro webfont, drop the files into `fonts/` and we'll point
   `--font-ui` at them.
3. 🚩 **No app codebase or Figma was provided** — the iOS UI kit is inferred
   from the brand manual + the company brief. The information architecture
   (tab structure, redeem flow, loyalty tier system) is reasonable but may
   not match the real product. **A link to the codebase or Figma will let us
   make this pixel-accurate.**
4. 🚩 **No web / marketing-site reference** — only the iOS app kit has been
   built. If you'd like a marketing-site kit too, point us at the live site or
   a Figma file.
5. 🚩 **Brand manual asset images** (logo variants, esquineros mockups, real
   campaign photography, vehicle/textile mockups) couldn't be extracted from
   the PDF in this environment. The original Adobe Illustrator / InDesign
   source files would unblock a proper recreation.

---

## Using these tokens

```html
<link rel="stylesheet" href="colors_and_type.css">
<button class="s-h3" style="
  background: var(--primary);
  color: var(--fg-on-primary);
  border-radius: var(--r-pill);
  padding: var(--space-3) var(--space-6);
">Reclamar →</button>
```

Semantic classes available on any element: `.s-display`, `.s-h1`, `.s-h2`,
`.s-h3`, `.s-eyebrow`, `.s-lead`, `.s-body`, `.s-caption`, `.s-claim`, `.s-mono`.
