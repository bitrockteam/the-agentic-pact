# Migration to Pact 2.0

This record translates the source baseline's September 19, 2026 migration matrix. It
explains which text is policy, which is a correction in attribution or scope, and which
remains historical. It does not certify an implementation, close an exception, or authorize
a new tool or deployment.

| Control | Pact 2.0 treatment | Basis and nature |
|---|---|---|
| C01 | measurable benefit includes latency for independent work; token use is not universal spend | local policy and correction; F01 |
| C02 | one writer applies to remote state and memory | local generalization; F01-F02 |
| C03 | exploratory review is distinct from criteria-based acceptance verification | correction and local policy; F01-F02 |
| C04 | authorize resource and operation, not only repository write permission | scope correction; F05, F20 |
| C05 | PR and human merge for shared code; effect-specific gate elsewhere | local policy and technical correction; F07, F16-F19 |
| C06 | no free administrative access; bounded D/A operations may be allowed | explicit local policy; F03, F05 |
| C07 | distinguish supervised delegation and autonomous workload identity | explicit local policy; F08-F13 |
| C08 | MCP HTTP authorization, audience, downstream tokens, and versions are contextual | protocol clarification; F27-F31 |
| C09 | inspect processes, files, caches, logs, and indirect access | boundary clarification; F22, F25 |
| C10 | content does not authorize; permitted destinations still need output checks | generalization; F21, F22, F36 |
| C11 | add finite limits, retry, stop, recovery, and supply-chain checks | local policy; F04, F24, F39 |
| C12 | append-only is relative to executor; test emission and classify partial/unknown states | local evidence policy; F06, F14-F15 |

## Document corrections retained

- NHI10 does not describe delegated OAuth; NHI7 is not only “never expires.” [F11](sources.md#f11), [F12](sources.md#f12)
- Commit author, committer, signature, push principal, and approver are distinct. [F14](sources.md#f14), [F15](sources.md#f15)
- MCP and A2A include logging or audit references, but protocol mechanisms do not guarantee durable implementation audit. [F33](sources.md#f33), [F37](sources.md#f37), [F38](sources.md#f38)
- A2A v1.0.1 is a patch release; wire negotiation uses Major.Minor. [F32](sources.md#f32), [F33](sources.md#f33)
- Incidents and demonstrations are bounded by product, vector, and date. [F21](sources.md#f21)–[F23](sources.md#f23)
- ACS and LLM 2026 have maturity and editorial limits and do not mandate a new framework. [F34](sources.md#f34), [F35](sources.md#f35)

The stable IDs remain C01–C12. Historical references are in
[historical-sources.md](historical-sources.md). No private exception or implementation
status is silently changed by this translation.
