# Broker-to-NEO agent instructions

Use this repository as the rule and skill source for broker-to-NEO Excel
conversion. Read the applicable scoped instruction files before producing a
mapping plan.

The AI must analyze workbook structure and propose a reusable mapping plan.
It must not emit thousands of already-transformed location records. Deterministic
Office Script processing applies the plan to source rows after approval.

Do not invent NEO or Zurich requirements. For unsupported semantics, missing
authority, conflicting evidence, or unresolved template details, return an
ambiguity with source evidence and `NEEDS_NEO_VALIDATION`.
