---
name: review-work
description: Review tests (B), review a passing candidate (D), or improve the spec from evidence (doctor). Use one mode per fresh session.
---

# Review work

Package version: [VERSION](../../VERSION). Release policy: [package versioning](../../README.md#package-versioning).

## Tests — B

Use A's approved behavior/public-interface inputs, permitted policy text from the task's pinned local revision, and proposed tests. The coordinator supplies the snapshot; do not retrieve it through Git history. Do not read implementation, its history/conversation, or LESSONS.md.

Check contract clarity, real observable assertions, independent expected values, negative/boundary behavior, and requirement coverage. Prefer meaningful E2E tests over mock-only or duplicate unit tests. Name a plausible wrong behavior the suite should detect. Return corrections to A. Do not implement or silently choose missing requirements.

Accepted tests still need meaningful failing evidence and a recorded Git test checkpoint before C.

## Candidate — D

Read the approved task, its pinned local policy revision, exact candidate, test checkpoint, and actual check evidence, not C's conversation. Form findings before consulting current-task implementation lessons.

Inspect behavior, security, public boundaries, and test/workflow changes. Compare the tested commit with the proposed merge. Missing/skipped/incomplete results are not success. Check the real product result, not only a summary or compilation.

Include simplification in this review: unnecessary wrappers, duplication, dependencies, and speculative features. Stay within the task. No extra simplification agent. Report concrete findings and evidence; do not fix the candidate and then approve it. Corrections use fresh C and renewed checks/D.

## Doctor

Use [DOCTOR-PROMPT.md](../../DOCTOR-PROMPT.md) and specification section 8. This is the explicit documentation-editing mode, not a product reviewer secretly changing the rules.

Inspect recent lessons and evidence. Fix verified gaps in the existing specification and directly affected instructions on a docs branch; prefer replacing/removing text. Do not change tests, workflows, runtime code, or thresholds. Show the diff and wait for owner approval before committing/pushing/merging. Preserve upstream provenance and the official package version; target Git records local changes and approval. Keep docs/PROJECT.md adaptation notes current. Do not change an active task's pinned rules. Upstream upgrades use specification section 10 to reconcile previous upstream, new upstream, and all adopted local instructions before approval and updating the base. `--check` writes nothing. No supported gap means no edit.

## Every mode

Keep results short and evidence-linked. Stop on material ambiguity or budget exhaustion. Append useful findings to LESSONS.md, except blind mode must append without reading or return the entry for someone else to append. Do not claim these prompt restrictions are mechanically enforced.
