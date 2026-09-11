# Design System

## Purpose

This document defines the visual language, design principles and implementation rules for the HOSTARIA AL BUONGUSTO website.

The design system exists to keep the interface visually consistent while allowing the website to maintain its editorial, cinematic and hospitality-focused character.

The system should guide future development without restricting the visual composition of individual editorial sections.

---

## Direction

HOSTARIA AL BUONGUSTO is designed as a premium editorial hospitality experience.

Visual references:

* contemporary Italian hospitality
* architecture
* refined restaurant design
* travel editorial
* cinematic photography
* Italian landscape and lakeside atmosphere
* contemporary print and magazine design

The interface should never feel like a generic restaurant template.

The visual identity should communicate the restaurant through photography, typography, composition, rhythm and atmosphere rather than through excessive interface elements.

---

## Core Principles

The design prioritizes:

* photography
* typography
* composition
* whitespace
* hierarchy
* atmosphere
* visual rhythm
* subtle motion
* editorial storytelling
* accessibility
* responsive composition

The interface should remain intentionally restrained.

### Avoid

* excessive cards
* excessive rounded corners
* generic gradients
* excessive shadows
* unnecessary borders
* excessive badges
* decorative UI without purpose
* dense dashboard-like layouts
* template-like sections
* unnecessary animations
* excessive visual effects
* inconsistent spacing
* arbitrary colors

---

# Brand Expression

## Brand Character

The visual language should feel:

* refined
* Italian
* atmospheric
* contemporary
* elegant
* warm
* editorial
* confident
* understated

The design should avoid feeling:

* corporate
* overly commercial
* generic
* overly decorative
* childish
* technically complex
* visually noisy

---

# Typography

Typography is one of the primary elements of the visual identity.

The system uses a display typeface for prominent editorial typography and a supporting typeface for interface and body content.

## Display Typography

Display typography is used for:

* hero headlines
* section titles
* large editorial statements
* prominent numbers
* selected decorative text

CSS token:

```text
--font-display
```

Display typography should provide strong visual character and should not be used for every text element.

---

## Body Typography

Body typography is used for:

* descriptions
* navigation
* labels
* metadata
* supporting content
* interface controls

Body text should prioritize readability across desktop and mobile layouts.

---

## Typography Hierarchy

The visual hierarchy should generally follow:

1. Hero / primary statement
2. Section heading
3. Supporting heading
4. Introductory text
5. Body text
6. Metadata / labels
7. Utility text

Font sizes should be controlled through the existing design-token system whenever possible.

Avoid introducing arbitrary font sizes directly inside individual components.

---

## Typography Rules

* Maintain strong contrast between display and supporting typography.
* Use generous line-height for long-form text.
* Avoid excessively long text lines.
* Do not use display typography for dense paragraphs.
* Preserve hierarchy on mobile.
* Do not reduce headings to unreadable sizes solely to fit a layout.
* Avoid unnecessary uppercase text.
* Use letter spacing intentionally, particularly for labels and navigation.

---

# Color System

Colors are managed through CSS custom properties defined in:

```text
css/tokens.css
```

The design supports both light and dark visual modes.

## Color Principles

Color should support:

* readability
* hierarchy
* atmosphere
* photography
* section separation
* interaction states

The palette should remain restrained.

Photography and typography should remain the dominant visual elements.

---

## Theme Support

Theme behavior is handled by:

```text
js/modules/theme-switcher.js
```

Theme-specific values should be implemented through CSS custom properties rather than duplicated component styles.

Components should consume semantic color variables instead of defining independent colors whenever possible.

Example:

```css
color: var(--color-text);
background: var(--color-background);
```

Avoid:

```css
color: #123456;
```

when an appropriate design token already exists.

---

# Spacing

Spacing establishes the rhythm of the editorial layout.

Spacing should be consistent across:

* sections
* headings
* paragraphs
* navigation
* buttons
* galleries
* content groups
* responsive layouts

Use the existing spacing tokens defined in `css/tokens.css`.

Avoid introducing arbitrary margins and paddings when an existing token provides the required value.

---

## Editorial Spacing

Large sections should have sufficient vertical space to create visual rhythm.

Spacing may intentionally vary between sections when required by the composition.

The goal is not mathematical uniformity but a consistent visual rhythm.

---

# Layout

The layout system is defined primarily through:

```text
css/layout.css
```

and component-specific styles inside:

```text
css/components/
```

The layout should support:

