# Quick start: Pinegrow, WordPress, and Codex

Use this page to start a new site project with the workflow described in the [community guide](workflow-guide.md). The starter files set persistent rules; this prompt starts the project brief. Keep all material decisions in the site's approved `PROJECT-SPEC.md`.

## Before the first Codex session

- Create or select the project's Pinegrow source folder.
- Install and run the local WordPress site in Local.
- Connect Pinegrow MCP and Novamira MCP using their supported setup steps. Verify each connection separately with a harmless read before depending on it.
- Make sure Codex can read the seven Project Starter Markdown files in the source folder. Use the current approved `PROJECT-SPEC.md` if this is an existing project.
- Install specialist skills globally for Codex if you want them across projects. Start a fresh Codex session after installation and confirm the skill is selectable or directly invokable. Skills guide work; they do not grant access or approve changes.

For example, to install only the two Corey Haines SEO skills:

```sh
npx skills add coreyhaines31/marketingskills --skill seo-audit --global --agent codex
npx skills add coreyhaines31/marketingskills --skill ai-seo --global --agent codex
```

The [Skills CLI agent table](https://github.com/vercel-labs/skills/blob/main/docs/agents.md) documents its current Codex global directory. Follow the installed skill's own `SKILL.md` for use instructions. Add Impeccable through its chosen trusted source separately.

## Copy-ready new-project prompt

```text
We are starting a Pinegrow → WordPress website project. In this local Codex project, locate and read AGENTS.md, START-HERE.md, HOW-WE-WORK.md, PINEGROW-WORDPRESS-PLAYBOOK.md, PROJECT-STARTER-CHECKLIST.md, HUMAN-CHECKLIST.md, PROJECT-SPEC-TEMPLATE.md, available references, and any existing approved PROJECT-SPEC.md. Tell me if anything required is missing; do not assume every Markdown file was loaded automatically.

Help me build the project brief before implementation. Understand the business, audience, target markets and languages, priority pages, desired customer actions, visual direction, content needs, existing constraints, and handover needs. For SEO, ask proportionate kickoff questions about organic search goals, priority topics or locations, known issues, available Search Console or analytics evidence, whether AI-answer visibility matters, and who will maintain SEO controls after handover.

Keep the tool roles clear: Pinegrow is the theme-authoring source; WordPress is the CMS and runtime; Local runs the private development site. Check Pinegrow MCP, Novamira MCP, local runtime, and browser access independently when they are relevant. Do not infer a capability from a connection.

Use specialist skills when relevant: Impeccable for visual design and frontend quality; seo-audit for scoped conventional SEO work; ai-seo when AI-search visibility, citations, or agent readability are a real goal. Do not run a full SEO audit unless I request one or broad launch/readiness work calls for it.

Use PROJECT-SPEC-TEMPLATE.md to organize requirements as Confirmed, Proposed, or To be decided. Discuss material architecture choices with me, identify the source owner for each behavior, and prepare the project-specific PROJECT-SPEC.md for review. Do not begin implementation until I approve the spec. Do not export, change WordPress data, publish, or deploy without the authorization required by the project instructions.

I use a separate ChatGPT Project for big-picture reasoning and strategic decisions. Treat it as separate from this local workspace: use only the brief, approved spec, and context I provide here. After I approve a decision in ChatGPT, I will bring it into this Codex conversation and project spec.
```

## Then work in normal task-sized requests

Once the spec is approved, describe the next concrete outcome. Codex should consult the relevant project rules and skills without you repeating the full kickoff.

**A focused design request**

> Refine the mobile layout of the approved About section. Use Impeccable for visual review. Keep Pinegrow as the source, preserve unrelated edits, and report the specific screen sizes or rendered routes you verified.

**A focused SEO request**

> Review the page title, headings, internal links, and indexability for the new Services page. Use seo-audit guidance for this page only. Don’t change SEOPress or WordPress data without my authorization.

**An AI-search request**

> Review whether the approved service pages are understandable and citable in AI answers. Use ai-seo, distinguish evidence from hypotheses, and recommend scoped changes. Don’t run a full technical SEO audit.

**A broad launch review**

> Prepare a launch-readiness review of the approved site. Use the project spec and relevant design and SEO skills. Identify which checks need local WordPress, browser, Search Console, or human review, and report evidence and gaps separately. Don’t publish or deploy.

## Keep the two AI workspaces aligned

Use ChatGPT for high-level questions and Codex for local implementation. They do not automatically share context. Update the approved spec and deliberately refresh ChatGPT Project materials when needed; don’t treat an old upload as current project state.
