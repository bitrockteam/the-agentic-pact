# Evidence and measurement

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
