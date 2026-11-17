# Human Project and Launch Checklist

> Shared Blueprint version: 1.3 · 2026-11-17

This is a reusable blank checklist. Complete only stages relevant to the project. Record completed decisions and evidence in the project’s `PROJECT-SPEC.md` or an explicitly identified supporting record; do not treat the shared checklist as project status. Blank fields are prompts, not approvals.

For each applicable item, record status, owner, date, and evidence. Mark unavailable required browser/environment checks as blocked instead of inferring a pass. Do not proceed to a consequential release gate while a required item lacks evidence or has unresolved blockers; a human records the decision and deployment requires separate explicit authorization.

## Project setup and scope

- [ ] The project brief and intended outcomes are understood.
- [ ] Requirements are labeled Confirmed, Proposed, or To be decided.
- [ ] Material architecture choices and project spec were reviewed and approved before implementation.
- [ ] For an existing site, changes are scoped against its approved spec and history.

Reviewer: ___ Date: ___ Evidence/decision: ___

## Implementation review

- [ ] Codex desktop findings, assumptions, and evidence limits were reviewed.
- [ ] Source ownership and proposed changes are clear.
- [ ] Existing work and unrelated files are preserved.
- [ ] Pinegrow-native behavior was considered and actual export behavior checked where relevant.
- [ ] Verification evidence and untested layers are clearly stated.
- [ ] Human visual acceptance is recorded separately from technical/rendered verification where visual review is required.
- [ ] The human reviewer records PASS, PENDING, BLOCKED, or N/A with evidence; unresolved required checks block the next consequential gate.
- [ ] Export/package commands are distinguished from observed automatic synchronization; actual generated PHP was linted where applicable.

Reviewer: ___ Date: ___ Evidence/decision: ___

## WordPress and release review

- [ ] Intended environment, active theme, and task-relevant access paths are identified using the [Playbook environment-readiness procedure](PINEGROW-WORDPRESS-PLAYBOOK.md#8-check-access-and-environment-readiness).
- [ ] WordPress data changes, if any, were authorized and verified with appropriate cleanup.
- [ ] Relevant file-based and database-saved templates/parts were considered.
- [ ] Content, media rights, forms, analytics, consent, privacy, SEO/schema, accessibility, performance, security, and legal review are addressed where relevant. In a clean anonymous context, record relevant storage, cookies, network destinations, and data flows; obtain qualified review for legal/privacy decisions. Analytics and consent services are not defaults.
- [ ] Production URLs, redirects, TLS, backups, caching, sitemap/robots, forms, and route behavior are checked before launch where applicable.
- [ ] The user explicitly approves consequential release actions.

For editor conflicts, generated-code checks, bounded UI retries, and ChatGPT Project resource refresh, follow the [Playbook release procedure](PINEGROW-WORDPRESS-PLAYBOOK.md#editor-state-build-export-and-reporting).

Reviewer: ___ Date: ___ Evidence/decision: ___

## Decision record

| Item | Status (Pending / Approved / Blocked / N/A) | Owner | Date | Evidence or next action |
|---|---|---|---|---|
| Scope and architecture |  |  |  |  |
| Design/content acceptance |  |  |  |  |
| Privacy/legal review (if applicable) |  |  |  |  |
| Implementation review |  |  |  |  |
| Runtime verification |  |  |  |  |
| Production verification (if applicable) |  |  |  |  |
| Release authorization |  |  |  |  |
