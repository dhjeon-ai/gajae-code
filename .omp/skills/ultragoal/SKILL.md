---
name: ultragoal
description: "GJC durable multi-goal execution ledger over Codex goal mode artifacts."
---

# GJC Ultragoal

Use this skill only for the approved `ultragoal` workflow surface.

## Public invocation

- CLI/runtime endpoint: `gjc ultragoal ...`
- State endpoint when needed: `gjc state ...`

## Contract

1. Maintain durable goals in `.omx/ultragoal/goals.json` and audit events in `.omx/ultragoal/ledger.jsonl`.
2. Checkpoint each goal with evidence after verification passes.
3. Use `gjc team` only when coordinated worker execution materially improves throughput or confidence.
4. Final completion requires quality evidence: cleanup review, verification, and code review.
5. Do not expose non-approved workflows or external connector surfaces.

## Stop condition

Stop when all goals are terminal and the final audit checkpoint is recorded.
