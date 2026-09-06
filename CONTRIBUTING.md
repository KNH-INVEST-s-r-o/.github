# Contributing to KNH INVEST repositories

This document defines the default contribution workflow for repositories owned by KNH INVEST s.r.o. Repository-specific rules may add stricter requirements.

## Workflow

Use GitHub Flow:

1. Start from an up-to-date `main` branch.
2. Create a short-lived branch for one coherent change.
3. Commit the change using Conventional Commits where practical.
4. Open a pull request into `main`.
5. Resolve review conversations and required checks.
6. Merge using **Squash and merge**.
7. Delete the source branch after merge.

Direct changes to protected `main` are not part of the normal workflow.

## Branch naming

Use a stable work-item ID when one exists:

```text
feature/AREA-012-short-description
fix/AREA-015-short-description
chore/AREA-004-short-description
docs/AREA-006-short-description
refactor/AREA-009-short-description
```

Examples:

```text
feature/ENERGY-012-manual-meter-reading
fix/NODE-015-uplink-normalization
chore/INFRA-004-ci-validation
```

For small governance/documentation changes without a work item, use a concise descriptive branch name such as `docs/update-contributing`.

## Commit messages

Prefer Conventional Commits:

```text
feat(scope): description
fix(scope): description
docs(scope): description
refactor(scope): description
test(scope): description
chore(scope): description
ci(scope): description
```

The stable work-item ID may be included when useful, but the pull request and linked issue remain the main traceability mechanism.

## Pull requests

A pull request should explain:

- what changes;
- why the change is needed;
- how it was tested or validated;
- the related GitHub issue when applicable;
- related documentation or ADR when applicable;
- any breaking or security-relevant impact.

Keep pull requests focused. Do not mix unrelated implementation, cleanup, and architecture changes in one PR.

## Issues and work-item IDs

GitHub Issues are used for concrete technical implementation work. Product, project, business, customer, roadmap, and broader decision context belongs in the project knowledge system and may link to the corresponding GitHub issue.

Stable IDs use the form:

```text
AREA-NNN
```

Examples include `INFRA-004`, `LORA-001`, `NODE-001`, `IOT-003`, and `PLAT-010`.

Issue titles should normally use:

```text
[AREA-NNN] Imperative technical title
```

Do not recycle stable IDs.

## Architecture decisions

Decisions with meaningful alternatives or long-term technical consequences should be recorded as ADRs in the owning repository. The ADR records the implementation-level decision and consequences; higher-level project context may remain in the project knowledge system.

## Security and secrets

Never commit production secrets or credentials, including passwords, private keys, API tokens, LoRaWAN root/session keys, MQTT credentials, VPN private keys, certificates containing private material, or populated `.env` files.

Use `.env.example` only for documented variable names and safe example values.

If a secret is committed accidentally, treat it as compromised: revoke or rotate it and remove it from normal repository history according to the incident procedure. Merely deleting it in a later commit is not sufficient.

## Generated and runtime data

Do not commit runtime databases, logs, caches, generated credentials, Node-RED credential stores, broker persistence files, or customer operational datasets unless a repository explicitly defines a safe fixture/test-data format.

## Ownership

Changes should be reviewed by the technical owner of the affected area when additional reviewers are available. Repository `CODEOWNERS` files provide the default ownership signal; project responsibility boundaries remain authoritative where explicitly documented.

## Licensing

Repositories are proprietary by default unless an explicit licensing decision states otherwise. Do not add an open-source license automatically.
