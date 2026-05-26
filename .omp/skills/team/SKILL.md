---
name: team
description: "GJC coordinated worker runtime for parallel implementation and verification lanes."
---

# GJC Team

Use this skill only for the approved `team` workflow surface.

## Public invocation

- CLI/runtime endpoint: `gjc team ...`
- Team API endpoint: `gjc team api <operation> --input '<json>' --json`
- State endpoint when needed: `gjc state ...`

## Contract

1. Use team mode for durable coordinated execution with explicit tasks, owners, verification, and shutdown.
2. Keep workers inside assigned scopes and require terminal task evidence before checkpointing an ultragoal.
3. Use worktrees/mailboxes/state files as runtime internals; expose status through `gjc team status` and API operations.
4. Do not mutate `.omx/ultragoal` from workers; the leader owns ultragoal checkpoints.
5. Do not expose non-approved workflows or external connector surfaces.

## Stop condition

Stop when all team tasks are terminal, verification evidence is collected, and `gjc team shutdown <team>` has completed.
