# Pinegrow → WordPress Playbook

> Shared Blueprint version: 1.3 · 2026-11-17

## Purpose

A reusable method for building and maintaining WordPress sites with Pinegrow. Adapt it to the actual project. Do not assume a sample folder layout, exporter behavior, runtime, or plugin applies everywhere. The site's approved `PROJECT-SPEC.md` records its specific architecture and evidence.

## 1. Establish scope and ownership

Record the audience, routes, content needs, user journeys, and verification expectations. Identify which system owns markup, design actions, blocks, templates, editorial content, plugin-managed fields, menus, SEO/schema, translation, forms, and runtime settings. Give each behavior one authoritative owner.

Common boundaries are starting points, not facts: Pinegrow often owns source markup, block definitions, design actions, and export configuration; WordPress often owns editorial records, menus, plugin settings, and saved Site Editor content. Confirm these in the project.

## 2. Brief and approve

For new projects, Codex desktop uses `PROJECT-SPEC-TEMPLATE.md`, reads the supplied brief and materials, labels requirements **Confirmed**, **Proposed**, or **To be decided**, and asks only essential questions. The user approves the spec and material architecture choices before implementation. Codex prepares the project-specific spec for review and proceeds with authorized work after approval. ChatGPT may contribute conceptual or independent analysis when useful, without requiring a handoff for routine technical steps.

For existing projects, use their approved spec and make scoped updates; do not restart briefing by default.

## 3. Map Pinegrow and WordPress layers

Inspect the actual Pinegrow project files, actions, framework configuration, block definitions, export settings, WordPress theme, and saved Site Editor state relevant to the task. Distinguish design/assembly pages, export pages, reusable block definitions, theme templates/parts, generated output, and database-saved templates/parts by behavior, not filename alone. A source page may define reusable blocks while not exporting as a classic template if the actions and export output prove that pattern.

A reusable block supplies a reusable content or structure unit. A page composition arranges blocks. A WordPress Site Editor template or part determines a broader route or shared composition. Verify how the specific site connects these layers.

## 4. Prefer Pinegrow-native behavior

When a Pinegrow WordPress Action, block feature, dynamic binding, template capability, or export mechanism reliably meets the requirement, prefer it over manual PHP, hardcoded URLs, or parallel custom implementations. Before custom code, identify the native feature, verify export-path support, and inspect generated output and runtime behavior. Document why custom code is needed when native support is unavailable, incompatible, or insufficient. A visible UI control alone does not prove support in every export mode.

## 5. Organize assets and code around the project

Inspect existing structure before proposing changes. Keep fonts, imagery, CSS, JavaScript, and PHP at the layer that owns them. Centralize shared assets where the project loader supports it; scope component assets when appropriate; keep editor-only assets out of the frontend when required. Treat Pinegrow-managed bootstrap/registration output separately from substantial custom integration logic when the project supports that boundary. Do not create folders merely to match an example.

## 6. Model content and dynamic behavior

Define content types, fields, taxonomies, relationships, empty states, and fallbacks with the user. Keep editorial values and plugin-managed models in their owning system. Avoid duplicating relationship data to simplify a query. Keep translation-aware URLs and dates where relevant, and do not ship dead placeholder links.

For dynamic blocks, verify context, query behavior, registration, child rendering, editor preview, and empty states. Keep field-bearing markup out of replacement subtrees unless that composition has been validated.

## 7. Handle SEO, schema, privacy, and integrations

Agree which system owns SEO metadata and schema before adding output; prevent duplicate tags or entities. Review analytics, consent, forms, embeds, pixels, and remote services against project requirements and applicable review. Do not select a plugin or enable an integration by default.

### SEO, privacy, consent, and launch readiness

This is a vendor-neutral review gate, not a recommendation for an SEO, analytics, or consent product. Do not install or activate analytics or consent software by default. Revisit the gate when adding forms, pixels, embeds, analytics, remote resources, or other data collection.

- **Before launch:** verify domain/canonical/redirect/TLS behavior, metadata and schema ownership, sitemap/robots and indexability, status codes, and internal links in the intended environment. In a clean anonymous browser context, inventory cookies, storage, network destinations, embeds, forms, and other relevant data flows; record the routes, browser, date, and observations. If browser inspection is unavailable, record the exact limitation as blocked. Obtain appropriate qualified review of privacy/legal obligations and copy; do not publish draft legal text as approved advice. Check accessibility, responsive layouts, performance, errors, backups, security, and form delivery as applicable.
- **At launch:** obtain human sign-off for content, legal/privacy text, design, SEO, security/backup readiness, and release scope. Confirm the target environment and active theme and use only the authorized release path with a usable rollback plan. Recheck live TLS, redirects, canonical/indexing behavior, sitemap, representative routes, metadata/schema, and relevant consent/storage/network behavior.
- **After launch:** review errors, uptime, backups, forms, broken links, and performance. Analytics/monitoring remain optional and require privacy review before activation. Repeat relevant checks after domain, theme, plugin, consent, form, tracking, hosting, or data-flow changes.

