# C09 — Secrets outside unconstrained execution

Keep secrets in the smallest isolated component that needs them. The boundary must include
files, processes, caches, temporary data, error messages, and logs.

If the boundary cannot be enforced, document the exposure and stop before using the secret.
Do not rely on prompt instructions, model behavior, or an unverified claim that a secret
was not exposed.
