# Johnson Family Resort

A static multi-page marketing site for the Johnson Family Estate, designed to present accommodations, amenities, guest logistics, local highlights, and host contact details in a polished, mobile-friendly experience.

## Live Site

Production URL: [https://johnson-family-resort.jaxsnjohnson.com/](https://johnson-family-resort.jaxsnjohnson.com/)

## Site Map

- `/` - Overview
- `/accommodations/` - Accommodations
- `/amenities/` - Amenities
- `/gallery/` - Gallery
- `/arrival-guide/` - Arrival & Stay Guide
- `/local-area/` - Local Area
- `/contact/` - Contact Host

## Tech Stack

- HTML5
- [Tailwind CSS CDN](https://cdn.tailwindcss.com)
- Google Fonts
- No build step
- No package manager
- No framework

## Project Structure

```text
.
├── CNAME
├── index.html
├── accommodations/
│   └── index.html
├── amenities/
│   └── index.html
├── arrival-guide/
│   └── index.html
├── contact/
│   └── index.html
├── gallery/
│   └── index.html
├── local-area/
│   └── index.html
└── images/
    └── *.jpeg / *.JPG
```

Key files and directories:
- `index.html`: homepage/overview
- `accommodations/`, `amenities/`, `gallery/`, `arrival-guide/`, `local-area/`, `contact/`: route folders, each with its own `index.html`
- `images/`: shared media assets
- `CNAME`: custom domain for GitHub Pages

## Run Locally

Use a local static server so root-relative links (`/...`) work correctly.

```bash
python3 -m http.server 8080
```

Then open:
- [http://localhost:8080](http://localhost:8080)

Note: opening pages directly with `file://` may break root-relative links and asset paths.

## Content Editing Guide

When updating content, check each page route because navigation/footer and metadata are duplicated across files.

Update locations:
- Page copy: each route's `index.html`
- Navigation and footer: replicated in every page file
- SEO tags per page: `title`, meta description, canonical, Open Graph, and Twitter tags
- Structured data per page: JSON-LD (`application/ld+json`)
- Media assets: add/update files in `images/` and keep `alt` text aligned with image content

## Deployment

### GitHub Pages + Custom Domain

1. Commit and push changes to the branch configured in GitHub Pages settings (the repository's publishing branch).
2. Confirm `CNAME` remains committed with:
   - `johnson-family-resort.jaxsnjohnson.com`
3. In GitHub, verify Pages build/publish status in repository settings.
4. After deploy completes, validate live routes, links, and image paths.

Important:
- DNS for `johnson-family-resort.jaxsnjohnson.com` must already be configured to point to GitHub Pages.

## Quality Checklist

Before merge/deploy:
- Navigation links work on desktop and mobile menus
- No broken image references
- No browser console errors
- Per-page metadata and canonical URLs match each route
- Responsive layout checks pass on common viewport sizes

## Contribution Notes

- Keep updates consistent with the existing estate visual system (palette, typography, spacing tone).
- Prefer focused commits with concise changes.
- For content updates that span multiple pages, use clear commit messages and, when practical, isolate one page per commit.

## Public Interfaces / Types

- No API/interface/type changes in this repository.
- This project is static documentation/content markup only.

## Test Cases and Validation Scenarios

1. README renders correctly on GitHub (headings, links, code blocks).
2. Local server command runs and all routes load from `http://localhost:8080`.
3. Route documentation in this README matches repository folders/files.
4. Deployment notes align with current `CNAME` and GitHub Pages flow.
5. README avoids sensitive operational data.

## Assumptions and Defaults

- Audience: balanced between project overview and contributor guidance.
- Deployment documentation: includes explicit GitHub Pages steps.
- Format: plain Markdown, no badges or screenshots.
- Scope: documentation-only; no CI/tooling/framework changes.

## License

No license specified yet.
