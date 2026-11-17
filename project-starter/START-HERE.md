# Start a Pinegrow → WordPress website project

> Shared Blueprint version: 1.3 · 2026-11-17

This folder is the ready-to-copy starter set and shared source of truth. Use the local Codex desktop project context as the primary technical workspace for each website. A ChatGPT Project may support conceptual or strategic work; keep reusable workflow guidance in a separate blueprint Project. Copy these seven shared Markdown files into the website’s Pinegrow source folder. ChatGPT Project uploads are optional, separate copies and are not automatically available to Codex. Shared workflow rules stay project-neutral, and the website’s approved `PROJECT-SPEC.md` is the sole mandatory project-specific briefing/status document. Local files and Project resources require deliberate manual refresh; Project memory does not replace reading the current spec.

## Read the guidance explicitly

Do not assume Codex desktop or ChatGPT automatically reads every Markdown file in a folder. In the local project context, have Codex locate and read these files before acting:

1. `AGENTS.md`
2. `START-HERE.md`
3. `HOW-WE-WORK.md`
4. `PINEGROW-WORDPRESS-PLAYBOOK.md`
5. `PROJECT-STARTER-CHECKLIST.md`
6. `HUMAN-CHECKLIST.md`
7. `PROJECT-SPEC-TEMPLATE.md`
8. The project brief, references, and the current project-specific `PROJECT-SPEC.md`, if present

If a required access channel fails, report the blocker before dependent work. Do not silently substitute another channel; use a documented, authorized fallback. An unavailable optional channel does not block independent work. If a required file is absent or inaccessible, report that and continue only with accessible evidence. Do not substitute a file from another project.

Before work that depends on a connected system, follow the [Playbook environment-readiness procedure](PINEGROW-WORDPRESS-PLAYBOOK.md#8-check-access-and-environment-readiness): select tools by the behavior and evidence needed, verify required channels independently, confirm site/runtime/theme with an actual supported read, and inspect the route visually in a fresh browser session when runtime verification is required.

Use the reusable connection gate in Playbook §8 before relevant work. It is a verification procedure, not authorization to write, export, restart services, regenerate certificates, or reauthorize. Number discrete scoped tasks when a durable record is useful; keep refinements under the active task and use decimal suffixes for follow-ups. Record the latest task number only in the project spec. Close out once with a summary proportionate to the work rather than creating a prompt/report handoff for each exchange.

Before source edits or export, reconcile Pinegrow’s in-memory editor state with canonical disk files and follow the [editor/build/export/reporting procedure](PINEGROW-WORDPRESS-PLAYBOOK.md#editor-state-build-export-and-reporting). Use Pinegrow MCP for supported live state, Computer Use for visual/UI checks, local source and Git for code, Novamira MCP for supported WordPress operations, and a browser for frontend verification. A tool connection is not authorization to make changes; MCP and Computer Use can expose editing capabilities even during read-only work.

For prelaunch review, use the Playbook’s vendor-neutral SEO/privacy/consent gate and the Human Checklist; neither analytics nor a consent product is a default.

## New-project briefing prompt

```text
We are starting a Pinegrow → WordPress website project. In this local Codex desktop context, first locate and read AGENTS.md, START-HERE.md, HOW-WE-WORK.md, PINEGROW-WORDPRESS-PLAYBOOK.md, PROJECT-STARTER-CHECKLIST.md, HUMAN-CHECKLIST.md, and PROJECT-SPEC-TEMPLATE.md. Also read the brief, references, and available project materials. Tell me if any source is missing or inaccessible; do not assume all Markdown is automatically loaded.

Use PROJECT-SPEC-TEMPLATE.md as the briefing schema. Classify requirements as Confirmed, Proposed, or To be decided, and ask only essential questions. Investigate technical questions directly in Codex and discuss findings with me. I decide scope and material architecture choices; obtain approval for those choices and the project spec before implementation.

During the brief, establish the SEO outcomes, audience and markets, languages, priority pages or topics, known issues, available Search Console or analytics evidence, whether AI-answer visibility matters, and what SEO controls the client will own after handover. Use the specialist skills when relevant: Impeccable for visual design and frontend quality; seo-audit for scoped conventional SEO work; ai-seo when AI-search visibility, citations, or agent readability are a real goal. Keep checks proportionate; do not run a full-site audit unless I request it or broad launch/readiness work calls for one.

I may use a separate ChatGPT Project for big-picture reasoning and strategic decisions. It is separate from this local workspace and does not receive local file updates automatically. Bring approved decisions and current context into this Codex project and record them in the project spec. Routine technical work does not require a ChatGPT → Codex handoff.

After approval, prepare the project-specific PROJECT-SPEC.md for review and proceed with authorized work. Complete only the task-relevant access-readiness checks before dependent operations. Never overwrite the reusable template or copy another website's spec.

Before source edits, reconcile Pinegrow’s in-memory editor state with canonical disk files. Inspect Git status, preserve existing changes, identify source ownership, and verify relevant access channels independently. Prefer supported Pinegrow-native capabilities, control exports, and report evidence and limits proportionate to the task. Do not infer authorization for export, WordPress writes, deployment, staging, or commits unless the task or prior approval explicitly covers them.
```

## Existing projects

Use the approved project spec as context and update only the affected sections when authorized. Preserve dated evidence and history; do not restart new-project briefing.

## Shared version and updates

The maintained `Project Starter` folder is the single authoritative shared blueprint and the ready-to-copy starter. Shared version: **1.1**. Archived versions are historical only. To update a website's local copies, compare the new version, review changes, then deliberately replace or merge the seven shared files. Preserve local instructions and project-specific spec content. Never overwrite `PROJECT-SPEC.md`.

ChatGPT Project files are separate optional uploads. When refreshing them is in scope, manually replace the corresponding shared files and confirm the uploaded version; local changes do not propagate to ChatGPT, and Project resources do not automatically load into Codex desktop.

## Documents

- [Agent instructions](AGENTS.md)
- [How we work](HOW-WE-WORK.md)
- [Pinegrow → WordPress Playbook](PINEGROW-WORDPRESS-PLAYBOOK.md)
- [Project Starter Checklist](PROJECT-STARTER-CHECKLIST.md)
- [Human Checklist](HUMAN-CHECKLIST.md)
- [Project Spec Template](PROJECT-SPEC-TEMPLATE.md)
