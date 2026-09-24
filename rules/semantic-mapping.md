# Semantic mapping rules

1. Inspect workbook structure first: worksheet names, header bands, merged
   cells, formulas, data types, repeated sections, and representative rows.
2. Interpret a field from combined evidence: header meaning, neighboring labels,
   worksheet context, units/currency, formulas, and row relationships. Similar
   wording alone is insufficient.
3. Map only when the source meaning is supported. A value's presence never
   authorizes changing its category.
4. A mapping plan must be reusable across all applicable rows and must include
   source selectors, transformation, rationale, confidence, and traceability.
5. Preserve missing values. Only explicit fixed-value rules may populate a
   missing source value.
6. Separate `companyName` from `locationName`; never use one as a silent
   fallback for the other.
7. Treat reporting year as metadata qualifying a value, never as a value
   category.
8. Contradictions, multiple plausible fields, and unsupported fields become
   ambiguities with `NEEDS_NEO_VALIDATION`.
