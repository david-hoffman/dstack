# Project

Package version: [VERSION](../VERSION). Release policy: [package versioning](../README.md#package-versioning). Replace this template with real decisions; placeholders do not establish approval.

## Purpose and non-goals
Who uses it, the first useful outcome, and what is out of scope.

## Constraints
Deployment, integrations, data/access, compatibility, operational needs, budget, and unresolved material questions.

## Stack and structure
Detected versus proposed choices, evidence, responsibilities, and public boundaries. Keep few components. Link existing architecture rather than duplicating it. Optional diagram only when useful.

## Public interfaces
Link canonical schemas/contracts. Distinguish current state from proposed changes.

## Verify and operate
Canonical build/lint/type/test/E2E/coverage commands, supported targets, dependency-lock identity, installation and test data setup, report locations, and recovery/release instructions. Record cheap bounded prerequisites: actual interpreter/platform, install/import health, required isolated/nested environments, and actual reviewer launch/authentication/connectivity. Stop expensive dependent checks on failure; an unchanged environment path is not perpetual proof of health.

Record the actual native fresh-root session, terminal wait/notification, and doctor invocations, available models/supported effort settings, and relevant public/synthetic calibration evidence. Do not invent tools or assume a configured reviewer can launch. Bounded waits need timeout/failure handling; new helpers, shards, or host setup require their own authorized infrastructure scope and independent review.

Record the actual exploration/intake and prototype-promotion entry points. Exploration may use provisional choices before this architecture record is approved; formal delivery returns to approved project/task records and the applicable tier/gate.

Link task Authorized execution records naming each author/mode and owned files/settings. High-risk infrastructure uses fresh blind A/B, a fresh root infrastructure author in the existing `implement-task` skill's `infrastructure author` mode, and fresh D; A/B own tests and that author owns only named infrastructure/settings. Mixed product/infrastructure work uses separately scoped fresh product C and fresh infrastructure author, with A/B and D covering the full behavior/authority contract and D inheriting neither conversation. Product C's restricted files remain absolute; policy documentation retains its separate worker/reviewer/patch-approval path. Promotion stops a bounded worker pending explicit owner approval of the identified high-risk contract, route, named infrastructure/settings ownership, checks, and budget. Infrastructure-author repair requires a fresh infrastructure author and fresh D within the same task-wide repair allowance; no author-session continuation exception applies to that mode.

Coverage policy and actual owner approval: behavior coverage with risk review; optionally add line, statement, branch, or combined measured targets. Record the choice and reason after explaining the tradeoffs under [specification section 5.1](../DELIVERY-SYSTEM-SPEC.md#51-agree-on-coverage-before-writing-tests). Behavior coverage is the recommendation for ordinary application work, not an assumed approval. For selected metrics, record the exact tool/command, threshold (100% is a valid choice), runtime/package/platform scope, aggregation, exclusions, and reporting limits. Lines and statements are distinct. The default measurement scope is instrumentable owned runtime globally and per package on each required platform, including never-imported files and relevant subprocesses/server/browser code. An approved narrower scope must be explicit. Mark unselected measurements advisory or unused. Tasks inherit this policy and add their relevant risks; do not repeat a settled interview or silently replace an installed gate.

Default submission gate: full canonical local checks for the exact candidate plus every required CI platform, satisfying the approved behavior/risk obligations and any selected measured targets. Disclose exclusions and unsupported measurement; missing required measurement remains a gap. Link evidence conventions covering revision/test/lock/environment/base and generated version/artifact inputs, including material ignored inputs. A gate change requires the policy amendment and any active-task migration in section 5.1, preserving spent allowances.

An optional CI-authoritative pilot for eligible settled mechanical/bounded work is a separate policy decision, requiring specific owner approval and read-only verification of effective native protections, trusted check sources, fail-closed complete platform/shard/report aggregation, bypass settings, and exact integration/artifact/version proof. High-risk work retains full local verification; execution/security authority changes are ineligible for the pilot. Record the identified approval and prerequisite evidence only if obtained. Unknown or ineffective controls retain the default; this project record does not activate the pilot or delegate merge/release authority.

## Delivery package provenance
Source repository; single package version; immutable release tag when published; full upstream commit before adaptations. Explicit owner choice for an unpublished/development snapshot; do not call it published. Link the adopted VERSION, changelog, and package policy reference at their installed paths. Record source-to-installed paths, omissions, and local adaptations, including reconciled existing instructions. Target Git records local policy revisions and owner approval. On upgrade, compare previous upstream, new upstream, and local instructions; reconcile the entire adopted package and migration notes before updating this base record.

Record the canonical target lesson home as root `LESSONS/`, with `LESSONS/README.md` mapped from the package's `LESSONS.md` guide. A/B may read the guide and their approved public packet, never entries or broad documentation trees. Existing-log relocation or append-only entry changes need a separate approved migration and preservation/link strategy; this record performs no migration.

## Approval and next slice
Reference the owner's actual approval of the identified record. List remaining decisions and the smallest next task. Architecture approval is not task approval.

Tasks pin an existing committed, owner-approved local policy revision and remain on it through completion. Policy adoption needs fresh independent policy review and explicit owner approval of the identified patch before activation. An explicitly approved in-flight migration preserves earlier attempts, review windows, spending, and repairs.
