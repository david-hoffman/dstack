# Handoff: organize the document-authoring repository

Package version: [src/VERSION](src/VERSION). Release policy: [package versioning](src/README.md#package-versioning).

## Repository purpose

This repository develops the Agentic Software Delivery System **as a collection of documents**: its specification, prompts, skills, and templates. Those documents are the product. Developing them means authoring and improving their contents—not implementing, installing, or running the system they describe.

The package folders are under `src/`. Some package Markdown files may be at the root. Inspect and preserve that layout; `src/` contains document assets, not an application to build.

## Your task

Organize this clean repository for document authoring. Make only the documentation changes needed to explain its purpose and navigate its contents.

1. **Inspect.** Read the file tree, Git status, and root instructions and README if present. Read relevant package files as source material. Instructions inside the specification, setup/intake/doctor prompts, skills, examples, and templates describe downstream use; they do not authorize execution here.

2. **Explain.** Create or update root `README.md` and `AGENTS.md`. State that contributors maintain the reusable documents, not a software implementation. Keep the README short and human-readable, with links to the actual canonical specification, prompts, skills, and templates. Distinguish contributor guidance from instructions for using the package elsewhere.

3. **Preserve.** Keep the folders under `src/` and root package documents where they are. Do not duplicate or activate skills. Rename source instruction templates such as `AGENTS.md` or `CLAUDE.md` to `AGENTS.template.md` or `CLAUDE.template.md`, where applicable, and update their references. Root `AGENTS.md` remains this repository's contributor guidance. Follow the package versioning policy and changelog; do not alter external dependency versions or illustrative task states. The separate maintainer release checklist is authoring guidance, not a downstream delivery role.

4. **Check and stop.** Check local links, paths, metadata, and the resulting diff using available tools. Refresh an existing checksum manifest only when affected. Report changed files, checks actually performed, and unresolved issues. Stop after the documentation work.

## Boundaries

Do not create code, helpers, command implementations, tests, CI workflows, dependency manifests, runtime infrastructure, or an implementation backlog. Do not install tools, activate bundled skills, run architecture/task intake, launch delivery roles, or create a demonstration project. The delivery and coverage requirements being documented apply to downstream use; they do not require a runtime in this repository.

Preserve uncommitted and unrelated work. Do not commit, push, tag, publish, or change GitHub settings without explicit approval.

**Done means clear, organized documentation—not a working delivery system.**