Launch readiness is a recorded human decision supported by environment-specific evidence. A local pass does not establish production readiness.

## 8. Check access and environment readiness

Use this procedure before development that depends on WordPress automation or runtime access. Check only channels needed for the task, but verify each independently. Record the intended site, runtime, active theme, time, evidence, and limits in its project spec.

### Choose tools by behavior and evidence

Use the first suitable supported channel for the behavior being inspected, and add other channels only when the task needs their evidence:

1. **Pinegrow MCP** for supported live project/editor state and Pinegrow-native operations.
2. **Computer Use** for visual inspection of native applications and UI-only tasks.
3. **Local source and Git** for repository inspection and code operations.
4. **Novamira MCP** for supported WordPress operations and site-context reads.
5. **Browser inspection** for frontend visual and behavioral verification.

This is a selection guide, not evidence that a channel is connected. Verify each required channel independently; Pinegrow MCP does not prove local source access, WordPress MCP does not prove browser rendering, and a screenshot does not prove saved disk state. Use the documented authorized fallback if a required channel fails; unavailable optional channels do not block independent work.

MCP servers and Computer Use may expose editing or other state-changing operations even in a read-only task. Inspect the available operations and side effects, call only the capability needed and authorized, and do not infer that a connection is read-only. Protect bearer tokens and other credentials; report authentication outcomes without copying secrets. Tool availability is not authorization to write, export, reload, restart, or change settings.

### Next-session connection gate

Use this short startup sequence, adapting it to the task. These checks do not authorize writes or exports.

1. Confirm project identity, canonical source root, applicable instructions/version, project spec, Git state, and export destination.
2. Verify Local site/runtime/database using current paths and sockets with appropriate read-only permissions.
3. Verify Novamira MCP with an actual harmless site/theme read.
4. Check CLI, REST, and WP-CLI separately when needed. An unavailable optional channel does not block independent work.
5. Inspect MCP logs before classifying a failure: network permissions, TLS/certificate, OAuth, or discovery.
6. Inspect certificate identity/trust and served HTTPS only when relevant. Do not regenerate certificates, restart services, or reauthorize speculatively.
7. Use Pinegrow MCP to inspect the current project, active document, open pages, and unsaved state when those abilities are exposed. Use Computer Use for visual/editor controls when needed. Reconcile in-memory editor state with canonical disk files before source edits; verify Quick Export on Save and compiler output target before authoring/build tasks.
8. Perform one fresh browser render for required visual readiness. State whether the route used HTTP or HTTPS and record verification limits.
9. Check Gutenberg Queue only when required for a planned write.

### Structured-tools-first

For applicable operations, prefer verified MCP abilities, supported APIs, filesystem inspection, a Local-bundled CLI, logs, and automated readback. Use screen interaction for UI-only operations and necessary visual checks. Arbitrary PHP execution alone is not a supported product API; do not invoke undocumented endpoints or write plugin-owned data directly to database tables. For TranslatePress, inspect the plugin's documented and installed interfaces first. If the setup has no supported structured string-writing channel, use its editor unless new evidence establishes another supported path. After two failures of the same screen interaction, stop, report the precise blocker, and give one precise manual action; continue independent work where possible. Always distinguish execution success, synchronization, rendered-content verification, and human visual acceptance. Recheck mutable or relevant facts without making the user repeat broad diagnostics already established.

1. **Inspect MCP startup.** Read the actual startup error/output from the MCP client or server process. A message such as `Auth: Unsupported` by itself is inconclusive: determine whether the server started, completed MCP initialization, and answered a harmless read. Do not infer an auth failure or success from that label alone.
2. **Check execution and network permissions separately from authentication.** Confirm the process can launch the configured command and reach the endpoint; inspect process environment and network policy as relevant. A denied process, blocked network, or missing certificate is distinct from an authorization response.
3. **For local HTTPS**, use the verified local CA/certificate with process-scoped `NODE_EXTRA_CA_CERTS` when the Node MCP process needs it. Scope the variable to that server process. Never disable TLS verification or use `NODE_TLS_REJECT_UNAUTHORIZED=0`.
4. **Restart Codex desktop after an authorized MCP configuration change when required.** Inspect the new startup output. A configuration entry or successful shell probe alone does not prove that Codex's MCP process can initialize or call the intended site.
5. **Authorize only when required.** Initiate OAuth or another login only when the actual MCP response shows authorization is needed. Complete any required browser approval, then retry the harmless read. Do not create a second authorization flow when the existing connection already works.
6. **Check channels independently:** MCP needs an actual harmless MCP read; CLI needs a CLI command/connection check; REST needs a REST request; browser needs a fresh visual page inspection; WP-CLI needs its own WP-CLI invocation. One channel's success does not prove another. Before dependent development, the MCP read must confirm the intended site, runtime, and active theme, and the homepage or requested route must be visually inspected in a fresh browser session.

