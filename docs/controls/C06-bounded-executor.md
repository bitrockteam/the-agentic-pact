# C06 — Bounded executor

**Policy.** Free-running reasoning or arbitrary code must not receive administrator shells,
production keys, or direct production access. A separate executor exposes typed operations
and validates identity, arguments, resource, recipient, consent, and limits before the effect.
A folder or router is not a boundary if the same process can recover credentials and call the
service directly.

Live modification or publication is allowed only through an authorized D or A profile. A
credentialed generic shell does not become bounded because it is called `deploy`. Least
functionality and application authorization are supported by [F03](../reference/sources.md#f03)
and [F05](../reference/sources.md#f05); the exact executor boundary is local policy.

**Applicability:** every privileged or live-system effect. **Evidence:** typed interface,
independent enforcement, bounded permissions, uncertain-result handling, stop, and recovery.
