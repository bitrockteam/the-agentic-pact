# C08 — Credentials scoped to the intended recipient

Verify the issuer, intended recipient or audience, scope, and validity of every credential
used by a workflow. A credential accepted by one service must not be forwarded as an
unexamined credential for another service.

Separate incoming authentication from credentials issued to downstream services. Token
passthrough is not an acceptable substitute for explicit audience and scope validation.
