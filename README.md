# The Agentic Pact

The Agentic Pact is a practical baseline for designing, implementing, and evaluating
agentic systems and workflows.

It exists to help a team explore agentic solutions without losing important questions
along the way: who is allowed to act, what the system can reach, what must be reviewed,
how effects are verified, and what evidence remains after execution.

This repository is a working engineering reference. It is not a vendor certification,
an assurance that a system is safe, or a replacement for product-specific security,
legal, privacy, or operational review.

## The core agreement

Every proposed agentic system should:

1. use the simplest architecture that is adequate;
2. assign one accountable writer to each shared artifact or state;
3. separate production from independent verification;
4. verify authority at entry and again at action time;
5. separate proposals from commitments and side effects;
6. execute production actions only through bounded, typed operations;
7. make identity and delegation explicit;
8. use credentials only for their intended recipient and scope;
9. keep secrets outside unconstrained execution;
10. treat content as data, never as authority;
11. enforce least capability, finite limits, and a tested stop path;
12. preserve observable, protected evidence of requests, decisions, and effects.

The detailed controls are in [`docs/controls/`](docs/controls/). They are the normative
core of this repository.

## How to use this repository

Use the Pact at the beginning of discovery and design, not only during implementation.

1. Define the system boundary, intended outcome, users, data, tools, and side effects.
2. Select the operating profile in [`docs/profiles/operating-profiles.md`](docs/profiles/operating-profiles.md).
3. Review every applicable control and record what is verified, partial, unsatisfied,
   unknown, or not applicable.
4. Design the approval, verification, identity, secret, limit, and audit paths before
   enabling the agent.
5. Test both permitted and refused actions, including failure and uncertain-outcome paths.
6. Record evidence and residual risks in a review artifact that another person can inspect.

The Pact does not require a pull request for every kind of action. The required gate must
match the actual effect: code integration, an external message, a data export, a payment,
an administrative change, and a document edit have different approval and evidence needs.

## Language and attribution

The documentation is intentionally written in English so that it can be used by
international engineering teams.

**Author and maintainer:** Franco Geraci (Voloire).

## Status

This is an evolving engineering baseline. A statement in this repository is one of:

- a **policy** adopted by this Pact;
- a **source-backed fact** with a stated scope;
- an **inference** that must not be presented as a universal requirement.

See [`docs/methodology/evidence-and-measurement.md`](docs/methodology/evidence-and-measurement.md)
for the distinction between documentation, configuration, and observed behaviour.
