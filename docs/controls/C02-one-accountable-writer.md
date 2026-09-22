# C02 — One accountable writer

**Policy.** One writer owns each artifact or shared resource. Parallel work is allowed only
when write boundaries are disjoint, the contract is explicit, and reconciliation has a named
owner. This includes code, documents, memory, tickets, and remote state.

Before integration, check invariants, concurrent changes, and conflicts. Prefer expected
versions or preconditions to overwriting state that changed. The policy is a conservative
local synthesis of the single-writer and separable-work patterns in [F01](../reference/sources.md#f01)
and [F02](../reference/sources.md#f02), not a universal claim that multi-writer systems are
always invalid.

**Applicability:** every shared artifact or mutable resource. **Evidence:** ownership map,
write boundary, reconciliation result, and conflict test.