If Gutenberg Queue is used, verify its runtime and fresh heartbeat; record serializer path and errors. A required unavailable path blocks only work that depends on it. For attribute writes, capture pre-write state, make a reversible isolated change, freshly read saved attributes, render the block, restore or delete test data, and scan for residue. State whether database-saved templates/parts and file-based theme output were checked.


### Conditional diagnostics

Treat these as hypotheses to test against the project's actual actions, generated output, registrations, saved state, and runtime:

- If repeated menu labels appear, inspect whether the repeated item still contains placeholder text instead of its current WordPress item data.
- If dynamic cards disappear, inspect conditions on the visual root and the exact Function → Content/Replace boundary around field-bearing markup.
- If PHP changes do not appear live, confirm whether a full theme export is required, then trace the generated and active-theme files.
- If frontend output differs from a correct file-based template, inspect saved Site Editor templates/parts that may override it before changing the file source.
- Before deleting a generated artifact, establish whether it is registered, referenced, instantiated in saved content, or reachable; a text search alone is not enough.
- If the Pinegrow canvas differs from the frontend, compare stylesheets and asset requests in both contexts before adding CSS. Treat canvas-only styles as editor-only and verify they do not become an unnecessary frontend dependency.
- If a route breaks after registration or structural changes, inspect rewrite and registration behavior before unrelated edits; refresh permalinks only through an authorized, relevant workflow.

### Editor state, build, export, and reporting

Use this procedure whenever Pinegrow source, generated CSS/PHP, or theme output is involved.

1. **Reconcile the editor before source edits.** Use Pinegrow MCP to identify the current project, active document, open pages, and dirty state when supported; use Computer Use to inspect visible state when needed. Compare the in-memory editor state with canonical disk files. If they conflict, preserve both before reload/save/export, compare them, merge unique work, and reopen the canonical project file. Do not use Save All for unrelated documents. If a safe capture method is unknown, pause the dependent edit and give the user one precise action based on controls actually observed.
2. **Verify source and compiler paths.** Identify the canonical source, compiler input, output stylesheet, and runtime stylesheet from project settings and working peer pages. Do not infer compiler ownership from a temporary stylesheet link or assume theme export runs CSS generation. Confirm required selectors in the actual canonical runtime output.
3. **Report actions and observations separately.** State whether you explicitly ran export/package, whether a user action or automatic synchronization was observed, whether the active theme received the change, and whether the rendered route was checked. Compare content/timestamps where useful; “no export command was run” does not prove no export happened. State unknown mechanism or actor plainly.
4. **Lint actual generated PHP.** After dynamic PHP changes, run the site's Local PHP `php -l` on the actual exported PHP and active-theme copies. Inspect all generated PHP changed by the export. Hand-constructed equivalent PHP is not evidence that Pinegrow emitted valid code.
5. **Use safe test data.** Prefer read-only or in-memory fixtures. Never create published synthetic records unless the user explicitly authorizes it. If authorized, clean up and scan for residue.
6. **Bound UI retries.** After two failures of the same UI action, stop repeating it. Report the exact error, checks not completed, and one precise manual action based only on controls observed; do not guess menu labels or change global settings speculatively.
7. **Complete shared-guidance releases.** Verify the seven shared filenames, matching version labels, and internal links. Then manually refresh the corresponding ChatGPT Project resources and confirm the uploaded version; local documentation does not synchronize those resources.

## 9. Export and reconcile

Export only when authorized. Read the export and packaging behavior first. Inspect generated changes, registration, template output, and all write/delete targets. Compare canonical source, export, package targets, active theme, and relevant database overrides. Generated output is not automatically canonical.

## 10. Verify and report

Verify the route and layers relevant to the task: source, generated output, package, active theme, saved WordPress state, and rendered behavior as applicable. Record date, environment, paths/routes, observed results, and limits in the project spec. Distinguish repository facts, runtime observations, documented decisions, proposals, and unknowns. Do not claim a live browser, GUI, WordPress, or production check without performing it.
