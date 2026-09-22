# Active sources and applicability limits

Registry for the Agentic Pact **2.0**. The source sections listed here were documented
as reviewed on **2026-09-19**. That is the source review date, not the publication date and
not a new verification performed by this extraction. No tests of the services described
by these sources were performed as part of that review.

The next complete review was recorded as **2026-12-18**. A partial reread does not move
that date. For every source, compare the claim with the cited passage, not only the title.
“Date not exposed” does not mean published in 2026.

F01–F39 are stable source IDs used throughout the controls and technical companions.
**Policy** text in the repository remains a local decision; a citation supplies scope and
technical grounding, not an external endorsement of the local requirement. Historical
references are kept separately and are not current evidence until revalidated.

<a id="f01"></a>
## F01 — Anthropic: multi-agent architectures

- [Source](https://claude.com/blog/building-multi-agent-systems-when-and-how-to-use-them).
- Declared date/version: 2026-01-23. Type: vendor experience.
- Sections used: “Outgrowing single-agent architectures”; “The verification subagent pattern”. Controls: C01–C03.
- Scope and limit: measured simplicity, parallelism, and criteria-bearing verification. The 3–10x figure concerns tokens in the reported experiments, not universal spend.

<a id="f02"></a>
## F02 — Cognition: Multi-Agents: What's Actually Working

- [Source](https://cognition.com/blog/multi-agents-working).
- Declared date/version: 2026-04-22. Type: vendor experience.
- Sections used: code-review experiments; “What We Know Today”. Controls: C01–C03.
- Scope and limit: independent-context reviewer and single writer; not a universal standard.

<a id="f03"></a>
## F03 — OWASP LLM06:2025 Excessive Agency

- [Source](https://genai.owasp.org/llmrisk/llm062025-excessive-agency/).
- Declared date/version: 2025 edition. Type: guidance.
- Sections used: “Prevention and Mitigation Strategies”, points 1–9. Controls: C04–C07, C10–C11.
- Scope and limit: minimum functions, permissions, autonomy, user context, and application authorization. Explicit 2025 edition, not `latest`.

<a id="f04"></a>
## F04 — OWASP Top 10 for Agentic Applications 2026

- [Source](https://genai.owasp.org/resource/owasp-top-10-for-agentic-applications-for-2026/).
- Declared date/version: page 2025-12-09; 2026 edition. Type: taxonomy and guidance.
- Sections used: ASI01–ASI10 and linked PDF. Controls: C04–C12.
- Scope and limit: risk categories, not certification or universal priority. Operational questions in this Pact are local choices.

<a id="f05"></a>
## F05 — OWASP Authorization Cheat Sheet

- [Source](https://cheatsheetseries.owasp.org/cheatsheets/Authorization_Cheat_Sheet.html).
- Declared date/version: not exposed. Type: guidance.
- Sections used: Deny by Default; Validate the Permissions on Every Request; Create Unit and Integration Test Cases. Controls: C04–C07, C12.
- Scope and limit: authentication differs from authorization, with checks on every path. It does not require a GitHub role for every system.

<a id="f06"></a>
## F06 — OWASP Logging Cheat Sheet

- [Source](https://cheatsheetseries.owasp.org/cheatsheets/Logging_Cheat_Sheet.html).
- Declared date/version: not exposed. Type: guidance.
- Sections used: events, attributes, exclusions, verification, and protection. Control: C12.
- Scope and limit: proportionality, attributes, protection, and log testing. The local high-impact block when audit is missing is Pact policy.

<a id="f07"></a>
## F07 — OWASP Transaction Authorization Cheat Sheet

- [Source](https://cheatsheetseries.owasp.org/cheatsheets/Transaction_Authorization_Cheat_Sheet.html).
- Declared date/version: not exposed. Type: guidance.
- Sections used: principles 2.1–2.9, especially final gate 2.8. Controls: C04–C06, C12.
- Scope and limit: consent bound to data and checked before execution; extension to tools is local policy.

<a id="f08"></a>
## F08 — Google Identity: OAuth 2.0

- [Source](https://developers.google.com/identity/protocols/oauth2).
- Declared date/version: updated 2026-05-26. Type: vendor documentation.
- Sections used: Basic steps; Installed applications; Web server applications; Service accounts; Refresh token expiration. Controls: C07, C09.
- Scope and limit: user delegation and application flows are distinct. An installed-client secret is not the same as a public user token.

<a id="f09"></a>
## F09 — Google IAM: service-account impersonation

- [Source](https://docs.cloud.google.com/iam/docs/service-account-impersonation).
- Declared date/version: updated 2026-09-16. Type: vendor documentation.
- Sections used: how impersonation works; local development; external applications. Control: C07.
- Scope and limit: temporary credentials and federation; not automatic proof of correct scope or a requirement for every program.

<a id="f10"></a>
## F10 — RFC 9700: OAuth 2.0 Security Best Current Practice

- [Source](https://www.rfc-editor.org/rfc/rfc9700.html).
- Declared date/version: 2025-01; BCP 240. Type: BCP within its defined roles.
- Sections used: 2.2.2, 2.3, 4.14, 4.15. Controls: C07–C09.
- Scope and limit: token protection and renewal; public-client replay protection is an authorization-server responsibility, not a client-invented obligation.

<a id="f11"></a>
## F11 — OWASP NHI7:2025: Long-Lived Secrets

- [Source](https://owasp.github.io/www-project-non-human-identities-top-10/2025/7-long-lived-secrets/).
- Declared date/version: 2025 edition; day not exposed. Type: taxonomy.
- Sections used: Description; How To Prevent. Controls: C07, C09.
- Scope and limit: excessive persistence, not only missing expiry; no universal duration.

<a id="f12"></a>
## F12 — OWASP NHI10:2025: Human Use of NHI

- [Source](https://owasp.github.io/www-project-non-human-identities-top-10/2025/10-human-use-of-nhi/).
- Declared date/version: 2025 edition; day not exposed. Type: taxonomy.
- Sections used: Description; Example Scenarios; How to Prevent. Control: C07.
- Scope and limit: humans using non-human identities; does not define the reverse direction or ban delegated OAuth.

<a id="f13"></a>
## F13 — GitHub: installation access token

- [Source](https://docs.github.com/en/apps/creating-github-apps/authenticating-with-a-github-app/generating-an-installation-access-token-for-a-github-app).
- Declared date/version: page-wide date not exposed. Type: vendor documentation.
- Sections used: About and Generating an installation access token. Control: C07.
- Scope and limit: one-hour duration; repository and permissions can be reduced explicitly, not automatically for each task.

<a id="f14"></a>
## F14 — Git: `git-commit`

- [Source](https://git-scm.com/docs/git-commit).
- Declared date/version: current manual 2.55.0, 2026-06-29. Type: project documentation.
- Sections used: COMMIT INFORMATION; `--author`. Controls: C07, C12.
- Scope and limit: author and committer are configurable; the name is not push authentication.

<a id="f15"></a>
## F15 — GitHub: commit signature verification

- [Source](https://docs.github.com/en/authentication/managing-commit-signature-verification/about-commit-signature-verification).
- Declared date/version: not exposed. Type: vendor documentation.
- Sections used: default statuses; persistent verification; SSH signatures. Controls: C07, C12.
- Scope and limit: verified signature differs from push principal and approver; persistent verification does not prove the key is still controlled.

<a id="f16"></a>
## F16 — GitHub: available rules for rulesets

- [Source](https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/managing-rulesets/available-rules-for-rulesets).
- Declared date/version: not exposed. Type: vendor documentation.
- Sections used: required PR before merge; required status checks. Control: C05.
- Scope and limit: PR, approval count, stale reviews, and check provenance are separate settings.

<a id="f17"></a>
## F17 — GitHub: managing rulesets

- [Source](https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/managing-rulesets/managing-rulesets-for-a-repository).
- Declared date/version: not exposed. Type: vendor documentation.
- Sections used: permissions; editing, disabling, and deleting rulesets. Control: C05.
- Scope and limit: an empty bypass list does not prevent authorized administrators from changing rules.

<a id="f18"></a>
## F18 — GitHub REST: merge a pull request

- [Source](https://docs.github.com/en/rest/pulls/pulls#merge-a-pull-request).
- Declared date/version: not exposed. Type: API contract.
- Sections used: fine-grained access tokens for merge. Controls: C05, C07.
- Scope and limit: installation tokens may use `Contents:write`; this does not prove that a particular installation can bypass every gate.

<a id="f19"></a>
## F19 — GitHub: troubleshooting required status checks

- [Source](https://docs.github.com/en/pull-requests/how-tos/merge-and-close-pull-requests/troubleshooting-required-status-checks).
- Declared date/version: not exposed. Type: vendor documentation.
- Sections used: required check against latest commit SHA; skipped required checks. Controls: C03, C05.
- Scope and limit: distinguish skipped jobs/workflows and success/skipped/neutral outcomes; inspect validation that actually ran.

<a id="f20"></a>
## F20 — GitHub: Copilot cloud-agent risks and mitigations

- [Source](https://docs.github.com/en/copilot/concepts/agents/cloud-agent/risks-and-mitigations).
- Declared date/version: not exposed. Type: product-specific guarantees.
- Sections used: push code changes; automations and triggers; mitigations. Controls: C04–C05, C09–C11.
- Scope and limit: branch and human-merge claims belong to that product; trigger defaults are configurable and are not guarantees for every agent.

<a id="f21"></a>
## F21 — Invariant: GitHub MCP Exploited

- [Source](https://invariantlabs.ai/blog/mcp-github-vulnerability).
- Declared date/version: 2025-05. Type: primary demonstrative research.
- Sections used: Attack Setup; Attack Demonstration; Scope and Mitigations. Controls: C04, C07, C10.
- Scope and limit: public-to-private repository flow with PR output; does not prove token passthrough or a current vulnerability in every MCP.

<a id="f22"></a>
## F22 — Comment and Control

- [Source](https://oddguan.com/blog/comment-and-control-prompt-injection-credential-theft-claude-code-gemini-cli-github-copilot/).
- Declared date/version: 2026-04-15; stated update 2026-05-04. Type: primary research.
- Sections used: Findings 1 and 3; Environment Filtering; Secret Scanning; Network Firewall; Timeline. Controls: C09–C10.
- Scope and limit: products, versions, and conditions of the writeup. The Anthropic product examined is Claude Code Security Review, not generically claude-code-action.

<a id="f23"></a>
## F23 — Nx: S1ngularity postmortem

- [Source](https://nx.dev/blog/s1ngularity-postmortem).
- Declared date/version: incident 2025-08-26; do not confuse with page date. Type: primary postmortem.
- Sections used: What Happened; Technical Details; Lessons Learned. Controls: C06, C09–C11.
- Scope and limit: shell injection and token theft precede malicious packages and later AI-tool attempts; the whole chain is not prompt injection.

<a id="f24"></a>
## F24 — OpenAI: agent approvals and security

- [Source](https://learn.chatgpt.com/docs/agent-approvals-security).
- Declared date/version: not exposed. Type: vendor documentation.
- Sections used: sandbox and approvals. Controls: C09, C11.
- Scope and limit: sandbox and approvals are distinct; cloud and CLI must be distinguished; no local-environment attestation.

<a id="f25"></a>
## F25 — OpenAI: cloud environments

- [Source](https://learn.chatgpt.com/docs/environments/cloud-environment).
- Declared date/version: not exposed. Type: vendor documentation.
- Sections used: environment variables and secrets. Control: C09.
- Scope and limit: configured secrets are available at setup and removed before agent execution; not a certification of every file or cache.

<a id="f26"></a>
## F26 — GitHub: push protection

- [Source](https://docs.github.com/en/code-security/concepts/secret-security/push-protection).
- Declared date/version: not exposed. Type: vendor documentation.
- Sections used: how push protection works, coverage, and limits. Controls: C10, C12.
- Scope and limit: supported secret types; not proof that every output lacks sensitive data.

<a id="f27"></a>
## F27 — MCP: versioning and compatibility

- [Source](https://modelcontextprotocol.io/specification/2026-07-28/basic/versioning).
- Declared date/version: 2026-07-28 revision. Type: specification.
- Sections used: Protocol Version Negotiation; Extension Negotiation; Backward Compatibility. Control: C08.
- Scope and limit: per-request version in the current revision; do not transfer the detail to handshake revisions.

<a id="f28"></a>
## F28 — MCP: authorization

- [Source](https://modelcontextprotocol.io/specification/2026-07-28/basic/authorization/index).
- Declared date/version: 2026-07-28 revision. Type: specification profile.
- Sections used: Purpose and Scope; Protocol Requirements; Resource Parameter Implementation; Token Handling. Controls: C07–C09.
- Scope and limit: HTTP implementations SHOULD conform when adopting auth; profile obligations and stdio must remain distinct.

<a id="f29"></a>
## F29 — MCP: authorization security considerations

- [Source](https://modelcontextprotocol.io/specification/2026-07-28/basic/authorization/security-considerations).
- Declared date/version: 2026-07-28 revision. Type: specification and linked guidance.
- Sections used: audience binding and validation; privilege restriction; token theft. Controls: C08–C09.
- Scope and limit: MCP audience and no forwarding of the received token; a distinct upstream/downstream token is allowed.

<a id="f30"></a>
## F30 — MCP: OAuth client credentials

- [Source](https://modelcontextprotocol.io/extensions/auth/oauth-client-credentials).
- Declared date/version: point date/version not exposed. Type: optional extension.
- Sections used: what it is; how it works; client support. Controls: C07–C08.
- Scope and limit: machine-to-machine authorization; verify client support and do not presume an identity per agent.

<a id="f31"></a>
## F31 — MCP: enterprise-managed authorization

- [Source](https://modelcontextprotocol.io/extensions/auth/enterprise-managed-authorization).
- Declared date/version: point date/version not exposed. Type: optional extension.
- Sections used: how it works; authorization servers; client support. Controls: C07–C08.
- Scope and limit: enterprise delegation and ID-JAG exchange; distinct from an autonomous workload identity.

<a id="f32"></a>
## F32 — A2A: release v1.0.1

- [Source](https://github.com/a2aproject/A2A/releases/tag/v1.0.1).
- Declared date/version: changelog 2026-05-26; publication 2026-05-28. Type: release.
- Sections used: bug fixes. Control: C08.
- Scope and limit: patch corrections, not a new governance architecture.

<a id="f33"></a>
## F33 — A2A: current specification

- [Source](https://a2a-protocol.org/latest/specification/).
- Declared date/version: moving `/latest` page read 2026-09-19. Type: specification.
- Sections used: 3.6; 4.4.1; 7.5; 7.6.4; 13.1; 13.4. Controls: C04, C07–C08, C12.
- Scope and limit: Major.Minor versioning, authorization, and audit are discussed; do not attribute every moving-page sentence to v1.0.1.

<a id="f34"></a>
## F34 — Agent Control Standard repository

- [Source](https://github.com/GenAI-Security-Project/agent-control-standard).
- Declared date/version: README read 2026-09-19; implementation says 0.1.0. Type: emerging specification and stated implementation status.
- Sections used: reference implementation status; failure posture. Controls: C04, C11–C12.
- Scope and limit: reference implementation reports unauthenticated channel and fail-open default; not prescribed as production-ready.

<a id="f35"></a>
## F35 — OWASP LLM Top 10 2026

- [Source](https://genai.owasp.org/resource/owasp-genai-llm-top-10-2026/).
- Declared date/version: page 2026-08-03; PDF has editorial date placeholders. Type: guidance with a document anomaly.
- Sections used: PDF LLM03, pp. 23–26; cover and revision history. Controls: C04–C07, C10–C11.
- Scope and limit: user context and mediation; supporting basis, not the sole source; do not confuse with Agentic Top 10.

<a id="f36"></a>
## F36 — OWASP File Upload Cheat Sheet

- [Source](https://cheatsheetseries.owasp.org/cheatsheets/File_Upload_Cheat_Sheet.html).
- Declared date/version: not exposed. Type: guidance.
- Sections used: threats, protection, and storage location. Controls: C10–C11.
- Scope and limit: active content, validation, and upload isolation; the output manifest is local policy derived from it.

<a id="f37"></a>
## F37 — MCP: logging

- [Source](https://modelcontextprotocol.io/specification/2026-07-28/server/utilities/logging).
- Declared date/version: 2026-07-28 revision. Type: specification.
- Sections used: opening warning; implementation considerations. Control: C12.
- Scope and limit: utility deprecated in the current revision; protocol conformance does not guarantee persistence.

<a id="f38"></a>
## F38 — MCP: specification

- [Source](https://modelcontextprotocol.io/specification/2026-07-28).
- Declared date/version: 2026-07-28 revision. Type: specification.
- Sections used: implementation guidelines; security and trust. Controls: C04–C05, C08.
- Scope and limit: protocol cannot enforce every consent principle; host evidence is required.

<a id="f39"></a>
## F39 — GitHub Actions: secure use reference

- [Source](https://docs.github.com/en/actions/reference/security/secure-use).
- Declared date/version: not exposed. Type: vendor documentation.
- Sections used: secrets; script injections; third-party actions. Controls: C04–C05, C09–C11.
- Scope and limit: protect permissions and workflows; immutable pins and supply-chain checks do not prove harmless content.

## Complementary links recorded in the source review

- [F04 Agentic Applications PDF](https://genai.owasp.org/download/52117/?tmstv=1765059207), ASI01–ASI10.
- [F27 MCP Versioning](https://modelcontextprotocol.org/docs/2026-07-28/learn/versioning), revisions and negotiation.
- [F29 MCP Security Best Practices](https://modelcontextprotocol.org/docs/2026-07-28/tutorials/security/security_best_practices), token passthrough; logging guidance is not durable-audit proof.
- [F34 OWASP ACS presentation](https://genai.owasp.org/resource/agent-control-standard-acs/), page dated 2026-09-01; not implementation maturity evidence.
- [F35 LLM 2026 PDF](https://genai.owasp.org/download/56857/?tmstv=1785822482), pp. 1–2 and 23–26; cover and history retain date placeholders.
- [F16 Creating rulesets](https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/managing-rulesets/creating-rulesets-for-a-repository) and [required reviews](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/reviewing-changes-in-pull-requests/approving-a-pull-request-with-required-reviews); do not confuse a GitHub role with intellectual authorship.

## Current revalidation log

On September 22, 2026, the following primary pages were opened during the public repair:

- [F05 authorization guidance](https://cheatsheetseries.owasp.org/cheatsheets/Authorization_Cheat_Sheet.html), confirming the current page exposes deny-by-default, per-request permission checks, and authorization test guidance.
- [F16 required-review guidance](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/reviewing-changes-in-pull-requests/approving-a-pull-request-with-required-reviews), which redirects to the current GitHub review page.
- [F28 MCP authorization](https://modelcontextprotocol.io/specification/2026-07-28/basic/authorization/index) and [F39 GitHub Actions secure use](https://docs.github.com/en/actions/reference/security/secure-use), confirming the linked public pages are reachable.

These page opens are not tests of service behavior, local installations, permissions, or
security posture. The September 19 baseline review date remains the recorded review date for
all other entries. The historical registry retains sources whose pages are moving, restricted,
or not revalidated here.

## Uncertain or historical material

Secondary references and unused incidents are preserved in the [historical registry](historical-sources.md), not declared false. If a source no longer supports a rule, record the finding rather than deleting the source to hide it. Emerging F34–F35 are not needed to mandate a new product, service, or framework.
