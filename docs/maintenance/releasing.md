# Releasing

The repository uses Semantic Versioning for the Pact's published policy baseline.
The current version is recorded in [`VERSION`](../../VERSION), and the corresponding
release notes are recorded in [`CHANGELOG.md`](../../CHANGELOG.md).

## Version changes

- Patch: editorial corrections or source clarifications that do not change a control.
- Minor: additive guidance, examples, or a backward-compatible change to the baseline.
- Major: a changed or removed requirement, control, profile guarantee, or compatibility expectation.

Every release should update `VERSION`, add a matching `CHANGELOG.md` heading, identify
affected controls, and explain the rationale. A maintainer creates the Git tag and
GitHub release only after the pull request has been reviewed and the repository checks
have passed.
