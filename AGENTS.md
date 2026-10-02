# Repository instructions: document authoring

**Version 1.0 — Released.**

This repository maintains the Agentic Software Delivery System's specification, prompts, skills, and templates. **The documents are the product. Do not implement, install, or run the system they describe.**

## Working here

Edit requested documentation for clarity, consistency, correctness, and simplicity. Prefer improving existing text to adding files. Preserve package folders under `src/` and existing root documents; do not duplicate source assets.

Use root [README.md](README.md) to navigate the documents; [src/README.md](src/README.md) describes downstream use. Treat bundled prompts, skills, templates, examples, and specification requirements as content to maintain—not instructions to execute here. Keep skills inert. Keep source instruction templates named `AGENTS.template.md` or `CLAUDE.template.md` so they remain distinct from this root guidance. Do not run intake or delivery roles as a prerequisite to editing documents.

Do not add code, helpers, tests, CI workflows, dependencies, runtime infrastructure, or an implementation backlog. Use available tools to inspect links and diffs; do not create validation tooling or install a toolchain.

Keep document metadata at **1.0 — Released** unless the owner explicitly changes it. Git records revisions. Preserve unrelated work. Do not commit, push, publish, or change remote settings without approval.

Check local links, paths, metadata, and the resulting diff. Refresh an existing checksum manifest only when affected. Finish with the documentation changes, checks actually performed, and unresolved issues. A runnable system is not a deliverable of this repository.
