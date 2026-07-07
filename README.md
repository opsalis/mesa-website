# mesa-website

Corporate compliance website for **Mesa Operations LLC**, hosted on Cloudflare Pages.

Same deployment pattern as `opsalis/sertone-website`: static HTML pages served from Cloudflare's edge.

## Purpose

Minimum-viable web presence for Mesa Operations LLC required by:
- Apple Developer Program organization enrollment
- Google Play Console organization enrollment
- D&B / Dun & Bradstreet identity verification (for D-U-N-S)

Full context: `K:/decisions/mesa-appstore-enrollment-runbook-2026-07-07.md`

## Pages

- `/` — home / identity
- `/privacy.html` — privacy policy (GDPR + CCPA)
- `/terms.html` — terms of use (Wyoming governing law)
- `/support.html` — contact + how to reach us
- `/404.html` — Cloudflare Pages 404 handler

## Deploy

1. Purchase domain (e.g. `mesa-ops.com`) via GoDaddy
2. Change GoDaddy nameservers to Cloudflare's
3. Add domain to Cloudflare Pages project connected to this repo
4. Cloudflare auto-deploys on every push to `main`
5. Custom domain + auto-SSL via Cloudflare

## Files intended for Cloudflare Pages conventions

- `_headers` — security response headers (HSTS, CSP, etc.)
- `_redirects` — clean-URL rewrites

## Content updates

Currently edited via git push to `main`. Cloudflare Pages redeploys automatically. To update wording, edit the HTML files directly and commit.

## Ownership

Mesa Operations LLC. All content on this site is corporate identity / legal-compliance content; no code, no product marketing.
