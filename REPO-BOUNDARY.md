# Repository boundary

This file states what this repository is for, what must never be added to it,
and where to look instead. It exists because two codebases ended up in the
wrong repositories, and both got there through a directory convention that
nobody enforced.

Governing decision: **ADR-0017**, Orchard and the Foundry layer separation.

## What this is

**Learner account, profile, and portable learning records.**

- Visibility: **public**

## What must never go here

| Do not add | Because | Where it belongs |
|---|---|---|
| **Owner or administrator functionality** | A learner surface that can administer the platform is a privilege escalation waiting to happen. | `admin.project-42.dev` |
| **Content of any kind** | Accounts are about people, not material. | `project42-platform` |
| **Real learner data, fixtures containing it, or exports of it** | Public repository. This one matters more here than anywhere else in the estate. | The runtime data store, never a repository |

## Looking for something else?

| Looking for | It lives in |
|---|---|
| The content, the content model, and the schemas | `project42-platform` |
| The content lifecycle tool: discovery, authoring, currency | `orchard` |
| The public marketing and entry surface | `project-42.dev` |
| The Learn delivery surface | `learn.project-42.dev` |
| The Field Guide delivery surface | `guide.project-42.dev` |
| Owner administration | `admin.project-42.dev` |
| Planning, sprints, ADRs, board records | `project42dev-ops`, private |
| An Azure AI Foundry deployment framework | `homestead-foundry` |
| One owner's Foundry instance and model registry | `my-homestead-foundry` |

## The rule in one line

**This repository is about a person and their record. It never decides what they can change about the platform.**
