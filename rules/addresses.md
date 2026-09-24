# Address rules

## Evidence layers

Keep these layers separate and traceable:

1. `originalBrokerAddress`: the unmodified source address.
2. `sourceAddressCandidate`: a candidate assembled only from source-supported
   components for Google.
3. `googleAddress`: the raw Google result and parsed components.
4. `neoAddress`: deterministic output fields with the evidence for each field.

Never invent a street, number, postal code, locality, or country before
geocoding. Google Maps Geocoding API is the external authority for geocoding
and returned components. A locality- or postal-code-level match is not
street-level validation.

## Component contract

| Google component type | NEO field | Condition |
|---|---|---|
| `street_number` | `addressNumber` | Preserve ranges, suffixes, leading zeros, and alphanumeric values when returned. |
| `route` | `addressLine1` | Use returned route; do not synthesize one. |
| `postal_code` | `postalCode` | Preserve alphanumeric formatting returned by Google. |
| `locality` | `city` | Use as city only when component type is present. |
| `postal_town` | `city` | Fallback only when `locality` is absent; record component type. |
| `country` | `country` | Preserve returned long name and short code separately in trace. |
| `geometry.location.lat` | `latitude` | Google-derived only. |
| `geometry.location.lng` | `longitude` | Google-derived only. |

`street_number` plus `route` may support street-level validation only when the
Google result and match metadata support that conclusion. Otherwise retain a
lower validation level and an ambiguity.

**TODO / NEEDS_NEO_VALIDATION:** define accepted countries, NEO country format,
Google request parameters, candidate selection thresholds, and exact output
status enum.
