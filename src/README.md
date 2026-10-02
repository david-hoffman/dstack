# Agentic Software Delivery System

Package version: [VERSION](VERSION). Release history: [CHANGELOG.md](CHANGELOG.md). This guide describes using the package in a separate target software repository. This repository maintains the documents; do not run setup here. The package is not installed software.

> You decide what to build. Separate agents write tests, implement, and review. GitHub runs the checks. Lessons improve the next task.

## The whole scheme

**One monorepo, four skills, ordinary CI, and a learning log. No custom delivery platform.**

First, reuse the approved architecture. If there isn't one, the intake conversation helps create it. For an existing application, it documents what is there and resolves what is intended. For an empty repository, it starts with your goals. You approve the resulting project record.

For each change:

```text
Clarify the request → you approve the task
    → A writes tests → B reviews tests
    → tests fail for the intended reason; save the test checkpoint
    → C implements → automated checks → D reviews
    → normal GitHub merge
```

A–D are fresh sessions, not four names in the same conversation. They may use the same model. The intake conversation is additional. Tests focus on actual user behavior: browser journeys, commands, or public APIs. Smaller tests fill genuine gaps, rather than duplicating everything.

## What you do

Describe the outcome. Answer the consequential questions. Approve the architecture, task, budget, and any material change. Review the final summary and merge normally. You are not expected to write code or pretend to perform expert code review.

The agents are told not to change reviewed tests or workflows to make their work pass. **That restriction is a prompt, not a technical barrier.** GitHub CI still runs the configured tests, but an agent could change those rules. This is an intentional simplicity tradeoff, not a guarantee of bug-free software.

## How the system learns

Agents append useful surprises and gotchas to [LESSONS.md](LESSONS.md), with evidence. They do not dump conversations there.

Run `delivery doctor` when experience reveals a gap. It checks the evidence and edits the existing specification/instructions on a documentation branch. You review the diff before it is committed and merged. Git records revisions. It does not repair a failing feature by rewriting the rules.

## Start here

| File | Use it for |
|---|---|
| [SETUP-PROMPT.md](SETUP-PROMPT.md) | Give a coding tool this prompt and the package to set up the target repository. |
| [DELIVERY-SYSTEM-SPEC.md](DELIVERY-SYSTEM-SPEC.md) | The single authoritative implementation specification. |
| [INTAKE-PROMPT.md](INTAKE-PROMPT.md) | Clarify an architecture, feature, or bug request. |
| [DOCTOR-PROMPT.md](DOCTOR-PROMPT.md) | Improve the specification from observed gaps, even before the command exists. |
| [GITHUB-SETUP.md](GITHUB-SETUP.md) | Configure ordinary CI and branch protections. |
| [WORKFLOW-EXAMPLES.md](WORKFLOW-EXAMPLES.md) | See an empty-project start, a feature, and a doctor update. |

The [skills directory](skills/) contains four procedures. The [project](templates/PROJECT.md), [task](templates/TASK.md), and [repository-instructions](templates/AGENTS.template.md) templates are starters for the target repository. Setup adapts `AGENTS.template.md` into that repository's `AGENTS.md`. [REFERENCES.md](REFERENCES.md) explains sources and deliberate omissions.

Do not overwrite an existing product README by copying this bundle into its root. Setup should preserve existing docs, install one canonical delivery spec, and update links. No older draft package is needed.

**Vocabulary:** the delivery system is this whole arrangement. A coding harness runs agents. A skill tells a role how to work. Continuous integration (CI) executes checks. No custom controller, external control repository, or tracing tool is part of this design.

## Package versioning

This section governs upstream package releases. The [specification](DELIVERY-SYSTEM-SPEC.md) governs downstream use. All files under `src/` form one package with one [version](VERSION); skills, prompts, and templates have no independent release numbers. Repository authoring guidance and the maintainer release skill outside `src/` are not downstream components. Git identifies each revision; a release identifies a reviewed package snapshot.

### Compatibility contract

