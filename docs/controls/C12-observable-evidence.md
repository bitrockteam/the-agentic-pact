# C12 — Observable evidence

**Policy.** Record requests, identity, delegation, permissions, approvals, actual effects,
refusals, results, and policy version with correlation IDs. The executor must not be able to
rewrite or delete its own trace. A file opened in append mode is insufficient if the executor
can replace it; use a separate collector or suitable protected storage.

OWASP logging guidance informs event attributes, exclusions, verification, and protection, but
the Pact's fail-closed behavior for unlogged high-impact effects is local policy. [F06](../reference/sources.md#f06)
MCP logging conformance does not guarantee durable persistence. [F37](../reference/sources.md#f37)
Git author, signature, push principal, and approver remain distinct evidence fields. [F14](../reference/sources.md#f14),
[F15](../reference/sources.md#f15)

**Applicability:** every privileged action, shared write, output, refusal, and policy change.
**Evidence:** searchable event, protected retention, effect correlation, emission test, and
failure/uncertain-result handling. Classify findings as verified, partial, unsatisfied,
unknown, or not applicable.
