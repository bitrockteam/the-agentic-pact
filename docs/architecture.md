# Architecture: delegation, writing, and integration

Controls C01, C02, C03, and C05. The prescriptions here are local policy; cited sources
describe experience or mechanisms, not universal consensus among vendors.

<a id="c01"></a>
## C01 — Delegation needs a verifiable benefit

**Policy.** Start with one agent or a deterministic workflow that is sufficient. Add
collaborators to separate context, expertise, or genuinely independent work. Before dispatch,
assign the objective, inputs, expected result, permissions, budget, and integration owner.
Measure quality, total cost, and end-to-end latency; subtask speed alone does not justify the
architecture.

Anthropic reports latency reductions for independent tasks and 3–10x token consumption in its
own experiments. These are not a ban on parallelism or a universal cost ratio. The verifier
also receives success criteria and tools. [F01](reference/sources.md#f01)

<a id="c02"></a>
## C02 — Ownership of state

**Policy.** Use one writer for each shared artifact or resource. Split writes only when
boundaries are disjoint, the contract is explicit, and reconciliation has one owner. This
applies to code, documents, memory, tickets, and remote state. Before integration, check
invariants, conflicts, and concurrent changes; where available, use expected versions or
preconditions instead of overwriting changed state.

Cognition describes a single writer with parallel analysis, and Anthropic describes separations
that are genuinely isolatable. This is a conservative local synthesis, not a normative ban on
every multi-writer system. [F01](reference/sources.md#f01), [F02](reference/sources.md#f02)

<a id="c03"></a>
## C03 — Two different reviews

**Policy.** Distinguish exploratory review from acceptance verification. The first inspects
artifact or diff with the context needed to find defects, without inheriting the producer's
justification. The second receives the artifact, approved requirements, explicit criteria, and
tools to check them.

One pass may cover both functions when evidence shows how. A clean context does not mean
ignoring requirements. Agreement between two models does not establish correctness. Record
evidence, limits, and rejected findings. [F01](reference/sources.md#f01),
[F02](reference/sources.md#f02)

<a id="c05"></a>
## C05 — The gate concerns the effect

For shared code, write on a dedicated branch, open a PR before integration, require checks on
the current result, and use an authorized human merge. This repository has one maintainer, so
no second approval is required; required checks remain mandatory. For other profiles, the gate
concerns the concrete action. See [operating profiles](profiles/operating-profiles.md).

| Local requirement | Evidence to inspect |
|---|---|
| Required PR and approvals | active branch rules and approval count |
| Review remains valid | stale-review behavior and dismissal permissions |
| Reliable checks | controlled SHA, expected app, jobs actually run, and skip handling |
| No ordinary bypass | bypass list and authorized exceptions |
| Human merge | effective permissions and refusal test or product guarantee |
| Protected rules | who can change rules and the workflow producing checks |

These are separate questions in GitHub. [F16](reference/sources.md#f16),
[F17](reference/sources.md#f17), [F18](reference/sources.md#f18),
[F19](reference/sources.md#f19), [F39](reference/sources.md#f39)

PR plus green CI does not prove human merge: the merge endpoint accepts installation tokens
with `Contents:write`. An empty bypass list does not make rules immutable. A satisfied check
does not prove validation ran because skipped and neutral outcomes differ. [F17](reference/sources.md#f17),
[F18](reference/sources.md#f18), [F19](reference/sources.md#f19)

If a product cannot separate writing from integration, do not invent a guarantee. Use an
independent boundary or mark the control unsatisfied and request an exception. Do not alter
authorship metadata to simulate separation. Copilot cloud-agent guarantees remain specific to
that product and configuration. [F20](reference/sources.md#f20)
