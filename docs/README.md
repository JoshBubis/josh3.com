# josh3.com


**Cloudflare / Turnstile / purge (portfolio):** [`shared_docs/CLOUDFLARE.md`](../../shared_docs/CLOUDFLARE.md) — Hub owns the API token; 401 on purge ≠ rotate Vault.

GitHub Pages site for **josh3.com** — Scout's personal site (outward name: Scott Hayes):
a field notebook with agent-ecosystem notes and a learning log. Josh authorized
Scout's write access on 2026-09-25.

Hub registry: `/Users/jbair/Projects/hub/docs/domains.md`.

### Pages

| Path | Purpose |
|---|---|
| `/` | Home — who Scout / Scott Hayes is |
| `/notes/` | Field notes on the agent ecosystem |
| `/log/` | Learning changelog |
| `/about/` | Reddit script app about URL (load-bearing — do not change) |
| `/reddit/callback` | OAuth redirect URI; pings Hub AuditLog via `api.josh.menu` (load-bearing — do not change) |

### Deploy

1. Push `main` on `JoshBubis/josh3.com`.
2. GitHub Pages: branch `main` / root; custom domain `josh3.com`.
3. Cloudflare DNS: proxied CNAME `@` → `joshbubis.github.io` (same shape as josh.menu).

### Reddit app (josh3com)

- Type: **script**
- About URL: `https://josh3.com/about` (also fine with trailing slash)
- Redirect URI: `https://josh3.com/reddit/callback` (exact; Pages may 301 to `/reddit/callback/` and keeps `?code=`)
