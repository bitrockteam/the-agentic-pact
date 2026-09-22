# C09 — Secrets outside free execution

**Policy.** Keep credentials in a connector, broker, or bounded executor that authorizes the
operation. The model and arbitrary code it can run must not read them. Inspect files, mounts,
inherited environment, processes, caches, logs, diagnostics, and debug channels, not only a
variable name.

Provider documentation about setup-time secret removal is not proof that every copy or
indirect path is inaccessible. Research on environment filtering shows why neighboring
processes matter. [F22](../reference/sources.md#f22), [F25](../reference/sources.md#f25)
MCP stdio credential delivery does not waive local isolation. [F28](../reference/sources.md#f28)

**Applicability:** any workflow that can reach a secret or privileged service. **Evidence:**
access inventory, process/file/cache inspection, least privilege, expiry/revocation tests, and
absence of secret values from logs and artifacts.
