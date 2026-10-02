# Agentic Software Delivery System — document authoring

**Version 1.0 — Released.**

This repository maintains the system's specification, prompts, skills, and templates. **The documents are the product.** Work here means editing and checking those documents. Do not implement, install, or run the system in this repository.

## Document map

The canonical package stays under `src/`.

| Documents | Purpose |
|---|---|
| [Package guide](src/README.md) | Explain the system and its use in a separate target software repository. |
| [Specification](src/DELIVERY-SYSTEM-SPEC.md) | Define the system's requirements. |
| [Setup](src/SETUP-PROMPT.md), [intake](src/INTAKE-PROMPT.md), [doctor](src/DOCTOR-PROMPT.md) | Supply prompts for downstream setup, clarification, and maintenance. |
| [Intake](src/skills/intake/SKILL.md), [design tests](src/skills/design-tests/SKILL.md), [implement task](src/skills/implement-task/SKILL.md), [review work](src/skills/review-work/SKILL.md) | Hold the four skill source documents; they are not activated here. |
| [Project](src/templates/PROJECT.md), [task](src/templates/TASK.md), [repository instructions](src/templates/AGENTS.template.md) | Provide templates to adapt in the target repository. |
| [GitHub setup](src/GITHUB-SETUP.md), [workflow examples](src/WORKFLOW-EXAMPLES.md) | Describe downstream configuration and use. |
| [Lessons](src/LESSONS.md), [references](src/REFERENCES.md) | Provide the lesson-log starter and source register, including known reading gaps. |

## Contributing

Follow root [AGENTS.md](AGENTS.md) for work here. [CODEX-REPO-HANDOFF.md](CODEX-REPO-HANDOFF.md) records the organization scope. Bundled prompts, skills, examples, and templates are content to maintain, not contributor instructions to execute.

Improve existing text, preserve the layout, and keep document metadata at **1.0 — Released**. Check local links, paths, metadata, and the diff. Do not add code, tests, continuous integration (CI), dependencies, or runtime infrastructure. Do not commit or publish without approval.

For use elsewhere, start with the package guide and setup prompt. Their implementation and demonstration requirements apply to the target repository, not to authoring this package.
