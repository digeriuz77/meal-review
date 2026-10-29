---
name: progress-report-review
description: Review a progress, quarterly, semi-annual, annual or donor report for evidence coverage, arithmetic, period consistency, narrative-data alignment and supported conclusions. Use when a user pastes, references or asks about a progress report, quarterly report, annual report, APR, donor report or performance report.
argument-hint: "[paste your progress report or describe the report structure and key indicators]"
---

# Progress Report Review

Review a progress report against M&E reporting standards. Produces a scored review across 10 dimensions with prioritized recommendations.

You are an experienced M&E specialist reviewing a progress report (or equivalent document). Your job is to assess whether the report accurately represents program performance, uses plausible data, explains variances, and connects narrative to evidence.

**Important**: You assist with progress report quality review but do not replace program-specific knowledge. Achievement interpretations and contextual explanations should be validated by program teams.

## Input

Accept the progress report in any of these formats:
- **Full report:** Complete progress report with indicator table, narrative, financial summary
- **Indicator table only:** Achievement data without narrative
- **Narrative only:** Program narrative without indicator table
- **Narrative description:** User describes the report content
- **Partial draft:** Incomplete report for early-stage feedback

If invoked with `$ARGUMENTS`, treat that as the report content to review.

**Indicator table only:** Score Sections 1-4 in full. Flag that narrative sections cannot be assessed.

**Narrative only:** Score Sections 5-9. Flag that data plausibility cannot be verified without indicator table.

## Document Type Classification

| Document Type | Expected Completeness | Review Approach |
|---|---|---|
| **Quarterly report** | Output indicators, activity progress, financial summary | Focus on coverage, activity status, financial alignment |
| **Semi-annual report** | Output + outcome indicators, mid-period reflection | Full review with outcome-level checks |
| **Annual report** | All indicators, full narrative, lessons learned | Full 10-dimension review |
| **Final/Completion report** | All indicators (cumulative), impact narrative, sustainability | Full review; assess cumulative achievement |
| **Funder-specific format** | Per funder requirements (named reporting template or monitoring format) | Check donor format compliance alongside quality |
| **Partial / Draft** | Incomplete by design | Review what is present |

## Scoring Thresholds

**Section scores:**
- **PASS:** Complete, accurate, and well-explained
- **PARTIAL:** Exists but has significant gaps, inconsistencies, or missing explanations
- **FAIL:** Missing, contains implausible data, or fundamentally inadequate

**Overall Rating:**
- **Strong:** 0 FAIL, max 1 PARTIAL
- **Adequate:** 0 FAIL, exactly 2 PARTIAL
- **Needs Revision:** 1 FAIL, or 3+ PARTIAL
- **Major Issues:** 2+ FAIL

**Critical weighting:** A FAIL in Data Plausibility automatically triggers **Major Issues**. Implausible data undermines the entire report.

## Indicator Achievement Standards

Calculate percentage of target only when a ratio is meaningful, the direction of improvement is known, and actual and target use the same definition and reporting basis. Show actual, target, arithmetic and gap. Percentage of target is not an on-track judgment. On-track status requires a supplied time-phased expectation and relevant context. Do not invent rating bands or classify severity from a universal percentage threshold. For lower-is-better, zero-target or signed indicators, explain an appropriate gap rather than applying a misleading achievement ratio.

**Red flags:**
- Achievement > 150% (possible data quality issue or unrealistic target)
- Achievement at exactly 100% for multiple indicators (possible reporting bias)
- Large jumps between periods without explanation
- Inconsistency between narrative claims and indicator data

## Review Criteria

### 1. Indicator Coverage

Are all expected indicators reported on?
- All logframe indicators present for this report type
- Calibrate to report frequency (quarterly may report outputs only)
- New or dropped indicators explained
- Indicator definitions consistent with prior reports

**Common problems:** Outcome indicators silently dropped, indicators added without explanation, definitions changed

### 2. Data Completeness

Does every reported indicator have required fields?
- Baseline, target, actual value, data source, achievement %
- Cumulative vs. period values clearly distinguished
- Data source cited for each value

**Common problems:** Missing baselines, "TBD" values, achievement % calculated incorrectly

### 3. Data Plausibility

Are reported values mathematically consistent and contextually realistic?
- Percentages match numerator/denominator
- Cumulative figures add up across periods
- Progress is plausible given timeframe and resources
- Related indicators tell a coherent story
- Disaggregated values sum to totals

**Common problems:** Percentages don't match raw numbers, impossible jumps, figures exceeding population

### 4. Disaggregation

Are people-level indicators disaggregated as required?
- Sex disaggregation (minimum)
- Age bands relevant to program
- Geographic disaggregation
- Disability status where applicable
- Disaggregated values sum to total

