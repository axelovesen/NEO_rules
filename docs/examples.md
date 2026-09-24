# Examples

## Mapping plan shape

```json
{
  "planId": "plan-001",
  "workbookId": "broker-001",
  "mappings": [
    {
      "mappingId": "map-company",
      "targetField": "companyName",
      "source": { "kind": "column", "worksheet": "Sites", "column": "Account" },
      "decision": "Context identifies the legal insured name.",
      "confidence": 0.94,
      "trace": {
        "evidence": ["Sites!A1 header", "Repeated value across site rows"],
        "sourceRows": [2, 3]
      }
    }
  ],
  "ambiguities": []
}
```

An ambiguous “property value” field must not be assigned to building value
without supporting context. It should be returned as an open ambiguity with
`NEEDS_NEO_VALIDATION`.
