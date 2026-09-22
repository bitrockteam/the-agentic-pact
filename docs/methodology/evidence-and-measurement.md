# Evidence and measurement

For the full test method and C12 acceptance matrix, see the
[measurement companion](measurement.md).

The Pact distinguishes what is documented, configured, observed in a test, and observed
in operation. These are different levels of evidence.

| State | Meaning |
|---|---|
| Verified | An applicable criterion is satisfied by relevant, dated, repeatable evidence |
| Partial | Some sub-criteria are satisfied and the remainder is named |
| Unsatisfied | A test or configuration contradicts an applicable requirement |
| Unknown | Access, information, or testing is insufficient; this is not a pass |
| Not applicable | The relevant surface or operation is absent, with a reason and review condition |

## Minimum review record

For each applicable control, record:

- scope, profile, components, versions, environment, and date;
- control ID and local requirement;
- documents, configurations, logs, and systems actually inspected;
- expected and observed results for positive and negative tests;
- conclusion, evidence level, limits, and explicit inferences;
- owner, priority, next step, and closure criterion.

Positive tests must be complemented by refusal, failure, expiry, revocation, or uncertain-
outcome tests where the control depends on them. Offline mocks do not prove permissions or
remote-service behavior. A log file is not an audit trail unless its protection and
correlation with the effect have also been tested.

## Minimum evidence matrix

| Surface | Positive test | Negative or failure test |
|---|---|---|
| Authorization | An allowed actor performs the intended operation | Another actor, object, or scope is refused |
| Integration | The real contract matches the client and version | Error, unexpected field, or incompatible version is handled |
| Output | Artifact and destination match approval | Sensitive data or a different destination is blocked |
| Credentials | Scope and audience are appropriate | Expiry, revocation, or wrong audience is refused |
| Approval | Consent covers the operation or approved repeatable mandate | Material change or reuse outside scope, duration, or count is refused |
| Execution | The intended effect occurs once | Uncertain outcome does not cause blind retry; stop works |
| Audit | Event is searchable and correlated with the effect | Collection failure is detected and policy is applied |

These are acceptance-policy examples, not authorization to run invasive or production
tests. Tests against stubs verify assumptions encoded in the stub; use an authorized
contract or integration check where remote behavior matters.

<a id="c12"></a>
## C12 — Trace the effect, not only the story

For privileged operations, writes, sends, authorization refusals, and policy changes,
record the fields needed to correlate the request, decision, execution, and result. Keep
the audit append-only with respect to the executor, using a separate collector or an
appropriate storage control. If protection is missing, that sub-requirement is not
satisfied; do not call a writable file immutable. For high-impact effects, block when
pre-execution authorization cannot be recorded, and reconcile rather than blindly retry
when the outcome cannot be recorded afterward. This fail-closed rule is local policy.