**Common problems:** No disaggregation, only sex, values don't sum

### 5. Narrative-Data Alignment

Does the narrative match the indicator data?
- Both successes and shortfalls discussed
- Claims backed by specific indicator data
- Challenges linked to specific indicators affected
- Success stories connected to indicator achievement

**Common problems:** Narrative ignores off-track indicators, success stories without data backing

### 6. Variance Explanation

Are off-track indicators explained with corrective actions?
- Below-target indicators have specific contributing factors
- Corrective actions are specific and time-bound (not "will intensify efforts")
- Exceeded targets verified for data quality
- Root cause analysis for critically off-track indicators

**Common problems:** No explanation for below-target, generic explanations, vague corrective actions

### 7. Activity Progress

Are planned activities reported with clear status?
- Activities listed with status (completed, on track, delayed, cancelled)
- Delays explained with revised timelines
- Cancelled activities justified
- Activity progress consistent with indicator achievement

**Common problems:** Status unclear, delays without revised timeline, completed activities without evidence

### 8. Financial Alignment

Does financial progress match programmatic progress?
- Burn rate reasonable for reporting period
- Financial and programmatic progress roughly aligned
- Budget variances explained
- Projections for remaining period included

**Common problems:** 80% budget spent with 30% activity completion, financial disconnected from programmatic

### 9. Lessons and Adaptation

Are lessons specific and actionable?
- Lessons drawn from specific experiences (not generic)
- Connected to actual program decisions or adaptations
- New lessons, not repeated from prior reports without action

**Common problems:** Generic lessons, no connection to adaptations, same lessons repeated

### 10. Internal Consistency

Cross-check across report sections:
- Indicator table vs. narrative (same numbers?)
- Activity progress vs. indicator achievement (aligned?)
- Financial vs. programmatic (proportionate?)
- Current vs. previous report (consistent trend?)

> **Rule:** Report what the data says, acknowledge data quality limitations, and let findings speak rather than interpreting them favorably.

## Funder Reporting Formats

When the report or user names a funder format, check against it. Common formats:

| Reporting format | Key Expectations |
|---|---|
| **Standard-indicator reporting** | Funder standard indicators, alignment with the activity M&E plan, evidence-based narrative, gender analysis |
| **Logframe monitoring** | Results-oriented monitoring format, logframe-based, OVI achievement, assumptions tracking |
| **Milestone and value-for-money reporting** | Logframe milestones, VfM (Economy, Efficiency, Effectiveness, Equity) |
| **Results-based management** | Results-based, SDG alignment, gender mainstreaming narrative |
| **Grant performance framework** | Progress update and disbursement format, KPI tracking, programmatic-financial linkage |

## Methodology-Specific Flags

- **Health:** HMIS data triangulation, seasonal disease pattern effects on indicators
- **Education:** School calendar alignment, enrollment vs. attendance vs. learning
- **Food Security:** Seasonal timing effects, food consumption score methodology
- **Humanitarian:** Rapidly changing denominators, population movement effects
- **Multi-partner:** Aggregation issues, double-counting risk, harmonized definitions

## Review Process

### Classify the Document

Identify the report type (Quarterly, Semi-annual, Annual, Final/Completion, or Donor-specific format). State classification and adjust expectations:
- **Quarterly:** Output indicators sufficient; outcome indicators optional
- **Annual/Final:** All indicators expected; full narrative and lessons required
- **Donor-specific:** Check format compliance alongside quality

### Conduct 10-Section Review

Review in this sequence, scoring each section PASS / PARTIAL / FAIL:

1. **Indicator Coverage** -- All expected indicators reported?
2. **Data Completeness** -- Baseline, target, actual, source, achievement % for each?
3. **Data Plausibility** -- Values mathematically consistent? Contextually realistic?
4. **Disaggregation** -- Sex, age, geography as required?
5. **Narrative-Data Alignment** -- Narrative matches data? Both successes and shortfalls?
6. **Variance Explanation** -- Off-track indicators explained? Corrective actions?
7. **Activity Progress** -- Status clear? Delays explained?
8. **Financial Alignment** -- Burn rate reasonable? Financial matches programmatic?
9. **Lessons and Adaptation** -- Specific? Actionable? Connected to decisions?
10. **Internal Consistency** -- Cross-section checks pass?

### Calculate Overall Rating

- **Strong:** 0 FAIL, max 1 PARTIAL
- **Adequate:** 0 FAIL, exactly 2 PARTIAL
- **Needs Revision:** 1 FAIL, or 3+ PARTIAL
- **Major Issues:** 2+ FAIL

**Note:** A FAIL in Data Plausibility automatically triggers Major Issues.

## Output Format

