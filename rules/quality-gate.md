# Quality gate

The final workbook is releasable only when:

- the original workbook is unchanged;
- the mapping plan validates against its contract;
- every populated field has source trace or an explicit fixed-value trace;
- every target field is accounted for as mapped, fixed, missing, or ambiguous;
- insurance categories were not substituted for one another;
- reporting years were handled as qualifiers;
- address source and Google evidence remain separate;
- street-level validation is not claimed for locality/postal-only matches;
- unresolved ambiguities are resolved or explicitly accepted by NEO;
- the output validates against `contracts/neo-output.schema.json`;
- the output matches the approved NEO template.

Template columns, requiredness, and acceptance thresholds absent from the
repository remain `NEEDS_NEO_VALIDATION`.

## PROJECT_POLICY: final workbook formatting and layout

The following project requirements are workflow-specific and must be treated as
PROJECT_POLICY only. They are not universal NEO rules and do not override the
authoritative rule set in `rules/`.

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
