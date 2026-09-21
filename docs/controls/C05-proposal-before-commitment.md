# C05 — Proposal separated from commitment

The system must have a gate between proposing an outcome and causing the corresponding
effect. The gate must inspect the actual content, object, destination, permissions, and
consequences.

For shared code, this normally means a branch, required checks, independent approval, and
human-controlled integration. For other effects, use the gate appropriate to the action;
a pull request is not a substitute for approving an external message, export, payment, or
administrative change.
