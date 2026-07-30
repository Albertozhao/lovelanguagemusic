# Love Language Music

Static Astro site configured for Cloudflare Pages.

## Local development

Use Node.js 22.16.0 (pinned in `.node-version`), then install and run:

```sh
npm ci
npm run dev
```

## Deploy with Cloudflare Pages

### Git integration

Create a Pages project from this repository and use:

- Framework preset: Astro
- Production branch: `main`
- Build command: `npm run build`
- Build output directory: `dist`
- Root directory: `/`

Cloudflare will install dependencies and deploy every push to the production
branch. Pull requests receive preview deployments.

### Wrangler

Authenticate once, then build and deploy:

```sh
npx wrangler@latest login
npm run deploy
```

The first deployment may prompt you to create the `love-language-music` Pages
project. If that project name is unavailable, update `name` in
`wrangler.jsonc`.

To test the built site in the Pages runtime locally:

```sh
npm run pages:dev
```

The static build is written to `dist/`. No Astro Cloudflare adapter is needed
unless the site later adds server-side rendering or Pages Functions.
# lovelanguagemusic
