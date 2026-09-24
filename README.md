# Broker-to-NEO Conversion Rules

This repository is the authoritative rule and skills source for an agent that
converts arbitrary broker Excel workbooks into the approved NEO workbook
template. It contains semantic interpretation guidance, contracts, validation
rules, and quality gates. It does not contain application code.

## Architecture

1. Microsoft Copilot Studio receives an arbitrary broker workbook.
2. An Office Script reads worksheets, headers, rows, values, and formulas without
   modifying the source workbook.
3. AI identifies source meaning and returns a reusable semantic mapping plan,
   not transformed location records.
4. Rules in this repository guide mapping, calculations, addresses, and quality
   control.
5. Google Maps Geocoding API is the external authority for geocoding and
   returned address components.
6. Power Automate orchestrates only.
7. Office Scripts apply the approved mapping plan deterministically in bulk.
8. The final workbook conforms to the authoritative NEO template; the original
   workbook remains unchanged.

## Repository layout

- `.github/copilot-instructions.md` and `.github/instructions/` — agent skills
- `rules/` — semantic, value, calculation, address, ambiguity, and gate rules
- `contracts/` — machine-readable inspection, mapping, geocoding, and output
  contracts
- `docs/` — architecture, flow, and examples

## Authority and unresolved requirements

Rules explicitly stated in the conversion brief are normative. The repository
contained no prior NEO field specification or Zurich internal requirements.
Any provisional field name, template detail, currency rule, rounding rule,
country-code rule, or required/optional status not stated in the brief is
marked `TODO` or `NEEDS_NEO_VALIDATION` and must not be silently implemented.

## Status

This is the initial rule structure. No unsupported NEO business rule has been
invented.

## PROJECT_POLICY: final workbook formatting and layout

The following are project-specific output requirements only. They are not
universal NEO rules and must not be treated as authoritative beyond this
workflow.

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