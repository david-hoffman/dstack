# <task-id>: <observable outcome>

Package version: [VERSION](../VERSION). Release policy: [package versioning](../README.md#package-versioning).

Task status: draft / approved / blocked / done. This records task progress, not a package release or technical enforcement.

## Delivery policy baseline

- Upstream provenance reference in docs/PROJECT.md at the pinned local revision:
- Existing committed, owner-approved local policy revision (full target Git commit):
- Adopted policy paths governed by that revision:

Pin this revision before task approval; do not use this task's own eventual commit hash. It governs this task through completion. A/B receive only role-permitted policy text from this snapshot, without implementation or history access.

For a policy-change task, distinguish the governing baseline from the proposed patch. Fresh independent policy review and explicit owner approval of that identified patch are required before downstream activation. An approved migration for an in-flight task must identify the changed rules and preserve earlier attempts, spending, and allowances.

## Contract

- Project/interface references:
- Purpose and non-goals:
- R1: <observable requirement>
- R2: <observable requirement>
- Inputs, outputs, errors, and permissions:
- Success, error, and boundary examples:
- S1: <distinct approved decision and observable outcome; requirement IDs>
  - Optional coverage examples: <equivalent values and the accepted decision they exercise>
- Unresolved material decisions:

Start with roughly five behavioral scenarios as a planning heuristic. A distinct rejection, interpretation, output guarantee, or boundary outcome is a separate scenario. Approve a larger coherent contract once when needed; equivalent data within accepted behavior and budget need no new approval. Neither parameterized-test counts nor branch counts determine contract size. Do not combine unrelated obligations to meet the heuristic.

For a bug: observed versus expected behavior, environment, reproduction evidence, and hypotheses. Unknown causes do not authorize a speculative fix.

## Authorized execution

Tier and reason; role route; named author/mode and owned files/settings; exact edit scope; prerequisite and canonical checks; per-role model/effort and selection reason; local/CI gate mode; escalation triggers; preparation/execution budget; review windows/caps and remaining allowances:

- Mechanical/documentation: one worker for non-policy deterministic changes; owner acceptance, plus any review required by this contract.
- Bounded behavior/infrastructure: explicitly authorized product, test, fixture, and maintenance paths; one worker plus a fresh independent reviewer of oracle, behavior, infrastructure/gates, scope, and exact passing candidate.
- High-risk product: initially fresh root A/B/C/D; A/B remain blind and own tests; C owns authorized product paths and retains all restricted-file rules. An authorized A or C may continue its own session for an in-scope correction while A's blindness holds; B/D verdicts remain fresh and independent.
- High-risk infrastructure: fresh blind A, fresh blind B, fresh root infrastructure author using the existing `implement-task` skill's `infrastructure author` mode, then fresh D. That author owns only the named infrastructure files/settings; A/B own tests, and policy documentation retains its separate path. Mixed product/infrastructure work requires separately scoped fresh product C and fresh infrastructure author; A/B and D cover the full behavior and authority contract, and D inherits neither author's conversation. Infrastructure-author repair uses a fresh infrastructure author and fresh D within the existing task-wide repair allowance; the A/C continuation exception does not extend to this mode.
- Policy documentation: separate worker and fresh independent policy reviewer; no fabricated product-red evidence. Identify the proposed patch and required owner approval before activation.

Record the selected route and named edit ownership, not every option above. Uncertain impact promotes the tier; mixed scope takes the highest tier unless separately approved contracts justify a split. Changed tests/fixtures and dependency/workflow/gate maintenance require independent review. Removed assertions need a reviewed obligation mapping; unsettled semantics or execution/security authority require the high-risk route. Stop a bounded worker on promotion pending explicit owner approval of the identified high-risk contract, route, named infrastructure/settings ownership where applicable, checks, and budget. Do not merely switch worker modes; product C's restrictions remain absolute. These changes need their own authorized scope.

Default gate: full canonical local verification of the exact submission candidate, then every required CI platform, with 100% measured statements and branches globally and per package across instrumentable owned runtime, including never-imported files and applicable subprocesses. Incremental checks guide edits. An optional CI-authoritative pilot for eligible settled mechanical/bounded work requires separate specific owner approval and verified native protection, trusted-check, aggregate, integration, and exact artifact/version prerequisites; this template does not activate it. High-risk work retains full local verification; execution/security authority changes are ineligible for that pilot. Record its policy/evidence reference if approved; otherwise use the default.

Record each review window and approved round cap. Every completed correction review consumes a round in its recorded window. After two nonacceptances, stop and diagnose; another attempt needs a bounded diagnosed correction under the approved path and remaining allowances. Default: at most one implementation repair across the task. Preserve previous windows, spending, and repairs; a new session, renamed task, narrower review, model change, or migration does not replenish them.

## Owner approval

Actual owner instruction/approval reference and identified document/commit:

A complete explicit owner instruction may authorize a mechanical or bounded task. Record its exact scope, tier, checks, budget, and inherited constraints, then send a concise read-back without requiring a redundant approval. High-risk work requires explicit approval of the identified contract. Policy work requires fresh independent policy review and explicit approval of the identified patch before activation. Silence and an agent's own decision are never approval.

Approval authorizes the recorded routine role transitions, checks, in-scope correction within remaining allowances, and approved unchanged-scenario redistribution. Changed behavior, interfaces, permissions, data sharing, tier downgrade, budget extension, or an exhausted repair allowance needs renewed approval. Unanswered material questions block dependent work.

## Current state

- Decision and status:
- Exact revision/tree and test checkpoint:
- Classified findings and unresolved limits:
- Applicable evidence/report links:
- Next role/action:
- Remaining budget, review-window rounds, and task-wide repair allowance:

Maintain this one concise state; link earlier accepted reports instead of copying them. A/B receive a separate approved public-contract packet, never implementation-bearing status.

## Evidence and metrics

- Role/session and accepted-report links; original test checkpoint and intended baseline result where applicable; correction diffs/dependency mapping; supplemental-test labels:
- Evidence receipt links: tested revision/tree, test revision, canonical command, dependency-lock identity, relevant environment/tool versions and platform, integration base, exact result/coverage, and unresolved limits. Fingerprint material ignored/untracked inputs separately; keep final candidate identity/results outside its tracked tree.
- Build/install version evidence when Git-derived: commit/tag/dirty state, build configuration, resolved version, and artifact identity. Head, test-merge, and actual merge identities may differ.
- Per-role model/effort, responses, input/cached/output tokens, available monetary cost, elapsed/owner-wait minutes, and check wall time, including calibration, failed launches, and rework:
- Task critical-path timestamps/dependencies, time to PR/readiness/merge, repeated checks, scenarios versus coverage examples, review windows/rounds, repairs, found/missed defects, source exposure, and owner effort:

Reuse evidence only while all relevant inputs remain unchanged and no new failure challenges it. Run cheap bounded environment/install/reviewer-launch prerequisites before expensive dependent checks; stop and diagnose a failed prerequisite. Environment or generated-version changes can invalidate evidence at an unchanged source tree. Missing metering is **unknown**, not zero; avoid double-counting overlapping elapsed time, cumulative counters, or child sessions. No full conversations or implementation rationale for blind roles.

Relevant non-obvious discoveries belong in root `LESSONS/`, following `LESSONS/README.md`, not a duplicate log here. A/B may read only that guide and their approved packet, never lesson entries.
