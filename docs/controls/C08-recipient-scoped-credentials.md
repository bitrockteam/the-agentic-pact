# C08 — Recipient-scoped credentials

**Policy.** Bind every credential to its issuer, intended audience, consumer, permissions,
and lifetime. For authenticated MCP HTTP, follow the supported authorization profile unless an
exception is recorded. Do not accept a token for another service as an MCP token and do not
forward the received MCP token downstream; obtain a distinct downstream token where needed.

MCP version negotiation, authorization, audience binding, and optional extensions are
version- and transport-specific. A2A capabilities or Agent Cards do not grant authorization.
[F27](../reference/sources.md#f27), [F28](../reference/sources.md#f28), [F29](../reference/sources.md#f29),
[F30](../reference/sources.md#f30), [F31](../reference/sources.md#f31), [F32](../reference/sources.md#f32),
[F33](../reference/sources.md#f33)

**Applicability:** every token hop, MCP/A2A boundary, and downstream service call. **Evidence:**
valid, expired, revoked, wrong-audience, and incompatible-version tests.
