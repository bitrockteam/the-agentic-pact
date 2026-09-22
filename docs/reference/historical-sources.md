# Historical source registry — non-normative

This registry preserves the bibliography from the pre-2.0 baseline. The dates below are
the dates recorded at that time, not a new verification. Use [active sources](sources.md)
for current source claims. Historical references remain useful for provenance and
comparison; they do not prove current behavior.

## Architecture and vendor claims

| Source | Recorded date | Controls or use | Historical note |
|---|---|---|---|
| [Anthropic, Building multi-agent systems](https://claude.com/blog/building-multi-agent-systems-when-and-how-to-use-them) | 2026-01-23 | C01–C03 | Retained in active F01 |
| [Cognition, Multi-Agents: What's Actually Working](https://cognition.com/blog/multi-agents-working) | 2026-04 | C01–C03 | Retained in active F02; original registry used April 2026 |
| [Anthropic, Building effective agents](https://www.anthropic.com/engineering/building-effective-agents) | 2024-12 | C01 vocabulary | Historical vocabulary only |
| [GitHub Agent HQ, multi-agent development](https://code.visualstudio.com/blogs/2026/02/05/multi-agent-development) | 2026-02 | C01, C05 | Historical vendor material |
| [Microsoft Agent Framework, handoff orchestration](https://devblogs.microsoft.com/agent-framework/a-tour-of-handoff-orchestration-pattern/) | 2026 | C01 | Historical vendor material |
| [Cognition, Don't Build Multi-Agents](https://cognition.com/blog/dont-build-multi-agents) | 2025-06 | Prior position | Superseded or narrowed by later material; not a current position |

## Vendor-specific security material

| Source | Recorded date | Controls |
|---|---|---|
| [GitHub Copilot cloud-agent risks](https://docs.github.com/en/copilot/concepts/agents/cloud-agent/risks-and-mitigations) | 2026, undated page | C04, C05, C09, C10 |
| [OpenAI agent approvals and security](https://developers.openai.com/codex/agent-approvals-security) | 2026, undated page | C09–C11 |
| [Anthropic claude-code-action security](https://github.com/anthropics/claude-code-action/blob/main/docs/security.md) | 2026, undated page | C04, C07, C09, C10 |
| [Anthropic claude-code-action setup](https://github.com/anthropics/claude-code-action/blob/main/docs/setup.md) | 2026 | C07 |
| [OpenAI cloud environments](https://learn.chatgpt.com/docs/environments/cloud-environment) | 2026 | C09 |
| [GitHub Copilot cloud-agent secrets](https://docs.github.com/en/copilot/how-tos/copilot-on-github/customize-copilot/customize-cloud-agent/configure-secrets-and-variables) | 2026-05 | C09 |
| [GitHub Copilot cloud-agent resource access](https://docs.github.com/en/copilot/tutorials/cloud-agent/give-access-to-resources) | 2026 | C07 |

## Taxonomies and incidents

| Source | Recorded date | Controls |
|---|---|---|
| [OWASP Top 10 for Agentic Applications 2026](https://genai.owasp.org/resource/owasp-top-10-for-agentic-applications-for-2026/) | 2025-12 | C06, C10–C12 |
| [OWASP LLM06 Excessive Agency](https://owasp.org/www-project-top-10-for-large-language-model-applications/2_0_vulns/LLM06_ExcessiveAgency.html) | 2025 | C11 |
| [OWASP Non-Human Identities Top 10 2025](https://owasp.org/www-project-non-human-identities-top-10/2025/top-10-2025/) | 2025 | C07 |
| [Comment and Control](https://oddguan.com/blog/comment-and-control-prompt-injection-credential-theft-claude-code-gemini-cli-github-copilot/) | 2026-04 | C09, C10 |
| [Invariant GitHub MCP server](https://invariantlabs.ai/blog/mcp-github-vulnerability) | 2025-05 | C07, C08 |
| [CamoLeak](https://www.legitsecurity.com/blog/camoleak-critical-github-copilot-vulnerability-leaks-private-source-code) | 2025-10 | C07, C10 |
| [Wiz s1ngularity](https://www.wiz.io/blog/s1ngularitys-aftermath) and [Nx postmortem](https://nx.dev/blog/s1ngularity-postmortem) | 2025-08/09 | C11 |
| [Flatt Security bot-actor bypass](https://flatt.tech/research/posts/poisoning-claude-code-one-github-issue-to-break-the-supply-chain/) | 2026-01–06 | C04 |
| [The Register Replit/SaaStr](https://www.theregister.com/2025/07/21/replit-saastr-vibe-coding-incident/) and [Fortune](https://fortune.com/2025/07/23/ai-coding-tool-replit-wiped-database-called-it-a-catastrophic-failure/) | 2025-07 | C06 |

## Identity, protocols, and forge controls

| Source | Recorded date | Controls or use |
|---|---|---|
| [MCP Security Best Practices](https://modelcontextprotocol.io/specification/2026-07-28/basic/security_best_practices) | 2026-07-28 | C08 |
| [MCP Authorization and RFC 8707](https://modelcontextprotocol.io/specification/latest/basic/authorization) | 2025–26 | C07, C08 |
| [MCP specification](https://modelcontextprotocol.io/specification/latest) | 2026 | C08 |
| [GitHub installation access token](https://docs.github.com/en/apps/creating-github-apps/authenticating-with-a-github-app/generating-an-installation-access-token-for-a-github-app) | 2026 | C07 |
| [GitHub Actions OIDC](https://docs.github.com/en/actions/concepts/security/openid-connect) | 2026 | C07 |
| [GitHub personal access token policy](https://docs.github.com/en/enterprise-cloud@latest/admin/enforcing-policies/enforcing-policies-for-your-enterprise/enforcing-policies-for-personal-access-tokens-in-your-enterprise) | 2026 | C07 |
| [GitHub push protection](https://docs.github.com/en/code-security/secret-scanning/introduction/about-push-protection) | 2026 | C12 |
| [Linux Foundation A2A 1.0](https://www.linuxfoundation.org/press/a2a-protocol-surpasses-150-organizations-lands-in-major-cloud-platforms-and-sees-enterprise-production-use-in-first-year) | 2026-04 | Protocol context |
| [Linux Foundation Agentic AI Foundation](https://www.linuxfoundation.org/press/linux-foundation-announces-the-formation-of-the-agentic-ai-foundation) | 2025 | Protocol context |
| [GitHub rulesets](https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/managing-rulesets/about-rulesets) and [available rules](https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/managing-rulesets/available-rules-for-rulesets) | 2026 | C05 |
| [GitHub creating rulesets](https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/managing-rulesets/creating-rulesets-for-a-repository) | 2026 | C05 |
| [GitHub status checks](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/collaborating-on-repositories-with-code-quality-features/about-status-checks) | 2026 | C05 |
| [GitHub required reviews](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/reviewing-changes-in-pull-requests/approving-a-pull-request-with-required-reviews) | 2026 | C05 |
| [GitHub App permissions](https://docs.github.com/en/apps/creating-github-apps/registering-a-github-app/choosing-permissions-for-a-github-app) | 2026 | C07 |

Every historical entry was originally marked as verified in September 2026 in the source
registry, but that statement is preserved only as history here. It is not a current
attestation, and no private exception, personal memory, local host, or account detail is
included.
