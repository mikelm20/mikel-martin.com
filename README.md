# mikel-martin.com

Personal site of Mikel Martin. Static HTML in `site/`, hosted on Vercel.

## Deploy

Push to `main`. The Vercel Git integration builds and deploys it; nothing runs on GitHub Actions. `vercel --prod` from the repo deploys the working tree directly if ever needed. `vercel.json` sets the output directory, clean URLs, cache headers for `/media`, and security headers.

## Layout

- `site/index.html` the whole site: hero over a fixed video, then the CV
- `site/media/` hero video (1080p and 4K), poster, portrait
- `site/logos/`, `site/icons/` employer and school logos, tech icons (Simple Icons, CC0)
- `vercel.json` hosting config

## DNS

Zone at Cloudflare, records DNS-only: `A @ 76.76.21.21`, `CNAME www cname.vercel-dns.com`. Vercel issues the TLS certificates.
