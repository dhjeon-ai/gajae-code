---
name: ralplan
description: "GJC consensus planning workflow that creates PRD and test-spec artifacts before durable execution."
---

# GJC Ralplan

Use this skill only for the approved `ralplan` workflow surface.

## Public invocation

- CLI/runtime endpoint: `gjc ralplan ...`
- Optional state endpoint: `gjc state ...`

## Contract

1. Convert clarified requirements into a concise PRD plus test specification under `.omx/plans/`.
2. Include decisions, drivers, rejected alternatives, risks, and verification shape.
3. Recommend only approved follow-up surfaces: `gjc ultragoal` for durable goal tracking and `gjc team` for coordinated parallel execution.
4. Do not expose non-approved workflow names or external connector surfaces.
5. Stop after a plan/handoff artifact; do not implement unless the user explicitly launches an execution workflow.

## Required artifacts

- `.omx/plans/prd-<slug>.md`
- `.omx/plans/test-spec-<slug>.md`
- optional `.omx/ralplan/handoff-<slug>.json`
