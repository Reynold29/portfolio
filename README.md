# Reynold's Portfolio

Personal portfolio site for Reynold Preetham — full-stack and Flutter developer.

**Live site:** [portfolio.reyziehomelab.com](https://portfolio.reyziehomelab.com)

## Overview

A static single-page site built with plain HTML, CSS, and JavaScript. No build step or package manager required.

## Project structure

```
portfolio/
├── index.html              # Main site
└── assets/
    ├── Profile-Icon.jpg    # Profile photo & favicon
    └── Resume.pdf          # Downloadable resume
```

## Run locally

Serve the project root with any static file server:

```bash
# Python
python3 -m http.server 8080

# Node (npx, no install needed)
npx serve .
```

Then open [http://localhost:8080](http://localhost:8080).

## Deploy

Upload the repo contents to any static host (Vercel, Netlify, Cloudflare Pages, GitHub Pages, or a homelab reverse proxy). Point `portfolio.reyziehomelab.com` at the deployment.

No `npm install` or build command is needed — deploy the files as-is.

## External dependencies

Loaded at runtime from CDNs:

- [Font Awesome](https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.2/css/all.min.css) — icons
- [Simple Icons](https://cdn.simpleicons.org/) — tech stack logos

## Links

- [GitHub](https://github.com/Reynold29/)
- [LinkedIn](https://www.linkedin.com/in/reynoldpreetham/)
- [Email](mailto:reynoldclare02@gmail.com)
