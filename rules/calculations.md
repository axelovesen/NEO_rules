# Calculations and fixed values

Normative fixed values:

- `clientLocationId` is blank.
- `biType` is exactly `Loss of gross profit`.
- `numberOfWorkingDays` is numeric `365`, not text and not a formatted date.

If the broker source contains a value that conflicts with one of these fixed
project-policy values, do not silently overwrite the conflict. Preserve the
source value in the mapping trace/evidence, apply the fixed project-policy value
to the NEO output, and record the conflict as an ambiguity or documented
conflict for follow-up review. This rule applies only to the existing fixed-value
policies above.

Intermediate calculation results must not be rounded. Preserve full numeric
precision during calculation. Rounding may occur only at the final required
output/display step, and only if an authoritative final display precision rule
already exists elsewhere in the repository; otherwise no new decimal precision
rule is introduced here.

No other calculation, aggregation, conversion, imputation, rounding, currency
conversion, or default is authorized by the current repository. Such behavior
requires an explicit NEO-approved rule and must be marked
`NEEDS_NEO_VALIDATION` until then.
