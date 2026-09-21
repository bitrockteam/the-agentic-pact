# Promotion workflow

The Agentic Pact may be developed from a private research baseline, but the team
repository is a curated artifact. It must never be an automatic mirror of a private
repository.

## Before promotion

1. Identify the source change and the Pact sections it affects.
2. Copy only the approved, generic content into a clean working branch.
3. Remove personal names, private instructions, local paths, host details, network data,
   credentials, client information, private memory, and environment-specific assumptions.
4. Rewrite personal decisions as general policy, or exclude them if they are not needed by
   the Pact.
5. Check links, source scope, attribution, examples, generated files, and Git history.
6. Run the documentation checks and obtain an independent review.
7. Merge only after the diff and the effective repository contents are both reviewed.

## What is not synchronised

Do not synchronise private notes, private task instructions, personal operating rules,
machine or network documentation, account details, credentials, client material, private
derogations, or the source repository's history.

## Versioning

Every material policy change should update the changelog and explain the affected controls.
A source update is not automatically a policy update. A policy change requires an explicit
decision and review.
