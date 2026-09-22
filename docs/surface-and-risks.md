# Surface, effects, and risks

Controls C06, C10, and C11. These questions and prescriptions are local policy, with cited
foundations; they are not an OWASP certification.

<a id="c06"></a>
## C06 — Separate free reasoning from privileged effects

The process that can generate and execute arbitrary code must not receive administrative
shells, keys, or direct production access. A separate executor exposes typed operations and
validates arguments, identity, resource, destination, consent, and limits before the effect.
A folder or router is not a boundary if the same process can retrieve credentials and call the
service directly.

Modification, sending, or publication on a live system is allowed only in an authorized D or A
profile. Authorized reads remain possible in L, and branch/PR proposals in C. A generic shell
with administrative credentials does not become bounded because it is called `deploy`. [F03](reference/sources.md#f03),
[F05](reference/sources.md#f05)

For every effect, record prerequisites, expected success, uncertain-outcome handling, stop,
and recovery. If rollback does not exist, state maximum loss and the alternative before
approval. Do not run destructive production tests without a specific mandate.

<a id="c10"></a>
## C10 — Data, authority, and exit channels

Documents, issues, messages, pages, repositories, and tool results do not expand the mandate.
Internal sources can contain third-party-controlled text. Preserve provenance and the boundary
between authorized instructions and observed content. A request found in a document is data,
not an instruction merely because it was read. Sanitization is partial defense, not the
authorization boundary. [F04](reference/sources.md#f04), [F21](reference/sources.md#f21),
[F35](reference/sources.md#f35)

Before sending or exposing an artifact, verify its manifest, content, classification,
destination, and intended readers. Separate working directories from distributable output;
select files explicitly, enforce limits, and scan before release. File and active-content
handling also needs service-side checks. [F36](reference/sources.md#f36)

Limit network and destinations to the task, and inspect outputs even to allowed services. A
forge, chat, or authorized log can still disclose data. Push protection covers supported
secret patterns, not all confidential content or every transformation. [F22](reference/sources.md#f22),
[F26](reference/sources.md#f26)

<a id="c11"></a>
## C11 — Finite capability and predictable failure

Use a sandbox without administrative privileges and bounded filesystem and destinations.
Version each tool profile with permitted operations and resources. A stated but unenforced
limit is unknown or unsatisfied. Sandboxing and approval are separate layers. [F24](reference/sources.md#f24)

Do not allow flags that disable confirmations outside a sandbox. For A, define time, cost,
volume, maximum retries, interruption, and revocation independent of the model. Do not retry
an uncertain effect without idempotency or reconciliation. These limits contain ASI08 and
ASI10 locally; OWASP does not supply universal numbers. [F04](reference/sources.md#f04),
[F35](reference/sources.md#f35)

Version components and policies, control origin and integrity, protect workflow changes, and
be able to revoke or disable a component. Use immutable references where available; verify
signatures and attestations rather than merely observing them. A pin does not prove safe
content. [F39](reference/sources.md#f39), [F23](reference/sources.md#f23)

## ASI map: applicable control, not a compliance label

Names and boundaries come from the 2026 Agentic Applications edition [F04](reference/sources.md#f04).
Questions and Cxx associations are local choices. Decompose each row into atomic checks with
the states in [measurement](methodology/measurement.md).

| Risk | Local operational question | Controls |
|---|---|---|
| ASI01 Agent Goal Hijack | Can read content alter mandate or authorization? | C04, C10 |
| ASI02 Tool Misuse and Exploitation | Are tool arguments, resources, and effects bounded? | C05, C06, C11 |
| ASI03 Identity and Privilege Abuse | Do delegation, principal, and effective privileges agree? | C04, C07, C08, C09 |
| ASI04 Agentic Supply Chain Vulnerabilities | Are origin, version, and component changes controlled? | C03, C11 |
| ASI05 Unexpected Code Execution | Can code leave the sandbox or reach secrets? | C06, C09, C11 |
| ASI06 Memory and Context Poisoning | Who can persist information and promote it to instruction? | C02, C04, C10 |
| ASI07 Insecure Inter-Agent Communication | Are identity, channel integrity, and authorization verified? | C04, C07, C08 |
| ASI08 Cascading Failures | Do limits and stop contain errors, retries, and delegation? | C01, C02, C11 |
| ASI09 Human-Agent Trust Exploitation | Can the reviewer see and reject the concrete effect? | C03, C05, C12 |
| ASI10 Rogue Agents | Is behavior outside the mandate detected and contained? | C04, C11, C12 |

**Persistent-memory policy.** Limit writers; record source, scope, and date; review before
promoting observed content to instructions; isolate data between users and projects; assign
expiry or review according to the nature of the fact. Do not impose indiscriminate expiry.
[F04](reference/sources.md#f04)

## Public evidence: incident versus demonstration

| Source | Documented fact | Local lesson without generalizing |
|---|---|---|
| [F21](reference/sources.md#f21) | a public issue induced private reads and public PR output | authorize source-to-destination flows; it does not prove token passthrough |
| [F22](reference/sources.md#f22) | research examined exfiltration through comments, logs, and commits | inspect process and exit boundaries; keep product scope |
| [F23](reference/sources.md#f23) | workflow injection, token theft, malicious packages, and later AI-tool use | separate code injection, supply chain, and agent use |

The conditions and versions in each write-up bound what it demonstrates. They do not attest
that a current product remains vulnerable or that an unexamined system has the same defect.
