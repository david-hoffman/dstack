# <task-id>: <observable outcome>

Package version: [VERSION](../VERSION). Release policy: [package versioning](../README.md#package-versioning).

Task status: exploring / promoted / draft / approved / blocked / done. This records progress, not a package release, approval, or technical enforcement. `Promoted` records a prototype handoff; it does not authorize delivery. Use the exploration section while experimenting; the delivery baseline, contract, and authorized execution sections apply to formal delivery.

## Exploration handoff (when applicable)

- Stable exploration ID and branch:
- Purpose, requested scope, boundaries, and supplied budget:
- Base/latest committed references (full target Git commits when available):
- Threads actually visible to the recording agent:
- Uncommitted work and how to reproduce the latest result:
- Useful results, known defects, unresolved choices, and next experiment:
- Promotion reference (full prototype commit, or unresolved uncommitted reference):
- Desired behavior and observed choices, accidental behavior, or bugs to preserve/reject:
- Promotion approach: implementation from the integration baseline / prototype hardening:

Update this compact handoff at useful checkpoints across threads. The branch is the exploration session boundary; its moving name is not a fixed reference. No commit, approved architecture, or formal contract is required to start exploring. Keep supplied boundaries and budgets. Freeze the prototype reference before formal delivery execution; then use normal intake and authorization. Do not invent approval or test-first history. Keep useful learning under the existing lesson guide, not a transcript here.

## Delivery policy baseline

- Upstream provenance reference in docs/PROJECT.md at the pinned local revision:
- Existing committed, owner-approved local policy revision (full target Git commit):
- Adopted policy paths governed by that revision:

Pin this revision before formal task execution; do not use this task's own eventual commit hash. It governs this task through completion. A/B receive only role-permitted policy text from this snapshot, without prototype internals, exploration notes, implementation, or history access.

For a policy-change task, distinguish the governing baseline from the proposed patch. Record the owner’s amendment/adoption request and fresh independent policy review before activation within that scope. A request only to inspect/propose does not authorize adoption. An in-flight migration needs explicit owner authorization identifying the changed rules; preserve earlier attempts, spending and any actual owner-set limits.

## Contract

- Project/interface references:
- Purpose and non-goals:
- R1: <observable requirement>
- R2: <observable requirement>
- Inputs, outputs, errors, and permissions:
- Success, error, and boundary examples:
- Independent expectation sources, units/conventions and success criteria; justified test tolerances where applicable:
- Approved project coverage policy reference at the pinned revision; inherited choice and any explicitly approved policy change/migration:
- Relevant high-risk paths, required observable outcomes, and unresolved risk decisions:
- S1: <distinct approved decision and observable outcome; requirement IDs>
  - Optional coverage examples: <equivalent values and the accepted decision they exercise>
- Unresolved material decisions:
- For prototype promotion: frozen prototype commit and approved behavior/choices to preserve or reject:

There is no default scenario count. A distinct rejection, interpretation, output guarantee or boundary outcome is a separate scenario; equivalent values can be coverage examples. Split only for coherent contracts and feasible dependencies. Preserve the requested outcome and cumulative accounting; branch/test counts do not determine scope.

For a bug: observed versus expected behavior, environment, reproduction evidence, and hypotheses. Unknown causes do not authorize a speculative fix.

Resolve an undefined request for “complete coverage” before tests are written, using [specification section 5.1](../DELIVERY-SYSTEM-SPEC.md#51-agree-on-coverage-before-writing-tests). Inherit settled project choices without another interview. Behavior coverage and risk review always apply to the approved scope; numerical line/statement/branch targets apply only as selected. Map scenarios and risks to test/review evidence below. An accepted A/B suite is the test baseline, not proof of every possible behavior or immunity to a concrete omission found later.

## Authorized execution

Tier and reason; role route; named author/mode and owned files/settings; exact edit scope; prerequisite and canonical checks; per-role model/effort and selection reason; local/CI gate mode; escalation triggers; actual owner-set limits with units/hard stops, or not set:

- Mechanical/documentation: one worker for non-policy deterministic changes under the owner’s request, plus any review required by this contract.
- Bounded behavior/infrastructure: explicitly authorized product, test, fixture, and maintenance paths; one worker plus a fresh independent reviewer of oracle, behavior, infrastructure/gates, scope, and exact passing candidate.
- High-risk product: initially fresh root A/B/C/D; A/B remain blind and own tests; C owns authorized product paths and retains all restricted-file rules. An authorized A or C may continue its own session for an in-scope correction while A's blindness holds; B/D verdicts remain fresh and independent.
- High-risk infrastructure: fresh blind A, fresh blind B, fresh root infrastructure author using the existing `implement-task` skill's `infrastructure author` mode, then fresh D. That author owns only the named infrastructure files/settings; A/B own tests, and policy documentation retains its separate path. Mixed product/infrastructure work requires separately scoped fresh product C and fresh infrastructure author; A/B and D cover the full behavior and authority contract, and D inherits neither author's conversation. Infrastructure-author repair uses a fresh infrastructure author and fresh D within authorized scope and any actual owner-set limits; the A/C continuation exception does not extend to this mode.
- Policy documentation: separate worker and fresh independent policy reviewer; no fabricated product-red evidence. Identify the proposed patch, requested adoption scope and independent review before activation.

Record the selected route and named edit ownership, not every option above. Uncertain impact promotes the tier; mixed scope takes the highest tier unless separately approved contracts justify a split. Changed tests/fixtures and dependency/workflow/gate maintenance require independent review. Removed assertions need a reviewed obligation mapping; data-loss behavior, unsettled semantics or execution/security authority require the high-risk route. Stop a bounded worker on promotion while the coordinator records the higher-risk contract, ownership and checks and establishes fresh required roles. Ask only for missing material meaning or authority. Do not merely switch worker modes; product C's restrictions remain absolute. These changes need their own authorized scope.

Default gate: full canonical local verification of the exact submission candidate, then every required CI platform, satisfying the referenced coverage policy. Selected metrics retain their exact thresholds, measurement scope, and complete required reports; an unselected metric alone cannot block acceptance. Incremental checks guide edits. An optional CI-authoritative pilot for eligible settled mechanical/bounded work requires separate specific owner approval and verified native protection, trusted-check, aggregate, integration, and exact artifact/version prerequisites; this template does not activate it. High-risk work retains full local verification; execution/security authority changes are ineligible for that pilot. Record its policy/evidence reference if approved; otherwise use the default.

There are no default review or repair quotas. Record actual owner-set limits with units; absent limits are **not set**. Diagnose each correction, retain cumulative reviews/repairs/failed attempts and obtain fresh required verdicts. Continue until completion or an actual limit, missing material decision or unavailable authority blocks progress. Session changes, splits, narrower reviews, model changes and migration reset no history or spending.

## Owner approval

Actual owner instruction/approval reference and identified document/commit:

A complete direct owner request authorizes its intended scope across every route, including high-risk work and policy documentation. Record the actual instruction and concrete contract, then send a concise read-back and proceed. Required independent review, role/file restrictions and the pinned policy remain binding. Resolve missing material choices or outside-request objectives; a proposal-only request is not adoption authority.

Authorization covers routine role transitions, needed in-scope checks, diagnosed corrections and fresh required reviews. New permissions/sharing, outside-request behavior, missing material meaning or extension of an actual owner-set limit needs an answer. Commit, push, merge, release and settings changes need explicit authorization. Silence supplies no missing decision or authority.

## Current state

- Decision and status; independent assessment complete/incomplete/unavailable, with a verdict only when complete:
- Exact revision/tree and test checkpoint; assigned review scope, context provenance, and exclusions/filtering:
- Classified findings, dispositions, and unresolved limits:
- Applicable evidence/report links:
- Next role/action:
- Actual owner-set limits and cumulative attempts/spending; absent limits not set:

For independent review, apply the [review-result contract](../DELIVERY-SYSTEM-SPEC.md#review-results-and-finding-disposition) within these existing fields. Missing material context or unfinished review portions prevent acceptance; verify findings and record confirmed, rejected, unresolved, or advisory dispositions. Severity and repair cost cannot waive approved obligations.

Maintain this one concise state; link earlier accepted reports instead of copying them. A/B receive a separate approved public-contract packet, never prototype internals, exploration notes, or implementation-bearing status.

For a coverage finding, record the concrete missing behavior/risk or selected metric shortfall and its classification under [specification section 5.2](../DELIVERY-SYSTEM-SPEC.md#52-classify-coverage-findings-before-correction): test gap, unnecessary implementation complexity, unresolved semantics, measurement defect, or policy conflict. Route it to the corresponding owner within authorized scope and any actual owner-set limits; a bare uncovered branch does not automatically return to A.

## Evidence and metrics

- Role/session and accepted-report links; original test checkpoint and intended baseline result where applicable; correction diffs/dependency mapping; supplemental-test labels:
- Requirement/scenario-to-test mapping and short independent risk-audit disposition; concrete omissions and their resolution (or why runtime obligations are unaffected for non-behavioral work):
- Evidence receipt links: tested revision/tree, test revision, canonical command, dependency-lock identity, relevant environment/tool versions and platform, integration base, exact result/coverage, and unresolved limits. Fingerprint material ignored/untracked inputs separately; keep final candidate identity/results outside its tracked tree.
- Build/install version evidence when Git-derived: commit/tag/dirty state, build configuration, resolved version, and artifact identity. Head, test-merge, and actual merge identities may differ.
- Per-role model/effort, responses, input/cached/output tokens, available monetary cost, elapsed/owner-wait minutes, and check wall time, including calibration, failed launches, and rework:
- Task critical-path timestamps/dependencies, time to PR/readiness/merge, repeated checks, scenarios versus coverage examples, cumulative reviews, repairs, found/missed defects, source exposure, and owner effort:

Reuse evidence only while all relevant inputs remain unchanged and no new failure challenges it. Run cheap bounded environment/install/reviewer-launch prerequisites before expensive dependent checks; stop and diagnose a failed prerequisite. Environment or generated-version changes can invalidate evidence at an unchanged source tree. Missing metering is **unknown**, not zero; avoid double-counting overlapping elapsed time, cumulative counters, or child sessions. For prototype promotion, label regression and supplemental tests honestly; neither a forced rewrite nor manufactured red evidence establishes original test-first history. No full conversations or implementation rationale for blind roles.

Relevant non-obvious discoveries belong in root `LESSONS/`, following `LESSONS/README.md`, not a duplicate log here. A/B may read only that guide and their approved packet, never lesson entries.
