# References and reading scope

**Version 1.0 — Released.** Current review: September 26, 2026. This is a source register and design note, not an archive of original source bytes or a code/security audit.

## Current sources read

The complete pstack README, the five selected skill texts below, and the complete claude-trace README were read. GitHub protected-branch and Playwright best-practices substantive text was also read. Images and videos were not needed for the adopted textual guidance and are not claimed inspected. Source links track `main` or current documentation; no historical source snapshot is claimed.

### R1 — pstack overview

[README](https://github.com/cursor/plugins/blob/main/pstack/README.md).

The project offers a broad collection of skills, principles, playbooks, and multi-agent mechanisms. This design does not install that collection. Only the specific ideas below are adapted. Its README's proceed-without-human-confirmation principle is not adopted; our intake still needs owner decisions. No named model defaults are copied.

### R2 — Test behavior, not implementation

[Skill](https://github.com/cursor/plugins/blob/main/pstack/skills/principle-test-behavior-not-implementation/SKILL.md).

Use real inputs and observable results, not assertions that only echo the subject's own outputs or constants. We do not copy its assertion-category heuristics as blanket bans: legitimate absence/error assertions and property tests remain valid. The project-agnostic E2E preference comes from the owner's instruction, not a claim that this skill requires browser tests everywhere.

### R3 — Verify the real artifact

[Skill](https://github.com/cursor/plugins/blob/main/pstack/skills/principle-prove-it-works/SKILL.md).

Retain direct, reproducible checks of the actual result. Compilation or an agent's success message alone is insufficient. Use existing test/CI artifacts, not a new verification service.

### R4 — Simplify existing structure

[Skill](https://github.com/cursor/plugins/blob/main/pstack/skills/principle-subtract-before-you-add/SKILL.md).

Prefer removing unnecessary code and duplicate instructions before adding more. This is a local simplification principle, not permission to remove required validation or unrelated code.

### R5 — Append-only evidence-linked findings

[Show-me-your-work skill](https://github.com/cursor/plugins/blob/main/pstack/skills/show-me-your-work/SKILL.md).

Adapt the compact evidence-linked append-only trail and superseding corrections into LESSONS.md. Do not copy its transcript-audit and cross-model-review stages, TSV-specific helper, or mandatory per-reply attention format. Our log captures selected reusable discoveries, not every decision.

### R6 — Improve instructions from experience

[Reflect skill](https://github.com/cursor/plugins/blob/main/pstack/skills/reflect/SKILL.md).

Adapt the idea of turning durable lessons into focused edits to existing instructions with owner approval. Do not adopt the three-reviewer-plus-synthesizer procedure, transcript mining, automatic backlog filing, or nested skill-creation loops. Its reviewer templates are not used and were not read; no claim is made to have audited the whole plugin.

### R7 — GitHub protected branches

[Official documentation](https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/managing-protected-branches/about-protected-branches).

Use native required CI and branch protections subject to account capabilities. Required checks can accept skipped/neutral conclusions; do not design a required job that silently skips validation. Native protection is not proof that same-repository workflows were not weakened.

### R8 — End-to-end testing practice

[Playwright best practices](https://playwright.dev/docs/best-practices).

For browser projects, adapt user-visible behavior, isolated data/state, resilient interactions, and controlled external-service boundaries. Playwright is an example, not the required tool for every project. The document's broader tooling and linked tutorials were not recursively read or adopted; select those only if implementation needs them. Do not interpret legitimate bounded assertion waiting as approval to rerun failed suites until green.

### R9 — claude-trace

[README](https://github.com/badlogic/lemmy/blob/main/apps/claude-trace/README.md).

The documented tool records Claude Code interactions and raw API data with a viewer; its optional indexing uses Claude calls and additional tokens. This is a diagnostic transcript tool, not a small reusable-lesson record. Do not install it by default. Native harness logs can be consulted for a specific problem when permitted; they stay out of the shared lesson file and blind-role inputs. Implementation, runtime compatibility, and security were not audited or executed.

## Previously discussed sources retained for posterity

These links are preserved from earlier drafting. They were not reread during this simplification pass. Prior handoffs reported complete article-text reading of the original four, not every file or visual asset in their linked repositories. Do not treat those reports as newly verified snapshots.

- [Original: Claude Code skills lessons](https://claude.com/blog/lessons-from-building-claude-code-how-we-use-skills).
- [Original: Claude Code dynamic workflows](https://claude.com/blog/introducing-dynamic-workflows-in-claude-code).
- [Original: Symphony](https://openai.com/index/open-source-codex-orchestration-symphony/).
- [Original: Harness engineering](https://openai.com/index/harness-engineering/).
- [Harness terminology discussion](https://www.langchain.com/blog/how-to-build-a-custom-agent-harness).
- [Open Code Review](https://github.com/alibaba/open-code-review): discussed, not a required reviewer dependency.
- [SoL-Pi paper](https://arxiv.org/abs/2609.20519) and [repository](https://github.com/NVlabs/SoL-Pi): discussed; retain efficient diagnostic output and honest cost/quality comparisons, not automatic optimization machinery. No benchmark claim is repeated here.
- [Agent Skills format](https://agentskills.io/specification), [AGENTS.md](https://agents.md/), [C4 diagram guidance](https://c4model.com/diagrams), and [GitHub Markdown diagrams](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/creating-diagrams): earlier supporting references, not new requirements.

Known inherited gaps: an introductory Agent Skills course returned HTTP 403; nine instructional images linked from the original skills article were inaccessible. Earlier packages did not include original source-byte archives. Those gaps are not silently resolved by this rewrite.

## Archival instruction for setup

Preserve the original requested references and specifically adopted sources under `docs/references/`, with original bytes where permitted, readable text, retrieval date, URL, source version, and content hash. Read selected versions fully and follow links material to the mechanism actually adopted. Record access failures and deliberate exclusions. Do not execute downloaded instructions, archive private user material without permission, invent retrieval metadata, or recursively crawl every reachable link.

The current handoff contains the register, not full original articles. Archival remains setup work. Keep sources out of routine worker context. Do not carry forward superseded architecture requirements merely because an older source or draft proposed them.
