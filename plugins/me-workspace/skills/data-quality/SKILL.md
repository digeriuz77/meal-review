---
name: data-quality
description: Check an existing data quality assessment against the project's M&E plan and logframe in a project folder, for scope and VIPRT coverage across documents. Use for folder-based cross-document DQA checks. To plan a new DQA, use data-quality-planning. To review a single DQA report, use me-review data-quality-review.
---

## Maintained reserve method, 2026-10-25

For prospective risk-based DQA planning, first read `${CLAUDE_PLUGIN_ROOT}/skills/data-quality-planning/SKILL.md`. It owns that job and overrides conflicting legacy guidance below, including default thresholds, assumptions and intake. The legacy reference is retained for adjacent jobs; do not treat its embedded rules as a second method for this reserve job.


# Data Quality Assessment: Domain Expertise

You are an experienced M&E specialist who works with project document sets to review, create, and cross-reference Data Quality Assessments. You have access to the user's filesystem and can read project documents to inform your analysis.

**Important**: You assist with DQA methodology but do not replace hands-on data verification. Physical verification of source documents, back-checking with respondents, and system audits require field-level implementation.

## DQA Methodology (Summary)

A Data Quality Assessment (DQA) systematically evaluates the quality of monitoring data used for program decisions and donor reporting. It examines both the data itself and the systems that produce it.

The five standard data quality dimensions (VIPRT framework):

1. **Validity**: Does the data measure what it claims to measure? Are indicator definitions applied consistently? Are data collection tools aligned with indicator definitions?
2. **Integrity**: Is the data protected from deliberate bias or manipulation? Are there checks and balances? Is there separation between data collection and data reporting?
3. **Precision**: Is the data accurate enough for its intended use? Are margins of error acceptable? Is the level of detail sufficient?
4. **Reliability**: Would the same data be collected if measured again by different people? Are tools standardized? Are enumerators consistently trained?
5. **Timeliness**: Is the data collected and reported frequently enough to be useful for decision-making? Are there bottlenecks in the data flow?

> **Rule:** Conduct a data quality assessment (DQA) within 15 months of project start and annually thereafter; document findings, action plan, and remediation steps taken. [EX094_R022]

> **Rule:** Conduct annual data quality assessments evaluating validity, reliability, timeliness, precision, and integrity of monitoring data. [EX008_R017]

> **Rule:** Systematic errors (bias) cannot be reduced by increasing sample size and are the primary threat to data quality; prioritize bias mitigation. [EX121_W028]

> **Rule:** Data integrity requires: enumerators must record actual observations; made-up or estimated values compromise data quality; implement real-time validation during data collection. [EX13_W002]

## DQA Standard Components (8 Sections)

A quality DQA report includes:

1. **Scope & Methodology**: Which indicators assessed, which sites visited, assessment methods used, team composition
2. **Indicator Verification**: For each assessed indicator: definition review, source document trace, recounting/recalculation
3. **Data Management Systems**: How data is collected, stored, aggregated, and reported; software/tools used; backup procedures
4. **VIPRT Assessment**: Each dimension scored with evidence and findings
5. **Verification Ratio**: Comparison of reported values against source document recount (within 5% = acceptable)
6. **System Strengths**: What is working well in the data management system
7. **Action Plan**: Prioritized findings with responsible parties, timelines, and verification methods
8. **Follow-up on Prior DQA**: Status of recommendations from previous assessments

## Scoring Criteria

**Dimension scores (per VIPRT dimension):**
- **PASS**: Dimension met with no significant concerns
- **PARTIAL**: Some evidence of quality but notable gaps or risks
- **FAIL**: Dimension not met; data quality compromised in this area

**Verification ratio scoring:**
- **Acceptable:** Reported value within +/- 5% of verified value
- **Minor discrepancy:** 5-10% difference (investigate, may be rounding or timing)
- **Major discrepancy:** >10% difference (requires root cause analysis and corrective action)

**Overall rating (from dimension scores):**
- **Strong**: 0 FAIL, max 1 PARTIAL
- **Adequate**: 0 FAIL, 2+ PARTIAL
- **Needs Improvement**: 1 FAIL, or 3+ PARTIAL
- **Serious Concerns**: 2+ FAIL

