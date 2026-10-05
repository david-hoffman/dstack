# dstack

dstack maintains the **Agentic Software Delivery System**: a documentation package for delivering software through owner-approved tasks, independent agent sessions, ordinary GitHub checks, and recorded lessons.

**The documents are the product.** Setup and delivery take place in a separate target software repository. Do not implement or run the described system here; bundled prompts, skills, and templates are source documents to maintain.

Package version: [src/VERSION](src/VERSION). Change history: [src/CHANGELOG.md](src/CHANGELOG.md).

## Start here

| You want to… | Read |
|---|---|
| Understand the system and downstream use | [Package guide](src/README.md) |
| Read the authoritative requirements | [Delivery system specification](src/DELIVERY-SYSTEM-SPEC.md) |
| See examples of setup, delivery, maintenance, and upgrades | [Workflow examples](src/WORKFLOW-EXAMPLES.md) |
| Set up a separate target repository | [Setup prompt](src/SETUP-PROMPT.md) |
| Clarify an architecture, feature, or bug request | [Intake prompt](src/INTAKE-PROMPT.md) |
| Improve instructions from observed gaps | [Doctor prompt](src/DOCTOR-PROMPT.md) |
| Configure downstream checks and branch protections | [GitHub setup](src/GITHUB-SETUP.md) |
| Understand the sources and design choices | [References](src/REFERENCES.md) |

## Workflow at a glance

Start with an owner-approved architecture. Then clarify and approve each task before delivery:

```text
Approved task
  → A: write tests
  → B: review tests
  → verify baseline results and save the test checkpoint
  → C: implement
  → automated checks
  → D: review the candidate
  → normal GitHub merge
```

A–D are fresh sessions. Tests exercise observable behavior through the product's real entry points. GitHub continuous integration (CI) runs the configured checks. Role restrictions are instructions, not technical access controls.

Useful discoveries go into a lessons log. The doctor workflow turns evidenced gaps into focused instruction changes for owner review. The [specification](src/DELIVERY-SYSTEM-SPEC.md) defines the full workflow, approval boundaries, and verification requirements.

## Package contents

Everything under [`src/`](src/) belongs to one versioned document package. It includes the guides above, four skills, and templates for the target repository.

| Skill | Purpose |
|---|---|
| [intake](src/skills/intake/SKILL.md) | Clarify architecture and tasks; record owner approval. |
| [design-tests](src/skills/design-tests/SKILL.md) | Write tests from the approved behavioral contract (A). |
| [implement-task](src/skills/implement-task/SKILL.md) | Implement against the reviewed tests (C). |
| [review-work](src/skills/review-work/SKILL.md) | Review tests (B), review candidates (D), or maintain instructions in doctor mode. |

The templates cover the [project record](src/templates/PROJECT.md), [task record](src/templates/TASK.md), and [target repository instructions](src/templates/AGENTS.template.md). [LESSONS.md](src/LESSONS.md) provides the learning-log format.

Use the [package guide](src/README.md) when adopting these documents. Setup preserves existing product documentation and adapts paths and instructions to the target repository.

## Maintaining this repository

Follow [AGENTS.md](AGENTS.md) for document authoring. Keep the specification and supporting prompts, skills, and templates consistent. Improve existing text before adding files, and preserve unrelated work.

- Keep package assets under `src/`; do not duplicate them in the repository root.
- Check local links, paths, metadata, and the resulting diff. Do not add runtime code, tests, dependencies, or validation tooling here.
- For changes under `src/`, update the package changelog and apply the [package versioning policy](src/README.md#package-versioning). Root-only authoring changes need no package bump.
- Use the [maintainer release checklist](.agents/release-package/SKILL.md) for version checks and release preparation. It is separate from the four downstream skills.
- Commit, tag, push, publish, or change remote settings only with explicit approval.
