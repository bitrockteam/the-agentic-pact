# Agentic system design review

Use this review before enabling a new agentic workflow or materially expanding an existing
one.

## System boundary

- What outcome is the system responsible for?
- Which components are models, tools, services, users, and workloads?
- What data can each component read, transform, retain, or emit?
- Which actions have external, irreversible, financial, privacy, or administrative impact?

## Control review

For each applicable control C01–C12, record the requirement, implementation, evidence,
status, residual risk, owner, and next action. Do not mark a control verified from a design
description alone.

## Approval and recovery

- What is proposed, and what is committed?
- Who can approve the actual effect?
- What changes invalidate the approval?
- What happens on timeout, partial success, duplicate delivery, or uncertain outcome?
- How is the workflow stopped, revoked, and recovered?
