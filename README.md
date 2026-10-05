# dstack

dstack is a workflow for building software with coding agents, from architecture intake in an empty repository to tested changes in an existing application. You decide what to build and authorize the scope. The task's risk determines which agent sessions do the work and review the result.

The workflow starts by agreeing on the architecture and observable behavior. High-risk work uses independent test writing and review before implementation; settled repairs use a worker and fresh reviewer, while non-normative documentation can use one worker. Useful discoveries feed back into the instructions through an independently reviewed maintenance process that you approve.

This repository packages the **Agentic Software Delivery System** as a specification, prompts, four agent skills, and templates. A skill is a reusable procedure for a particular job. These documents are the product; they describe a workflow to adapt in a separate software repository, rather than installed software or an already available `delivery` command.

The operating model is small: one monorepo, one active task, an existing coding tool, independent sessions where required, Git, the project's test tools, and ordinary GitHub Actions. Product code, tests, and delivery instructions stay together. No custom controller, separate control repository, GitHub App, or evidence service is required.

## Use it in your project

1. Read the [package guide](src/README.md) for the process, your role, and package policy.
2. Open your software project's repository in your coding tool. Supply the complete [`src/` package](src/) from one upstream commit and the [setup prompt](src/SETUP-PROMPT.md). Setup inspects the project, routes architecture decisions, and presents an adaptation plan for your approval.
3. After setup, use the [intake prompt](src/INTAKE-PROMPT.md) to describe a feature or bug fix. Record its authorized scope, risk tier, route, checks, and budget, then follow the corresponding delivery process below.

You provide the outcome, consequential decisions, architecture approval, task authorization, and budget. Agents handle testing, implementation, and technical review. You review the final summary and decide whether to merge; you are not expected to write code or perform expert code review.

## Setup and architecture intake

Setup starts with read-only discovery of the target repository's instructions, manifests, interfaces, tests, and documentation. It preserves useful product documentation and sound tooling. It does not run repository setup scripts merely to discover the project.

**Architecture intake is an explicit part of setup.** The same [intake skill](src/skills/intake/SKILL.md) handles architecture and individual tasks, using the appropriate mode:

| Starting point | What happens |
|---|---|
| Empty repository with no architecture | Interview you about the first useful outcome and constraints, then propose a small architecture and suitable stack for approval. |
| Existing application without usable architecture | Document the observed structure, clarify what is intended, and resolve material gaps. Existing code is evidence, not automatic agreement about desired behavior. |
| Usable, approved architecture | Reuse it and link its canonical documents instead of repeating the interview or duplicating the design. |
| Architecture that is unapproved, contradictory, or affected by the task | Reconcile the affected decisions and obtain approval for the resulting record. |

The result is a short `docs/PROJECT.md`, based on the [project template](src/templates/PROJECT.md). It records purpose and non-goals, constraints, stack, component responsibilities, public interfaces, verification commands, operation, approval, and the next useful task. It favors few components, usually one deployable component; diagrams are optional. **Architecture approval is separate from approval to implement a feature.**

Once you approve the setup plan, adaptation installs one canonical copy of each skill in the coding tool's supported location, reconciles repository instructions into `AGENTS.md`, and records actual launch and check commands. It selects or preserves suitable formatting, linting, type checks, testing, coverage, dependency locking, and security checks. Approved setup may create initial CI and minimal test infrastructure, including a callable scaffold for the first tests, while leaving product features to task delivery.

Repeating setup completes approved gaps without replacing working conventions. Changing the upstream package follows the upgrade process below. Missing architecture blocks A's test-writing session and product implementation, while read-only discovery and approved setup can still proceed. An existing baseline that fails checks or lacks required coverage is a reported gap to address.

Setup is called usable only after actual demonstrations: architecture routing and authorization, a high-risk delivery through fresh roles and meaningful failing tests/checkpoint to passing exact-candidate checks and review, applicable approved lower-tier pilots, a failing PR blocked by native CI where available, a passing PR, a recorded lesson, and an independently reviewed doctor diff. Missing evidence or unavailable GitHub protections are reported plainly. The [workflow examples](src/WORKFLOW-EXAMPLES.md) illustrate these paths; they are not records of executed demonstrations.

