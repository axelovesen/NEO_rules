# NEO address skill

Preserve the original broker address and separately retain the source-supported
candidate sent to Google Maps. Do not invent missing components before
geocoding. Keep source-derived and Google-derived components separately
traceable.

A locality or postal-code match is not street-level validation. Preserve house
number ranges, suffixes, leading zeros, and alphanumeric postal codes when
Google supports them. Apply the deterministic component mapping in
`rules/addresses.md`; unresolved country and template requirements are
`NEEDS_NEO_VALIDATION`.
