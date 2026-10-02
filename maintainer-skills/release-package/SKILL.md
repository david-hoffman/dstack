---
name: release-package
description: Use when checking dstack package versions, preparing a document-package release, or publishing an explicitly approved release. Not for downstream delivery or local doctor edits.
---

# Release the document package

This is maintainer skill source and a readable checklist, outside automatic skill discovery. It is not installed by downstream setup. Read root [AGENTS.md](../../AGENTS.md), the [versioning policy](../../src/README.md#package-versioning), [VERSION](../../src/VERSION), and [changelog](../../src/CHANGELOG.md). The policy is authoritative; do not copy its rules into another manifest.

## Choose the requested mode

- **Check:** read-only; identify the required bump and report inconsistencies.
- **Prepare:** make scoped documentation/metadata edits and return a reviewable candidate. This does not authorize committing, tagging, pushing, publishing, or settings changes.
- **Publish:** only perform actions explicitly authorized for the verified candidate. Reuse existing authorization for that candidate; do not broaden it.

Run no bundled delivery roles, installers, tests, or new release tooling. A checklist is not enforcement. Use existing Git/file tools and available GitHub access; never infer that a missing tool or failed request means success.

## Evidence required

1. **Identity:** repository/remote, working-tree inventory, previous stable tag and full resolved commit, proposed version, and complete `src/` diff. For bootstrap, verify local and remote history and the changelog baseline. Include added, deleted, and untracked files; preserve unrelated work.
2. **Compatibility:** classify the highest impact across all changes since stable. Changed approvals, role authority, required records, or integration names cannot hide under "clarification." Review every coupled prompt/skill/template affected. Do not select patch merely because the files are Markdown.
3. **Package:** check version syntax/state, changelog rationale/migration/date, local links/anchors, and stale release/per-skill metadata. Compare the complete package inventory and contents to the intended revision; distinguish reviewed edits from foreign/copied bytes. Review the policy's downstream provenance and active-task rules.
4. **Candidate:** show the preparation diff and results. After an authorized commit, require a clean tree, the exact approved commit, matching version/notes, and explicit authorization for the remaining actions. Do not tag working-tree edits. Any changed candidate invalidates prior checks and candidate approval.
5. **Remote:** inspect tags and releases immediately before publishing. Require verified release immutability. A reused version pointing elsewhere, unavailable remote, unexplained existing draft/tag, or disabled/unverified protection stops publication. For an interrupted operation, resume only matching approved objects; never force, delete, or overwrite a collision.
6. **Result:** bind the annotated tag to the approved commit, publish the matching release only when authorized, and read back its resolved commit, version, preview/stable status, and immutability. Report partial success precisely; never repair an unexpected result through further unapproved mutations.

## Return a release record

Report in the conversation or existing review record:

- Mode; repository; baseline and candidate commit (or **uncommitted**).
- Proposed version and bump rationale; migration notes.
- Each check: **passed**, **failed**, or **unverified**, with actual evidence.
- Actions authorized, actions performed, and remaining blockers.
- Published tag and release link only after read-back verification.

Keep this record outside the candidate bytes when it names that commit. A prepared diff, successful check, approval, and published release are distinct states. Continue safe preparation when publication is blocked; never describe missing evidence as a passed release check.
