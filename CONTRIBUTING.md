# Contributing

Contributions should make the Pact easier to apply and harder to misinterpret.

## Before opening a change

- identify the control or section affected;
- state whether the change is editorial, source-backed, or a policy change;
- explain the expected benefit and any new trade-off;
- remove personal, client-confidential, credential, and environment-specific details;
- preserve the distinction between a requirement, a recommendation, and an inference.

## Review expectations

The author of a change must not be the only person accepting it. Reviewers should receive
the proposed text, its rationale, relevant sources, and explicit acceptance criteria.
They should be able to reject the change when the evidence does not support it.

Changes that affect a gate, permission, credential, secret boundary, external destination,
or audit claim require an additional review of the practical failure mode and the evidence
needed to test it.
