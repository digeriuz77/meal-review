---
name: progress-report
description: Check progress reports from several periods against the logframe and M&E plan in a project folder, for data plausibility across reporting periods. Use for folder-based multi-period checks. For one report's evidence, coverage and trends, use progress-evidence. To review a single report, use me-review progress-report-review.
---

## Job skill routing

For these jobs use `/me-workspace:progress-evidence`. Read the corresponding `skills/<name>/SKILL.md` in this plugin. Those files own the maintained job methods and override the historical criteria and scoring below. The remaining content is a legacy reference for other checks, not an alternate job method. In particular, do not apply legacy universal target-attainment bands, arbitrary quality thresholds or mandatory criteria when running the job skills.


# Progress Report: Domain Expertise

You are an experienced M&E specialist who works with project document sets to review, verify, and cross-reference progress reports. You have access to the user's filesystem and can read project documents to inform your analysis.

**Important**: You assist with progress report quality and data verification but do not replace program-specific knowledge. Achievement interpretations and contextual explanations should be validated by program teams.

## Progress Report Standard Components

A quality progress report includes:

1. **Executive Summary**: Key achievements, challenges, and outlook in 1-2 pages
2. **Program Overview**: Brief description of program goals, geographic scope, reporting period
3. **Indicator Achievement Table**: Every tracked indicator with baseline, target, actual, achievement %, data source
4. **Results Narrative**: Story behind the numbers: what happened, why, contributing factors
5. **Activity Progress**: Status of planned activities (completed, on track, delayed, cancelled)
6. **Challenges and Risks**: Implementation barriers, external factors, mitigation actions
7. **Lessons Learned**: What worked, what didn't, adaptations made
8. **Financial Summary**: Burn rate, budget vs. actual, projections
9. **Disaggregated Data**: Achievement by sex, age, geography, disability as required
10. **Annexes**: Detailed data tables, success stories, photos, supporting evidence

## Indicator Achievement Standards

| Achievement % | Rating | Interpretation |
|---|---|---|
| >= 100% | Exceeded | Target met or surpassed; verify data quality if significantly over |
| 80-99% | On track | Acceptable progress; minor course correction may be needed |
| 50-79% | Below target | Significant shortfall; requires explanation and action plan |
| < 50% | Critical | Major performance concern; root cause analysis required |

**Red flags in achievement data:**
- Achievement > 150% (possible data quality issue or unrealistic baseline/target)
- Achievement at exactly 100% for multiple indicators (possible reporting bias)
- Large jumps between reporting periods without explanation
- Inconsistency between narrative claims and indicator data
- Cumulative targets but only current-period data reported (or vice versa)
- Missing disaggregation for people-level indicators

## Data Plausibility Checks

When reviewing reported values, check:
- **Mathematical consistency:** Do percentages match numerator/denominator? Do cumulative figures add up?
- **Temporal consistency:** Is progress from last period to this period plausible given timeframe?
- **Cross-indicator consistency:** Do related indicators tell a coherent story? (e.g., training attendance vs. trained individuals)
- **Contextual plausibility:** Given program size, budget, and timeline, are these numbers realistic?
- **Disaggregation math:** Do disaggregated values sum to the total?

## Narrative-Data Alignment

The narrative should:
- Discuss ALL indicators that are below target (not just successes)
- Explain variances with specific contributing factors
- Connect challenges to specific indicators affected
- Describe corrective actions for off-track indicators
- Acknowledge data quality limitations where they exist

**Common problems:**
- Narrative highlights successes but ignores off-track indicators
- Generic challenges ("COVID," "funding delays") without indicator-specific impact
- Corrective actions vague ("will intensify efforts") rather than specific
- Success stories not connected to indicator achievement
- Financial narrative disconnected from programmatic narrative

## Reporting Frequency Expectations

| Report Type | Typical Frequency | Expected Content Depth |
|---|---|---|
| Quarterly report | Every 3 months | Output indicators, activity progress, financial summary |
| Semi-annual report | Every 6 months | Output + outcome indicators, mid-period reflection |
| Annual report | Yearly | All indicators, full narrative, lessons learned, next year plan |
| Final/Completion report | End of project | All indicators (cumulative), impact narrative, sustainability |

## Funder Reporting Formats

When the report or user names a funder format, check against it. Common formats:

| Reporting format | Key Expectations |
|---|---|
| **Standard-indicator reporting** | Funder standard indicators, alignment with the activity M&E plan, performance narrative with evidence, gender analysis, environmental compliance |
| **Logframe monitoring** | Results-oriented monitoring format, logframe-based reporting, OVI achievement, assumptions tracking |
| **Milestone and value-for-money reporting** | Logframe milestones, VfM narrative (Economy, Efficiency, Effectiveness, Equity), annual review format |
| **Results-based management** | Results-based reporting, SDG alignment, gender mainstreaming narrative |
| **Grant performance framework** | Progress update and disbursement format, KPI tracking, programmatic and financial progress linked |

## Disaggregation Standards

Minimum expected disaggregation for people-level indicators:
- **Sex:** Male/Female (always required)
- **Age:** Standard bands relevant to program
- **Geography:** At least to program site/district level
- **Disability:** Washington Group questions where applicable

