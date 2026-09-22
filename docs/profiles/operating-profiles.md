# Operating profiles

These profiles are local policy. They choose how the twelve controls apply; they do not
disable any control. Their design separates capability, permission, and autonomy. [F03](../reference/sources.md#f03),
[F05](../reference/sources.md#f05)

## Choose the profile before the tool

| Profile | Permitted effect | Required gate | Identity |
|---|---|---|---|
| **L — Read and analyze** | consultation and local artifacts within assigned scope | authorized assignment and access; no implicit external send | user delegation or bounded read principal |
| **C — Shared-code development** | changes on a branch and an integration proposal | PR, required checks, independent approval when configured, authorized human merge | authenticated principal and documented permissions |
| **D — Supervised delegated action** | explicit operation on identified object, content, and recipients | sufficiently specific human request; confirmation before effects not already approved | traceable user delegation, not arbitrary impersonation |
| **A — Bounded automation** | only operations in an approved contract | prior authorization of trigger, scope, limits, duration, and stop path | dedicated/federated workload identity unless an explicit exception exists |

A workflow may cross profiles. Analysis to sending, draft to publication, or supervision to
autonomy is a new authorization decision. A credential that can write does not authorize a
write. [F05](../reference/sources.md#f05)

## Minimum contract for D and A

Record before enablement:

- responsible owner, requester, and system-recognized principal;
- permitted resources and operations, recipients, and data classification;
- trigger, assignment expiry, time/cost/volume quotas, and parallelism;
- argument checks outside the model and covered alternate paths;
- conditions requiring human approval and conditions that block;
- credentials, storage, renewal, revocation, and effective permissions;
- retry semantics and uncertain-result handling;
- audit, stop, recovery, tests, and known limits.

This is a verifiable Pact decision derived from application authorization, least privilege,
and transaction authorization. The cited sources do not state this exact checklist. [F03](../reference/sources.md#f03),
[F07](../reference/sources.md#f07)

## When a person is required

Require explicit human approval before irreversible operations, access expansion, sensitive
exports, administrative changes, or costs beyond the authorized limit. Show the actual object,
content, recipients, and consequences. A sufficiently specific request can be the approval;
the same consent need not be requested twice. A generic delegation or text returned by a tool
is not approval. Material changes to content, destination, or permissions invalidate approval.
[F07](../reference/sources.md#f07)

Automation may execute ordinary actions already covered by the A contract. It may not extend
the contract, approve its own exception, or replace required consent for high-impact actions.
Without an A contract, remain in L/C or request D authorization.

## Avoid fictitious requirements

A read does not require a PR. A send requires a send-control, not a commit. C05 for shared
code does not authorize publishing sensitive data in a branch, PR, log, or comment; those are
also output channels. [F21](../reference/sources.md#f21), [F22](../reference/sources.md#f22)

For a documented maintenance contract that explicitly authorizes a direct commit and push,
apply D: named scope, reviewed diff, fresh checks, and Git audit. Do not extend that contract
to shared code, deployment, or another repository.
