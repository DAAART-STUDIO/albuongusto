# HOSTARIA AL BUONGUSTO — PROJECT INSTRUCTIONS

## 1. PROJECT

This project is a new independent restaurant website for:

**HOSTARIA AL BUONGUSTO**

Address:

Via Fontana, 2  
25010 Limone sul Garda BS  
Italy

GitHub repository:

https://github.com/DAAART-STUDIO/albuongusto

GitHub Pages:

https://daaart-studio.github.io/albuongusto/

---

# 2. PROJECT FOUNDATION

This project is created as a copy/clone of the existing:

**Bastione — Lounge & Restaurant**

Bastione website:

https://daaart-studio.github.io/bastione/

The Bastione source code is the starting point and technical foundation of this project.

The new project should initially preserve the Bastione website as closely as possible.

The purpose is to create a working copy first and then progressively adapt it for HOSTARIA AL BUONGUSTO.

---

# 3. DEVELOPMENT APPROACH

The project must be developed incrementally.

Do NOT immediately redesign or rebuild the website.

Do NOT create a new architecture unless there is a specific technical reason.

Do NOT convert the project into a generic restaurant template.

Do NOT unnecessarily refactor working code.

The preferred workflow is:

1. Clone/copy Bastione into this project.
2. Verify that the copied project works correctly.
3. Preserve the existing structure and functionality.
4. Gradually replace Bastione-specific content with HOSTARIA AL BUONGUSTO content.
5. Gradually replace images and visual content.
6. Gradually adapt sections where necessary.
7. Update SEO and structured data.
8. Verify all links, contacts, maps and reservations.
9. Perform final QA.
10. Deploy to GitHub Pages.

---

# 4. BASTIONE MUST NOT BE MODIFIED

Bastione is the source/reference project.

Never modify the original Bastione project as part of this work.

Never push changes to the Bastione repository.

All modifications must be made only inside:

**DAAART-STUDIO/albuongusto**

The final project must be completely independent from Bastione.

---

# 5. PRESERVE THE EXISTING WEBSITE STRUCTURE

Initially preserve the Bastione structure, design system and functionality.

The following elements should remain functionally equivalent unless there is a specific reason to change them:

- header
- navigation
- mobile navigation
- hero
- page sections
- scroll behavior
- scroll progress indicator
- animations
- transitions
- theme switching
- language switching
- responsive behavior
- gallery
- menu section
- location section
- events section
- visit section
- reservation section
- reservation modal
- buttons
- CTA behavior
- footer
- accessibility behavior

The Bastione section structure currently includes:

**Hero → View → Experience → Moments → Cuisine → Menu → Place → Events → Visit**

Keep this structure initially.

Sections may later be renamed, modified, removed or replaced only when there is a clear content/design reason for HOSTARIA AL BUONGUSTO.

---

# 6. IMPORTANT: CONTENT FIRST, CODE SECOND

The main task is to transform the content of the existing website.

Do not rewrite working components simply because the content is changing.

If an existing component can display the new restaurant content, reuse it.

For example:

If Bastione has a Hero component, replace:

- title
- subtitle
- description
- image
- CTA
- metadata

inside the existing Hero implementation rather than creating an entirely new Hero component.

The same principle applies to:

- About
- Experience
- Cuisine
- Menu
- Gallery
- Place
- Events
- Visit
- Reservation
- Footer

---

# 7. CONTENT REPLACEMENT

Every piece of Bastione-specific restaurant information must eventually be replaced with information about HOSTARIA AL BUONGUSTO.

This includes:

- restaurant name
- logo
- descriptions
- headings
- subtitles
- address
- telephone
- email
- website
- social links
- opening hours
- menu
- prices
- reservation information
- location
- coordinates
- events
- history
- restaurant story
- cuisine descriptions
- gallery
- images
- SEO metadata
- structured data
- Open Graph data
- favicon if appropriate
- page title

Do not simply replace the restaurant name.

All content must be reviewed for relevance to the new restaurant.

---

# 8. VERIFIED INFORMATION ONLY

Never invent factual information about HOSTARIA AL BUONGUSTO.

This is especially important for:

- address
- phone
- email
- website
- opening hours
- menu
- prices
- reservation system
- booking URLs
- cuisine
- restaurant history
- owner
- chef
- awards
- events
- facilities
- parking
- terrace
- accessibility
- coordinates
- social media
- ratings
- reviews

If information is not verified, do not present it as fact.

If information is uncertain or conflicting, clearly indicate this and wait for verification before adding it to the production website.

---

# 9. RESEARCH SOURCES

When restaurant information needs to be researched, use current and reliable sources.

Prefer:

1. Official restaurant website
2. Official Google Business profile
3. Official Instagram
4. Official Facebook
5. Official menu
6. Official reservation platform
7. Reputable local tourism sources
8. Reputable restaurant directories

When sources conflict:

1. Prefer the official source.
2. Prefer the most recently updated reliable source.
3. If uncertainty remains, do not guess.

---

# 10. LOCATION

The confirmed project location is:

**HOSTARIA AL BUONGUSTO**

Via Fontana, 2  
25010 Limone sul Garda BS  
Italy

Never use Bastione's:

- address
- city
- coordinates
- map location
- telephone
- contact information

The geographic coordinates must be verified before being used.

---

# 11. IMAGES

The Bastione images are only temporary source assets during the migration process.