## Task intake and authorization

Task intake turns a request into one authorized behavior contract using the [task template](src/templates/TASK.md). It resolves material questions about scope, data access, interfaces, errors, cost, and acceptance, usually asking no more than three high-value questions per turn. It uses concrete examples, recommends simple defaults for your agreement, and reuses settled answers.

The task record contains:

- Observable requirements with stable IDs, purpose, and non-goals.
- Public interfaces, inputs, outputs, permissions, and success, error, and boundary examples.
- Risk tier and reason, role route, named ownership and edit scope, checks, model/effort choices, and local/CI gate mode.
- Unresolved decisions, escalation triggers, preparation/execution budget, review windows, and remaining round/repair allowances.
- The actual authorization reference, one concise Current state, and evidence links.

A behavioral scenario is a distinct approved decision and observable outcome. Five scenarios is an initial planning heuristic, not a test-count or coverage cap; a larger coherent contract can be approved once. Equivalent values for an accepted decision can be coverage examples. New rejection rules, interpretations, guarantees, or boundary outcomes are separate scenarios rather than extra data for an old one.

For bugs, intake separates observed behavior, expected behavior, reproduction evidence, and hypotheses about the cause. An uncertain report can receive a bounded investigation whose deliverable is a report; that approval does not authorize a speculative fix. Intake drafts examples rather than executable tests.

Each task pins an existing committed, owner-approved **local delivery-policy revision** and its adopted paths before authorization. This keeps the task's rules stable through completion, even if the package or local instructions change.

A complete explicit instruction can authorize a mechanical or bounded task under inherited constraints; intake records that instruction and sends a concise read-back without requiring a redundant second approval. High-risk contracts and delivery-policy patches need explicit approval of the identified proposal. Routine authorized transitions, checks, in-scope repairs, and approved redistribution of unchanged scenarios need no repeat permission. Changed behavior, interfaces, permissions, data sharing, tier downgrade, budget extension, or exhausted repair allowance returns to you and renews affected tests/reviews. Silence never authorizes missing decisions.

For example, a customer-data export request needs agreement on who can export which records, which fields belong in the file, and what happens on failure. Its permission boundary makes it high risk; those decisions become the contract the independent test author receives.

## Delivery routes by task risk

Choose the route before choosing sessions or models. Risk follows the hardest acceptance decision, not the number of changed lines.

| Tier | Suitable work | Delivery route |
|---|---|---|
| **Mechanical or documentation** | Non-normative prose, links, formatting, or deterministic edits that change no behavior, dependency, verification rule, permission, or policy. | One worker checks the diff and relevant deterministic results. Owner acceptance suffices unless the task requires independent review. |
| **Bounded behavior or infrastructure maintenance** | Small conventional repairs/refactors or scoped dependency/lint/workflow maintenance with settled expectations and preserved platform/check semantics. | One worker can inspect implementation and edit explicitly authorized product, tests, fixtures, and maintenance files. A fresh independent reviewer checks expectations, behavior, infrastructure, preserved gates, scope, and the exact passing candidate. |
| **High risk** | Scientific/numerical behavior, binary formats, custom test oracles, security/permissions, substantial interfaces, unresolved semantics, or uncertain impact. | Fresh blind A and B, a fresh product C and/or separately authorized infrastructure author, then fresh D. |

Uncertainty promotes a task; mixed work takes the highest tier unless separately scoped contracts justify a split. Changed tests/fixtures and dependency/workflow/gate maintenance always receive independent review. Removed assertions require a reviewed mapping of retained obligations. A bounded worker stops on promotion until you approve the identified high-risk contract, route, ownership, checks, and budget; changing its label or mode cannot expand its authority.

**Delivery-policy documentation has its own path:** a documentation worker prepares the patch, a fresh independent policy reviewer checks rule interactions and supporting-document agreement, and you explicitly approve it before activation. It cannot classify itself as mechanical or fabricate product-red evidence. The four [skills](src/skills/) support all routes: `intake`, `design-tests`, `implement-task`, and `review-work`.

