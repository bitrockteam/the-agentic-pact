# C04 — Authority verification

**Policy.** Verify identity and permission at entry, then revalidate resource, arguments,
recipient, delegation, and limits immediately before the effect. Deny by default. Apply the
same boundary to CLI, API, UI, scheduled, and agent-to-agent paths.

Authentication is not authorization, and a message claiming authority does not prove it.
OWASP supports deny-by-default and checking permissions on every request. [F05](../reference/sources.md#f05)
GitHub's agent behavior is product-specific and cannot be generalized to every bot. [F20](../reference/sources.md#f20)

**Applicability:** all effects beyond local analysis, including reads of protected resources.
**Evidence:** identity, permission decision, resource/argument checks, refusal tests, and
revocation or expiry behavior.