Use [Semantic Versioning](https://semver.org/spec/v2.0.0.html): `MAJOR.MINOR.PATCH`. The public contract includes required workflow, role/input boundaries, permissions, approvals, evidence and template fields, skill/mode names, documented commands, and integration paths. Compatibility concerns these documented promises, not identical model outputs.

| Change | Required bump | Example |
|---|---|---|
| Correction preserving obligations and supported use | Patch | Repair a link, typo, or example without changing the rule. |
| Compatible optional capability or announced deprecation | Minor | Add an optional task field; retain a deprecated skill name until a later major release. |
| Changed obligation, authority, accepted evidence, or unsupported old integration | Major | Add a mandatory approval/field, change a coverage requirement or role permission, or remove a referenced path. |

Classify the full difference from the last stable release and use its highest required bump. Reset lower components when increasing a higher one. A wording change that changes behavior is not merely editorial. An uncertain compatibility impact must be resolved before release preparation is called ready. Root-only authoring changes need no package release.

### Version and release identity

`VERSION` contains exactly one version and a trailing newline: no `v` prefix, date, status, or commit ID. Working package edits use the next intended version with `-dev`; raise that intended version if later edits require a larger bump. The first package edit after a release starts the next development version and an `Unreleased` changelog entry. Do not bump on every edit. A prepared stable candidate contains `X.Y.Z`; an optional preview contains `X.Y.Z-rc.N`, with positive, increasing `N`. Never publish a `-dev` snapshot or use build metadata to disguise changed release contents.

A version string alone does not prove publication. A release consists of an annotated `v<version>` tag on an exact commit, a matching dated changelog entry, and a published GitHub Release. Uncommitted or untagged candidates remain unpublished even when `VERSION` has no suffix. Record the full source commit externally in the release record and downstream provenance; never put a commit's own ID inside the bytes it identifies. A remote tag must resolve to that exact commit, not merely share its name.

Published versions and their package contents are permanent. Never move/delete/reuse their tags, alter their attached assets, or rewrite their historical changelog entries. Correct a defective release in a new version and identify the affected release in the new notes. A partial publication is resumed only after checking existing objects match the approved candidate; a collision or unknown outcome is not permission to overwrite. Support the latest stable release; keep older snapshots available without a backport promise.

Require GitHub release immutability before publication. It protects the published tag and attached assets; GitHub still permits editing release notes, so the committed changelog is the canonical history. This setting does not check version classification or instruction quality. See [GitHub's protection limits](https://docs.github.com/en/code-security/concepts/supply-chain-security/immutable-releases) and [owner configuration steps](https://docs.github.com/en/code-security/how-tos/secure-your-supply-chain/establish-provenance-and-integrity/prevent-release-changes). Do not change repository settings without owner authorization or claim protection without checking it.

### Release checklist

1. Identify the source repository, last stable release/commit, intended version, and complete package diff, including new/deleted files. Verify remote tags and releases; unavailable access is an unresolved check, not an empty release history. For a first release, confirm no prior release exists and document the bootstrap baseline. Until the first stable release, compare against that recorded bootstrap baseline; intervening previews do not reset it.
2. Review compatibility, supporting-document agreement, local links/anchors, installed paths, and metadata. Compare the entire `src/` inventory and contents against the intended source revision; matching headers do not prove a coherent package. Use available read-only Git/file tools; do not install a toolchain, create validation tooling, or run delivery roles here.
3. Prepare `VERSION` and one changelog entry with version, intended release date, changes, compatibility rationale, and explicit migration steps (or "None" with a reason). Keep `Unreleased` for subsequent work. If the actual publication date changes, update it before final approval. A preview's notes do not establish a stable release; review all changes since the previous stable release again before promotion.
4. Present the exact diff and check results for approval to commit. After an authorized commit, verify a clean working tree and present its full ID, version, baseline, migration notes, remote/immutability evidence, and planned publication actions. Obtain explicit authorization for tagging/pushing/publishing that candidate; do not repeat authorization already supplied for the same candidate and actions. Any candidate change requires renewed checks and approval. Never include unrelated work or stash/reset it to manufacture a clean tree.
5. Recheck remote availability, tag/version collisions, and immutability immediately before authorized publication. Create the annotated tag at the approved commit and publish a matching GitHub Release; prepare any assets before publishing. Do not create the tag implicitly from a moving branch. Verify the remote tag's resolved commit, release version, preview/stable status, and immutability afterward. An unexpected result stops further mutations and must be reported precisely.

Report preparation, verification, approval, and publication separately. A check has an observed result or an unresolved reason; unchecked is not passed. A local tag or pushed commit alone is not a published release. These checks are procedural except for protections actually enabled on GitHub.

### Downstream provenance and upgrades

Setup records the upstream repository, package version, full upstream commit, installed path mapping, omissions, and adaptations in the project record. Carry this policy, `VERSION`, and `CHANGELOG.md` as package reference material at documented paths. Verify that original inputs come from one source commit before adapting them; record adaptations separately. Do not mix files from different releases and call the result an unchanged release. Development or unverified sources require explicit owner acceptance and must retain that label.

Local doctor changes retain their upstream base identity and are identified by downstream Git history and approval, not a fabricated upstream patch version. For an upgrade, compare the recorded upstream base, the target release, and local changes; reconcile all adopted components and migration instructions before updating the base record. Preserve local work and in-flight tasks' approved policy revision. Unknown provenance blocks a verified-upgrade claim until reconstructed or explicitly accepted as an unverified migration. Historical project/task records retain their original meaning; a new required field needs migration guidance, not silent rewriting of old approvals.