### High-risk tests, implementation, and review

Initial high-risk roles start in new root sessions in the coding tool. Do not simulate them in one chat, substitute a nested reviewer for a fresh root, or fork an implementation author's conversation for review. Required correction verdicts remain fresh and independent. Intake is a separate conversation when needed.

| Role | Responsibility | Skill |
|---|---|---|
| **A: test author** | Write behavior-focused tests from approved requirements and public interfaces, without inspecting implementation, its history, or lesson entries. | [design-tests](src/skills/design-tests/SKILL.md) |
| **B: test reviewer** | Review requirement coverage, independent expectations, errors, boundaries, and whether tests detect plausible wrong behavior. Return corrections to A. | [review-work, tests mode](src/skills/review-work/SKILL.md#tests--b-high-risk-blind) |
| **C: implementer** | Make the smallest approved product change against the reviewed tests. Preserve tests, fixtures, snapshots, workflows, coverage settings, and delivery instructions. | [implement-task](src/skills/implement-task/SKILL.md) |
| **Infrastructure author** | Apply only the expressly approved infrastructure/settings change; tests, fixtures, product code, and delivery policy keep their separate owners. | [implement-task, infrastructure author mode](src/skills/implement-task/SKILL.md) |
| **D: final reviewer** | Inspect the exact candidate, real behavior, security, interfaces, check evidence, restricted-file changes, and opportunities to simplify. | [review-work, candidate mode](src/skills/review-work/SKILL.md#candidate--d-high-risk) |

A/B receive a narrow packet of approved behavior, public contracts, fixtures, test conventions, and permitted policy text from the pinned revision. They do not receive the intake transcript, private implementation ideas, implementation conversations, or lesson entries. B also receives A's tests. The coordinator sanitizes diagnostics into source-free public reproductions; coverage-line maps and implementation-bearing reports are not blind inputs. Clearing context or rerunning clean diagnostics cannot restore an exposed role's blindness.

Infrastructure-only high-risk work uses A → B → infrastructure author → D. Mixed product/infrastructure work names separate fresh C and infrastructure-author sessions, and A/B/D cover the complete behavior and authority contract. This gives infrastructure an explicit owner without relaxing product C's file prohibitions. Bounded work uses `implement-task` worker mode and `review-work` bounded mode; policy review and doctor are separate `review-work` modes.

The delivery sequence preserves independent expectations:

1. **Review tests before implementation.** After B accepts them, run feature or bug tests against the approved baseline. They must fail for the intended behavioral reason; broken imports, dependencies, or services do not count. A new-project scaffold demonstrates missing behavior, while a behavior-preserving refactor needs regression evidence rather than an invented failure.
2. **Save the test checkpoint.** Commit the reviewed tests and record that commit in the task before starting C or the infrastructure author. The checkpoint is frozen by convention.
3. **Implement and verify locally.** The approved implementation author makes the change and runs cheap prerequisites before expensive checks. Full canonical local verification must pass on the exact candidate before opening/updating its PR. Bad or incomplete tests return to blind A and fresh blind B; implementation authors do not repair them to fit the code.
4. **Complete CI and independent review.** Every required CI platform must pass, and fresh D assesses actual results and the exact candidate before readiness. D cannot fix a candidate and approve that same repair. Further code or material evidence-input changes need renewed checks/review.
5. **Present the result for merge.** You decide whether to merge through the normal GitHub process. Production deployment remains a separate explicit owner action, with the project's smoke check and recovery instructions.

After a test checkpoint has been accepted, a correction may retain unaffected accepted evidence only if B agrees it still applies. Shared fixtures, parsers, observers, tolerances, schemas, or expectations widen review to every dependent case. New public meaning requires intake approval; changed meaning or inadequate dependency mapping requires a fresh complete review of affected behavior. Tests added after implementation remain supplemental rather than original test-first evidence.

Where explicitly approved in the installed policy governing the task, A may continue its own author session while still blind, and C may continue its own implementation session for a repair, within authorized scope and allowances. B/D verdicts remain fresh. Infrastructure repairs require a fresh infrastructure author and D. Session continuation, narrower corrections, or model changes grant no new scope or repair allowance.

## Testing and GitHub checks

Tests primarily exercise the real product entry point: browser journeys through the actual application and backend, CLI execution with outputs and exit codes, or public service/library APIs. Expected results come from the contract, not the implementation being tested. Integration and unit tests fill genuine gaps such as difficult error injection or combinatorial logic; there is no unit-test quota or fixed test-type percentage.

Tests use synthetic data, isolated state, readiness checks, and bounded waits. Uncontrollable external services can be stubbed at their boundary, with untested behavior documented and an approved provider sandbox check when needed. Tests should not mock away the owned path whose behavior is the requirement. A pass on retry does not settle a flaky failure.

The specified coverage requirement is **100% measured statement and branch coverage** across instrumentable owned runtime code, globally and per package on every required platform, from the combined suite. Measurement includes relevant subprocesses, servers, browser code, and never-imported files, using exact metrics rather than rounded displays. Only narrow documented exclusions for vendor, generated, or non-executable files apply. Missing or unsupported measurement is a reported gap. Complete measured coverage does not prove complete behavior.

Ordinary GitHub Actions runs canonical checks with locked dependencies: formatting, linting, types where applicable, build, tests, and coverage. It retains useful failure reports and uses native failures for empty test discovery, unexpected skipped/focused tests, and missing required reports where supported. A single required job, preferably `verify`, is usually enough; genuinely necessary additional targets must also run. Required validation must not disappear through path filters, conditional skips, or error suppression.

The [GitHub setup guide](src/GITHUB-SETUP.md) describes native PR and branch protections, required CI, current branches, and restrictions on force pushes, deletion, and bypass where supported. Setup proposes the settings changes, applies them only with permission, and verifies that a failing temporary PR is blocked. If access or account capabilities are missing, it gives exact remaining owner actions. CI uses necessary token permissions and keeps production secrets out of test runs.

**Full local verification before PR submission is the default.** An optional CI-authoritative route requires a separately approved policy pilot for eligible settled mechanical/bounded work. It passes focused public-behavior tests and inexpensive local checks before submission, then full canonical CI on every required platform and independent review before readiness. Eligibility requires verified native protection, trusted check sources, current-base/integration and bypass controls, complete aggregate failure semantics, and exact candidate/artifact/version proof. High-risk work, diagnosis, uncertain evidence, and changes to the pilot's own gates, coverage/discovery, protections, build/release proof, or authority are excluded. Unknown controls block eligibility; waiting for CI means unverified, not ready. Known failures still block submission, and lapsed prerequisites restore default local gating. Editing the package does not activate the pilot or delegate merge authority.

**Role independence, restricted-file rules, and append-only lessons are procedural safeguards.** Agents retain technical access; GitHub executes the submitted repository configuration and does not prove compliance with those instructions. The workflow does not claim tamper-proof enforcement or guaranteed freedom from bugs.

## Budgets and evidence

Use the authorized tier's route, with at most one implementation repair task-wide by default, shared across workers and implementation authors. Preparation, calibration, failed launches, escalation, and rework count toward the approved budget. Each completed correction review consumes a round in its recorded window; after two B nonacceptances, stop and diagnose before further approved work. New sessions, narrower reviews, renamed tasks, model changes, and migrations do not reset attempts, spending, or allowances. Work stops and reports at the limit; native controls are used where available. A prompt budget is not a hard spending guarantee.

Keep one concise Current state with the decision, exact revision, classified findings, evidence links, next role, and remaining allowances. Evidence receipts identify candidate/tree and tests/checkpoint, canonical commands, dependency lock, environment/tools/platform, integration base, exact results/coverage, and unresolved limits. Fingerprint material ignored/untracked inputs separately and keep final candidate identities/results outside the tracked tree. Git and ordinary artifacts provide history without an evidence database; routine roles load relevant context instead of replaying the package and archives.

Reuse evidence only while relevant inputs are unchanged and no new failure challenges it. Changes to the head/base, tests, dependencies, checks, environment, or generated version invalidate affected claims. Git-derived build/install versions need commit/tag/dirty state, build configuration, and resolved artifact/version: equal source trees at different PR-head, test-merge, or actual-merge identities need not produce the same artifact.

Choose supported model/effort settings for semantic and acceptance complexity, not role names or code volume. A/B must be capable of independently deriving the test oracle; D must match the hardest acceptance claim. Reuse applicable bounded calibration, with independently reviewed public/synthetic material for blind roles. Same-model reviewers are permitted; a different model alone does not prove independence. Escalate after diagnosis, return missing semantics to intake, and record actual configurations and reasons. Model swaps clear neither exposure nor allowances.

Before expensive dependent phases, verify cheap environment/install prerequisites and actual reviewer launch, authentication, and connectivity. A configured reviewer name is not evidence that it can review. Use supported bounded waits with timeout/failure handling, yield during unchanged status, and diagnose failures before retries. There is no automatic retry loop or new scheduler.

Profile slow tests before restructuring. Reuse immutable builds only when all material build/version inputs match; preserve isolated environments and each clean-state or packaging claim. Authorized, independently reviewed sharding must retain every shard/report and complete coverage separately per platform/package. Do not delete slow tests or union platforms to hide coverage gaps.

Measure elapsed critical path separately from aggregate model/runner cost, including calibration, rework, owner waits, and owner effort. Record available per-role usage, tokens, spend, check wall time, review rounds, scenarios/examples, repairs, and defects. Overlapping durations are not additive elapsed time; missing metering is unknown, not zero. Savings claims need a complete comparable baseline and current verified prices, with small-sample limits reported.

## Lessons and doctor maintenance

New target installations use root `LESSONS/`, with `LESSONS/README.md` adapted from the [format guide](src/LESSONS.md) and individual append-only entries. It records useful surprises, gotchas, failed approaches, and instruction gaps. Entries distinguish confirmed findings from hypotheses and link evidence such as tests, commits, or CI runs. Corrections append a superseding entry; owner-authorized sensitive-data removal is the exception. No useful finding means no entry. Secrets, personal data, full prompts, transcripts, and private reasoning do not belong in the log.

Lessons are observations, not automatically activated policy or model memory. A/B may read the format guide and approved public packet, but never lesson entries or broad documentation/history. They can append without reading others or hand an entry to the coordinator. The coordinator/doctor verifies useful lessons before promoting public facts into approved contracts; other roles search relevant entries, and D assesses the candidate before consulting current-task implementation lessons.

Existing log layouts stay in place until a separate coordinated migration is approved. Preserve original Git bytes, IDs, dates, and evidence; agree link handling and any explicit exception for editing append-only bodies, update installed references/packet allowlists, verify links, and leave one canonical live home.

**Doctor turns an evidenced instruction gap into a focused documentation patch.** Target setup provides `delivery doctor` as a thin invocation of `review-work` in doctor mode. Before that invocation exists, supply the [doctor prompt](src/DOCTOR-PROMPT.md) to a fresh coding session. Run it on demand after a recurring failure, meaningful project change, or suspected gap; `--check` inspects and reports without edits.

Doctor distinguishes product bugs, test defects, workflow problems, and documentation gaps. For a verified documentation gap, it edits the existing specification and directly affected instructions on a documentation branch, preferring replacement or simplification over more rules. Fresh independent policy review and your explicit approval of the identified patch precede activation; committing, pushing, and merging follow the agreed owner authority. No supported gap means no edit.

Doctor preserves unrelated work and active tasks. It does not change runtime code, tests, workflows, coverage thresholds, or desired behavior to make a failure pass. Approved changes retain the recorded upstream package version and commit; target Git records local revisions and approval, and `docs/PROJECT.md` keeps adaptation notes current. Existing tasks retain their pinned policy.

Policy rollout reconciles one coherent reviewed patch across the specification and affected generated/installed instructions, prompts, procedures, templates, guides, and examples. Separately approved pilots cover documentation, a conventional bounded repair, authorized infrastructure, and high-risk public/synthetic work, with agreed budget and acceptance criteria. Do not rerun completed owner data merely to benchmark. In-flight migration needs explicit approval and preserves attempts/spending. Suspend a lighter route after a missed material obligation, source exposure, false acceptance, or unresolved gap; comparison and owner approval precede wider adoption. A small pilot does not establish defect-rate equivalence.

## Package provenance, versions, and upgrades

All files under `src/` form one package with one [version](src/VERSION) and [changelog](src/CHANGELOG.md). The [versioning policy](src/README.md#package-versioning) uses Semantic Versioning: patches preserve obligations, minor releases add compatible optional capabilities, and major releases change obligations, authority, accepted evidence, or supported integrations. Development snapshots and release candidates are distinct from published releases. Publication requires an annotated tag at an exact commit, a matching dated changelog, and a GitHub Release; a version string alone is not evidence of publication.

Published package contents are permanent; corrections use a new version, and publication requires GitHub release immutability. Support targets the latest stable release, with older snapshots retained without a backport promise.

Setup verifies that the complete supplied package comes from one upstream commit before adapting it. Published sources require a verified immutable tag and full commit; choosing an unpublished or development snapshot requires your explicit agreement and keeps it labeled unpublished. The project record retains the upstream repository/version/tag/commit, installed path mapping, omissions, and local adaptations. Version, changelog, and package policy remain available as references. Local doctor edits do not invent a new upstream release number.

Upgrades compare **previous upstream, proposed upstream, and current local instructions**. Setup reads migration notes and reconciles the entire adopted package, including prompts, skills, templates, references, paths, and local changes. Independent policy review and your approval of the full diff precede activation and updating the recorded upstream base. Active tasks keep their approved policy revision; later tasks use the approved update. Unknown provenance must be reconstructed or explicitly accepted as an unverified migration, rather than silently invented.

The [source register](src/REFERENCES.md) records adopted ideas, deliberate omissions, and reading limitations. Setup preserves selected source material where permitted, with retrieval metadata and access gaps, once per selected version. Those sources are background rather than additional requirements, and routine workers do not reread the archive.

## Reference

| Document | What it covers |
|---|---|
| [Package guide](src/README.md) | Downstream use, owner responsibilities, and package versioning policy. |
| [Specification](src/DELIVERY-SYSTEM-SPEC.md) | The complete workflow, responsibilities, approvals, and verification requirements. |
| [Setup prompt](src/SETUP-PROMPT.md) | Discover the target project, route architecture intake, and adapt the package. |
| [Intake prompt](src/INTAKE-PROMPT.md) | Clarify architecture and tasks, recording risk, route, and authorization. |
| [Doctor prompt](src/DOCTOR-PROMPT.md) | Inspect evidence and patch verified gaps in existing instructions. |
| [Workflow examples](src/WORKFLOW-EXAMPLES.md) | Project setup, risk-specific routes, corrections, maintenance, pilot rollout, and upgrades. |
| [Agent skills](src/skills/) | The four procedures: `intake`, `design-tests`, `implement-task`, and `review-work`. |
| [Project template](src/templates/PROJECT.md) | Architecture, operation, provenance, approval, and the next slice. |
| [Task template](src/templates/TASK.md) | Behavioral contract, pinned policy, authorized execution, Current state, and evidence/metrics. |
| [Repository-instructions template](src/templates/AGENTS.template.md) | Adapt and reconcile the target repository's `AGENTS.md`. |
| [GitHub setup](src/GITHUB-SETUP.md) | Automated checks, native protection, default submission gates, and pilot prerequisites. |
| [Lessons format](src/LESSONS.md) | Brief, evidence-linked findings and appended corrections. |
| [Version](src/VERSION) and [changelog](src/CHANGELOG.md) | The package's current version and change history. |
| [References](src/REFERENCES.md) | Sources, adopted ideas, reading limits, and archival guidance. |

To contribute to these documents, see [AGENTS.md](AGENTS.md). Upstream release preparation follows the [maintainer checklist](.agents/skills/release-package/SKILL.md); it is separate from using the delivery workflow in a target project.
