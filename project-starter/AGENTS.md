# Shared agent instructions

> Shared Blueprint version: 1.3 · 2026-11-17

Use these rules with [START-HERE.md](START-HERE.md), [HOW-WE-WORK.md](HOW-WE-WORK.md), [PINEGROW-WORDPRESS-PLAYBOOK.md](PINEGROW-WORDPRESS-PLAYBOOK.md), [PROJECT-STARTER-CHECKLIST.md](PROJECT-STARTER-CHECKLIST.md), [HUMAN-CHECKLIST.md](HUMAN-CHECKLIST.md), and the website's own approved `PROJECT-SPEC.md`.

## Roles and decisions

- Codex desktop is the primary environment for technical investigation, planning, authorized implementation, and verification. Work directly from the local project context, discuss findings and choices with the user, and provide a concise closeout.
- ChatGPT can support conceptual and strategic discovery or provide optional independent analysis. Its Project resources are separate from local files and are not automatically available to Codex.
- The user decides scope and material choices. Do not repeat a permission request when existing authorization covers the action.
- For a new project, use the reusable `PROJECT-SPEC-TEMPLATE.md` as the briefing schema. Classify requirements **Confirmed**, **Proposed**, or **To be decided**. Present material architecture choices for user approval before implementation; routine technical choices within approved scope do not require a separate handoff.
- Codex desktop prepares the project-specific `PROJECT-SPEC.md` for user review after requirements and material architecture choices are approved. Do not begin implementation before the spec is approved. Optional ChatGPT analysis does not replace reading the local spec.
- Existing projects use their approved spec and receive scoped updates; do not restart new-project briefing for each task. Never replace a project spec with the reusable template or a spec from another site.

## Project separation and records

- Keep reusable workflow guidance in a separate blueprint Project. A ChatGPT Project may support conceptual work for a website, but it is not the Codex local workspace.
- Each website's local project context receives the seven shared documents and its current `PROJECT-SPEC.md`; ChatGPT Project uploads are separate optional copies. Shared rules remain project-neutral; the spec is the sole mandatory project-specific briefing/status document. Optional implementation records must not duplicate its current status.
- Keep `HUMAN-CHECKLIST.md` blank and reusable. Record completed decisions/evidence in the spec or an explicitly identified supporting record. Local files and Project resources require deliberate manual refresh; Project memory does not replace reading the current spec.

## Before acting

- Read the applicable instructions and project spec. Inspect `git status --short` before changes and record existing work.
- Identify the source that owns the behavior. Preserve unrelated changes and files.
- Treat read-only requests as read-only. Do not export, package, stage, commit, deploy, or change WordPress data without authorization.
- Follow the [Playbook environment-readiness procedure](PINEGROW-WORDPRESS-PLAYBOOK.md#8-check-access-and-environment-readiness) for relevant access checks. If a required channel fails, report the blocker before dependent work; do not silently substitute another channel. Use a documented, authorized fallback. Unavailable optional channels do not block independent work. Distinguish channels; never infer access or verification.
- Before source changes, reconcile Pinegrow's in-memory editor state with canonical disk files using the [editor/build/export/reporting procedure](PINEGROW-WORDPRESS-PLAYBOOK.md#editor-state-build-export-and-reporting). If state cannot be reconciled safely, pause only the dependent edit and give the user one precise next action.

## External specialist skills

Codex may autonomously select and invoke installed specialist skills when they materially improve the requested task. Skills supplement the project's approved instructions and do not override its architecture, source ownership, scope, authorization boundaries, or verification requirements.

Read-only tasks remain read-only. Using a skill does not independently authorize source modifications, exports, deployment, or WordPress data changes.

Impeccable may be selected automatically for relevant design, interface, accessibility, and frontend-quality work, or invoked explicitly by the user.

Use `seo-audit` for relevant conventional SEO work, such as crawlability, indexability, metadata, semantics, canonical or redirect behavior, structured data, internal linking, local SEO, or SEO-related performance. Keep checks scoped to the changed page or feature; do not run a full-site audit for a small change unless requested or required by broad launch/readiness work.

Use `ai-seo` when the task concerns AI-search visibility, citations or recommendations in AI answers, or agent/crawler readability. Do not add an AI-search review to unrelated routine work.

Impeccable Live Mode and automatic hooks remain disabled unless separately authorized.

## Prompt and report records

- Number discrete scoped tasks with a descriptive title when a durable task record is useful. Keep a follow-up under the same number with a decimal suffix. Do not create a new prompt/report handoff for each conversational refinement; close out the work once with a concise summary proportional to its complexity.
- Store the latest sequence number in that project's `PROJECT-SPEC.md`, never in shared guidance.
- Select tools by behavior and owner: Pinegrow MCP for supported live-editor state and native operations; Computer Use for visual/native UI inspection and UI-only tasks; local source and Git for repository inspection and code operations; Novamira MCP for supported WordPress operations; browser inspection for frontend visual and behavioral verification. Verify each required capability independently; one connection does not prove another.
- MCP and Computer Use connections may expose editing or other state-changing abilities even during a read-only investigation. Inspect capabilities and side effects, use only the operation authorized for the task, and do not treat tool availability as authorization. Do not expose credentials or initiate authorization unless the actual response requires it. Arbitrary PHP execution, undocumented endpoints, and direct database writes are not substitutes for a supported API.
- After two failures of the same screen interaction, stop that path, report the blocker, and give one precise manual action. Continue independent work when possible.
- Report execution, synchronization, rendered-content checks, and human visual acceptance separately. Recheck only facts that can change or matter to the task; do not repeat established broad diagnostics.

## Pinegrow and WordPress

- Prefer Pinegrow-native features when they meet the requirement and support the actual export/runtime path. Verify generated output and relevant runtime behavior before relying on them. Document an exception when native behavior is unavailable or insufficient.
- Respect project ownership: Pinegrow typically owns source markup, block definitions, design actions, and export configuration; WordPress typically owns editorial data, plugin-managed models/settings, menus, and saved Site Editor content. Confirm each project's actual boundaries in its spec.
- Treat export and packaged files as generated output unless the project spec establishes otherwise. Make lasting changes at the canonical source.
- A saved WordPress template or part can override a theme file. Check the relevant database state when it may affect the requested route.
- Verify only relevant layers and state what was and was not checked. Do not claim a live runtime, browser, GUI, or production check without performing it.

## Documentation roles

- This file: concise operational rules.
- Playbook: reusable technical methodology.
- Starter checklist: chronological implementation gates.
- Human checklist: human review and release decisions.
- Project `PROJECT-SPEC.md`: that site's decisions, evidence, exceptions, statuses, and unresolved items.
