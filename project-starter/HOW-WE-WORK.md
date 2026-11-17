# How we work

> Shared Blueprint version: 1.3 · 2026-11-17

## Roles

| Role | Responsibility | Decision boundary |
|---|---|---|
| Codex desktop | Primary technical environment: investigates the local project, traces ownership, discusses findings and choices with the user, implements authorized work, and verifies relevant layers. | Works within approved scope, preserves existing work, and reports evidence and limits. |
| ChatGPT | Optional conceptual and strategic partner; may support discovery or provide independent analysis when useful. | Does not decide scope or material architecture choices. Project uploads are separate from local Codex context. |
| User | Sets scope, approves material architecture and project-spec decisions, accepts visual results, and authorizes consequential operations and release. | Retains decision authority throughout; routine technical steps within approved scope need no separate handoff. |

## Project separation and documentation

- Use the local Codex project context as the technical workspace for each website. A ChatGPT Project may support conceptual work for that website; keep reusable workflow guidance in a separate blueprint Project.
- Local shared documents and each website's current `PROJECT-SPEC.md` are authoritative to Codex. ChatGPT Project uploads are separate copies and are not automatically available to the local session. The shared workflow remains project-neutral.
- `PROJECT-SPEC.md` is the sole mandatory project-specific briefing and status document. Optional implementation documents may be kept when useful, but do not duplicate the spec’s current status.
- `HUMAN-CHECKLIST.md` is a reusable blank checklist. Record completed project decisions and evidence in `PROJECT-SPEC.md` or an explicitly identified supporting record.
- Project resources and local files are separate copies and require deliberate manual refresh. Project memory does not replace reading the current spec.

## New-project workflow

1. The user provides the brief, references, and local project-folder access.
2. Codex reads the shared guidance and project materials, then uses `PROJECT-SPEC-TEMPLATE.md` as the briefing schema. Requirements are labeled **Confirmed**, **Proposed**, or **To be decided**.
3. Codex investigates and discusses material architecture choices with the user. ChatGPT may contribute conceptual framing or independent analysis when useful, without creating a required handoff.
4. After the user approves requirements and material choices, Codex prepares the project-specific `PROJECT-SPEC.md` for review.
5. Once the user approves that spec, Codex uses it as authoritative context and proceeds with authorized implementation. Routine technical work continues in the same conversation through investigation, discussion, implementation, and concise closeout.

## Existing-project workflow

Start from the existing approved spec. Codex investigates only what the requested scope requires, discusses findings and material choices directly with the user, then updates affected project-specific sections with dated evidence when authorized. Proceed with routine steps already covered by the request; do not re-run new-project briefing or create an intermediate prompt/report handoff by default. A no-change conclusion is valid when evidence does not justify implementation.

## Prompt and report numbering

Give discrete, scoped work a descriptive title and sequential number when a durable task record is useful. Use decimal suffixes for follow-ups, such as `38.1`, and keep the latest sequence number in that project's `PROJECT-SPEC.md`; never put a project's current number in shared guidance. Conversational refinements within an active task do not need new prompts or reports. Close out once with a concise summary proportional to complexity, preserving material decisions, evidence, verification limits, and follow-up in the spec or an explicitly identified supporting record when appropriate.

## Implementation and verification

Codex identifies the source owner, checks Git status, and follows the [Playbook environment-readiness procedure](PINEGROW-WORDPRESS-PLAYBOOK.md#8-check-access-and-environment-readiness) for task-relevant access paths before dependent work. It prefers Pinegrow-native capabilities where they support the required export path, controls exports, preserves unrelated work, and reports what it actually checked across source, generated files, WordPress state, and rendered routes. Ask for a decision when scope or a material choice is unresolved; do not pause for approval of routine steps already authorized by the user.

A connected tool or local runtime is not proof of general access. Check only channels needed for the task. If a required access channel fails, report the blocker before dependent work; do not silently substitute another channel. Use only a documented, authorized fallback. An unavailable optional channel does not block independent authorized work. Never claim verification that was not performed.

Choose tools by behavior ownership and the evidence needed: Pinegrow MCP for supported live-editor state and native operations; Computer Use for visual inspection and UI-only work; local source and Git for repository inspection and code operations; Novamira MCP for supported WordPress operations; browser inspection for frontend visual and behavioral checks. Use only capabilities exposed by the connected tools and verify each required channel independently. MCP and Computer Use can expose state-changing capabilities during a read-only task; inspect operation scope and side effects, use only authorized operations, and protect credentials. Tool access alone is not authorization. Arbitrary PHP execution, undocumented internal endpoints, and direct database writes do not establish or replace a supported API. After two failures of the same screen interaction, stop that path, report the blocker, and give one precise manual action; continue independent work where possible. Distinguish execution from synchronization, rendered verification, and human visual acceptance. Do not repeat broad diagnostics already established; recheck mutable or task-relevant facts.

Before editing canonical source, reconcile Pinegrow's in-memory state with the disk version using the [editor/build/export/reporting procedure](PINEGROW-WORDPRESS-PLAYBOOK.md#editor-state-build-export-and-reporting). Resolve conflicts without losing either version; if safe reconciliation is unavailable, pause the dependent edit and give one precise manual action. Use the linked procedure for compiler paths, generated-PHP linting, export/synchronization reports, bounded UI retries, and safe fixtures.

## Authoritative starter and project copies

Maintain the seven shared documents in one `Project Starter` folder. That folder is both the source of truth and the ready-to-copy distribution. Keep historical and retired files in the sibling `Archive` folder; do not load them as current instructions. Update the authoritative starter first, increment its shared version consistently, then deliberately refresh existing website copies and any ChatGPT Project uploads when that separate work is authorized. Never overwrite a website's `PROJECT-SPEC.md`.

## Local copies and ChatGPT Project files

The seven shared documents may be copied into each website's Pinegrow source folder and uploaded manually into its ChatGPT Project. These are separate copies: local edits do not update uploads, and uploads do not update local files. Use the shared version identifier to review updates, then deliberately refresh the relevant copies when authorized. Shared guidance updates never overwrite a project's `PROJECT-SPEC.md`.
