# NEO target field catalog

The repository has no prior NEO template specification. The names below are a
machine-friendly **provisional 25-field catalog** derived only from the
conversion brief. Field type and business meaning are normative where stated;
template placement, requiredness, units, currency, and exact NEO labels are
`NEEDS_NEO_VALIDATION`.

| # | Property | Meaning |
|---:|---|---|
| 1 | `companyName` | Insured/company name; must not be used as location name. |
| 2 | `locationName` | Name identifying the insured location/site. |
| 3 | `clientLocationId` | Client location identifier; fixed blank. |
| 4 | `addressLine1` | Street address text, excluding a separately represented number when possible. |
| 5 | `addressNumber` | House number, range, suffix, or alphanumeric number. |
| 6 | `postalCode` | Postal code, preserving source/Google-supported formatting. |
| 7 | `city` | City/locality. |
| 8 | `country` | Country name or code; exact NEO representation is TODO. |
| 9 | `latitude` | Google-derived latitude. |
| 10 | `longitude` | Google-derived longitude. |
| 11 | `buildingValue` | Explicit building/property value. |
| 12 | `machineryEquipment` | Explicit machinery/equipment value. |
| 13 | `contentsValue` | Explicit contents value. |
| 14 | `stockSuppliesValue` | Explicit stock/supplies value. |
| 15 | `otherPdValue` | Explicit other property-damage value. |
| 16 | `biValueReported` | Explicit business-interruption value reported by the broker. |
| 17 | `biOther` | Explicit business-interruption “other” value. |
| 18 | `biType` | Fixed value `Loss of gross profit`. |
| 19 | `numberOfWorkingDays` | Fixed numeric value `365`. |
| 20 | `currency` | Currency attached to a value; source/NEO rule is TODO. |
| 21 | `occupancy` | Source-supported use/occupancy description; semantics TODO. |
| 22 | `constructionYear` | Source-supported construction year; validation TODO. |
| 23 | `floorArea` | Source-supported area; unit and field placement TODO. |
| 24 | `geocodingStatus` | Address validation outcome, not a broker value. |
| 25 | `sourceRowReference` | Trace to source row(s) used for the output record. |

**NEEDS_NEO_VALIDATION:** Confirm the exact 25 target columns, labels, types,
requiredness, ordering, units, and whether fields 20–25 belong in the final
NEO template or only in the trace/audit layer.
