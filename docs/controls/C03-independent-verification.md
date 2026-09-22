# C03 — Independent verification

**Policy.** Separate exploratory review from acceptance verification. The acceptance reviewer
receives the artifact, approved requirements, explicit criteria, relevant dependencies, and
the tools needed to test them. The reviewer must be able to reject the producer's result.

Clean context does not mean missing requirements, and agreement between models is not proof.
The different reviewer patterns in [F01](../reference/sources.md#f01) and [F02](../reference/sources.md#f02)
support this distinction, but neither source certifies a local review.

**Applicability:** every control claim and material change. **Evidence:** independent inputs,
positive and negative tests, current commit/configuration, findings, and limits. A skipped
required check is not an executed verification. [F19](../reference/sources.md#f19)
