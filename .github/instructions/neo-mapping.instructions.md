# NEO mapping skill

- Infer meaning semantically from workbook context; do not use a hard-coded
  broker-header dictionary.
- A mapping must identify its source worksheet/column or an explicit constant,
  interpretation rationale, confidence, and source trace.
- Never map a source category into a different NEO category merely because a
  numeric value exists.
- Missing source values remain missing unless an explicit fixed-value rule in
  `rules/` applies.
- Return ambiguities for collisions, weak evidence, unsupported fields, and
  unresolved NEO requirements.
- Emit a reusable mapping plan. Do not emit one AI decision per output row.
