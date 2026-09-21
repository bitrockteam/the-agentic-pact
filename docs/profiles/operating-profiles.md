# Operating profiles

Profiles choose how the twelve controls are applied. They do not remove controls.

| Profile | Permitted effect | Required gate |
|---|---|---|
| L — Reading and analysis | Read within the assigned boundary and create local artifacts | Authorised assignment and bounded access; no implicit external send |
| C — Shared development | Modify a branch or proposed shared artifact | Required checks, independent review, and authorised integration |
| D — Supervised delegated action | Perform an explicitly specified operation | Human request covering object, content, destination, and effect |
| A — Bounded automation | Perform operations covered by an approved contract | Pre-authorised trigger, scope, limits, duration, identity, and stop path |

Moving from analysis to sending, from proposal to publication, or from supervision to
autonomy is a new authorization decision. A credential that can technically write does not
by itself authorize a write.

## Minimum contract for D and A

Before enabling a delegated or automated action, record the responsible party, requester,
principal, allowed resources and operations, destinations, data classification, trigger,
expiry, budgets, concurrency, approval conditions, blocking conditions, credentials,
retry semantics, audit, stop, recovery, and evidence to be produced.
