# standard-dictionaries

Reusable `data-dict::`-format data dictionaries for cross-matter wage-and-hour
data contracts (starting with combined timekeeping and payroll; more may be
added over time — e.g. combined HRIS — following the same pattern).

Each dictionary here describes a **target** schema: the intended shape of a
harmonized data frame that matter-specific load scripts (in each matter's
`scripts/jr_working/load/`) should converge on — not a live snapshot of any
one matter's actual output. Matter-specific extension columns (a vendor's
extra exception code, a labor-category path, etc.) are expected to keep
appearing beyond the core columns defined here; that matter's own import
scripts remain authoritative for those.

## Contents

- `dictionaries/time_combined.yml` — target schema for the combined
  timekeeping table (`time_combined`) produced by each matter's
  `time_combine.R`. Drafted 2026-09-21 from a code review of three matters:
  `id_fregozo_000062`, `apex_mangiafico_000092`, `crown_north_000151`.

## Format

Dictionaries follow the [data-dict spec](https://data-dict.tidyverse.org/spec.html)
(YAML, `$version: 0.1.0`), meant to be read by the `data-dict::` R package.
