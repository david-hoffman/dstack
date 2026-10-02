# <task-id>: <observable outcome>

Package version: [VERSION](../VERSION). Release policy: [package versioning](../README.md#package-versioning).

Task status: draft / approved / blocked / done. This records task progress, not a package release or technical enforcement.

## Delivery policy baseline

- Upstream provenance reference in docs/PROJECT.md at the pinned local revision:
- Existing committed, owner-approved local policy revision (full target Git commit):
- Adopted policy paths governed by that revision:

Pin this revision before task approval; do not use this task's own eventual commit hash. It governs this task through completion. A/B receive only role-permitted policy text from this snapshot, without implementation or history access.

## Contract
- Project/interface references:
- Purpose and non-goals:
- R1: <observable requirement>
- R2: <observable requirement>
- Inputs, outputs, errors, and permissions:
- Success, error, and boundary examples:
- Allowed scope and applicable checks:
- Budget, risk, and unresolved decisions:

For a bug: observed versus expected behavior, environment, reproduction evidence, and hypotheses. Unknown causes do not authorize a speculative fix.

## Owner approval
Actual approval reference and identified document/commit. A material change needs a new read-back and approval. Do not fill this in from an agent's own decision.

## Execution record
A/B session references and concise test review; test checkpoint and intended failing result; C/D session/candidate references; commands/results and CI/PR links; unresolved findings; spending when measurable. No full conversations or implementation rationale for blind roles.

Relevant non-obvious discoveries belong in LESSONS.md, not a duplicate log here.
