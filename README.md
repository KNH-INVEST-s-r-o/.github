# KNH INVEST GitHub standards

This repository contains organization-wide GitHub defaults and contribution templates for repositories owned by **KNH INVEST s.r.o.**

## Purpose

The repository standardizes the technical workflow used across KNH INVEST projects, including SmartGovIOT.

It provides shared defaults for:

- issue forms,
- pull request descriptions,
- organization profile content,
- common contribution conventions.

Repository-specific requirements may override these defaults when needed.

## Working model

The default development workflow is:

1. Create a short-lived branch from `main`.
2. Implement and test the change.
3. Open a pull request.
4. Review and run required checks.
5. Squash-merge into `main`.

Preferred branch naming:

- `feature/<ID>-short-description`
- `fix/<ID>-short-description`
- `chore/<ID>-short-description`
- `docs/<ID>-short-description`
- `refactor/<ID>-short-description`

Preferred commit prefixes follow Conventional Commits where practical: `feat`, `fix`, `docs`, `refactor`, `test`, `chore`, and `ci`.

## Project management boundary

- **Notion** is the source of truth for product, project, business, process, and decision context.
- **GitHub** is the source of truth for technical implementation, source code, configuration, issues, pull requests, and versioned technical decisions.

Technical work should reference the corresponding stable project ID when one exists, for example `INFRA-004`, `LORA-007`, or `ENERGY-012`.

## Security

Do not commit secrets, credentials, private keys, API tokens, passwords, production `.env` files, or customer-sensitive data to Git repositories.

## Public repository notice

This `.github` repository is intentionally public because GitHub requires a public organization `.github` repository for default issue and pull request templates to apply to repositories across the organization. Do not store confidential project information here.

Copyright © KNH INVEST s.r.o. All rights reserved.
