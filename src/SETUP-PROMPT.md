# Setup prompt

Package version: [VERSION](VERSION). Release policy: [package versioning](README.md#package-versioning). Supply the whole package to a fresh coding-harness session at the target monorepo, then use this prompt. Nothing here claims that a `delivery` command is already installed.

```text
Set up the Agentic Software Delivery System described in DELIVERY-SYSTEM-SPEC.md.
Read that file once. It supersedes the earlier conversation drafts. Follow the package
versioning policy in README.md; VERSION is the one package version, not a per-file
or per-skill version. Verify the complete supplied package is one upstream commit
before adapting it. For a published release, verify its immutable tag and full commit.
Use an unpublished/development snapshot only with my explicit choice; never call it
published. Record the source repository, package version, tag when published, and full
upstream commit in existing docs/PROJECT.md.

Use ONE monorepo, existing coding-harness sessions, four skills, ordinary GitHub
Actions, and Git. Do not build a custom controller, separate control repository,
GitHub App, immutable test store, permission enforcement, or agent swarm.
Restrictions on editing reviewed tests/workflows and append-only lessons are prompts.

Start read-only. Preserve existing product docs and sound tooling. Find usable
approved architecture; otherwise route to architecture intake. An empty repo needs
an owner-approved minimal project record before choosing a stack. Existing code is
evidence, not automatically the intended behavior. Repeated setup must not overwrite
working choices. Do not implement product features during setup.

Show the small setup plan and obtain approval. Adapt paths and instructions without
creating two live specs or overwriting the product README. Put LESSONS.md at the repo
root. Install the four skills in the selected harness's supported location, with
one canonical copy of each. Generate or reconcile the target repository's AGENTS.md
from templates/AGENTS.template.md and add a thin native bridge only when required.
Record actual launch and check commands. Record the source-to-installed mapping,
omissions, and local adaptations in docs/PROJECT.md. Carry VERSION, CHANGELOG.md,
and the package policy as references at mapped paths; adapt every relative reference.
Target Git records adapted instructions and approval. If changing the upstream base,
compare previous upstream, new upstream, and local instructions. Reconcile the entire
adopted package and migration notes, show the diff, and obtain approval before updating
its recorded upstream base. Do not silently overwrite adaptations or mix versions.

Infer languages/frameworks. Research suitable native formatting/lint/type/test tools.
Create or adapt ordinary CI and minimal test infrastructure as authorized setup work.
Prefer real end-to-end/public-entry-point tests, smaller tests only for useful gaps.
Retain 100% measured statement/branch coverage and report unsupported measurement.
Use GITHUB-SETUP.md; apply settings only with permission or give exact owner actions.

Implement delivery doctor as a thin invocation of review-work in doctor mode using
DOCTOR-PROMPT.md. No daemon or scheduled LLM loop. Default behavior writes an evidenced
spec/instruction patch on a docs branch, then waits for owner approval; --check only
reports. Doctor preserves upstream provenance and never bumps the official package
version; target Git records approved local changes. Obtain approval for and commit the
local policy before starting delivery. Each task pins an existing approved local policy
commit, not its own eventual hash. A/B receive permitted policy text from that revision
without implementation or history access. Active tasks retain their pinned rules.

Demonstrate fresh A/B, meaningful red tests and a committed test checkpoint, fresh C,
green checks, fresh D, and a normal PR. Add one honest lesson and demonstrate doctor
editing the spec. Label setup evidence honestly; do not fabricate independent sessions
or active protections. Preserve required source references once; do not make routine
agents reread the archive. Stop at the approved budget and report remaining gaps.
```
