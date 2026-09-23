# Link Hub

A lightweight personal link hub built with semantic HTML and modern CSS, focused on performance, accessibility, privacy, and security.

No frameworks. No JavaScript. No tracking.

![Link Hub preview](docs/link-hub-preview.png)

**Live Demo:** [arthurfranklin.com.br/links](https://arthurfranklin.com.br/links)

## Overview

Link Hub is a static page that centralizes my portfolio, projects, professional profiles, and contact channels in a single responsive interface.

The project intentionally uses a minimal architecture based on HTML and CSS only. It prioritizes fast loading, straightforward maintenance, accessibility, and a reduced client-side attack surface without relying on JavaScript frameworks, third-party scripts, or runtime dependencies.

The production instance is part of my personal portfolio ecosystem and is served under the `/links` path.

## Features

- Responsive interface for desktop and mobile devices
- Semantic HTML structure
- Zero JavaScript
- Zero runtime dependencies
- Self-hosted Inter font
- Local favicon assets
- Keyboard-visible focus states
- Reduced-motion support with `prefers-reduced-motion`
- Custom 404 page
- Open Graph metadata
- Canonical URL
- `robots.txt` and XML sitemap
- Restrictive Content Security Policy
- Additional HTTP security headers

## Tech Stack

| Technology | Purpose |
| --- | --- |
| HTML5 | Semantic structure and content |
| CSS3 | Layout, responsive design, animations, and visual styling |
| Inter | Self-hosted interface typography |
| Static hosting | Deployment without an application runtime |

The project has no package manager, build process, JavaScript bundle, or client-side framework.

## Project Structure

```text
link-hub/
├── docs/
│   └── link-hub-preview.png
├── public/
│   ├── css/
│   │   └── style.css
│   ├── favicon/
│   └── fonts/
├── .gitignore
├── 404.html
├── _headers
├── index.html
├── LICENSE
├── README.md
├── README.pt-BR.md
├── robots.txt
└── sitemap.xml
```

## Security & Privacy

Link Hub follows a deliberately restrictive security model suited to its static architecture.

The application does not require JavaScript execution, external API connections, embedded frames, third-party fonts, analytics, advertising, or tracking scripts.

The deployment defines a restrictive Content Security Policy and additional HTTP security headers, including:

- `Content-Security-Policy`
- `X-Content-Type-Options`
- `X-Frame-Options`
- `Referrer-Policy`
- `Permissions-Policy`
- `X-XSS-Protection`

The Content Security Policy explicitly restricts capabilities that are unnecessary for the application, including scripts, external connections, objects, frames, forms, media, workers, and manifests.

Images, fonts, and styles are limited to same-origin resources according to the requirements of the interface.

External services are only accessed when a visitor explicitly follows one of the links available on the page.

## Accessibility

The interface includes accessibility considerations throughout its structure and styling:

- Semantic HTML elements
- Descriptive accessible labels
- Decorative graphics excluded from the accessibility tree where appropriate
- Keyboard-visible focus states with `:focus-visible`
- Logical heading and content structure
- Responsive layouts
- Reduced-motion support through `prefers-reduced-motion`

Core content and navigation remain available without client-side scripting.

## SEO

The project includes metadata and crawler resources for its production page:

- Page title and meta description
- Canonical URL
- Open Graph metadata
- Twitter card metadata
- `robots.txt`
- XML sitemap

The canonical production URL is:

```text
https://arthurfranklin.com.br/links
```

## Deployment

The production implementation is designed to be served from:

```text
/links
```

Static assets are therefore scoped under:

```text
/links/public/
```

For example:

```text
/links/public/css/style.css
/links/public/fonts/Inter-Regular.woff2
/links/public/favicon/favicon-192x192.png
```

This base path is intentional and reflects the production deployment architecture.

Because Link Hub has no build step or runtime dependencies, it can be deployed as static content. When deploying the project under a different base path, the corresponding asset references and production metadata must be adjusted.

## Customization

This repository contains my personal implementation of Link Hub, but its structure can be adapted for other profiles.

Typical customization points include:

- Name and professional description
- Portfolio and project links
- Social profiles
- Contact channels
- Metadata and canonical URL
- Favicons and visual identity
- Typography and styling
- Deployment base path
- `robots.txt`
- `sitemap.xml`

Since the project does not use a framework or build system, these changes can be made directly in the HTML and CSS source files.

## License

This project is licensed under the MIT License. See [`LICENSE`](LICENSE) for details.

---

Developed by **Arthur Franklin** · [Português](README.pt-BR.md) · [MIT License](LICENSE)
