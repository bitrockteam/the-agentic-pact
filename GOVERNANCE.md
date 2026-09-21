# Governance

The Agentic Pact is authored and maintained by Franco Geraci (Voloire).

## Changes

Changes to a control, operating profile, approval gate, or evidence requirement must:

- explain the problem or new evidence;
- identify the affected controls;
- distinguish policy changes from editorial corrections;
- include updated examples or acceptance criteria where needed;
- be reviewed independently of the author of the change;
- record the resulting version and rationale.

Research notes may inform a change, but they do not become policy automatically.
Vendor guidance and protocol requirements must retain their scope and version. A local
policy must be labelled as a local policy rather than attributed to an external source.

## Publication stages

The repository may be private while the structure and wording are being tested. Promotion
to a public repository is a separate decision. Before publication, review the complete
history, issue tracker, generated artifacts, examples, links, and repository settings for
personal or confidential information.

The repository is a curated publication of the Pact, not a mirror of a private research
repository. Content is promoted deliberately after sanitisation and review.

## Main branch protection

The `main` branch is protected. Changes must arrive through a pull request, pass the
required repository checks, and be merged by the maintainer represented by `@Voloire` in
[`CODEOWNERS`](.github/CODEOWNERS). A second approval is intentionally not required while
the maintainer is the only maintainer, so the maintainer can merge their own PR. Contributors
within Bit Rock can propose changes from company branches, and external contributors can
propose changes from forks. Force-pushes and branch deletion are not part of the normal
workflow.
