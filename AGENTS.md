# Project 42 Account — Agent Instructions

## What this repo is
The learner identity, profile, and account worker service for the official Project 42 hosted platform.

## Start here
Use the HCS Governance MCP server as the standards source of truth:
```text
bootstrap(repo="account.project-42.dev", client="<client>")
```

## Hard rules
1. Never commit secrets or user tokens.
2. Comply with zero-PII data minimization and privacy policies.
3. Commit format: `type(scope): description (AB#<id>)`.
