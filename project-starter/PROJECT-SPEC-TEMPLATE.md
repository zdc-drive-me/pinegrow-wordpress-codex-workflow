# Project Spec Template

> Shared Blueprint version: 1.3 · 2026-11-17

Use this schema during project briefing, then create a separate project-specific `PROJECT-SPEC.md` after the user approves the requirements and material architecture choices. Never replace this reusable template with project facts. Existing sites should update their approved spec in scope rather than restart briefing.

Label each requirement **Confirmed**, **Proposed**, or **To be decided**. Distinguish inspected repository facts, runtime evidence, approved decisions, recommendations, and assumptions. Record dates and evidence for facts that can change. Use Codex desktop as the primary technical workspace; ChatGPT analysis is optional and separate from local project context. Record durable task outcomes and material decisions, not every conversational refinement. Remove sections that do not apply; add project-specific sections as needed.

## 1. Project identity and goal

- Project name: [ ]
- Latest discrete task sequence number: [project-specific; e.g. 0]
- Repository/source location: [ ]
- Primary goal and audience: [ ]
- Target runtime and environments: [ ]
- Spec approval/date: [ ]

## 2. Scope and decisions

| Requirement or decision | Status | Owner/approver | Evidence or notes |
|---|---|---|---|
|  |  |  |  |

## 3. Ownership and architecture

- Pinegrow source owns: [ ]
- WordPress owns: [ ]
- Other systems/plugins and responsibilities: [ ]
- SEO/schema, menus, forms, translation, media owners: [ ]
- Material architecture choices and approval: [ ]

## 4. Access and automation readiness

Record only channels relevant to the task; recheck when used. Do not infer one channel's access from another. Follow the [Playbook environment-readiness procedure](PINEGROW-WORDPRESS-PLAYBOOK.md#8-check-access-and-environment-readiness), and record relevant endpoint, process-scoped certificate setting (path only), restart, authorization outcome, actual read result, visual inspection, and remaining trust or channel gaps. Never record bearer tokens, passwords, or other secrets. MCP and Computer Use may expose editing abilities; record the operation used and verify its scope rather than assuming a connected tool is read-only.

| Channel | Scope | Status | Checked at | Evidence or blocker |
|---|---|---|---|---|
| Pinegrow MCP live project/editor state and supported native operations |  |  |  |  |
| Computer Use native-app visual/UI inspection |  |  |  |  |
| Local source/Git and Pinegrow export authorization |  |  |  |  |
| WordPress runtime/active theme and Novamira MCP |  |  |  |  |
| Browser/visual inspection |  |  |  |  |
| WP-CLI |  |  |  |  |
| REST API |  |  |  |  |
| Other MCP integration |  |  |  |  |
| CLI integration (when relevant) |  |  |  |  |
| Queue/serializer (if used) |  |  |  |  |

For writes, record pre-state, isolated change, fresh read, rendered result, cleanup, and residue scan. Note whether database-saved and file-based templates/parts were checked.

## 5. Routes, pages, and journeys

| Route/page | Purpose | Source/composition | Data and states | QA notes |
|---|---|---|---|---|
|  |  |  |  |  |

## 6. Content model

For each post type or content model, document fields, ownership, validation, relationships, and empty states.

| Type/field | Purpose | Owner | Relationship/constraints | Status/evidence |
|---|---|---|---|---|
|  |  |  |  |  |

Taxonomies and term fields: [ ]

## 7. Blocks and templates

| Block/template/part | Canonical source | Dynamic behavior/data | Export/runtime verification |
|---|---|---|---|
|  |  |  |  |

## 8. Design system and assets

- Typography and fonts: [ ]
- Shared and component CSS: [ ]
- JavaScript and loading scope: [ ]
- Images/media ownership, fallback, and accessibility: [ ]
- Editor/canvas-only assets: [ ]

## 9. Runtime integration

- Pinegrow-managed bootstrap/registration: [ ]
- Custom PHP and other runtime code: [ ]
- Plugins/services and selected responsibilities: [ ]
- Menus, forms, translation, and external integrations: [ ]

## 10. SEO, schema, privacy, and legal

- Metadata/schema owners and duplicate prevention: [ ]
- Indexing, sitemap, canonical, and redirects: [ ]
- Consent, analytics, forms, embeds, and data flows: [ ]
- Legal/business review required: [ ]

## 11. Verification record

| Date | Environment/layer/route | Check and result | Evidence | Limits or follow-up |
|---|---|---|---|---|
|  |  |  |  |  |

For editor-state reconciliation, compiler/output-path checks, export reporting, generated-PHP linting, bounded UI retries, and shared-resource release, use the [Playbook procedure](PINEGROW-WORDPRESS-PLAYBOOK.md#editor-state-build-export-and-reporting).

## 12. Open decisions and project-specific exceptions

| Item | Status | Decision owner | Evidence/next step |
|---|---|---|---|
|  |  |  |  |

## 13. Change history

| Date | Change | Evidence/approval |
|---|---|---|
|  |  |  |
