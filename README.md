# HOSTARIA AL BUONGUSTO

Premium editorial website for **HOSTARIA AL BUONGUSTO** in Limone sul Garda, Lombardy, Italy.

The project combines cinematic photography, editorial typography, subtle motion and a refined contemporary Italian hospitality aesthetic.

The website is designed as a cinematic digital experience rather than a conventional restaurant landing page.

---

## Project

**Website:**  
https://daaart-studio.github.io/albuongusto/

**Restaurant:**  
HOSTARIA AL BUONGUSTO

**Location:**  
Via Fontana, 2 · 25010 Limone sul Garda BS · Italy

**Repository:**  
https://github.com/DAAART-STUDIO/albuongusto

**Organization:**  
DAAART-STUDIO

---

## Design Direction

The website is based on an editorial and cinematic approach to restaurant web design.

Core visual principles:

- Contemporary Italian hospitality
- Editorial / architectural design
- Cinematic photography
- Strong serif typography
- Minimal interface
- Generous whitespace
- High visual hierarchy
- Restrained motion
- Smooth scrolling interactions
- Responsive desktop and mobile compositions
- Elegant dark and light visual modes
- Clear reservation and visit actions

The design aims to communicate the character of HOSTARIA AL BUONGUSTO through photography, typography, space and motion rather than through a conventional corporate layout.

---

## Website Structure

The current website architecture is based on the following editorial sections:

- Hero
- View
- Experience
- Moments
- Cuisine
- Menu
- Place
- Events
- Visit
- Reservation

The exact content and presentation of each section are adapted specifically for HOSTARIA AL BUONGUSTO.

The website also includes:

- Responsive navigation
- Mobile navigation
- Scroll progress
- Smooth transitions
- Editorial animations
- Reservation modal
- Location / map integration
- Multilingual content
- Light / dark mode
- Responsive image compositions

---

## Reference Project

The project was initially created from the technical and visual foundation of:

**Bastione — Lounge & Restaurant**

Reference website:

https://daaart-studio.github.io/bastione/

Repository:

https://github.com/DAAART-STUDIO/bastione

Bastione provided the initial technical foundation, layout system and interaction patterns.

HOSTARIA AL BUONGUSTO is an independent project and is developed separately from Bastione.

Changes made to this project must never modify the original Bastione project or repository.

---

## Tech Stack

The project intentionally uses a lightweight static architecture.

- HTML5
- CSS3
- Vanilla JavaScript
- JavaScript ES Modules
- JSON
- SVG
- WebP
- CSS Custom Properties
- Responsive CSS
- GSAP / ScrollTrigger where required for cinematic interactions

There is currently **no frontend framework and no required build step**.

No React, Vue or Tailwind is used.

---

## Languages

The website uses a multilingual architecture.

Primary language:

- Italian

Additional supported languages:

- English
- German

Italian is the primary language because the restaurant is located in Italy.

Restaurant-specific content must be written specifically for HOSTARIA AL BUONGUSTO.

Translations should preserve the meaning, tone and character of the original Italian content and should not be treated as literal machine translations.

---

## Content Accuracy

Restaurant information must be based on current and reliable sources.

The project must never invent factual information.

This applies particularly to:

- Restaurant information
- Address
- Telephone
- Email
- Website
- Opening hours
- Menu
- Prices
- Reservation information
- Booking URLs
- Restaurant history
- Chef / owner information
- Events
- Facilities
- Coordinates
- Social media profiles
- Awards
- Ratings
- Reviews

When information cannot be reliably verified, it must not be presented as fact.

When reliable sources provide conflicting information, the most authoritative and current source should be preferred.

---

## Location

**HOSTARIA AL BUONGUSTO**

Via Fontana, 2  
25010 Limone sul Garda BS  
Italy

The location, map and geographic coordinates must always correspond to HOSTARIA AL BUONGUSTO.

Bastione location data must never be used in the final production website.

---

## Images

Photography is an important part of the website's visual identity.

Final production images should represent HOSTARIA AL BUONGUSTO and its actual environment, cuisine or location.

Bastione-specific restaurant photography should not be used as final production content.

Images should be optimized for:

- Desktop
- Mobile
- Responsive layouts
- Performance
- Correct aspect ratios
- Fast loading

Meaningful `alt` attributes should be provided for relevant images.

---

## SEO

The website uses independent SEO metadata for HOSTARIA AL BUONGUSTO.

SEO implementation may include:

- Page title
- Meta description
- Canonical URL
- Open Graph metadata
- Social sharing metadata
- Favicon
- Restaurant structured data
- LocalBusiness structured data

All structured data must contain verified information.

The project must not inherit Bastione-specific:

- Titles
- Descriptions
- Canonical URLs
- Addresses
- Phone numbers
- Coordinates
- Social profiles
- Restaurant schema
- Open Graph information

---

## Local Development

Do not open `index.html` directly using `file://`.

The project uses JavaScript ES modules and should be served through HTTP.

### Python

```bash
cd albuongusto
python -m http.server 8002