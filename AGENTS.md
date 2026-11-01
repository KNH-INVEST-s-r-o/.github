# Agent instructions — KNH INVEST GitHub standards

Read README.md and the relevant contribution templates before changes. This repository is public: keep internal Knowledge base URLs, budgets, private project details, infrastructure identities and sensitive data out of files and PR descriptions. These files govern this repository; do not assume GitHub automatically inherits agent instructions into other repositories.

<!-- KNH-AGENT-COLLABORATION:v1.0:begin -->
## Shared agent collaboration — v1.0 (2026-11-01)

This section supplements existing project rules; it does not replace project routing, domain constraints, approval gates or tool restrictions. Follow the current task authorization. A policy file is guidance, not an access grant or proof of technical enforcement.

### Roles and scope
- Codex desktop coordinates: clarify the outcome, consult the relevant Knowledge base and project authority, assign a bounded task, inspect results and maintain evidence.
- Choose one implementation owner: Codex desktop or an explicitly assigned Codex partner agent. Use the partner agent only when a self-contained background task has a clear benefit; do not duplicate implementation across agents.
- Copilot Code Review is the default reviewer. Giving an implementation task to Copilot is an explicit ownership handoff, not an automatic response to every review comment.
- The user owns acceptance, merge and deployment decisions. Already granted, specific authorization remains valid; do not request it again. Missing authorization for a consequential action requires a concrete proposal and decision.

### Preparation and handoff
- Verify repository identity, working directory when available, branch, base SHA, current diff and existing work before writing. Read applicable root and nested instructions and the project's authoritative context.
- One branch has one writing implementation owner at a time. Parallel implementation uses separate branches/worktrees, bounded file scopes and an integration owner. Preserve unrelated work; do not force-push or reset/clean another contributor's changes.
- Before transferring ownership, stop the prior writer and record the current head SHA and work state. The receiving owner verifies them before continuing.
- A delegated task must include the goal, repository/issue, base SHA and target branch, allowed paths, exclusions, readable context, acceptance criteria, required checks, authority boundaries and expected PR/handoff.
- Do not assume another agent knows this conversation, can access Notion, or shares memory. Supply a minimal sanitized context summary and dated references. If required context is inaccessible, report the gap and continue only independent authorized work.

### Implementation, review and completion
- Work in an isolated branch. Inspect the diff and sensitive-data exposure before pushing. Use checks appropriate to the change; do not weaken tests to obtain a green result.
- Keep draft PRs for incomplete or unaccepted work. Describe the problem, resulting behavior, validation, remaining risks and gates.
- Where configured, let automatic Copilot review run on PR creation and subsequent pushes, including drafts. Instructions alone do not enable rulesets, grant credits or create background monitoring.
- The implementation owner evaluates each finding: fix and verify valid findings; explain rejected findings with evidence; investigate uncertainty and escalate material scope changes to the coordinator.
- Push coherent corrections rather than repeated bookkeeping commits. Check review.commit_id and CI against the current head SHA. Stop unproductive repeated review/fix cycles and report the unresolved conflict.
- The coordinator checks the acceptance criteria, final diff/SHA, relevant tests/CI and remaining findings. Coordination review is not automatically an independent expert audit.
- Report PASS, PARTIAL and NOT_RUN with exact scope. Distinguish direct observation, implementer/user reports, documentation and hypotheses. Commit, CI or AI APPROVED is not deployment or business acceptance and does not replace the applicable human decision.
- Handoff includes outcome, PR/branch/SHA, checks and evidence, unresolved questions, merge/deploy status and the next precise step.

### Knowledge base, cost and continuity
- Search the relevant Knowledge base before technical diagnosis, integration or configuration. After a proven resolution or user confirmation, update the existing canonical case; create one only if no suitable case exists.
- Record technology/model, environment, symptoms, diagnosis, cause, solution, parameters, verification, limits, official sources and verification date. Cross-link related technologies. On KB failure, report it and preserve a sanitized pending summary.
- Never copy secrets or unrelated customer data into code, tasks, PRs or KB. Delegation cannot expand the task's host, environment, communication, secret-access or deployment permissions.
- ChatGPT subscription usage and GitHub AI/Actions usage are separate. Respect current approved budgets; do not change billing controls or paid permissions to finish a task.
- Do not assume continuous coordination after a chat ends. Persistent monitoring or automated dispatch requires a separately defined authorized mechanism.
- Before dispatching through an @codex mention, identify the intended integration; a partner agent and another Codex connector may both respond.
- Keep repository copies versioned with their source. An open PR is a candidate, not an organization-wide rollout or proof that every client loaded these instructions.
<!-- KNH-AGENT-COLLABORATION:v1.0:end -->

Source: KNH INVEST shared collaboration policy v1.0, user-approved 2026-11-01. This public operational summary omits internal links and account details. Repository-specific copies must preserve their own rules.