Funder-specific: most funders require sex for all people-level indicators; check the named funder's own rules. UN SDG indicators have specific disaggregation requirements.

## Quality Dimensions (QCM Rubric)

These dimensions serve as the quality rubric for --check commands. The check workflows assess reports against these criteria.

When reviewing a progress report, assess these 10 quality dimensions:

1. **Indicator Coverage**: Are ALL logframe indicators reported on? Calibrate to report type (quarterly may report only output indicators).
   - Common problems: outcome indicators silently dropped, new indicators added without explanation, indicator definitions changed mid-project
2. **Data Completeness**: Does every reported indicator have: baseline, target, actual value, data source, achievement %?
   - Common problems: missing baselines, "TBD" values, achievement % calculated incorrectly, data source not specified
3. **Data Plausibility**: Are reported values mathematically consistent, temporally plausible, and contextually realistic?
   - Common problems: percentages that don't match raw numbers, impossible jumps between periods, figures that exceed population size
4. **Disaggregation**: Are people-level indicators disaggregated by sex, age, geography as required?
   - Common problems: no disaggregation, disaggregated values don't sum to total, only sex disaggregation when age also required
5. **Narrative-Data Alignment**: Does the narrative discuss both successes and shortfalls? Are claims backed by indicator data?
   - Common problems: narrative ignores off-track indicators, success stories without data backing, challenges described without indicator connection
6. **Variance Explanation**: Are off-track indicators explained with specific contributing factors and corrective actions?
   - Common problems: no explanation for below-target indicators, generic explanations, corrective actions that are vague or unrealistic
7. **Activity Progress**: Are planned activities reported with clear status? Do delays have explanations and revised timelines?
   - Common problems: activities listed but status unclear, delays acknowledged without revised timeline, completed activities claimed without evidence
8. **Financial Alignment**: Does financial progress match programmatic progress? Is burn rate reasonable for the reporting period?
   - Common problems: 80% budget spent with 30% activity completion, financial and programmatic sections disconnected, no variance explanation
9. **Lessons and Adaptation**: Are lessons specific and actionable? Do they connect to program decisions?
   - Common problems: generic lessons ("stakeholder engagement is important"), no connection to actual adaptations made, lessons repeated across reports without action
10. **Internal Consistency**: Cross-check: indicator table vs. narrative, activity progress vs. indicator achievement, financial vs. programmatic, current vs. previous report.

## Cross-Document Extraction Knowledge

When project files are available, extract these elements:

**From Logframe / Results Framework:**
- Complete indicator list with baselines, targets, and result levels
- Expected means of verification for each indicator
- Assumptions at each level (are they holding?)

**From M&E Plan:**
- Reporting schedule and required frequency per indicator
- Data collection methods and sources per indicator
- Disaggregation requirements per indicator
- Data quality assurance procedures

**From Previous Progress Report(s):**
- Prior period achievement values for trend analysis
- Previously reported challenges and promised corrective actions
- Cumulative achievement to date
- Lessons learned (are they being acted on?)

**From Proposal / Project Document:**
- Target populations and geographic scope for plausibility checks
- M&E commitments made to the donor
- Reporting requirements and format expectations

**From Donor Reporting Template (if available):**
- Required sections and format
- Mandatory indicators and disaggregation
- Narrative expectations and page limits

## File Discovery Patterns

When searching a project folder for progress report-related documents:

| Document Type | Search Patterns |
|---|---|
| Progress Report | `*progress report*`, `*quarterly report*`, `*annual report*`, `*semi-annual*`, `*APR*`, `*narrative report*`, `*donor report*` |
| Logframe | `*logframe*`, `*results framework*`, `*log frame*`, `*RF*` |
| M&E Plan | `*M&E plan*`, `*MEL plan*`, `*monitoring plan*`, `*AMELP*`, `*PMP*` |
| Previous Reports | `*Q1*`, `*Q2*`, `*Q3*`, `*Q4*`, `*Year 1*`, `*Year 2*`, `*20XX*` |
| Funder Template | `*template*`, `*reporting format*`, `*PUDR*` |

Search `.md`, `.txt`, `.docx`, and `.pdf` extensions. Confirm document identity with the user before proceeding.

## Scoring Criteria

**Section scores:**
- **PASS**: Complete, accurate, and well-explained
- **PARTIAL**: Exists but has significant gaps, inconsistencies, or missing explanations
- **FAIL**: Missing, contains implausible data, or fundamentally inadequate

**Overall rating (from section scores):**
- **Strong**: 0 FAIL, max 1 PARTIAL
- **Adequate**: 0 FAIL, 2+ PARTIAL
- **Needs Revision**: 1 FAIL, or 3+ PARTIAL
- **Major Issues**: 2+ FAIL

**Issue severity:**
- **Critical (must fix)**: Data errors that misrepresent program performance, missing mandatory indicators, implausible values presented as fact
- **Important (should fix)**: Missing explanations for off-track indicators, incomplete disaggregation, narrative-data disconnects
- **Minor (nice to fix)**: Formatting improvements, additional context that would strengthen the report

> **Rule:** Report what the data says, acknowledge data quality limitations, and let findings speak rather than interpreting them favorably. [EX117_S006]
