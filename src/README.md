# Agentic Software Delivery System

Package version: [VERSION](VERSION). Release history: [CHANGELOG.md](CHANGELOG.md). This guide describes using the package in a separate target software repository. This repository maintains the documents; do not run setup or delivery here. The package is not installed software.

> You decide what to build. Choose the approved route by risk, keep independent review where required, verify the exact candidate, and record useful lessons.

## The whole scheme

**One monorepo, four skills, ordinary CI, and a learning log. No custom delivery platform.**

Reuse an approved architecture. If there is none, intake resolves your goals and the material decisions in a small project record. Existing code describes what happens, not automatically what you intend. Architecture approval does not approve a feature.

Record each task's scope, risk tier and reason, role route, authorized files/checks, per-role model/effort choice, gate mode, budget, escalation triggers, and allowances before execution. Risk follows the hardest acceptance decision, not line count.

| Tier | Work and route |
|---|---|
| Mechanical or documentation | Non-normative prose, links, formatting, or deterministic edits with no changed behavior, dependency, verification, permission, or policy. One worker; owner acceptance is sufficient unless the contract requires independent review. |
| Bounded existing behavior or infrastructure maintenance | A small repair/refactor with settled conventional expectations, or scoped dependency/lint/workflow maintenance preserving established platform/check semantics. One worker may inspect implementation and edit authorized tests/maintenance files; a fresh independent reviewer challenges the oracle, behavior, infrastructure diff, preserved gates, scope, and exact passing candidate. |
| High risk | Scientific/numerical behavior, binary formats, custom oracles, security/permissions, substantial interfaces, unresolved semantics, or uncertain impact. Start fresh root blind A and blind B, then fresh root product C and/or the expressly authorized infrastructure author in their separate scopes, and fresh root D for the verified candidate. |

Mixed work takes the highest tier unless independently scoped contracts justify a split. Changed tests/fixtures always receive independent review; high-risk test changes use A/B. Removing assertions needs a reviewed mapping of preserved obligations or promotion. Infrastructure review cannot authorize new permission or execution authority; uncertain semantics return to intake. Coverage, discovery, fixture, and policy changes need their own authorized scope.

Authority/permission promotion stops the bounded worker until the owner explicitly approves the identified high-risk contract, route, named infrastructure/settings ownership, checks, and budget. For infrastructure-only high-risk work, the route is fresh blind A → fresh blind B → fresh root infrastructure author → fresh D. The author uses the existing [implement-task](skills/implement-task/SKILL.md) infrastructure author mode and owns only expressly named infrastructure/settings; tests remain with A/B and policy uses the separately reviewed documentation path. Product C retains its absolute restricted-file boundaries. Mixed work records separate fresh product C and infrastructure author sessions; A/B and D cover all behavior/authority, and D inherits neither author conversation. Promotion cannot silently switch modes or relax C's permissions.

Policy editing uses a documentation path: explicit owner approval of the identified patch and fresh independent policy review before activation. It cannot classify itself as mechanical. It does not require fabricated product-red evidence or scientific tests. Keep the specification and affected instructions consistent before using changed rules.

## What you do

Describe the outcome and answer consequential questions. Approve the architecture, task scope, budget, material changes, and final merge/release actions. For the first two tiers, a complete explicit instruction may itself authorize the named scope; intake records that instruction and sends a concise read-back without requiring a redundant approval. High-risk contracts and policy patches retain explicit proposal approval. Silence never approves missing decisions or a new allowance.

Routine role transitions, authorized checks, approved unchanged-scenario redistribution, and an in-scope repair within its allowance need no repeat approval. Changed behavior, interfaces, permissions, sharing, a tier downgrade, budget extension, or exhausted repair allowance returns for approval. Five distinct behavioral scenarios is an initial planning heuristic; approve a larger coherent contract once. Equivalent values for the same decision/outcome can be coverage examples; distinct rejection rules or guarantees stay separate scenarios.

The high-risk route keeps product C's restrictions on tests, fixtures, coverage/discovery, workflows, infrastructure/settings, and delivery rules. A may continue its own author session only while approved scope and blindness remain intact; product C may continue its own session for an authorized repair. The infrastructure author has no continuation exception: an authorized repair uses a fresh root infrastructure author and fresh D within the existing task-wide default single implementation repair across both authors. Initial roles stay fresh roots, and correction/final reviewers stay fresh and independent. Clearing context never restores blindness. Continuation grants no new scope, budget, rounds, or repairs.

Independent correction review may retain unaffected accepted evidence. A supplies the changed tests, approved public reproduction, checkpoint, finding/diff, and dependency mapping; fresh B reviews every affected case. Shared fixtures, parsers, observers, tolerances, schemas, or expectations expand scope. The reviewer decides whether retained evidence applies. A/B never receive implementation-bearing reports or coverage-line maps. Supplemental tests added after implementation do not recreate test-first evidence. Completed correction reviews count in the recorded window; diagnose after two nonacceptances and retain all spent rounds/budget across sessions. The default task-wide limit is one implementation repair.

## Verification and evidence

The default submission gate is full canonical local verification of the exact candidate plus every required CI platform. Keep 100% measured statement and branch coverage globally and per package on each required platform, including never-imported owned runtime and applicable subprocesses. Disclose exclusions and unsupported measurement. Complete coverage cannot prove complete behavior.

