# Identity, delegation, triggers, and credentials

Controls C04, C07, C08, and C09. The policy distinguishes who authorizes, who is
authenticated, which application acts, and which operation is executed.

<a id="c04"></a>
## C04 — Recognizing the sender is not enough

**Policy.** Verify identity and the right to request that class of action at entry; before
the effect, revalidate resource, arguments, destinations, delegation, and limits. Deny by
default. A message claiming an identity does not prove it. CLI, API, UI, scheduled, and
inter-agent paths reaching the same effect must share the same boundary. [F05](reference/sources.md#f05)

A repository `write` trigger is suitable for a specific coding workflow, not every service.
Copilot documents that product default and configuration options; this does not create
universal permission for every bot. [F20](reference/sources.md#f20)

<a id="c07"></a>
## C07 — Two legitimate modes, not interchangeable

**Source-backed fact.** Google OAuth distinguishes user-delegated authorization from
application flows. Temporary credentials through impersonation involve the originating
principal and service account; workload federation can avoid persistent keys. [F08](reference/sources.md#f08),
[F09](reference/sources.md#f09)

**Policy:**

- In D, allow user delegation scoped to the request, with identified application, resources,
  and permissions. Use approved connectors without exporting tokens to free code. Check actual
  scopes, policies, and accessible resources.
- In A, require a dedicated or federated workload identity and temporary credentials. A
  persistent personal login is not autonomous infrastructure by convenience; it requires a
  specific exception. Creating a principal requires the authority in the contract.
- In both modes, document effective privileges, who can obtain or renew credentials, custody,
  expiry, revocation, and responsibility. An application name alone does not prove an
  authenticated workload. Ban personal PATs in free execution.

These are local choices, not an OAuth requirement to create a distinct identity for every
agent. [F08](reference/sources.md#f08), [F09](reference/sources.md#f09), [F10](reference/sources.md#f10)

## Access duration and delegation duration

A short-lived access token does not make a renewable grant short-lived. RFC 9700 addresses
refresh-token protections and sender-constraining; the client cannot invent that guarantee.
Record access-token expiry separately from renewal conditions, inactivity, revocation, and
refresh-token protection. Test revocation and expiry. [F10](reference/sources.md#f10)

A GitHub App installation token lasts one hour, but repository and permission reduction must be
requested; short expiry is not proof of least privilege. [F13](reference/sources.md#f13)

## Correct names, without automatic diagnosis

NHI7 concerns secrets without expiry or too persistent for the need; NHI10 concerns people
using machine identities and is not a definition of user-delegated OAuth. [F11](reference/sources.md#f11),
[F12](reference/sources.md#f12)

A file named `client_secret` does not by itself prove a leak: Google distinguishes installed,
non-confidential clients from web clients. Protect access and refresh tokens without copying
sensitive values. [F08](reference/sources.md#f08)

<a id="c09"></a>
## C09 — Verify the boundary, not the variable name

Credentials belong in a connector, broker, or separate executor that authorizes the operation;
the model or arbitrary code it can run must not read them. Inspect files, mounts, processes,
inherited environment, caches, logs, diagnostic tools, and debug channels. If the boundary is
absent, obtain a documented exception before use.

Provider documentation about removing configured secrets after setup does not certify absence
of copies or other accessible paths. Filtering only a child process environment may be
insufficient when neighboring processes remain readable. [F22](reference/sources.md#f22),
[F25](reference/sources.md#f25)

For MCP stdio, environment guidance describes credential provision, not an exemption from
local isolation. Audience and passthrough are handled by [C08](protocols.md#c08).

## Minimum inventory

| Field | Evidence |
|---|---|
| Requester and delegator | verified identity and mandate |
| Effective principal and application | service-recognized identity, grant, or installation |
| Credential type | flow, issuer, and recipient; never the token value |
| Resources and privileges | effective scope and authorization |
| Duration and renewal | expiry, custody, offboarding, and revocation |
| Trigger and approval | who can activate, what was approved, and consent validity |
| Secret boundary | what the executor can and cannot read |
| Trace | correlated request, action, result, and protected audit |

For Git operations, add HTTP/SSH principal, author, committer, and signer. Metadata does not
determine push authentication; a verified signature does not prove who approved or performed
the push. [F14](reference/sources.md#f14), [F15](reference/sources.md#f15)
