# AGENTS.md — josh3.com

Static GitHub Pages placeholder for **josh3.com** (personal / pre-product host).
Local path: `/Users/jbair/Projects/josh3.com`.

## What this is

- Reserved domain (Hub `docs/domains.md`). Candidate revive host for frozen
  `beanspill`; until a real product ships, this repo is a thin public face:
  `/about` (Reddit app about URL) and `/reddit/callback` (OAuth redirect).
- Not Josh Menu. Not the résumé. No Studio, no chat widget, no surname branding.

## Shipping

1. Bump `?v=` on `style.css` when styles change.
2. Push `main` → GitHub Pages.
3. Apex DNS is a proxied CNAME to `joshbubis.github.io` (Cloudflare). Do not
   point the apex at the home tunnel unless a real app is routed there.
4. Reddit OAuth redirect URI must match exactly:
   `https://josh3.com/reddit/callback`
5. Callback page pings Hub `POST https://api.josh.menu/webhooks/reddit_oauth`
   so hits show up in Hub AuditLog (never send client secrets or full codes).

## Boundaries

| Concern | Folder |
|---|---|
| This static site | `/Users/jbair/Projects/josh3.com` |
| Hub webhook / Vault / DNS | `/Users/jbair/Projects/hub` |
| Frozen GPU tracker | `/Users/jbair/Projects/beanspill` |
| Josh Menu sales | `/Users/jbair/Projects/josh.menu` |
