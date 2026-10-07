# JHM Lee Labs

Minimal static landing page for JHM Lee Labs, an independent applied-AI lab / studio.

Live site: <https://jhm-lee-labs.pages.dev>

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

## Future domain and email

When `jhmleelabs.com` is registered and its DNS is available, attach it to this Pages project through Cloudflare Pages' custom-domain flow. Do not change billing or register a domain as part of this site repository.

Email routing is a separate Cloudflare DNS/domain step and depends on the domain existing first. It is intentionally not configured here; add routes only after the domain purchase and email-routing approval.

## Scope and privacy

The page contains no analytics, trackers, cookies, contact form, database, or third-party JavaScript. The public GitHub profile and public project repositories are the only external links.
