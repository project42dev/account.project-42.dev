# account.project-42.dev

Project 42's learner account and profile surface, per
[ADR-0009's 2026-08-01 amendment](https://github.com/project42dev/project42dev-ops/blob/main/pmo/adrs/0009-owner-administration-surface.md).

This repository is currently a placeholder: it establishes the GitHub Pages
deployment and DNS boundary ahead of migrating the account/profile surface
out of `learn.project-42.dev/account`. Until that migration lands, the
learner-facing account page remains at `learn.project-42.dev/account`.

## Hosting

- GitHub Pages, deployed via `.github/workflows/deploy-pages.yml` on every push
  to `main`.
- DNS-only CNAME to `project42dev.github.io` (Cloudflare), matching the
  `learn.`/`guide.` pattern from `SPIKE-008-three-site-cutover.md`.
- No application code yet — see `project42dev-ops` for the migration plan.

## Security

Sign-in, session management, and every authorized operation stay entirely
server-side in the Cloudflare Worker API (`project42-platform`). This origin,
once it hosts the real account surface, receives only an opaque
`Secure`, `HttpOnly` session cookie — never provider tokens or credentials.
