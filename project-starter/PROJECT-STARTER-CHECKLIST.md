# Project Starter Checklist

> Shared Blueprint version: 1.3 · 2026-11-17

Use this sequence for new projects or a substantial implementation slice. The [Playbook](PINEGROW-WORDPRESS-PLAYBOOK.md) explains the method; [AGENTS.md](AGENTS.md) sets operating rules; the site's `PROJECT-SPEC.md` holds project facts.

## Phase 1 — Brief and approve

- [ ] Read the seven shared documents, the brief, references, and available project materials.
- [ ] Identify any existing project spec and determine whether this is a new or existing project.
- [ ] For a new project, use the template and label requirements Confirmed, Proposed, or To be decided.
- [ ] Obtain user approval for the project spec and material architecture choices.
- [ ] For an existing project, use its approved spec and plan only scoped updates.
- [ ] Keep work in one Codex desktop task through investigation, discussion, authorized implementation, and closeout. Number discrete work when a durable record is useful; use decimal suffixes for follow-ups and record the latest sequence only in the project spec.

**Gate:** approved project-specific context is ready before implementation.

## Phase 2 — Establish ownership and baseline

- [ ] Inspect Git status and record pre-existing work before edits.
- [ ] Identify owners for markup, blocks, templates, content, plugin models, PHP behavior, generated output, and database overrides.
- [ ] List routes, content types, fields, taxonomies, relationships, SEO/schema, menus, forms, translation, and media relevant to scope.

**Gate:** each requested behavior has an identified source of truth and verification layer.

## Phase 3 — Map Pinegrow and access

- [ ] Confirm project root, Pinegrow configuration, actual source pages, design actions, assets, blocks, templates, and export destination.
- [ ] Classify pages by behavior: design/assembly, block source, export page, or template source.
- [ ] Identify the intended WordPress runtime and active theme when runtime work is needed.
- [ ] Select tools using the [Playbook hierarchy](PINEGROW-WORDPRESS-PLAYBOOK.md#choose-tools-by-behavior-and-evidence): Pinegrow MCP for supported live state/native operations, Computer Use for visual or UI-only work, local source/Git for repository work, Novamira MCP for supported WordPress operations, and browser inspection for frontend verification. Verify each required capability independently; record scope, time, evidence, and limits.
- [ ] Confirm export authorization before exporting. Inspect package write/delete behavior before packaging.
- [ ] Reconcile Pinegrow's in-memory active/open document state with canonical disk files before source edits; verify canonical source, compiler input, and runtime output paths.

**Gate:** no planned action relies on assumed tool access, export behavior, or source ownership.

## Phase 4 — Define design system and representative slice

- [ ] Inspect existing typography, colors, spacing, media, fonts, CSS, and JavaScript before proposing structural changes.
- [ ] Verify asset loading at the intended editor/frontend layer.
- [ ] Implement one representative content → block → composition/template → frontend path when appropriate.
- [ ] Verify registration, context, relationships, fallbacks, empty states, and editor preview.

**Gate:** representative behavior works through its intended layers before expansion.

## Phase 5 — Export and reconcile (when authorized)

- [ ] Inspect export warnings and raw generated changes.
- [ ] Review changed, new, deleted, and stale files.
- [ ] Read the packaging script's targets and mutation behavior before running it.
- [ ] Compare source, export, package, active theme, database overrides, and Git diff as relevant.
- [ ] Lint actual generated and active-theme PHP after dynamic-code changes; report explicit actions separately from observed automatic synchronization.
- [ ] Use read-only/in-memory fixtures by default; never publish synthetic records without explicit authorization.
- [ ] Stop after two failures of the same UI action and hand off the exact observed manual action if needed.

**Gate:** generated output and runtime ownership are understood.

## Phase 6 — Verify relevant behavior

- [ ] Check representative routes, links, responses, responsive behavior, keyboard access, forms, media, and empty states as in scope.
- [ ] Check dynamic data, translation, SEO/schema, errors, and regressions as in scope.
- [ ] For WordPress writes, follow the isolated reversible check and cleanup procedure in the Playbook.
- [ ] Record environment, date, paths/routes, evidence, and untested layers in the project spec.

**Gate:** report states exactly what was verified and what remains unknown.

For the detailed editor/build/export/reporting procedure, see the [Playbook](PINEGROW-WORDPRESS-PLAYBOOK.md#editor-state-build-export-and-reporting). When releasing shared guidance, manually refresh the separate ChatGPT Project resources.

## Phase 7 — Review and release

- [ ] Review every changed file and preserve unrelated work.
- [ ] Obtain human review and authorization for consequential release actions.
- [ ] Complete applicable launch checks in the Human Checklist and the Playbook’s vendor-neutral SEO/privacy/consent gate; analytics and consent services are not defaults.
- [ ] Stage, commit, export, package, or deploy only when authorized.
