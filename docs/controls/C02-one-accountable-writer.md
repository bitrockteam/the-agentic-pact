# C02 — One accountable writer for each shared state

Do not allow concurrent writers to the same artifact or state without explicit ownership,
disjoint boundaries, and a reconciliation process with one accountable owner.

This applies to code, documents, memory, tickets, databases, and remote state. Before
integration, check invariants, conflicts, and concurrent modifications. Prefer version
preconditions or equivalent safeguards over blind overwrites.
