# Package changelog

Current candidate: [VERSION](VERSION). Rules: [package versioning](README.md#package-versioning). Entries describe the package as a whole; publication requires the matching tag and GitHub Release.

## Unreleased

### Changes

- Introduce one package version, compatibility rules, development/preview/release states, and a manual release checklist.
- Replace fixed release banners and independent skill version metadata with package references.
- Record upstream provenance, installed paths, local adaptations, and the policy revision used by each downstream task.
- Define upgrades that reconcile the upstream package with local changes, while keeping active tasks on their approved rules.

### Compatibility and migration

This prepares the first tagged release. On 2026-10-02, local and `origin` tag listings and the GitHub release list contained no releases. The earlier `1.0 — Released` labels did not identify a tagged package. The pre-policy repository baseline is commit `713621636ac68493e563a61d1f446970729a4e08`; this is a historical source reference, not a release tag. Recheck remote history before publication.

For an existing copy of the earlier documents, reconcile the complete adopted package, replace fixed banners with references, and record the actual upstream source and local changes in the project record. New tasks must identify their committed approved local policy revision. Preserve historical task records and active approvals. If an old copy's exact source cannot be established, record unknown provenance and obtain owner acceptance before treating the reconciliation as an unverified migration; never invent a source commit.

No stable version or release date is claimed here. Later releases must classify these kinds of new downstream obligations as breaking changes against their established stable contract.
