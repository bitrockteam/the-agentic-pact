# C07 — Identity and delegation

**Policy.** Distinguish delegating user, authenticated application, workload principal, and
operation. For D, use traceable user delegation with explicit scope. For A, use a dedicated
or federated workload identity and temporary credentials where supported. Never put a personal
PAT or equivalent broad credential in free-running execution.

OAuth, impersonation, refresh-token protection, NHI classifications, and GitHub installation
tokens have different scopes. A short access-token lifetime does not shorten a renewable grant;
an author name or signature does not prove the push principal or approval. [F08](../reference/sources.md#f08),
[F09](../reference/sources.md#f09), [F10](../reference/sources.md#f10), [F11](../reference/sources.md#f11),
[F12](../reference/sources.md#f12), [F13](../reference/sources.md#f13), [F14](../reference/sources.md#f14),
[F15](../reference/sources.md#f15)

**Applicability:** every privileged connector, tool, trigger, and delegated action. **Evidence:**
effective principal, scope, lifetime, renewal, revocation, owner, and delegation record.
