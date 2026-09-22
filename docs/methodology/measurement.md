# Measurement: evidence that can falsify a claim

Control C12. This method is local policy. Its foundations are authorization integration tests
[F05](../reference/sources.md#f05) and testing logging operation and protection
[F06](../reference/sources.md#f06). A public source does not certify an installation.

## States and evidence levels

| Control state | Meaning |
|---|---|
| Verified | applicable criterion satisfied by relevant, dated, repeatable evidence |
| Partial | some subcriteria satisfied; missing ones named separately |
| Unsatisfied | a test or configuration contradicts an applicable requirement |
| Unknown | access, test, or information is insufficient; not a pass |
| Not applicable | surface or operation is absent, with reason and review condition |

Also distinguish documented by a provider, configured, observed in a test, and observed in
operation. Configuration proves an intended setting, not end-to-end behavior. A positive test
does not prove illicit requests are refused.

## Minimum review record

| Field | Content |
|---|---|
| Boundary | profile, components/versions, commit or configuration, environment, date |
| Control | C01–C12 and subrequirement; source and local decision |
| Access | documents, configurations, logs, and systems actually inspected |
| Test | procedure, expected result, observed result, redacted artifact if sensitive |
| Conclusion | state, evidence level, limits, and explicit inferences |
| Action | owner, justified priority, next step, closure criterion |

Do not assign operational severity to a bibliographic imprecision alone. For a risk, state
prerequisites, reachable resources, effect, and compensating controls. Do not invent time or
cost estimates: provide assumptions and an interval, or mark it to be estimated.

## Profile-proportionate minimum tests

These are acceptance-policy examples, not permission for invasive or production tests.

| Surface | Positive test | Negative or failure test |
|---|---|---|
| Authorization | allowed actor performs intended operation | other actor, object, or scope is refused |
| Integration | real contract matches client and version | error, unexpected field, or incompatible version is handled |
| Output | artifact and recipient match approval | sensitive data or different destination is blocked |
| Credentials | scope and audience are appropriate | expiry, revocation, or wrong audience is refused |
| Approval | consent covers operation or approved repeatable mandate | material change or reuse outside scope/duration/count is refused |
| Execution | intended effect occurs once | uncertain result does not cause blind retry; stop works |
| Audit | event is searchable and correlated with effect | collection failure is detected and policy applies |

Stub or mock tests check assumptions encoded in the double. Where applicable, pair them with
an authorized real-contract or integration check. Offline results do not prove remote
permissions, configuration, or service behavior.

<a id="c12"></a>
## C12 — Trace the effect, not only the story

For privileged operations, writes, sends, authorization refusals, and policy changes, record
time, correlation ID, requester, effective principal, delegation, operation/resource,
recipient or audience, decision/reason, approval reference, policy version, and returned
outcome. Do not archive internal reasoning, secrets, or unnecessary sensitive content. [F06](../reference/sources.md#f06)

The executor must not rewrite or delete its own trace. An append-open file is insufficient if
that actor can replace it. Use a separate collector or suitable storage control, with explicit
retention and access. If protection is missing, that subrequirement is unsatisfied; do not
call it immutable audit.

Test emission, logging level, and correlation with an effect. For high-impact effects, block
when pre-execution authorization cannot be recorded; if the result cannot be recorded,
signal uncertainty and reconcile without blind retry. This fail-closed behavior is local
policy, not a universal OWASP logging requirement.

Git records artifacts and history, not every remote effect. Commit author, signature, push
principal, and approver are distinct fields. [F14](../reference/sources.md#f14),
[F15](../reference/sources.md#f15)
