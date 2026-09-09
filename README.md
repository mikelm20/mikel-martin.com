# mikel-martin.com

Personal site and portfolio of Mikel Martin. Static HTML served by Caddy in a container, deployed on Fly.io.

## Local

    docker build -t mikel-martin.com .
    docker run --rm -p 8080:8080 mikel-martin.com

Open http://localhost:8080.

## Fly.io

    fly launch      # first time: creates the app and fly.toml from the Dockerfile
    fly deploy      # every time after

Then point mikel-martin.com at the app: `fly certs add mikel-martin.com` and add the A/AAAA records it prints.

## Layout

- `site/` static files, the whole website
- `Caddyfile` server config: gzip, security headers, clean URLs
- `Dockerfile` two-line Caddy image
