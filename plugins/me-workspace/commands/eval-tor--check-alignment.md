---
description: Check whether evaluation TOR questions align with the logframe indicators and M&E plan data collection
argument-hint: "[path to TOR file and logframe/M&E plan files]"
---

# /eval-tor--check-alignment: Evaluation Question Alignment Check

Compare an evaluation TOR's questions against the project's logframe and M&E plan to identify gaps, orphans, and misalignments between what the evaluation asks and what the project actually measured.

## Invocation

```
/me-workspace:eval-tor--check-alignment

[path to TOR, logframe, and M&E plan files]
```

## Workflow

### Step 1: Identify Documents

Three documents needed:
- **Required:** Evaluation TOR (or draft)
- **Required:** Logframe / Results Framework
- **Optional but valuable:** M&E Plan

If `$ARGUMENTS` contains paths, use them directly. If a folder path is given, search for candidates using the eval-tor skill's file discovery patterns. Confirm document identity with the user.

If no M&E plan is available, the check still works, it compares TOR questions against logframe indicators. The M&E plan adds data availability and method information.

### Step 2: Extract from TOR

Read the TOR and extract:
- Each evaluation question (numbered)
- DAC criterion each question maps to (if stated; infer if not)
- Any sub-questions
- Methodology requirements or expectations per question
- Scope boundaries (geographic, temporal, thematic)

### Step 3: Extract from Logframe

Read the logframe and extract:
- Full results hierarchy (goal → outcomes → outputs)
- Every indicator with its baseline, target, and data source
- Assumptions at each level
- Result-level descriptions

Build a flat indicator table:

| Result Level | Result Statement | Indicator | Baseline | Target | Data Source |
|---|---|---|---|---|---|

### Step 4: Extract from M&E Plan (if available)

Read the M&E plan and extract:
- Which indicators are actively tracked (some logframe indicators may not be measured)
- Data collection methods per indicator
- Data collection frequency
- Disaggregation categories
- Most recent data available
- Known data quality issues or gaps

### Step 5: Build Alignment Matrix

For each evaluation question, identify:
- Which logframe result(s) it maps to
- Which indicator(s) would answer it
- Whether data exists (from M&E plan) to answer it
- What methodology would be needed

```
| Eval Question | DAC Criterion | Logframe Result(s) | Indicator(s) | Data Available? | Method Needed |
|---|---|---|---|---|---|
| Q1: [text] | Effectiveness | Outcome 1.1 | Ind 1.1.1, 1.1.2 | Yes (annual survey) | Secondary analysis |
| Q2: [text] | Impact | Goal | None mapped | No baseline comparison | Would need quasi-experimental |
```

### Step 6: Identify Gaps and Issues

Check for these specific problems:

**Question-side gaps:**
- Evaluation questions with NO corresponding logframe indicators
- Questions requiring counterfactual data when no comparison design exists
- Questions about results levels not in the logframe scope
- Questions that duplicate or substantially overlap each other
- DAC criteria referenced in questions but not represented in logframe

**Indicator-side gaps:**
- Logframe indicators at outcome/goal level NOT addressed by any evaluation question
- Indicators where data exists but no question uses it (missed opportunity)
- Indicators where the M&E plan shows no data was collected (evaluation can't verify)

**Methodology gaps:**
- Questions requiring methods not supported by available data
- Mixed-methods claims without both quantitative and qualitative data sources
- Impact questions without comparison group or baseline

**Scope misalignments:**
- TOR geographic scope wider/narrower than logframe coverage
- TOR temporal scope doesn't match implementation period
- TOR asks about activities/outputs but evaluation type is impact-level

Classify each finding: **Critical**, **Important**, or **Minor** per the eval-tor skill's severity framework.

### Step 7: Generate Output

## Output Format

```markdown
## Evaluation Question Alignment Check

**TOR:** [filename]
**Logframe:** [filename]
**M&E Plan:** [filename or "not provided"]

### Alignment Matrix

| # | Evaluation Question | DAC Criterion | Logframe Result | Indicators | Data Available | Alignment |
|---|---|---|---|---|---|---|
| Q1 | [abbreviated text] | Effectiveness | Outcome 1.1 | 1.1.1, 1.1.2 | Yes | ALIGNED |
| Q2 | [abbreviated text] | Impact | Goal | None | No comparison | GAP |
| Q3 | [abbreviated text] | Relevance | - | - | - | NO MATCH |

### Coverage Summary

- **Evaluation questions:** [N] total
- **Fully aligned (question + indicator + data):** [N]
- **Partially aligned (question + indicator, no data):** [N]
- **No match (question has no logframe anchor):** [N]
- **Logframe results NOT covered by any question:** [list]

### Critical Issues
1. [Issue, why it matters, specific fix]

### Important Issues
1. [Issue, why it matters, specific fix]

### Minor Improvements
1. [Improvement, rationale]

### Recommendations

**Questions to revise:**
- Q[N]: [Current text] → Suggested: "[revised text that maps to available indicators]"

**Questions to add:**
- [Suggested question targeting uncovered logframe result]

**Questions to remove or merge:**
- Q[N] and Q[N]: [overlap explanation, suggest merged version]

**Data gaps to address in TOR methodology section:**
- [Indicator X has no data source, TOR should specify primary data collection]
```

## Notes

- The goal is alignment, not perfection. Not every logframe indicator needs its own evaluation question. Evaluations are strategic, they focus on key results.
- Evaluation questions at outcome/impact level that map to multiple indicators are normal and expected.
- If the logframe has 20+ indicators, it's fine for the evaluation to focus on 8-12 key ones. Flag only goal/outcome-level indicators that are completely ignored.
- When recommending revised question text, provide specific language the user can insert, not abstract advice.
- If the TOR is post-hoc (evaluation already underway), reframe as lessons for future TOR development rather than required fixes.
