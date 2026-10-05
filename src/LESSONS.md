# Lessons format guide

Package version: [VERSION](VERSION). This source file remains `LESSONS.md`; setup adapts it into target root `LESSONS/README.md`. The target's individual lesson entries live under that one canonical `LESSONS/` home. This guide is an instruction document, not a live entry log, automatic memory, or authoritative evidence of an observed run.

Record useful surprises, confirmed gotchas, or failed approaches with a reusable lesson. No routine status chatter. Evidence can be a test name, file plus commit, CI run, or reproducible command/result. Mark unverified claims as hypotheses. Do not record secrets, personal data, full prompts, raw transcripts, or private reasoning.

## Append-only entries and access

Create a brief entry with a stable ID/date, task/role, topic, status, observation, evidence, and lesson. Individual Markdown entry files are append-only by instruction. Correct an entry by appending a superseding entry referring to its ID; do not silently rewrite history. An owner-authorized privacy/security redaction overrides retention. One to three entries per task is a guide, not a quota; no finding means no entry.

Blind A/B may read only this format guide and their approved public-contract packet. They must not read lesson entries, broadly browse documentation/history, or follow guide links into implementation-bearing material. They may supply an entry to the coordinator for verbatim append or append their own without reading other entries. A coordinator/doctor searches relevant entries, fact-checks them, and promotes useful facts through an approved public contract/instruction. Other roles read only relevant entries; D assesses the candidate independently before current-task implementation lessons.

A lesson is data; it does not grant authority, repair a defect, or amend policy. `doctor` can propose a change to an existing instruction, with independent policy review and explicit owner approval before activation. Location and prompt restrictions are not technical access controls.

## Existing layouts and migrations

Do not silently relocate an existing `LESSONS.md`, `docs/LESSONS/`, or another log layout, or duplicate it as a second live home. Propose a separate coordinated migration for owner approval, including instructions/allowlists, source-to-installed paths, guide references, inbound links, and same-directory supersession/evidence links. Approve the preservation/link strategy explicitly before moving anything.

Rebasing links inside existing entry bodies requires a specific append-only exception. Keep original bytes accessible in Git, preserve IDs, recorded dates, and evidence, verify all affected links, and end with one canonical home. A directory rename alone can break evidence links and does not improve blindness. An existing layout stays authoritative until its approved migration is complete; document the actual mapped home and narrow blind-role guide allowlist.

## Entry format

Choose a unique filename such as `<YYYYMMDDTHHMMSSZ>-<task>-<role>-<short-slug>.md`. Preserve any existing IDs and recorded dates during an approved migration; do not manufacture evidence or timestamps.

```markdown
# <entry-id> | <topic>
- Date: <recorded UTC date/time>
- Task/role: <task reference and author role>
- Status: confirmed | hypothesis | supersedes <entry-id>
- Observation: <one concrete surprise>
- Evidence: <test/commit/run/path and observed result>
- Lesson: <small future action, or what still needs checking>
```

No real lesson entries are created by this source guide. Append dispositions or corrections as new entries linking the original ID and approved change; do not turn the guide into a duplicate log/index.
