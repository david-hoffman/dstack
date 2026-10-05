# Repository instructions: document authoring

Package version: [src/VERSION](src/VERSION). Release policy: [package versioning](src/README.md#package-versioning).

This repository maintains the Agentic Software Delivery System's specification, prompts, skills, and templates. **The documents are the product. Do not implement, install, or run the system they describe.**

## Working here

Edit requested documentation for clarity, consistency, correctness, and simplicity. Prefer improving existing text to adding files. Preserve package folders under `src/` and existing root documents; do not duplicate source assets.

Use root [README.md](README.md) to navigate the documents; [src/README.md](src/README.md) describes downstream use. Treat bundled prompts, skills, templates, examples, and specification requirements as content to maintain—not instructions to execute here. Keep bundled delivery skills inert. Keep source instruction templates named `AGENTS.template.md` or `CLAUDE.template.md` so they remain distinct from this root guidance. Do not run intake or delivery roles as a prerequisite to editing documents.

Do not add code, helpers, tests, CI workflows, dependencies, runtime infrastructure, or an implementation backlog. Use available tools to inspect links and diffs; do not create validation tooling or install a toolchain.

Use one package version from `src/VERSION`; do not add independent document/skill versions or permanent "Released" banners. For changes under `src/`, update `src/CHANGELOG.md` under `Unreleased` and classify the complete change against the last stable release. Apply the highest required bump; a new obligation or changed authority is breaking even when called a clarification. Follow the development/release transitions in the package policy. Root-only authoring changes need no package bump.

For version checks or release preparation, read the [maintainer release checklist](.agents/skills/release-package/SKILL.md) as authoring guidance. It is a repository maintainer skill, separate from the four inert delivery skills under `src/`; do not install or activate bundled delivery skills. Ordinary content edits need only the version/changelog checks, not a publication workflow.

Preserve unrelated work. Do not commit, tag, push, publish, or change remote settings without explicit approval for those actions. Preparation is not publication approval. Never replace a published tag or assume a failed remote check means a version is unused. Report missing evidence and stop the affected release step; continue safe local authoring. The release checklist requires GitHub release immutability before publication, but writing these instructions does not enable it.

Check local links, paths, metadata, and the resulting diff. Refresh an existing checksum manifest only when affected. Finish with the documentation changes, checks actually performed, and unresolved issues. A runnable system is not a deliverable of this repository.
