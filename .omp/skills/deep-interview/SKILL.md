---
name: deep-interview
description: "GJC Socratic requirements interview for clarifying ambiguous work before planning or execution."
---

# GJC Deep Interview

Use this skill only for the approved `deep-interview` workflow surface.

## Public invocation

- CLI/runtime endpoint: `gjc deep-interview ...`
- Structured question endpoint when needed: `gjc question --input '<json>' --json`
- State endpoint when needed: `gjc state ...`

## Contract

1. Ask one concise, material question at a time when requirements are ambiguous.
2. Prefer local repo inspection over asking when facts are discoverable safely.
3. Produce a clarified handoff artifact under `.omx/specs/` or `.omx/interviews/` when the interview is complete.
4. Do not expose or recommend workflows outside the approved four: `deep-interview`, `ralplan`, `ultragoal`, `team`.
5. Use only local/inline tools and the private GJC runtime endpoints above.

## Stop condition

Stop when ambiguity is low enough to hand off to `gjc ralplan`, `gjc ultragoal`, or `gjc team`, or when the user explicitly cancels.
