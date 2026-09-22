# C01 — Justified complexity

**Policy.** Start with the simplest workflow that can meet the requirement. Add agents or
delegation only to separate context, expertise, or genuinely independent work. Before
dispatch, record objective, inputs, output, permissions, budget, and integration owner.
Measure quality, total cost, and end-to-end latency.

Anthropic reports latency benefits for independent work and 3–10x token consumption in its
own trials. Cognition reports single-writer and independent-review patterns. These observations
inform the policy; they are not universal multipliers or a requirement to use multi-agent
systems. [F01](../reference/sources.md#f01), [F02](../reference/sources.md#f02)

**Applicability:** any delegated, parallel, or multi-agent workflow. **Evidence:** compare
against a simpler design and record measured benefit, cost, and unresolved trade-offs.
