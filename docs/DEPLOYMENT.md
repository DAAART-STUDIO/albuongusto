# Deployment

## Deployment Model

HOSTARIA AL BUONGUSTO is a static website built with HTML, CSS and vanilla JavaScript ES modules.

There is no build step.

The production environment only needs to serve the project files over HTTPS.

---

## Repository

```text
https://github.com/DAAART-STUDIO/albuongusto
```

Branch:

```text
main
```

The `main` branch is the production source branch.

---

## Hosting — GitHub Pages

The website is hosted on GitHub Pages and is deployed directly from the `main` branch.

### GitHub Pages Configuration

1. Open the repository **Settings → Pages**.

2. Under **Build and deployment → Source**, select:

   **Deploy from a branch**

3. Configure:

   **Branch:** `main`
   **Folder:** `/ (root)`

4. Save the configuration.

5. Production URL:

```text
https://daaart-studio.github.io/albuongusto/
```

6. A new push to `main` triggers a GitHub Pages deployment automatically.

Deployment availability may take some time after a new push.

---

## Custom Domain

If a custom domain is connected in the future, configure it through:

**Repository → Settings → Pages → Custom domain**

The domain configuration must also be completed at the DNS provider.

After the custom domain becomes the production URL, update all domain-dependent resources, including:

* `robots.txt`
* `sitemap.xml`
* canonical URL
* Open Graph URLs
* structured data
* `site.webmanifest`
* any absolute URLs used by the website

HTTPS should be enabled through GitHub Pages after the domain has been correctly configured.

---

## Project-Subpath Constraint

The current production website is served from:

```text
https://daaart-studio.github.io/albuongusto/
```

The website therefore operates under the `/albuongusto/` project subpath.

Asset and internal resource references should remain **relative**.

Preferred:

```html
<link rel="stylesheet" href="css/base.css">
<script type="module" src="js/app.js"></script>
<img src="assets/images/example.webp" alt="">
```

Avoid root-relative paths such as:

```html
<link rel="stylesheet" href="/css/base.css">
<script type="module" src="/js/app.js"></script>
<img src="/assets/images/example.webp" alt="">
```

Root-relative paths resolve from the domain root and can result in broken resources when the website is deployed under `/albuongusto/`.

Keep paths compatible with the current GitHub Pages project-subpath deployment.

---

## Deployment Checklist

Before pushing production changes to `main`, verify:

### Content

* Restaurant name
* Address
* Telephone
* Email
* Opening hours
* Menu information
* Reservation information
* Location data

All restaurant information must be verified.

### Technical

* `index.html` loads correctly
* CSS loads correctly
* JavaScript modules load correctly
* Images load correctly
* SVG assets load correctly
* Mobile navigation works
* Reservation modal works
* Language switching works
* Theme switching works
* Animations work
* Responsive layouts work

### SEO

* Page title
* Meta description
* Canonical URL
* Open Graph metadata
* Structured data
* `robots.txt`
* `sitemap.xml`
* Favicon
* Web manifest

All production URLs and structured data must correspond to HOSTARIA AL BUONGUSTO.

### GitHub Pages

* Changes are committed
* Changes are pushed to `main`
* GitHub Pages deployment completes successfully
* Production URL is checked after deployment

---

## Local Verification

Because the project uses JavaScript ES Modules, do not open `index.html` directly using `file://`.

Run a local HTTP server before deployment.

### Python

```bash
cd albuongusto
python -m http.server 8002
```

Open:

```text
http://localhost:8002
```

Verify the website locally before pushing changes to `main`.

---

## Production Branch Policy

The `main` branch represents the production version of the website.

Changes should be:

1. Developed locally
2. Tested locally
3. Reviewed for content and technical correctness
4. Committed to Git
5. Pushed to `main`
6. Verified on the live GitHub Pages website

Avoid committing unfinished or experimental changes directly to the production branch.

---

## Privacy Note

GitHub Pages serves the website as static HTML, CSS, JavaScript and other public web assets.

Visitors can inspect the deployed frontend through browser developer tools or page source.

Repository visibility controls access to the GitHub repository itself; it does not make the rendered frontend code private once it has been published as a public website.
