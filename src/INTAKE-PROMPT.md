# Intake prompt

Package version: [VERSION](VERSION). Use the `intake` skill. This prompt starts a conversation; it is not an authorization service.

```text
Use intake mode exploration, task, or architecture according to my intent.
First read the supplied context and relevant repository instructions.

When I want to experiment or build a prototype, enter exploration directly. State
the next useful experiment and proceed; ask only for input or authority needed for
that experiment. Product code and tests may evolve together without approved
architecture, a formal delivery contract, or A/B/C/D sessions. Existing repository
permissions, privacy, spending, publication rules, and my scope still apply.
Exploration does not authorize policy changes or publication. Keep choices tentative
and honor supplied budgets without requiring a formal intake interview first.

Keep a compact branch handoff in the task record: stable exploration ID, branch,
base/latest full commit references when available, threads actually visible,
uncommitted work, reproducible results, known defects, and next step. A commit is not
a prerequisite to exploring. Participating agents may observe at useful checkpoints
and record brief evidence-linked confirmed or hypothesis lessons under the existing
lesson guide. Identify the threads actually seen; zero lessons is valid. Observers
cannot approve requirements, change policy, or certify the prototype.

On requested prototype promotion, start fresh architecture/task intake. Inspect
and pin the prototype's full commit before formal delivery approval; record any
uncommitted reference as unresolved until frozen. Separate desired behavior from
observed choices, accidental behavior, and known bugs. Read back material choices to
preserve or reject, then use the normal authorization and risk route below. Either
implement from the integration baseline using the prototype as reference or harden
the prototype. Do not require a rewrite or manufacture failing tests to claim
test-first history; label regression and supplemental evidence honestly.

Before formal delivery, find an approved project
record. Reuse it, including architecture under another filename. If it is missing,
unapproved, or materially inconsistent, interview me about architecture first and
then resume the original task. Do not redesign unrelated parts or repeat answers.

Ask about material ambiguities, usually no more than three questions per turn.
Use contrasting examples. Follow up on vague or contradictory answers. Recommend
simple defaults and explain the consequences; do not assume I accepted them.
No speculative future questionnaire and no demand for every internal coding detail.

Architecture produces one short docs/PROJECT.md: outcome, constraints, stack,
components, public interfaces, verification and operation. A task produces one
behavior contract with stable requirement IDs, scenarios, non-goals and authorized
execution. A scenario is a distinct approved decision and observable outcome;
equivalent values may be coverage examples. Distinct rejection, interpretation,
output guarantees or boundary outcomes are separate scenarios. Start with roughly
five as a planning heuristic, approve a larger coherent contract once if needed,
and do not combine unrelated obligations to meet that heuristic. Extra equivalent
data within accepted behavior and budget do not need fresh approval.
For bugs, separate observation, expected behavior and unverified cause. Unknown
reproduction may need a bounded report-only investigation, not a speculative fix.

Select the route by risk, not changed-line count, and record its reason:
- Non-policy mechanical/documentation: one worker, reviewable deterministic diff,
  owner acceptance and any contract-required review; no changed executable
  behavior, dependencies, checks, permissions or policy.
- Bounded settled behavior or explicitly scoped infrastructure: one worker may
  inspect implementation and edit authorized product/tests/maintenance paths;
  a fresh independent reviewer checks oracle, behavior, gates, scope and candidate.
- High-risk product or uncertain meaning: initially fresh root A/B/C/D, blind A/B
  owning tests and product C retaining all restricted-file rules. Scientific/binary/
  custom oracles, permission/security authority and unsettled interfaces belong here.
- High-risk infrastructure: fresh blind A, fresh blind B, fresh root infrastructure
  author using existing implement-task in `infrastructure author` mode, then fresh D.
  A/B own tests; that author owns only the named infrastructure files/settings.
Mixed product/infrastructure work requires separately scoped fresh product C and
fresh infrastructure author. A/B and D cover the full behavior/authority contract;
D inherits neither author's conversation. Infrastructure authorization never relaxes
product C's restrictions; policy documentation retains its separate path.
Policy documentation uses a separate worker and fresh independent policy reviewer,
with explicit owner approval of the identified patch before downstream activation.
It cannot call itself mechanical or fabricate product-red evidence. Changed
tests/fixtures and dependency/workflow/gate maintenance need independent review
and their own authorized scope. Removed assertions need a reviewed obligation
mapping. Promote uncertain or mixed impact unless separately approved contracts
justify a split; a lower-tier failure does not authorize a new scientific repair.
Stop the bounded worker on promotion pending my explicit approval of the identified
high-risk contract, route, named infrastructure/settings ownership where applicable,
checks and budget. Do not merely switch the bounded worker to a different mode.

Before task approval, record an existing committed, owner-approved local delivery
policy revision, its full target Git commit, adopted policy paths, and the upstream
provenance reference as recorded at that revision. Do not use the task's eventual hash.
Keep that policy baseline through completion; newer rules do not silently replace it.

Read back the exact interpretation and Authorized execution once: tier/reason,
role route, named author/mode and owned files/settings, edit scope, prerequisite/
canonical checks, per-role model/effort and selection reason, local/CI gate mode,
escalation triggers, budget, review windows/caps and allowances. Choose configurations
for semantic/review complexity, using
applicable calibration; do not assume A/B need less capability than C. Missing
semantics return to intake, and model changes do not reset blindness or allowances.

A complete explicit instruction from me may itself authorize a mechanical or
bounded task. Record the actual instruction, scope, tier, checks, budget and inherited
constraints; send a concise read-back without asking for a redundant second yes.
High-risk contracts require explicit approval of the identified proposal, including
the route and named edit ownership. Policy changes require independent policy review
and explicit approval of the identified
patch before activation. Record my real response/reference and the document/commit
it covers. Never manufacture approval or infer it from silence. Material unanswered
questions, new scope or a new budget require an answer before dependent work.
Approved routine transitions, checks, unchanged-scenario redistribution and an
in-scope correction within remaining allowances need no repeat approval. Changed
behavior/interfaces/permissions/data sharing, tier downgrade, budget extension or
exhausted repair allowance need renewed approval. Approved in-flight rule migration
must preserve earlier windows, attempts, spending and repairs.

Use full canonical local verification of the exact submission candidate and all
required CI as the default, retaining 100% measured statement/branch coverage.
A CI-authoritative pilot for eligible settled mechanical/bounded work needs separate
specific policy approval plus verified native protection/trusted-source/complete
aggregate/integration/artifact prerequisites. It is not activated here; high-risk
work retains full local verification and execution/security authority changes are
ineligible for the pilot.
Cheap bounded interpreter/lock/install/isolation and actual
reviewer-launch prerequisites precede expensive dependent checks. Stop and diagnose
their failures instead of treating a configured name or unchanged path as proof.

Record approved per-window review caps. Every completed correction review consumes
a round. After two nonacceptances, stop and diagnose; another attempt needs a bounded
diagnosed correction under the approved path within remaining allowances. Default:
one task-wide implementation repair. New sessions/windows or narrower reviews never
reset spending or repairs. Authorized A/C may continue their own correction session
while scope and A's blindness hold; B/D verdicts remain fresh and independent.
Infrastructure-author repair requires a fresh infrastructure author and fresh D
within that same task-wide repair allowance; the A/C continuation exception does
not extend to infrastructure author.

No code or executable test suite during architecture/task intake. Stop formal
preparation on an unanswered material question or its budget. No additional
interviewing agents.

Prepare behavior/public-interface inputs and role-permitted policy text from the
pinned revision for A/B, excluding this conversation, prototype internals,
exploration notes, and implementation ideas. Supply the
snapshot without requiring implementation or history access. The package LESSONS.md
guide is installed as root LESSONS/README.md; A/B may read it and the approved packet,
never LESSONS/ entries, broad documentation trees or implementation-bearing status.
The authorized product worker/C may receive the pinned prototype reference; a
separately authorized infrastructure author receives only relevant references
within its named scope. Expected results still need independent justification.
Maintain one concise Current state and linked evidence/metrics in the task. Preserve
applicable accepted reports, rerun invalidated evidence, and record missing metering
as unknown rather than zero. Do not create a controller or evidence database.
Start with what is already known and the highest-impact unanswered question.
```

Append the request, sources, and existing budget/context. A complete brief may need only a final clarification/read-back rather than a long interview.
