# mta-sts.auxodata.com
Hosts the MTA-STS policy for auxodata.com (enforces TLS for inbound mail to Google Workspace MX).
Policy: `.well-known/mta-sts.txt`. When the policy changes, bump the `id` in the `_mta-sts` TXT record.
