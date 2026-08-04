# josh3.com

Thin GitHub Pages site for the **josh3.com** personal / pre-product host.

Hub registry: `/Users/jbair/Projects/hub/docs/domains.md`.

### Pages

| Path | Purpose |
|---|---|
| `/` | Quiet landing |
| `/about/` | Filler “about” for the Reddit script app about URL |
| `/reddit/callback` | OAuth redirect URI; pings Hub AuditLog via `api.josh.menu` |

### Deploy

1. Push `main` on `JoshBubis/josh3.com`.
2. GitHub Pages: branch `main` / root; custom domain `josh3.com`.
3. Cloudflare DNS: proxied CNAME `@` → `joshbubis.github.io` (same shape as josh.menu).

### Reddit app (josh3com)

- Type: **script**
- About URL: `https://josh3.com/about` (also fine with trailing slash)
- Redirect URI: `https://josh3.com/reddit/callback` (exact; Pages may 301 to `/reddit/callback/` and keeps `?code=`)
