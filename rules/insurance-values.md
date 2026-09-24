# Insurance value rules

## Categories

Only explicit source evidence may populate the corresponding category:

- `buildingValue`: building, property, premises, or equivalent structural
  value when context supports that meaning.
- `machineryEquipment`: machinery, plant, equipment, production equipment, or
  equivalent operational equipment value.
- `contentsValue`: contents, furniture, fixtures, or general contents value.
- `stockSuppliesValue`: stock, inventory, raw materials, goods, or supplies.
- `otherPdValue`: explicitly identified other property-damage value.
- `biValueReported`: explicitly reported business-interruption value.
- `biOther`: explicitly reported BI “other” value.

These are semantic categories, not a synonym dictionary. Do not transfer a
source value between categories because another category is empty.

## Reporting years

A reporting year is a temporal qualifier and must never be treated as an
insurance value category. If equivalent values for the same category are
reported for multiple years, select the latest **explicitly reported relevant**
year, retain the selected year and source trace, and record superseded
equivalent candidates. If the years are not comparable, relevance is unclear,
or the latest value is inferred rather than explicitly reported, return an
ambiguity.

Missing source values remain missing unless an explicit fixed-value rule applies.
Currency, unit conversion, aggregation, and rounding are `TODO` unless the
source and NEO template provide authoritative instructions.