Use one concise Current state and ordinary evidence receipts: candidate/tree and test identities, canonical commands, dependency lock, relevant environment/platform/tools, integration base, exact results/coverage, and unresolved limits. Fingerprint material ignored/untracked inputs separately. Git-derived versions also need commit/tag/dirty/build inputs and the resolved artifact version; identical source trees at different commits can build differently. Head, base, environment, dependencies, checks, or version changes invalidate affected claims. Reuse evidence only while its inputs and meaning remain applicable.

Before expensive dependent checks, verify cheap prerequisites: interpreter/platform, locks, install/import health, required isolated environments, and actual reviewer launch/authentication/connectivity. A configured name is not a working reviewer. Use bounded native waits for terminal results or required action; preserve failures and diagnose before retries. Profile slow tests before restructuring. Build/environment reuse must preserve each clean-state and packaging claim; sharding must retain every report and complete coverage separately per platform/package. New helpers or shards need authorized infrastructure work and independent review.

A CI-authoritative submission route is an optional separately approved policy pilot for eligible settled lower-tier work. It is not activated by editing the package. First verify effective native target-branch protections, trusted check sources, current-base/integration requirements, and bypass settings read-only. Unknown/ineffective controls or unavailable exact artifact proof block eligibility. Exclude high risk, uncertain evidence, and edits to the pilot's own gates, coverage/discovery, build/release proof, protections, or authority.

In that approved pilot, focused public-behavior tests and inexpensive local checks precede submission; full exact-candidate CI on every required platform plus independent review precede readiness and an owner-authorized merge. A failed, cancelled, skipped, neutral, absent, or incomplete platform/shard/report must fail the aggregate. Known applicable failures still block submission until classified repair and relevant local checks establish that their cause is addressed. A PR waiting for full CI is unverified and never ready; CI failure stops readiness and spends existing allowances. Revert to full local gating if prerequisites lapse. No route delegates merge/release authority.

Model quality follows the oracle/acceptance complexity. A/B are not default choices for weaker models than C; same-model reviewers remain permitted, and using a different model is not proof of independence. Record actual model/effort identity and reasons, reuse applicable bounded calibration, and use independently reviewed public/synthetic material for blind-role calibration. Escalation follows diagnosis; it never resolves missing semantics or resets allowances. Compare complete cost per accepted task, including failed launches, checks, calibration, rework, and owner time. Missing metering is unknown, not zero; overlapping durations are not additive elapsed time.

## How the system learns and changes

Adapt [LESSONS.md](LESSONS.md), the source format guide, into target root `LESSONS/README.md`; append individual evidenced entries under that one canonical log. A/B may read only the guide and their approved public packet, never lesson entries or broad documentation/history. Coordinator/doctor verify relevant lessons and promote approved public facts through contracts. D assesses the candidate before current-task implementation lessons.

Existing `LESSONS.md`, `docs/LESSONS/`, or another layout stays in place until a separate migration is approved. Agree preservation and link handling; any entry-body/link rewrite needs an explicit append-only exception, original Git bytes, preserved IDs/dates/evidence, verified links, and one final home. Location alone does not create blindness.

Run `delivery doctor` for an evidenced process gap. It classifies product, test, workflow, and policy defects; it edits the smallest affected instructions on a documentation branch. Independent policy review and your explicit patch approval precede activation. Git records revisions. Doctor cannot repair a feature by weakening its rules.

Roll out policy changes through one coherent reviewed patch, aligned generated/installed instructions, then separately approved pilots for a documentation task, a conventional bounded repair, an infrastructure task, and high-risk public/synthetic work. Agree acceptance criteria and budget before starting; do not rerun completed owner data for a benchmark. Keep in-flight tasks on their original policy unless migration is explicitly approved; retain prior attempts and spending. Suspend an affected lighter route on a missed material obligation, exposure, false acceptance, or unresolved gap. Wider adoption requires comparison and owner approval; any ten-task follow-up is separately budgeted and does not establish defect-rate equivalence.

## Start here

| File | Use it for |
|---|---|
| [SETUP-PROMPT.md](SETUP-PROMPT.md) | Supply this prompt and the package to set up a separate target repository. |
| [DELIVERY-SYSTEM-SPEC.md](DELIVERY-SYSTEM-SPEC.md) | The authoritative delivery requirements. |
| [INTAKE-PROMPT.md](INTAKE-PROMPT.md) | Clarify architecture and tasks; approve risk and execution scope. |
| [DOCTOR-PROMPT.md](DOCTOR-PROMPT.md) | Propose evidenced policy/instruction corrections. |
| [GITHUB-SETUP.md](GITHUB-SETUP.md) | Configure ordinary CI and native protections; verify pilot prerequisites. |
| [WORKFLOW-EXAMPLES.md](WORKFLOW-EXAMPLES.md) | Compare routes, corrections, pilot rollout, and upgrades. |

The [skills directory](skills/) contains four procedures. The [project](templates/PROJECT.md), [task](templates/TASK.md), and [repository-instructions](templates/AGENTS.template.md) templates are starters. Setup adapts `AGENTS.template.md` into target `AGENTS.md` and records source/installed mappings. [REFERENCES.md](REFERENCES.md) explains sources and deliberate omissions.

Preserve the target product README and existing documentation, install one canonical delivery specification, and reconcile upgrades with local adaptations. No older draft package is needed. Role/file restrictions and append-only lessons are instructions, not access controls; native CI cannot prove agents obeyed them.

**Vocabulary:** the delivery system is the arrangement; a coding harness runs agents; a skill supplies a role procedure; CI executes checks. No custom controller, control repository, or tracing service is part of the design.

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
