# NEO quality skill

Apply `rules/quality-gate.md` before output. A result is not ready when required
mapping evidence, address traceability, validation status, or ambiguity
resolution is missing. The original workbook must remain unchanged and the
output must validate against `contracts/neo-output.schema.json`.

## PROJECT_POLICY: final workbook formatting and layout

The following requirements are project-specific output rules only. They are not
universal NEO rules and must not be promoted beyond this workflow.

- Final workbook contains exactly two sheets: `template_locations` and
  `explanations`.
- `template_locations` is always the first sheet.
- The template header starts at `A10`.
- No frozen panes exist in the final workbook.
- All visible font is black.
- All other authoritative template styling is preserved.
- Numeric Excel values remain numeric and are never stored as text merely for
  formatting.
- Numeric values use comma thousands separators.
- Integers display with no decimals.
- Values containing decimals are rounded only at the final required step and
  displayed with exactly one decimal.
- Month values remain numeric months and are never converted to days merely for
  output formatting.
- Validation uncertainty must not introduce custom fill colors or font colors.
- The final workbook must preserve the authoritative template layout and
  formatting.
