# Workflow examples

Package version: [VERSION](VERSION). Release policy: [package versioning](README.md#package-versioning). These are illustrative downstream examples, not executed runs, approved requirements, or active pilots. The specification governs the route and gates.

## Explore across conversations, then promote

Request: “I do not know the right interface yet. Help me hack together a prototype so I can try it.”

Intake enters exploration mode directly. The engineer and agent try provisional code and tests, changing direction as they learn. They defer architecture approval, the delivery contract, and delivery roles. Repository permissions, unrelated work, privacy, spending limits, and commit/push/merge/release authority still apply; exploration cannot change policy or weaken required checks. Ask only when a consequential unanswered question blocks the next useful experiment.

The existing task record keeps one compact handoff: stable exploration ID, branch, base/latest full commits when available, uncommitted work, relevant conversation references and actual visibility, experiment, reproducible results, known defects, and next step. A second conversation resumes from this record without resetting spending or pretending a branch name identifies fixed source. No commit is needed merely to begin experimenting.

At useful checkpoints, a participating agent can observe friction. It records that the engineer needed experiments before choosing an interface, with evidence, and separately hypothesizes that intake should offer an example earlier. It appends only useful notes under the actual canonical lessons home and identifies which threads/artifacts it saw. It cannot approve requirements, redirect the experiment, revise policy, or certify readiness. There is no required observer agent or extra skill. No useful lesson is a valid outcome.

Later request: “Use this prototype as a reference and deliver it according to the repository rules.”

Fresh architecture/task intake pins the prototype at a full commit and extracts desired public behavior, accidental behavior, defects, and implementation suggestions. It obtains the applicable architecture/task, route, ownership, checks, and budget approvals. It chooses new implementation from the integration baseline or hardening/refactoring the prototype. A requested promotion starts intake; it does not automatically approve everything the prototype happens to do.

Suppose the prototype performs scientific fitting with unresolved numerical behavior. That uses high-risk delivery. A/B receive only the approved public contract and permitted policy, without prototype source, exploration transcripts, or lesson entries. Expected values need independent references, examples, or properties. C can use the pinned prototype as an implementation reference. Tests added after prototyping remain supplemental/regression evidence and may pass initially; a rewrite solely to manufacture red is unnecessary. Test checkpoint, restricted ownership, exact-candidate checks, fresh review, and normal merge/release authority still apply.

## Mechanical documentation

Request: “Correct these three broken product-guide links without changing any requirements.”

Under an adopted tier policy, this complete instruction can authorize the mechanical scope. Intake records the actual instruction, tier/reason, allowed files, deterministic link checks, budget, and full-local gate mode, then sends a concise read-back. No second approval is needed just because the record was written afterward. One worker fixes the links, checks the relevant targets and diff, completes the applicable canonical local checks on the exact candidate and required CI, and presents it for owner acceptance. Independent review is optional unless the contract requires it.

Changing the delivery rule while repairing a link would require explicit policy-patch approval and independent policy review; a small prose diff cannot approve itself as mechanical.

## Bounded conventional repair

Request: “Restore the documented alphabetical ordering of this existing command's output; preserve its format and error behavior.”

The ordering contract is already settled. Intake records a bounded tier, the worker's authorized product/test files, canonical checks, model/effort choices, budget, and reviewer route. The worker may inspect implementation and add distinguishing public-command cases. A fresh independent reviewer checks the expected order against the approved contract, challenges discrimination and positive/boundary cases, reviews both tests and product changes, and assesses the exact passing candidate after full local checks and required CI. The worker cannot approve their own repair.

Several input permutations with the same ordering decision are coverage examples. A distinct empty-input guarantee or rejection rule is a separate behavioral scenario. Five scenarios is a planning heuristic; a larger coherent contract can be approved once. Parameterized test count does not define scope, and removing assertions needs a reviewed obligation mapping.

The same applies to a settled function contract with 33 input examples: approve the coherent outcomes once, then let the worker choose ordinary test values. Distinct rejection rules or new guarantees remain material behavior requiring authorization. Review valid alternatives as well as rejection cases, and verify that a plausible wrong implementation would fail the relevant assertion.

If review reveals an unsettled collation convention, stop dependent work and return that meaning to intake. A lower-tier failure does not authorize a new interface or scientific repair.

## Authorized infrastructure maintenance

Request: “Update the pinned lint tool and its invocation, preserving existing supported platforms, required checks, discovery, coverage, and permissions.”

An explicit maintenance contract assigns the bounded worker the named dependency/configuration/workflow files and relevant checks. It does not give high-risk C permission to edit workflows during a product task. First verify the lock/interpreter/install health and actual reviewer availability. A fresh independent reviewer examines dependency changes, the infrastructure diff, failure propagation, preserved gates, scope, and the exact passing candidate. Full local verification and all required CI still apply; each required platform/package retains complete coverage, including never-imported runtime and applicable subprocesses.

A proposed execution-authority, CI-credential, or permission change stops the bounded worker. Before proceeding, the owner explicitly approves the identified high-risk contract, fresh-root route, named infrastructure/settings ownership, checks, and budget. For infrastructure-only work, fresh blind A authors the public authority/behavior tests and fresh blind B reviews; a fresh root infrastructure author uses the existing `implement-task` in `infrastructure author` mode for only the named infrastructure/settings; fresh D reviews the exact passing candidate. Tests remain A/B's scope and policy patches follow separate independent policy review. Product C cannot edit infrastructure or settings, and promotion never relaxes those restrictions.

If the approved task also changes product behavior, record separate fresh product C and infrastructure author sessions. A/B and D cover all approved behavior/authority, and D inherits neither author's conversation. An infrastructure repair uses a fresh root infrastructure author and fresh D within the existing task-wide default single implementation repair across both authors; A/C's continuation exception does not apply to this author.

A proposed shard/helper or slow-test restructuring is separate authorized infrastructure work: profile first, retain all distinct clean-install and packaging claims, require every shard/report, and combine coverage per platform/package. Do not union platforms or delete slow obligations to obtain a green result.

This task is initially excluded from a CI-authoritative pilot if it changes that pilot's own gates, coverage/discovery, build/release proof, protection, or authority.

## High-risk empty-project start

Request: “Build a local tool that counts non-empty lines in a file.”

Intake first settles the environment, encoding, whitespace meaning, output, and error behavior, proposes a small architecture record, and obtains owner approval. The first substantial public interface or unresolved semantics uses high risk; architecture approval alone does not authorize it. The approved task pins an existing approved local policy commit and records the fresh root A/B/C/D route, scope, checks, model/effort choices, budget, and allowances.

The coordinator supplies A/B only the approved public contract, fixtures/conventions, permitted policy text, and lesson format guide from that revision. They do not browse implementation, history, lesson entries, or broad documentation. Fresh root A writes tests through the real command for the distinct approved outcomes. Fresh blind root B independently checks the oracle and discrimination. Run the accepted tests against the baseline: a scaffold can demonstrate missing functionality, not an invented historical bug. Save the reviewed test checkpoint. Fresh root C implements without changing tests/fixtures, coverage/discovery, workflows, or policy. Run full canonical local checks on the exact candidate, then fresh root D reviews the behavior, diff, evidence, and required CI before owner merge.

A later settled formatting repair may qualify for a lower tier after approval; risk is decided from that contract, not inherited from a previous task or inferred from its size.

## High-risk permissions and correction

Request: “Export my customers as CSV.”

Intake resolves whose records, allowed fields, escaping, download behavior, and failure outcomes. The permission boundary requires high-risk A/B/C/D. Browser journeys run through the actual backend and an isolated test database; one scenario proves that a user cannot export another organization's records. A mock-only browser test does not prove server access control. A/B configurations meet the oracle complexity; a cheap implementation does not justify a weak oracle review.

Suppose a finding reveals a wrong shared CSV observer. C stops rather than changing expectations. The coordinator converts the discovery into an approved public reproduction, excluding implementation-bearing reports and coverage-line maps. Blind A may continue its own session if blindness, scope, and allowances remain intact; otherwise use a fresh author. Fresh blind B reviews the changed observer and every dependent case against the previous accepted checkpoint and dependency mapping. Shared expectation changes expand review scope; B decides which unchanged evidence remains valid. Changed public meaning needs renewed intake approval. Supplemental tests do not recreate original test-first evidence.

An authorized implementation repair may continue C's own session; its reviewer is fresh D. Every completed correction review counts in its recorded window. After two nonacceptances, diagnose and stop until an approved resolution exists within remaining allowances. New sessions, a smaller delta, or a model change never resets spending, review windows, or the default task-wide one implementation repair.

## Optional CI-authoritative submission pilot

An owner separately approves a policy pilot for an eligible settled lower-tier task. A read-only check first establishes effective native target-branch protections, trusted check sources, current-base/integration rules, and bypass settings. Unknown or ineffective controls block eligibility; configuring them is separately authorized setup. The pilot excludes high risk, uncertain evidence, and changes to its own gates, coverage/discovery, build/release proof, protection, or authority. Editing these examples does not activate it.

Focused public-behavior tests and inexpensive local checks pass before opening/updating a PR. Known applicable failures block submission until classified repair and relevant local checks establish that their cause is addressed. A PR awaiting the full suite is unverified and never ready. Full CI covers the complete owned runtime at 100% measured statements/branches per required platform/package, including never-imported files and subprocesses. Its aggregate fails on any failed, cancelled, skipped, neutral, absent, or incomplete platform/shard/report. A green check name alone proves neither complete results nor protection.

CI evidence identifies the candidate/head, current base/integration state, environment/lock, artifact/version, and result. If Git determines versions, PR head, synthetic merge, and eventual merge/squash/rebase identities can produce different versions even with matching source trees. Unavailable exact artifact proof blocks eligibility. A fresh independent reviewer assesses the final candidate and required evidence; head/base/environment/check/version changes invalidate affected checks and review. CI failure stops readiness; a repair update spends existing allowances, passes the approved local gate, and renews full CI. The owner still performs the explicit merge action. If prerequisites lapse, use the default full-local route.

## Learn, then improve policy

Suppose an end-to-end test fails because its process does not wait for application readiness. Append an evidenced entry under target root `LESSONS/`, with the reproducible failure and readiness evidence. The source [LESSONS.md](LESSONS.md) is the guide adapted to target `LESSONS/README.md`; it is not the live entry log. A/B may read the guide and their approved public packet, never entries. D assesses the candidate before current-task implementation lessons.

Run `delivery doctor`. If readiness is already covered, doctor reports a test/workflow defect and leaves policy alone. For an evidenced policy gap, it edits the smallest affected existing instructions on a documentation branch. Fresh independent policy review and explicit owner approval of the identified patch precede activation; no fabricated product-red evidence is needed. Git records the change and an appended disposition links it. Doctor cannot repair a red build by dropping requirements. Upstream provenance stays recorded, and active tasks retain their pinned policy unless explicitly migrated without erasing attempts or allowances.

If the review finds no missing rule, record that no-gap outcome. Do not invent a lesson or policy patch to finish a demonstration.

An existing `LESSONS.md` or `docs/LESSONS/` log stays in place pending separate migration approval. Agree preservation and link handling first. Entry-body/link edits require an explicit append-only exception with original Git bytes, preserved IDs/dates/evidence, verified inbound/supersession links, and one canonical home. Moving a directory is not a blindness improvement.

## Verify the actual operation

Suppose a copied interpreter cannot find its shared library on a required platform. Classify the fixture/environment failure before repair. Its exit cannot prove that product preflight rejected the intended input if the relevant assertion never executed. Repair the authorized fixture, then run the real command on that supported environment.

Suppose a subprocess can redirect a verification report's output directory through a symlink after initial validation. Test that operation-time transition and protect tracked files and Git metadata at the actual report write. An initial path check or damage detection afterward cannot establish safe writing.

Suppose an unchanged verification plugin reads an external file that changed since a cached pass. That pass is stale for the affected claim. Prefer ordinary commands and retained artifacts; add custom receipts/caches only under authorized scope with known relevant inputs and demonstrated total benefit. Faster wall time alone does not prove lower accepted-task cost when runner consumption, failed attempts, or owner effort increase.

## Roll out changed delivery rules

Prepare one coherent specification patch covering tier boundaries/ownership, scoped corrections, author continuation, model/effort criteria, gate mode, approval rules, and budgets. Explicit owner approval and independent policy review precede activation. Align generated/installed AGENTS, task/intake records, directly affected procedures, guides, and examples; do not activate a permissive sentence while retaining incompatible restrictions elsewhere.

Before any pilot, agree criteria and a bounded budget for one documentation task, one conventional bounded repair, one authorized infrastructure task, and one high-risk public/synthetic task. Check correct tier/authority, preserved behavior and gates, independent review, expanded shared-oracle review, renewed invalidated evidence, exact-candidate verification, honest failures, and unchanged allowances. Do not rerun completed owner-data conversion for a benchmark. Suspend a lighter route on missed material obligations, exposure, false acceptance, or unresolved gaps; diagnose within existing allowances before retrying.

Compare complete cost per independently accepted task and elapsed critical path separately: model/effort usage, tokens/cost when available, calibration, checks, failed launches, rework, reviewer/owner time, scenarios versus coverage examples, windows/rounds, repairs, and defects. Unknown metering stays unknown. Overlapping checks/reviews are not additive elapsed time, though all resource usage counts. Wider adoption, or a ten-task comparable-maintenance follow-up, needs owner approval and an explicit budget; a small sample does not prove quality equivalence. No pilot or setup is executed in this document repository.

## Upgrade an adapted package

Suppose installed instructions include a locally approved data-access rule. Setup verifies the new upstream snapshot, reads the changelog and migrations, and compares previous upstream, new upstream, and current local instructions. It reconciles every adopted file/path with the local rule and presents the diff for independent policy review and owner approval. Target Git then records the approved change; the project record updates upstream base and adaptations. In-flight tasks keep their pinned rules unless explicitly migrated, retaining spent attempts/budget. An explicitly chosen development snapshot remains labeled unpublished; unchanged trees alone do not establish build/version identity.
