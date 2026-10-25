# mta-sts.auxodata.com
Hosts the MTA-STS policy for auxodata.com (enforces TLS for inbound mail to Google Workspace MX). Served by GitHub Pages from `main` (custom domain in `CNAME`).

Policy: `.well-known/mta-sts.txt` — `mode: enforce`, `mx: aspmx.l.google.com` and `*.aspmx.l.google.com` (covers the `alt1`–`alt4` MX hosts), `max_age: 604800` (7 days).

DNS (GoDaddy):
- `mta-sts` CNAME → `admin-auxo.github.io`
- `_mta-sts` TXT `v=STSv1; id=<timestamp>` — when the policy changes, bump the `id`.
- `_smtp._tls` TXT `v=TLSRPTv1; rua=mailto:admin@auxodata.com` (TLS reports)
