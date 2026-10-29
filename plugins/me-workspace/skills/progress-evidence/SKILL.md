---
name: progress-evidence
description: Check progress-report evidence, indicator coverage, and period-to-period comparisons. Use when reported results need a traceable evidence review with gaps and supported trends identified.
---

# Progress evidence and trend checking

## Purpose and trigger
Check whether progress claims are supported, indicators are covered, and comparisons use compatible periods and denominators. This does not verify source data independently or establish causal attribution.

## Minimum inputs
- At least one progress report or results extract.
- Results framework or indicator definitions when available.
- A prior comparable period for trend analysis. Without it, perform single-period evidence checks only.

Accept explicitly uploaded files or a user-designated folder and file list. Upload mode uses attachments/text only. Folder mode inspects only the named folder and lists files used. Confirm ambiguous reports. State intake mode.

## Starter prompt
> Use progress-evidence on the attached files [or folder: path]. Check indicator coverage and evidence, and compare periods only when definitions, cohorts, denominators, and periods are comparable. Keep the exact headings Critical Issues, Important Issues, and Minor Improvements. Mark single-period analysis as not a trend assessment.

## Procedure
1. Confirm intake mode, report period, report type, framework, and whether the request is coverage, data checks, trends, or all three.
2. Extract every indicator value with period, unit, numerator/denominator if available, population/cohort, cumulative or period basis, target, source, and disaggregation. Cite `filename#heading`, page, table, or row.
3. Compare the expected indicator set with reported coverage. Distinguish “not reported in supplied material” from “not collected.”
4. Recalculate percentages only when numerator, denominator, unit, and population are clear. Check whether disaggregated values reconcile to totals. State arithmetic and source IDs.
5. Assess evidence quality and narrative alignment. Separate reported claims from verified arithmetic and interpretation. Flag missing source, unsupported explanation, and data-quality limitation.
6. For trends, compare only matching definitions, units, populations/cohorts, denominators, reporting periods, and cumulative-versus-period basis. Show mismatches and decline comparison where necessary.
7. Do not infer trend direction from a single period. Do not treat cumulative values as period values. Do not infer causal attribution from pre/post change alone.
8. Return the report structure below and prioritize issues by severity. Preserve the exact three issue headings.

## Output structure
- Scope and intake mode
- Sources and evidence register
- Coverage and value reconciliation table
- Comparison eligibility table: indicator; periods; definition/population/denominator match; cumulative or period basis; eligible comparison; reason
- Supported findings and limitations
- Decisions and source data needed

Include these exact headings in the produced artifact:

```markdown
## Critical Issues
## Important Issues
## Minor Improvements
```

## Rules
Keep denominators, periods, cohort/population, units, and cumulative or period basis visible in every reported comparison. Distinguish counts of people from service contacts or events. Do not make targets, thresholds, or status bands up. Preserve indicator definitions; flag silent changes. A report may support a mathematical check without supporting the narrative explanation. Use “not assessable from supplied files” where appropriate.

## Reconciliation checks
- Match indicator labels and definitions across periods before comparing values. Similar names do not prove identical definitions.
- Keep reporting period and value basis visible. Do not subtract a cumulative total from a single-period count without a valid calculation path.
- For percentages, verify numerator and denominator definitions, population universe, unit, and observation window. Numeric denominator counts may differ across periods when population size or coverage changes; compare rates only when denominator meaning and population composition are sufficiently comparable, and disclose differences that limit interpretation.
- For disaggregation, check whether categories are exhaustive and mutually exclusive before summing. Report unclassified or missing categories separately.
- For counts, look for duplicate units or repeated service contacts when the source permits the check.
- Reconcile narrative claims to table values and sources. A success story illustrates an experience but does not establish prevalence.
- Compare achievements to explicit period targets only when the target covers the same period and definition.
- Treat target revisions as changes requiring documentation, not evidence that prior performance changed.
- A blank field is not zero. “Not reported” does not establish that data were not collected.
- Do not project trajectory without adequate comparable observations and a justified model. A simple arithmetic rate is descriptive, not a prediction.
- When comparing percentage changes, distinguish percentage-point change (subtract the two percentages) from relative percent change (change divided by the earlier value). State which calculation is shown; do not use “percent increase” ambiguously.

Use **Critical Issues** for a defect that invalidates a current material finding or its intended use, or presents a serious ethical risk. **Important Issues** affect usefulness or confidence but still allow a bounded output. **Minor Improvements** are editorial or detail refinements with limited effect on conclusions. An unsupported claim that does not appear in the supplied material is a limitation or preventive caution, not an actual critical defect. State evidence and a practical correction for each actual issue. If none are identified at a severity, write “None identified from supplied files.”

## Missing, conflicting, or unsuitable inputs
- Single period only: report coverage and evidence checks; state clearly that no trend can be assessed.
- Missing definitions or denominators: do not calculate rates or compare affected values.
- Conflicting values: show each source and evidence ID, then flag reconciliation as needed.
- Missing expected indicator framework: assess supplied indicators only; do not claim complete coverage.
- Non-M&E request: explain the scope and stop.

## Completion checklist
- Exact severity headings are present.
- Periods, denominators, populations/cohorts, units, and cumulative/period basis are explicit.
- Single-period inputs are not described as trends.
- Missing data is not treated as zero or proof of noncollection.
- Arithmetic, source claims, and interpretations are separated.
- Comparisons use compatible definitions and periods or are declined.
- No causal attribution is inferred from simple pre/post change.

## Interruption and resumption
If interrupted, preserve the actual evidence review, extracted values, evidence register with source filenames/versions or dates, and unresolved reconciliation decisions. Resume only from files and handover supplied for the resumed task. Check whether sources changed and flag differences. Record recalculations and edits. Never upgrade a proposal, assumption, or pending decision into an approved result or correction.
