# Data flow

```text
broker workbook
  -> Office Script inspection (read-only)
  -> broker-inspection.schema.json
  -> AI semantic analysis
  -> mapping-plan.schema.json
  -> Google candidate construction and geocoding
  -> geocoding-result.schema.json
  -> deterministic Office Script bulk application
  -> quality gate
  -> new NEO-template workbook
```

Failures and ambiguities stop or quarantine the affected output; they are not
converted into guessed values.
