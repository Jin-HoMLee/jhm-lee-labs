# JHM Lee Labs

Minimal static landing page for JHM Lee Labs, an independent applied-AI lab / studio.

Primary site: <https://jhmlee.com>

Fallback site: <https://jhm-lee-labs.pages.dev>

Active mailbox (iCloud-backed): <jin-ho.lee@jhmlee.com>

## Local preview

This site has no build step or runtime dependencies. From the project root:

```sh
python3 -m http.server 8080
```

Then open <http://localhost:8080>. Stop the server with `Ctrl-C`.

## Cloudflare Pages deployment

The site is deployed as static files. With an authenticated Wrangler session, use the current Wrangler help to confirm command options, then create a Pages project (once) and deploy the project root:

```sh
npx wrangler pages project create <project-name> --production-branch main --force
npx wrangler pages deploy . --project-name <project-name> --branch main
```

With Wrangler 4.148.0, `--force` is needed only when creating the Pages project to bypass the Workers delegation; do not pass it on later deploys. The `main` branch produces the project’s production `pages.dev` address. There is no build command and no framework adapter to configure.

## Domain and email

The primary domain is `jhmlee.com`; the Pages address remains available as a fallback. The active mailbox is the iCloud-backed `jin-ho.lee@jhmlee.com`. Domain, DNS, Cloudflare, and account settings are managed outside this repository.

## Scope and privacy

The page contains no analytics, trackers, cookies, contact form, database, or third-party JavaScript. The public GitHub profile and public project repositories are the only external links.
