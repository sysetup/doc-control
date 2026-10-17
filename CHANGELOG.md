# Changelog

Meaningful changes to the SYSETUP document-control templates and repository documentation, covering repository initialization, the proposal-catalog relocation, and subsequent documentation corrections.

## Unreleased

No tagged releases or versioning policy are established in this repository. The entries below describe repository changes awaiting a named release.

### Added

- Empty Markdown index templates for approved operational documents and proposals, with matching fields for scope, ownership, and edition.
- [Setup and usage guidance](README.md) for host and workspace catalogs, the draft–publish–consult workflow, and separately supplied `doc-specs`, `doc-set`, and `doc-get` resources.
- [Contribution guide](CONTRIBUTING.md) covering focused changes, schema compatibility, Markdown validation, and protection of sensitive information in public contributions.
- [MIT license](LICENSE).
- This changelog for tracking meaningful changes without reproducing the commit log.

### Changed

- Moved the proposal catalog from `.agents/doc-operations/pull-request/` to `.agents/doc-requests/` (`8f01aede`), separating proposals from approved documentation. Existing installations must migrate their proposal catalog as described in [Usage](README.md#usage).

### Removed

- Removed the `Authoring contract, specification used` column from both index templates and its requirements from repository guidance.

### Fixed

- Corrected setup instructions to install both catalogs and documented migration for existing installations.
- Aligned the README directory list with the `doc-set` hierarchy (`00-governance/` through `04-control/`).

## Sources and coverage

The initial templates, README, and license come from commit `5ce93e5`; the contribution guide comes from `8bfec8e`, and this changelog was introduced in `2f66633`. These commits are dated 2026-10-12. Commit `8f01aede`, dated 2026-10-15, moved the proposal catalog to `doc-requests/` and updated the workflow references. The setup, migration, and directory-list corrections are documented in the current [README](README.md). Dates identify commits, not releases; entries do not establish publication, approval, or deployment.
