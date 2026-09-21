# Contributing

Contributions should make the Pact easier to apply and harder to misinterpret.

## Before opening a change

- identify the control or section affected;
- state whether the change is editorial, source-backed, or a policy change;
- explain the expected benefit and any new trade-off;
- remove personal, client-confidential, credential, and environment-specific details;
- preserve the distinction between a requirement, a recommendation, and an inference.

## Review expectations

For an external contribution, the author must not be the only person accepting it.
Reviewers should receive the proposed text, its rationale, relevant sources, and explicit
acceptance criteria. They should be able to reject the change when the evidence does not
support it. The sole maintainer may merge their own maintenance PR after the required
checks pass; a second maintainer approval is not required.

Changes that affect a gate, permission, credential, secret boundary, external destination,
or audit claim require an additional review of the practical failure mode and the evidence
needed to test it.

## Versioning

For a material change, update [`VERSION`](VERSION) and add a matching entry to
[`CHANGELOG.md`](CHANGELOG.md). Use the rules in [`docs/maintenance/releasing.md`](docs/maintenance/releasing.md)
to choose the version increment. Pull requests should be focused and leave a clear
acceptance criterion for the maintainer.

The `main` branch is maintainer-controlled. Bit Rock contributors can collaborate through
branches and pull requests; external contributors should work from a fork and submit a
pull request. Required checks must pass before integration. The repository intentionally
does not require a second approval, so the sole maintainer can merge independently. See
[`docs/maintenance/branching-strategy.md`](docs/maintenance/branching-strategy.md)
for branch names and the pull request flow.
