# kaplan-certprep-site

Static HTML rebuild of the Kaplan CertPrep website.

## Structure

```
index.html     – Single-file static site (all JS, CSS, and content inline)
README.md      – This file
.gitignore     – Git ignore rules
```

## Features

- Full single-page app routing (CDL, HR, Trades, AI, Social Work categories)
- 50-article blog with search, category filters, and pagination
- Product detail pages with sidebar
- Blog article detail pages with related posts
- Contact form with validation
- Fade-in animations on scroll
- Responsive design (mobile-friendly)
- All images embedded as base64 (no external image dependencies)
- Google Fonts loaded via CDN

## Deployment

This site is a single static HTML file. It can be deployed to:
- GitHub Pages
- Netlify (drag-and-drop or connected repo)
- Vercel
- Any static host

## Local Development

Open `index.html` directly in a browser — no build step needed.

## Notes

- All content (blog posts, product data, brand constants) is embedded in JavaScript within the HTML file
- Navigation uses client-side routing with no URL changes
- Images are base64-encoded to ensure they display without a server
