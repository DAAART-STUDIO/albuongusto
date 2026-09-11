# Architecture

## Overview

HOSTARIA AL BUONGUSTO is a lightweight static website built with HTML, CSS and vanilla JavaScript.

The project intentionally avoids a frontend framework and does not currently require a build step.

The architecture is modular: page structure, styling, data, internationalization and interactive behavior are separated into dedicated directories and JavaScript modules.

---

## Stack

* HTML5
* CSS3
* Vanilla JavaScript
* JavaScript ES Modules
* JSON
* SVG
* WebP
* CSS Custom Properties
* Responsive CSS
* GSAP / ScrollTrigger where required for cinematic interactions

There is no React, Vue, Tailwind or other frontend framework.

There is currently no required build step.

---

## Project Structure

```text
albuongusto/
├── assets/
│   ├── icons/
│   ├── images/
│   └── logo/
│
├── css/
│   ├── components/
│   ├── animations.css
│   ├── base.css
│   ├── layout.css
│   ├── reset.css
│   └── tokens.css
│
├── data/
│   └── i18n/
│       ├── de.json
│       ├── en.json
│       └── it.json
│
├── docs/
│   ├── ARCHITECTURE.md
│   ├── DEPLOYMENT.md
│   ├── DESIGN-SYSTEM.md
│   ├── I18N.md
│   └── README.md
│
├── js/
│   ├── modules/
│   │   ├── cuisine.js
│   │   ├── dashboard.js
│   │   ├── dishes-wheel.js
│   │   ├── earth-scene.js
│   │   ├── experience.js
│   │   ├── header.js
│   │   ├── i18n.js
│   │   ├── moments.js
│   │   ├── navigation.js
│   │   ├── observer.js
│   │   ├── particles.js
│   │   ├── product-modal.js
│   │   ├── radar-effect.js
│   │   ├── reservation-modal.js
│   │   ├── roadmap-render.js
│   │   ├── scroll-morph.js
│   │   ├── scroll-progress.js
│   │   ├── smooth-scroll.js
│   │   ├── theme-switcher.js
│   │   └── view-gallery.js
│   │
│   └── app.js
│
├── .gitignore
├── .nojekyll
├── AGENTS.md
├── README.md
├── favicon.ico
├── index.html
├── robots.txt
├── site.webmanifest
└── sitemap.xml
```

---

## Directory Responsibilities

### `assets/`

Contains static visual assets used by the website.

```text
assets/
├── icons/
├── images/
└── logo/
```

* `icons/` — interface and decorative icons
* `images/` — restaurant, location and editorial photography
* `logo/` — HOSTARIA AL BUONGUSTO branding assets

Assets should be optimized for responsive rendering and web performance.

---

### `css/`

Contains the complete visual system and layout styles.

```text
css/
├── components/
├── animations.css
├── base.css
├── layout.css
├── reset.css
└── tokens.css
```

Responsibilities:

* `reset.css` — browser normalization and baseline reset
* `tokens.css` — CSS custom properties, design tokens and theme values
* `base.css` — global typography and base element styles
* `layout.css` — page-level layout and structural rules
* `components/` — reusable component-specific styles
* `animations.css` — shared animation and transition styles

Visual changes should use the existing design-token system where applicable rather than introducing isolated values unnecessarily.

---

### `data/`

Contains structured content data.

```text
data/
└── i18n/
    ├── de.json
    ├── en.json
    └── it.json
```

The `i18n` directory contains localized website content.

Italian is the primary language.

Translations must preserve the meaning, tone and intended context of the Italian source content.

Restaurant-specific factual information must be verified before being added to any language file.

---

### `js/`

Contains the application entry point and modular JavaScript functionality.

```text
js/
├── modules/
└── app.js
```

`app.js` acts as the main JavaScript entry point and initializes the required application modules.

The `modules/` directory contains isolated functionality for navigation, internationalization, animations, sections, interactions and other site behaviors.

---

## JavaScript Modules

The current module architecture includes:

