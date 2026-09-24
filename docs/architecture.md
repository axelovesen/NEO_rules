# Architecture

Copilot Studio owns intake and AI interaction. Office Script performs
read-only inspection, then later deterministic bulk transformation. The AI
returns a mapping plan governed by this repository. Power Automate passes
artifacts between steps and does not make domain decisions. Google Maps
Geocoding API is the address authority. Output is written to a new workbook
that conforms to the approved NEO template; the broker workbook is immutable.

The repository deliberately separates semantic decisions from row processing:
one plan maps source structure, and Office Script applies it to every applicable
row with traceability.
