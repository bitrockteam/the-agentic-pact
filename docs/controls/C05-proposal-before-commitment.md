# C05 — Proposal before commitment

**Policy.** Separate a proposal from its external effect. For shared code, use a branch, PR,
required checks, and an authorized human merge. This repository has one maintainer, so a
second approval is not required; required checks and PR flow remain mandatory. For data,
messages, deployments, and other effects, approve the actual content and recipient rather
than manufacturing a PR-shaped artifact.

GitHub documents separate rules for PRs, status checks, approvals, rule administration, and
merge permissions. An empty bypass list does not make rules immutable, and green CI does not
prove that a required job ran. [F16](../reference/sources.md#f16), [F17](../reference/sources.md#f17),
[F18](../reference/sources.md#f18), [F19](../reference/sources.md#f19)

**Applicability:** any change or effect with external, shared, irreversible, financial,
privacy, or administrative impact. **Evidence:** active rule, current-SHA checks, approval or
authorized decision, actual artifact/recipient, and merge principal.