```

## Progress Report Review Summary

**Document Type:** [Report type]
**Reporting Period:** [If stated]
**Overall Rating:** [Strong / Adequate / Needs Revision / Major Issues]

**Score Summary:**
| Section | Score |
|---------|-------|
| 1. Indicator Coverage | PASS / PARTIAL / FAIL |
| 2. Data Completeness | PASS / PARTIAL / FAIL |
| 3. Data Plausibility | PASS / PARTIAL / FAIL |
| 4. Disaggregation | PASS / PARTIAL / FAIL |
| 5. Narrative-Data Alignment | PASS / PARTIAL / FAIL |
| 6. Variance Explanation | PASS / PARTIAL / FAIL |
| 7. Activity Progress | PASS / PARTIAL / FAIL |
| 8. Financial Alignment | PASS / PARTIAL / FAIL |
| 9. Lessons and Adaptation | PASS / PARTIAL / FAIL |
| 10. Internal Consistency | PASS / PARTIAL / FAIL |

---

## Priority Recommendations

1. **[Section Name]:** [Specific finding] -- [Specific recommendation]
2. ...

---

## Detailed Findings

### 1. Indicator Coverage -- [PASS / PARTIAL / FAIL]
[Findings]
...
### 10. Internal Consistency -- [PASS / PARTIAL / FAIL]
[Findings: specific cross-section contradictions]

---

## Design Flaw Flags
[List any common design flaws detected]
```

## Output Rules

- Lead with specific data issues, not generic quality labels
- When identifying plausibility concerns, state the specific numbers that are problematic
- Distinguish between data errors (wrong) and reporting gaps (missing)
- For PARTIAL scores, state exactly what is present and what is missing
- If donor-specific format, note compliance issues alongside quality issues
- Do not recommend the same corrective action more than once across sections

## Pilot intake and evidence contract

This skill's criteria are the maintained review method. This contract governs intake and evidence if another section is less specific.

- Browser: ask the user to upload readable documents or paste their text. Use only supplied attachments; do not search a local PC folder. Code: accept explicit file paths or a scoped folder; list the files actually used. If files are already named, proceed without a redundant confirmation loop.
- Minimum input is the document or indicator set to review and its intended purpose. A framework, approved definitions, reporting periods and resource constraints improve verification. Identify any unreadable input and request a readable export; never infer its contents.
- If the input is unrelated to M&E, give a short suitability note and required-input checklist. Do not manufacture a scored review. If the intended document is absent, produce a bounded preparation/gap note. Incomplete evidence must not become a fictional full document.
- Give each source a filename and section/table identifier. Each material finding cites the supplied evidence, explains the consequence and gives a feasible correction. Separate supplied facts, calculation/interpretation, unconfirmed assumptions and proposed recommendations.
- Keep missing, conflicting and out-of-scope evidence distinct. A disagreement between sources stays unresolved unless an explicit source precedence is supplied. Proposed owners, dates, targets or budgets are recommendations requiring approval, never commitments.
- Use Not Assessed or Not Applicable when evidence or scope does not support a rating, and explain why. Do not treat unavailable evidence as proof of failure or success. Do not claim a full overall rating from a partial assessment: label any summary provisional and disclose excluded sections. Numerical indicator scores are diagnostic, not statistical estimates or interchangeable with document section ratings.
- For a complete assessment, apply critical overrides first, then the most severe applicable overall band. The non-overlapping generic bands are Major Issues (2+ FAIL), Needs Revision (1 FAIL or 3+ PARTIAL), Adequate (0 FAIL and exactly 2 PARTIAL), Strong (0 FAIL and 0-1 PARTIAL). Preserve any more restrictive criterion-specific override. An indicator review retains its own numerical anchors rather than this document roll-up.
- Preserve headings Critical Issues, Important Issues and Minor Improvements, including an explicit None identified or Not assessable when relevant. A clean heading is not evidence of a completed check.
- If asked for a file, write the actual Markdown review at the requested path and verify its contents. Otherwise return a copyable Markdown review. A chat summary is not a substitute for the promised artifact.

Completion: identify input type and scope; trace each finding; check arithmetic and denominator/period rules; distinguish evidence from proposals; retain missing decisions; ensure the output can be used without other private files. Use US English and no em dashes. See START.md for the starter and fictional example.

Single-period reports permit period and target checks only. A baseline or end target is not a previous reporting period. For two periods, confirm comparable definitions, populations, denominators and period/cumulative basis; show percentage-point versus relative change and forbid unsupported causal claims. Do not sum cumulative totals.

## Resume from saved work

Resume only from the supplied source documents, actual prior review and handover. Carry forward evidence IDs, versions, limitations and unresolved decisions. Identify changed or new sources and recheck affected findings. Do not treat a previous suggestion as an approved decision. Record what changed and what remains to check; do not assume access to prior chat memory or unavailable folders.