* `cuisine.js` — cuisine-related interactions
* `dashboard.js` — dashboard / interface functionality
* `dishes-wheel.js` — dishes wheel interaction
* `earth-scene.js` — location / Earth visual scene
* `experience.js` — experience section behavior
* `header.js` — header behavior
* `i18n.js` — internationalization and language switching
* `moments.js` — moments section interactions
* `navigation.js` — navigation and mobile navigation
* `observer.js` — intersection / viewport observation
* `particles.js` — particle-based visual effects
* `product-modal.js` — content / product modal behavior
* `radar-effect.js` — radar visual effect
* `reservation-modal.js` — reservation interface
* `roadmap-render.js` — roadmap rendering
* `scroll-morph.js` — scroll-based morphing effects
* `scroll-progress.js` — scroll progress indicator
* `smooth-scroll.js` — smooth scrolling behavior
* `theme-switcher.js` — light / dark theme switching
* `view-gallery.js` — gallery interactions

Modules should remain focused on their specific responsibilities.

New functionality should preferably be implemented as a dedicated module when it represents an independent interaction or feature.

---

## HTML

`index.html` is the main document and defines the page structure and semantic content.

The HTML layer is responsible for:

* semantic page structure
* section markup
* navigation
* content containers
* accessibility attributes
* SEO metadata
* structured data
* module loading

Content that is shared across languages should not be duplicated unnecessarily when it can be handled through the existing internationalization system.

---

## Data Flow

The general application flow is:

```text
index.html
    │
    ├── CSS
    │   ├── tokens
    │   ├── base
    │   ├── layout
    │   ├── components
    │   └── animations
    │
    └── js/app.js
            │
            └── JavaScript modules
                    │
                    ├── UI interactions
                    ├── section behavior
                    ├── animations
                    ├── navigation
                    ├── i18n
                    ├── theme
                    └── reservation
```

The architecture is intentionally client-side and does not require a backend application for the core website.

---

## Internationalization

Internationalization is handled through:

```text
data/i18n/
js/modules/i18n.js
```

Supported languages:

* Italian (`it`)
* English (`en`)
* German (`de`)

Italian is the canonical content language.

Language-specific content should be stored in the appropriate JSON file rather than duplicated directly throughout JavaScript modules.

---

## Styling Architecture

The CSS architecture separates:

1. Global reset
2. Design tokens
3. Base styles
4. Layout
5. Components
6. Animations

Design tokens should be defined in `tokens.css` and reused throughout the project.

Component-specific styling belongs in `css/components/`.

Global layout rules belong in `layout.css`.

Shared animation definitions belong in `animations.css`.

---

## Animation Architecture

The website uses lightweight CSS and JavaScript-driven animation.

Where required, GSAP / ScrollTrigger may be used for cinematic interactions and scroll-based effects.

Animation logic should remain isolated from unrelated application logic.

Animations must not compromise:

* page usability
* responsive behavior
* accessibility
* content readability
* loading performance

---

## Responsive Architecture

The website is designed for:

* desktop
* tablet
* mobile

Responsive behavior is implemented primarily through CSS media queries and responsive layout rules.

JavaScript should only introduce viewport-specific behavior when CSS alone is insufficient.

Mobile navigation and responsive interactions must remain compatible with the existing module architecture.

---

## Themes

The website supports light and dark visual modes.

Theme-related behavior is handled by:

```text
js/modules/theme-switcher.js
```

Theme values are defined through CSS custom properties in:

```text
css/tokens.css
```

Components should use the existing theme variables instead of hard-coded theme-specific values whenever possible.

---

## Architectural Principles

The project follows several practical principles:

* Keep the architecture lightweight.
* Avoid unnecessary dependencies.
* Preserve the existing static architecture.
* Keep JavaScript modules focused.
* Prefer reusable CSS tokens and components.
* Avoid broad refactoring without a specific requirement.
* Preserve existing responsive behavior.
* Preserve working animations and interactions.
* Keep restaurant content separate from presentation logic.
* Keep multilingual content in the i18n data layer.
* Do not introduce a frontend framework unless explicitly required.

Changes should be incremental and limited to the requested functionality.

---

## Production Constraints

Production content must represent **HOSTARIA AL BUONGUSTO** only.

Restaurant information, contact details, location data, menu information, reservation information, images, SEO metadata and structured data must be verified before publication.

The project must not contain unverified restaurant facts or unrelated production content.

---

## Local Development

Because the project uses JavaScript ES Modules, `index.html` should not be opened directly using `file://`.

Run a local HTTP server instead.

### Python

```bash
cd albuongusto
python -m http.server 8002
```

Then open:

```text
http://localhost:8002
```
