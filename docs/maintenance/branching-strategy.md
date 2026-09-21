# Branching strategy

The Pact uses a lightweight trunk-based workflow suitable for a company-owned
blueprint repository.

## Branches

- `main` is the only long-lived branch and must remain releasable.
- Contributors use short-lived branches named for the change, such as
  `docs/c05-approval-gate`, `fix/ambiguous-wording`, or `feat/release-metadata`.
- External contributors should create those branches in a fork and open a pull request.
- `hotfix/*` is reserved for urgent corrections and still merges through the normal
  pull request gate.

Do not create a permanent `develop` branch unless the repository later adopts a
separate release-train cadence. Tags such as `v0.1.0` identify releases from `main`.

## Pull request flow

1. Start from an up-to-date `main`.
2. Keep one coherent change per branch and pull request.
3. Rebase or update the branch when `main` moves, then run the checks locally.
4. Open a pull request that names the affected controls, rationale, and acceptance criteria.
5. Wait for the required checks and maintainer review.
6. The maintainer merges the pull request; the branch can then be deleted.
