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

## Deploy (GitHub Pages + Cloudflare)

Hosted on **GitHub Pages**, with **Cloudflare** handling DNS, proxy, and DDoS protection.

**Target URL:** `https://portfolio.reyziehomelab.com`

No build step — push to `main` and GitHub Pages deploys automatically.

### 1. GitHub Pages

1. Repo → **Settings** → **Pages**
2. **Source:** Deploy from branch `main` / root
3. **Custom domain:** `portfolio.reyziehomelab.com`
4. Wait for DNS check to pass, then enable **Enforce HTTPS**

The `CNAME` file in this repo tells GitHub which domain to use.

### 2. Cloudflare DNS

In the Cloudflare dashboard for `reyziehomelab.com`:

| Type  | Name        | Target               | Proxy   |
|-------|-------------|----------------------|---------|
| CNAME | `portfolio` | `reynold29.github.io` | Proxied |

- **Proxied** (orange cloud) = traffic goes through Cloudflare for DDoS protection and caching
- Do not use GitHub's A records when proxying through Cloudflare — use the CNAME above

### 3. Cloudflare SSL

Under **SSL/TLS**:

- Encryption mode: **Full (strict)**
- Enable **Always Use HTTPS** (SSL/TLS → Edge Certificates)

### 4. Verify

After DNS propagates (usually a few minutes):

- `https://portfolio.reyziehomelab.com` loads the site
- GitHub Pages shows a green check on the custom domain

## External dependencies

Loaded at runtime from CDNs:

- [Font Awesome](https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.2/css/all.min.css) — icons
- [Simple Icons](https://cdn.simpleicons.org/) — tech stack logos

## Links

- [GitHub](https://github.com/Reynold29/)
- [LinkedIn](https://www.linkedin.com/in/reynoldpreetham/)
- [Email](mailto:reynoldclare02@gmail.com)