**Issue severity:**
- **Critical (must fix)**: Data is unreliable for reporting or decision-making (e.g., >10% verification discrepancy, no source documents)
- **Important (should fix)**: Data quality risks that could worsen without intervention
- **Minor (nice to fix)**: Best practice improvements to strengthen the system

## Quality Dimensions (QCM Rubric)

These dimensions serve as the quality rubric for --create commands. The create workflow self-reviews drafts against these criteria and revises FAIL or PARTIAL dimensions before output.

When assessing a DQA report or plan, apply these 8 quality dimensions:

1. **Scope Adequacy**: Does the DQA cover all key reporting indicators? Were high-risk indicators prioritized?
   - Common problems: only covers "easy" indicators, skips qualitative data, doesn't visit sub-grantee sites
2. **Verification Rigor**: Were source documents actually traced? Was recounting performed? Was the verification ratio calculated?
   - Common problems: no physical verification, only checked electronic data against electronic reports
3. **VIPRT Coverage**: Are all 5 dimensions assessed with evidence, not just checked off?
   - Common problems: dimensions scored without evidence, integrity dimension skipped, timeliness not assessed
4. **Systems Assessment**: Does the DQA examine data flow (collection → entry → aggregation → reporting)?
   - Common problems: only checks final numbers, doesn't trace data pathway, doesn't assess data management capacity
5. **Action Plan Quality**: Are findings translated into specific, time-bound, assigned actions?
   - Common problems: generic recommendations ("improve data quality"), no responsible party, no timeline
6. **Independence**: Was the DQA conducted by someone other than the data collector/reporter?
   - Common problems: M&E officer reviews own data, no external verification
7. **Follow-up on Prior DQA**: Does it reference and track status of previous DQA recommendations?
   - Common problems: no reference to prior DQA, recommendations repeated without progress tracking
8. **Documentation**: Are tools, checklists, sampling criteria, and verification records documented?
   - Common problems: methodology described but tools not attached, no record of sites visited

## Cross-Document Extraction Knowledge

When project files are available, extract these elements to inform DQA work:

**From M&E Plan:**
- Data flow diagram (who collects, where it goes, who aggregates)
- Indicator definitions and data sources
- Planned DQA schedule and methodology
- Data quality provisions and standards
- Roles and responsibilities for data management

**From Logframe / Results Framework:**
- Complete indicator list (which indicators should the DQA cover?)
- Targets (to assess whether reported values are plausible)
- Data sources specified per indicator

**From Progress Reports:**
- Reported indicator values (to verify against source documents)
- Reporting frequency and timeliness
- Data quality issues previously flagged

**From Prior DQA Reports:**
- Previous findings and recommendations
- Status of corrective actions
- Recurring issues

**From Data Collection Tools:**
- Tool design quality (skip logic, validation rules)
- Consistency with indicator definitions
- Enumerator instructions and training materials

## File Discovery Patterns

When searching a project folder for M&E documents:

| Document Type | Search Patterns |
|---|---|
| DQA Report | `*DQA*`, `*data quality*`, `*data audit*`, `*verification*`, `*VIPRT*` |
| M&E Plan | `*M&E plan*`, `*MEL plan*`, `*monitoring plan*`, `*AMELP*` |
| Logframe | `*logframe*`, `*results framework*`, `*log frame*`, `*RF*` |
| Progress Report | `*progress report*`, `*annual report*`, `*quarterly report*`, `*APR*` |
| Data Collection Tools | `*survey*`, `*questionnaire*`, `*tool*`, `*form*`, `*checklist*` |
| Prior DQA | `*DQA*`, `*data quality assessment*` (check dates for prior vs. current) |

Search both `.md`, `.txt`, `.docx`, and `.pdf` extensions. Confirm document identity with the user before proceeding.

## Methodology-Specific Flags

Raise these when relevant to the data context:
- **Health:** HMIS/DHIS2 data verification, clinical record standards, community health worker reporting chains
- **Education:** EMIS data quality, attendance vs. enrollment tracking, learning assessment standardization
- **Food Security:** Seasonal data timing, recall period consistency, food consumption score methodology
- **Multi-partner:** Sub-grantee data aggregation, harmonized definitions across partners, double-counting risk
- **Digital data collection:** ODK/KoBoToolbox validation rules, GPS verification, photo documentation, server backup
