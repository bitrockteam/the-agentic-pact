# C06 — Production through a bounded executor

Do not place administrative shells or unrestricted production credentials in an agent's
free execution context.

Actions against live systems must pass through typed, authorized, and limited operations.
High-impact actions require human approval. The executor must enforce the operation's
scope rather than relying on the model to obey a description of the scope.
