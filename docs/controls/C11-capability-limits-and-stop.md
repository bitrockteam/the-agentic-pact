# C11 — Capability limits and stop

**Policy.** Use a sandbox without administrator privileges, bounded filesystem and network
destinations, finite time/cost/volume/retry budgets, explicit stop and revocation, and a
versioned tool profile. A stated but unenforced limit is unknown or unsatisfied.

Sandbox and approval are separate layers. Do not use flags that disable confirmations outside
the sandbox. Do not blindly retry an uncertain effect without idempotency or reconciliation.
Version components and workflows, protect their changes, and verify immutable references,
signatures, or attestations without treating them as proof of safe content. [F04](../reference/sources.md#f04),
[F24](../reference/sources.md#f24), [F39](../reference/sources.md#f39)

Public incident evidence reinforces separating injection, token theft, supply chain, and agent
use rather than collapsing them into one story. [F23](../reference/sources.md#f23)

**Applicability:** all autonomous or privileged execution. **Evidence:** enforced quotas,
negative over-limit tests, stop/revoke tests, dependency provenance, and recovery behavior.
