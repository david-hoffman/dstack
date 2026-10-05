# dstack

dstack is a workflow for building software with coding agents. You decide what to build and approve the scope. Separate agent sessions write tests, implement the change, and review the result.

The workflow starts by agreeing on observable behavior. Tests are written and reviewed against that agreement before implementation begins, so the implementation is judged against expectations established independently of its code.

This repository packages the **Agentic Software Delivery System** as a specification, prompts, four agent skills, and templates. A skill is a reusable set of instructions for a particular job. You adapt the package to a new or existing software project using your coding tool, the project's test tools, Git, and GitHub Actions.

## How a change moves through dstack

Suppose you ask for a customer-data export in an existing application. The request moves through four stages:

1. **Agree on the behavior.** An intake conversation establishes who can export which records, which fields belong in the file, and what should happen on failure. You approve the task, including its scope, acceptance criteria, and budget.
2. **Write and review the tests.** A test author works from the approved requirements and public interfaces without inspecting the implementation. A second agent reviews those tests. For the export, they check the downloaded data and verify that a user cannot export another organization's records. New-feature tests must fail for the intended reason before implementation starts; the reviewed tests are saved in a Git commit.
3. **Implement the change.** A fresh agent builds the feature against the reviewed tests. If it finds a problem in the tests, that problem goes back for test review instead of being silently changed to fit the code.
4. **Check and review the result.** Automated checks run in GitHub Actions. A fresh reviewer examines the change and the evidence that it works. You receive a summary of the outcome and decide whether to merge.

You provide the product decisions and approvals; agents do the testing, implementation, and technical review. The [workflow examples](src/WORKFLOW-EXAMPLES.md) also cover starting a new project and upgrading an existing setup.

Useful discoveries are recorded in a [lessons log](src/LESSONS.md). When experience reveals a gap in the instructions, the [doctor workflow](src/DOCTOR-PROMPT.md) proposes a focused revision for your review.

## Use it in your project

1. Read the [package guide](src/README.md) for the full process and your role in it.
2. Open your software project's repository in your coding tool. Supply the complete [`src/` package](src/) and the [setup prompt](src/SETUP-PROMPT.md). Setup inspects the project, reuses an approved architecture or helps you define one, and presents a plan for adapting the workflow to your repository.
3. Once setup is complete, use the [intake prompt](src/INTAKE-PROMPT.md) to describe your first feature or bug fix.

## Reference

| Document | What it covers |
|---|---|
| [Specification](src/DELIVERY-SYSTEM-SPEC.md) | The complete workflow, responsibilities, approvals, and verification requirements. |
| [Agent skills](src/skills/) | Instructions for intake, test writing, implementation, and review. |
| [Templates](src/templates/) | Starting points for the project record, task record, and repository instructions. |
| [GitHub setup](src/GITHUB-SETUP.md) | Automated checks and branch protection configuration. |
| [References](src/REFERENCES.md) | Sources, adopted ideas, and design decisions. |

The package has one [version](src/VERSION) and [changelog](src/CHANGELOG.md). To contribute to these documents, see [AGENTS.md](AGENTS.md); for releases, see the [versioning policy](src/README.md#package-versioning) and [maintainer checklist](.agents/release-package/SKILL.md).
