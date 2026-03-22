# cmayes.org

This is the [Hugo](https://gohugo.io/)-based source for the static site hosted by
[Cloudflare Pages](https://pages.cloudflare.com) at www.cmayes.org.

## Development

### Prerequisites

Install Hugo: https://gohugo.io/installation/

### Local server

```bash
hugo server
```

### Build

```bash
hugo
```

Output is written to `public/`.

## Deployment

The site is deployed automatically via Cloudflare Pages on push to the `main` branch.

**Cloudflare Pages build settings:**
- Build command: `hugo`
- Build output directory: `public`
- Environment variable: `HUGO_VERSION` — set to the Hugo version used locally

## Configuration

Site configuration is in `hugo.toml`. Content lives in `content/`. Layouts are in `layouts/`.