Do not assume that Bastione restaurant photography is appropriate for the final Al Buongusto website.

Progressively replace Bastione-specific images with relevant HOSTARIA AL BUONGUSTO images.

Do not use unrelated stock photography as if it represents the restaurant.

Every final production image must be relevant to HOSTARIA AL BUONGUSTO.

Optimize images for:

- performance
- responsive layouts
- mobile devices
- correct aspect ratios
- loading performance
- accessibility

Provide meaningful alt text.

---

# 12. DESIGN

The visual quality and design language of Bastione should initially be preserved.

Do not redesign the entire website during the initial content migration.

The new website should gradually develop its own identity through:

- restaurant photography
- colors
- typography where appropriate
- content
- imagery
- culinary storytelling
- local identity
- restaurant-specific details

The final website should feel like a website specifically created for HOSTARIA AL BUONGUSTO, while retaining the high-quality interaction and structural foundation of Bastione.

---

# 13. LANGUAGES

The existing Bastione website supports multiple languages.

Preserve the existing multilingual architecture.

The primary language for HOSTARIA AL BUONGUSTO is:

**Italian**

If the existing project supports:

- Italian
- English
- German

retain these languages unless explicitly instructed otherwise.

Do not simply copy Bastione translations.

All restaurant-specific content must be rewritten/adapted for HOSTARIA AL BUONGUSTO.

Translations should be natural and appropriate for a professional Italian restaurant.

---

# 14. MENU

The menu is factual content.

Never invent menu items or prices.

If an official current menu is available, use the verified information.

Preserve:

- dish names
- categories
- descriptions
- prices
- allergens

only when verified.

If a current menu cannot be verified, do not fabricate one.

The existing menu component can remain in place while awaiting verified content.

---

# 15. RESERVATION

The reservation system must represent the actual reservation method used by HOSTARIA AL BUONGUSTO.

Possible methods include:

- telephone
- email
- official website
- external reservation platform

Never invent a booking URL.

The existing Bastione reservation modal and interaction pattern should be preserved initially.

Only replace its restaurant-specific:

- name
- phone
- email
- reservation URL
- text
- CTA

with verified Al Buongusto information.

---

# 16. SEO

All Bastione SEO information must eventually be replaced.

Create independent SEO for HOSTARIA AL BUONGUSTO:

- page title
- meta description
- canonical URL
- Open Graph
- social metadata
- favicon
- structured data
- Restaurant schema
- LocalBusiness information

Use only verified information.

Never copy Bastione:

- title
- description
- canonical
- coordinates
- address
- phone
- email
- restaurant schema
- social profiles

---

# 17. STRUCTURED DATA

Use appropriate Schema.org structured data when supported by the existing project.

Restaurant information must correspond to HOSTARIA AL BUONGUSTO.

Only include verified properties.

Do NOT invent:

- ratings
- review counts
- prices
- opening hours
- menu URLs
- social profiles
- awards

---

# 18. BASTIONE CONTAMINATION

During the migration process it is acceptable for Bastione content to temporarily remain because the project is being progressively converted.

However, before production release there must be no Bastione-specific restaurant information remaining.

Before final deployment, search the complete project for:

- Bastione
- bastione
- Riva del Garda
- Riva
- Monte Rocchetta
- Trentino
- Via Monte Oro
- bastione.eu

Also search for all Bastione-specific:

- phone numbers
- email addresses
- coordinates
- URLs
- images
- menu items
- restaurant descriptions
- SEO metadata
- structured data
- social links

Any remaining occurrence must be reviewed.

---

# 19. DO NOT MAKE ASSUMPTIONS

When something can be checked in the source code, inspect the source code.

When something can be verified online, verify it.

When something is unknown, say that it is unknown.

Do not fill missing information with plausible-looking AI-generated content.

Accuracy is more important than completeness.

---

# 20. WORKING WITH THE USER

This project is developed interactively.

The user will provide instructions for individual changes in the chat.

Do not independently redesign or modify unrelated parts of the website.

When the user asks to change a specific section:

1. Inspect the existing implementation.
2. Identify the relevant files/components.
3. Understand how the section currently works.
4. Modify only what is necessary.
5. Preserve existing functionality.
6. Check responsive behavior.
7. Check desktop and mobile behavior.
8. Report what was changed.

Do not make unrelated changes unless they are necessary to complete the requested task.

---

# 21. CHANGE PHILOSOPHY

Prefer small controlled changes over large rewrites.

For example:

GOOD:

- replace Bastione hero text
- replace hero image
- replace restaurant address
- replace menu data
- replace reservation phone
- replace map coordinates

BAD:

- rewrite the entire component architecture
- replace the framework
- rebuild all CSS
- introduce unnecessary dependencies
- redesign unrelated sections

The existing Bastione implementation is already tested and working.

Preserve it whenever possible.

---

# 22. TESTING AFTER CHANGES

After significant changes verify:

- build succeeds
- development server works
- no JavaScript errors
- no console errors
- no broken images
- no broken links
- no missing fonts
- responsive layout works
- mobile navigation works
- animations work
- language switching works
- theme switching works
- reservation modal works

Do not consider a change complete if it breaks existing functionality.

---

# 23. GIT

This project is an independent repository:

**DAAART-STUDIO/albuongusto**

All changes belong to this repository.

Never push changes to Bastione.

Use clear commits.

Example:

```bash
git add .
git commit -m "Update Al Buongusto hero content"
git push