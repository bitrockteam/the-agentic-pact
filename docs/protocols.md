# Protocols: requirements, compatibility, and guarantees to test

Control C08. MUST and SHOULD apply within the cited specification, version, and role. Local
policy may be stricter, but must say so.

## MCP: actual version, not only `latest`

The baseline records MCP revision **2026-07-28**. It permits compatible changes without
changing the identifier. Record the version supported by host, client, and server, transport,
and extensions. An older version may be correct for the implementation under review; assess
compatibility, support, and security. [F27](reference/sources.md#f27)

In the 2026-07-28 revision, the version is declared per request and unsupported-version
errors identify accepted revisions. Do not confuse this with earlier initialization handshakes.

<a id="c08"></a>
## C08 — Authorization boundaries

MCP Authorization concerns HTTP transports. Authorization is optional; HTTP implementations
adopting it SHOULD conform to the profile. Stdio uses a different mechanism and environment
credentials. [F28](reference/sources.md#f28)

**Local policy.** For authenticated MCP HTTP, adopt the supported profile unless a documented
exception exists. State the requested resource and verify that the token was issued for the
destination MCP server. Do not accept a token for another service as the MCP credential, and
do not forward the received MCP token to a downstream API. The server may obtain a distinct
token issued for that API. [F28](reference/sources.md#f28), [F29](reference/sources.md#f29)

Design every hop with issuer, recipient, consumer, permissions, and duration. Test valid,
expired, revoked, and wrong-resource tokens according to the applicable mechanism. This is not
a generic ban on OAuth delegation or token exchange.

## Extensions: possibilities are not installations

- **OAuth Client Credentials:** a userless application-credential flow. [F30](reference/sources.md#f30)
- **Enterprise-Managed Authorization:** enterprise IdP authorization exchanged for an MCP
  server token. [F31](reference/sources.md#f31)

These optional extensions have variable client support and do not prove a distinct identity
for each agent. Verify support, represented identity, and revocation before depending on them.

## A2A: release and wire contract

The recorded release is **v1.0.1**: changelog May 26, 2026, publication May 28, 2026. The
current documentation negotiates Major.Minor; the patch must not be used as the negotiated
version. An Agent Card describes capabilities and security requirements; it does not grant
authorization. [F32](reference/sources.md#f32), [F33](reference/sources.md#f33)

Authenticate each channel, validate schema and permissions at each boundary, and never treat
another agent's message as superior authority. Waiting states for input or authorization do
not replace a valid decision on the destination system. [F33](reference/sources.md#f33)

## What protocol conformance does not prove

MCP has a logging utility deprecated in the recorded revision; persistence is not automatic.
MCP guidance also states limits on protocol enforcement. [F37](reference/sources.md#f37),
[F38](reference/sources.md#f38)

State where approval, cost/volume limits, revocation, isolation, durable audit, and recovery
are actually imposed. A tool response or `completed` state does not certify a remote effect.
Use forge controls for code and application contracts for other effects.

## ACS: reference to evaluate, not a mandatory dependency

The Agent Control Standard is an emerging runtime-control reference. Its repository reports
an unauthenticated channel, fail-open default, and partial hook coverage. Do not adopt an
enforcement component because of its standard name; test authentication, integrity,
unavailability behavior, and bypass resistance first. [F34](reference/sources.md#f34)
