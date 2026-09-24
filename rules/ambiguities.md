# Ambiguity handling

Return an ambiguity rather than inventing a mapping when evidence is absent,
conflicting, non-comparable, or only weakly inferred. Each ambiguity includes:

- stable `ambiguityId`
- affected target field or address layer
- source trace(s)
- competing interpretations
- reason and confidence
- `NEEDS_NEO_VALIDATION` when NEO authority is required
- resolution status

Typical cases include unclear insurance category, company/location collision,
multiple year candidates, missing unit or currency, duplicate source fields,
and non-street-level geocoding.
