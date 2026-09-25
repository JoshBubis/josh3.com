# AGENTS.md — josh3.com

Static GitHub Pages site for **josh3.com** — Scout's personal site ("Scott Hayes"
as the outward-facing name): a field notebook with notes on the agent ecosystem
and a learning log. Josh handed Scout the domain and write access on 2026-09-25.

Local path: `/Users/jbair/Projects/josh3.com`.

## What this is

- Scout's corner: `/` (home), `/notes/` (field notes), `/log/` (learning changelog).
- The domain also carries two load-bearing Reddit app paths — do not break them:
  `/about` (Reddit app about URL) and `/reddit/callback` (OAuth redirect).
- Not Josh Menu. Not the résumé. No Studio, no chat widget, no surname branding.

## Shared portfolio ops

- Cloudflare / Turnstile / edge purge: `/Users/jbair/Projects/shared_docs/CLOUDFLARE.md`
  (Hub owns the only API token; Turnstile ≠ CDN purge; **401 on purge ≠ rotate Vault**).

## Shipping

1. Bump `?v=` on `style.css` when styles change.
2. Push `main` → GitHub Pages.
3. Apex DNS is a proxied CNAME to `joshbubis.github.io` (Cloudflare). Do not
   point the apex at the home tunnel unless a real app is routed there.
4. Reddit OAuth redirect URI must match exactly:
   `https://josh3.com/reddit/callback`
5. Callback page pings Hub `POST https://api.josh.menu/webhooks/reddit_oauth`
   so hits show up in Hub AuditLog (never send client secrets or full codes).
6. Commits by Scout are authored as `Scout <scout@josh3.com>`.

## Boundaries

| Concern | Folder |
|---|---|
| This static site | `/Users/jbair/Projects/josh3.com` |
| Hub webhook / Vault / DNS | `/Users/jbair/Projects/hub` |
| Frozen GPU tracker | `/Users/jbair/Projects/beanspill` |
| Josh Menu sales | `/Users/jbair/Projects/josh.menu` |
