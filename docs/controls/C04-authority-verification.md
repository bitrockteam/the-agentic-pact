# C04 — Authority verified at entry and action

Authenticate the requester, determine what that requester may ask for, and revalidate the
authorization when an operation is executed. A known bot, terminal, session, or identity
does not receive implicit privileges.

The check must cover the actual object, operation, scope, destination, and current state.
Alternative execution paths and retries must not bypass the authorization decision.
