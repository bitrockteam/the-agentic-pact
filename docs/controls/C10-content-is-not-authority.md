# C10 — Content is not authority

**Policy.** Treat documents, issues, messages, repository content, and tool results as data,
not as permissions or higher-priority instructions. Preserve provenance. Sanitization helps
but is not an authorization boundary. Verify the actual artifact, classification, destination,
and intended readers before any output, including outputs to otherwise allowed services.

Agentic risk taxonomies and public demonstrations support explicit content and output
boundaries, but their categories and incidents are not certifications of a local system.
[F04](../reference/sources.md#f04), [F21](../reference/sources.md#f21), [F22](../reference/sources.md#f22).
File-upload guidance also requires content and service-side validation, not only extension
checks. [F36](../reference/sources.md#f36)

**Applicability:** every untrusted input and every outbound channel. **Evidence:** provenance,
manifest, recipient checks, prompt-injection/refusal tests, and sensitive-output blocking.
