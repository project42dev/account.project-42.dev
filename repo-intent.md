# Repo intent — account.project-42.dev

**Project 42 learner account and profile surface — deployed build output, not source.**

## What this repo is

Like `admin.project-42.dev`, the repo root holds compiled Next.js output
(`_next/`, `pages-manifest.json`, `vinext-client-entry-manifest.json`,
`release-facts.json`) rather than application source. This is a **deploy target
repo** — no README exists to confirm which source repo builds and pushes here.

## What this repo is not

- Not where the account/profile surface's source code lives — treat as generated
  output

## Status

Active (serving), but **undocumented**. Whoever next touches this repo's deploy
pipeline should update this file with the actual source repo and deploy mechanism.