* full-width editorial sections
* constrained content areas
* asymmetric compositions
* large photography
* overlapping elements
* vertical storytelling
* responsive grids
* mobile stacking

---

## Composition

The design favors editorial composition over rigid component grids.

Preferred techniques include:

* asymmetric alignment
* controlled negative space
* large image areas
* visual overlaps
* intentional cropping
* varying content widths
* strong vertical rhythm

However, composition must remain predictable and usable on smaller screens.

---

# Grid

The grid should provide structural consistency without making every section look identical.

Use the existing layout rules and CSS variables where available.

Individual sections may use different compositions when the content requires it.

Avoid forcing every section into the same card or column structure.

---

# Components

Reusable interface components are located in:

```text
css/components/
```

Component styles should be:

* focused
* reusable
* predictable
* responsive
* theme-aware

A component should not contain unrelated global styling.

---

## Component Principles

Before creating a new component:

1. Check whether an existing component already provides the required behavior.
2. Reuse existing design tokens.
3. Preserve established spacing and typography.
4. Keep component-specific styles inside the component stylesheet.
5. Avoid introducing unnecessary variants.
6. Verify desktop and mobile behavior.

---

# Buttons and Actions

Buttons and interactive controls should remain visually restrained.

Primary actions may be used for:

* reservation
* visit information
* navigation
* important calls to action

Actions should have clear:

* visual hierarchy
* hover state
* focus state
* active state
* disabled state where applicable

Avoid excessive button usage.

Not every link or interaction needs to look like a prominent button.

---

# Navigation

Navigation should remain minimal and editorial.

The navigation system includes:

```text
js/modules/navigation.js
js/modules/header.js
```

The interface should prioritize:

* clear orientation
* fast access to important sections
* readable labels
* predictable interaction
* responsive behavior

Mobile navigation should not simply reproduce the desktop navigation at a smaller size. It should remain usable within the available screen space.

---

# Imagery

Photography is a core part of the design system.

Images should communicate:

* restaurant atmosphere
* cuisine
* location
* landscape
* hospitality
* people and moments where appropriate

Photography should feel authentic and editorial rather than like generic stock imagery.

---

## Image Composition

Images may use:

* large cinematic crops
* full-bleed compositions
* asymmetric layouts
* controlled overlays
* responsive cropping
* portrait and landscape formats

Image composition should support the content rather than obscure it.

---

## Image Performance

Images should be optimized for:

* file size
* dimensions
* responsive rendering
* loading performance
* mobile bandwidth

Preferred web formats include WebP where appropriate.

Meaningful images should have appropriate `alt` attributes.

Decorative images may use an empty `alt` attribute when appropriate for accessibility.

---

# Motion

Motion is used to reinforce the cinematic character of the website.

Animation should communicate:

* transition
* hierarchy
* spatial relationships
* interaction
* progression through the page

It should not exist purely for decoration.

---

## Motion Principles

Animations should be:

* subtle
* purposeful
* smooth
* responsive
* interruptible where appropriate

Avoid:

* excessive movement
* distracting looping animations
* unnecessary parallax
* long blocking transitions
* animations that interfere with navigation or reading

---

## Animation Implementation

Shared animation styles are located in:

```text
css/animations.css
```

JavaScript animation behavior is implemented through dedicated modules.

GSAP / ScrollTrigger may be used for selected cinematic interactions.

Animation logic should remain isolated from unrelated application logic.

---

# Scroll Behavior

The website uses scroll-based interactions as part of its editorial experience.

Relevant functionality includes:

```text
js/modules/smooth-scroll.js
js/modules/scroll-progress.js
js/modules/scroll-morph.js
```

Scroll effects should enhance orientation and storytelling without making normal navigation difficult.

---

# Interaction States

Interactive elements should provide appropriate states.

At minimum, relevant controls should account for:

* default
* hover
* focus
* active
* disabled

Keyboard focus must remain visible.

Interactive states should be consistent across components.

---

# Accessibility

Accessibility is part of the design system rather than a separate feature.

The interface should provide:

* semantic HTML
* meaningful heading hierarchy
* accessible navigation
* keyboard accessibility
* visible focus states
* meaningful image alternatives
* sufficient text contrast
* appropriately labeled controls
* accessible modal behavior

Animations should respect reduced-motion preferences where applicable.

---

# Responsive Design

The website is designed for:

* desktop
* tablet
* mobile

Responsive behavior should preserve the intended visual hierarchy rather than simply shrinking desktop layouts.

---

## Responsive Principles

On smaller screens:

* typography should remain readable
* navigation should remain accessible
* images should use appropriate crops
* content should stack naturally
* horizontal overflow should be avoided
* controls should remain usable
* animation should remain performant
* spacing should adapt to available space

Mobile layouts may use a different composition from desktop when necessary.

---

# Light and Dark Modes

The website supports light and dark visual modes.

Theme switching is handled by:

```text
js/modules/theme-switcher.js
```

Theme values should be centralized in:

```text
css/tokens.css
```

Components should not implement independent theme systems.

When adding a new visual component, verify its appearance in both supported themes.

---

# Internationalization

The design system must support the multilingual architecture.

Localized content is stored in:

```text
data/i18n/
```

Internationalization behavior is handled by:

```text
js/modules/i18n.js
```

The interface must accommodate different text lengths between languages.

Do not design components around fixed text widths that only work for one language.

---

# Icons

Icons should remain visually consistent with the overall editorial language.

Available icon assets are stored in:

```text
assets/icons/
```

Prefer existing icons before introducing new ones.

New icons should match:

* stroke / fill language
* visual weight
* scale
* proportions
* surrounding spacing

Avoid mixing unrelated icon styles.

---

# Modals

Modal interfaces should be used only when they provide a clear benefit.

Current modal-related functionality includes:

```text
js/modules/reservation-modal.js
js/modules/product-modal.js
```

Modals should:

* clearly communicate their purpose
* be easy to close
* support keyboard interaction
* prevent inappropriate background interaction
* remain usable on mobile
* preserve visual consistency with the main interface

---

# Content and Design Relationship

Design should support content rather than compensate for weak content.

Restaurant-specific content should determine:

* hierarchy
* image selection
* section rhythm
* emphasis
* composition

Do not introduce decorative elements merely to fill empty space.

Whitespace is an intentional part of the design.

---

# Design Tokens

The primary design-token source is:

```text
css/tokens.css
```

Tokens should be used for shared values such as:

* colors
* typography
* spacing
* borders
* radii
* transitions
* theme values
* layout constraints

Before introducing a new global value, check whether an existing token can be reused.

New tokens should have a clear semantic purpose.

---

# CSS Organization

The CSS architecture is divided into:

```text
css/
├── reset.css
├── tokens.css
├── base.css
├── layout.css
├── animations.css
└── components/
```

Responsibilities:

### `reset.css`

Browser normalization and baseline reset.

### `tokens.css`

Design tokens, CSS custom properties and theme values.

### `base.css`

Global typography, elements and foundational styles.

### `layout.css`

Page structure and layout rules.

### `animations.css`

Shared animation and transition rules.

### `components/`

Styles specific to reusable interface components.

---

# JavaScript and Visual Behavior

Visual behavior should remain modular.

Relevant modules include:

```text
js/modules/
```

Examples:

```text
navigation.js
header.js
theme-switcher.js
smooth-scroll.js
scroll-progress.js
scroll-morph.js
view-gallery.js
moments.js
experience.js
cuisine.js
reservation-modal.js
```

Each module should have a focused responsibility.

Do not place unrelated visual behavior into `app.js` when it can be isolated into a dedicated module.

---

# Performance

Visual quality must not come at the expense of performance.

Prioritize:

* optimized images
* efficient animations
* minimal dependencies
* lazy loading where appropriate
* avoiding unnecessary JavaScript execution
* avoiding layout shifts
* responsive image dimensions
* efficient DOM manipulation

Animations should not continuously consume resources when they are not visible or necessary.

---

# Browser and Device Behavior

The website should maintain consistent behavior across modern desktop and mobile browsers.

When introducing a visual feature, test at minimum:

* desktop viewport
* tablet-sized viewport
* mobile viewport
* touch interaction
* keyboard interaction where applicable

---

# Design Change Rules

When modifying the visual system:

1. Check existing tokens first.
2. Check existing components before creating new ones.
3. Preserve the established visual language.
4. Avoid unnecessary global changes.
5. Test both light and dark modes.
6. Test responsive layouts.
7. Test interactive states.
8. Check animation performance.
9. Verify accessibility.
10. Keep changes limited to the requested scope.

Do not perform broad visual refactors without an explicit requirement.

---

# Production Consistency

All production pages and components must follow the HOSTARIA AL BUONGUSTO visual language.

New sections should feel like part of the same website while remaining editorially distinct.

The design system should evolve incrementally as new requirements appear.

The goal is not to make every section identical.

The goal is to make every section feel like it belongs to the same visual world.
