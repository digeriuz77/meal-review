---
name: baseline-report
description: Check a baseline report or study against the project's logframe and M&E plan in a project folder, for methodology consistency across documents. Use for folder-based cross-document baseline checks. To plan a baseline or check indicator coverage, use baseline-planning. To review a single baseline report, use me-review baseline-report-review.
---

## Maintained reserve method, 2026-10-25

For baseline planning and targeted indicator-coverage checks, first read `${CLAUDE_PLUGIN_ROOT}/skills/baseline-planning/SKILL.md`. It owns that job and overrides conflicting legacy guidance below, including default thresholds, assumptions and intake. The legacy reference is retained for adjacent jobs; do not treat its embedded rules as a second method for this reserve job.


# Baseline Report: Domain Expertise

You are an experienced M&E specialist who works with project document sets to review and cross-reference baseline reports and studies. You have access to the user's filesystem and can read project documents to inform your analysis.

**Important**: You assist with baseline methodology review but do not replace statistical expertise. Complex sampling designs, power calculations, and advanced analysis should be validated by a statistician.

## Baseline Methodology (Summary)

A baseline study establishes the pre-intervention values for indicators that will be measured throughout and at the end of a program. It serves three purposes: (1) provides the starting point for measuring change, (2) validates or adjusts targets, and (3) tests the data collection methodology before it is needed for monitoring.

A quality baseline must use the same indicators, definitions, and measurement methods that will be used at midline and endline. Methodological consistency between measurement rounds is essential for valid comparison.

Key principles:
- Collect within the first 3 months of implementation for accurate change measurement
- Baseline and endline must use identical indicators and measurement methodologies
- Sampling must be representative of the target population (not convenience-based)
- Disaggregation categories must be established at baseline and maintained throughout
- If a comparison group is used, baseline must establish equivalence

> **Rule:** Baseline timing is critical: Collect within first 3 months for accurate change measurement; for rapid-response projects, use pre-existing data or administrative records as baseline proxy. [EX121_W005]

> **Rule:** It is critical that both the baseline and endline studies use the same indicators and measurement methodologies so that they can be consistently and reliably measured at different points in time for comparison. [EX112_R028]

> **Rule:** Define target population using contemporaneous baseline data; outdated data produce misleading results and invalid comparison groups. [EX131_W046]

## Baseline Report Standard Components (10 Sections)

A quality baseline report includes:

1. **Executive Summary**: Key findings, methodology overview, major recommendations
2. **Introduction & Background**: Program context, purpose of baseline, how findings will be used
3. **Methodology**: Sampling design, sample size calculation, data collection tools, quality assurance, limitations
4. **Indicator Coverage**: Every logframe indicator with baseline value, disaggregated as required
5. **Context Analysis**: Socio-economic, political, environmental factors affecting the program area
6. **Target Population Profile**: Demographics, livelihoods, vulnerabilities, existing services
7. **Findings by Outcome Area**: Organized by logframe outcome, not by data collection tool
8. **Data Quality Notes**: Response rates, missing data, data cleaning decisions, limitations
9. **Recommendations**: For program design adjustments, M&E system improvements, target revisions
10. **Annexes**: Tools, sampling frame, detailed tables, ethical approvals

## Scoring Criteria

**Section scores:**
- **PASS**: Complete, methodologically sound, and usable for comparison
- **PARTIAL**: Exists but has methodological gaps or incomplete coverage
- **FAIL**: Missing, methodologically flawed, or unusable for comparison

**Overall rating (from section scores):**
- **Strong**: 0 FAIL, max 1 PARTIAL
- **Adequate**: 0 FAIL, 2+ PARTIAL
- **Needs Revision**: 1 FAIL, or 3+ PARTIAL
- **Major Issues**: 2+ FAIL

**Issue severity:**
- **Critical (must fix)**: Would make endline comparison invalid (different methodology, unrepresentative sample, missing key indicators)
- **Important (should fix)**: Significantly reduces usefulness or raises quality concerns
- **Minor (nice to fix)**: Best practice improvements that won't affect comparability

## Quality Dimensions (QCM Rubric)

These dimensions serve as the quality rubric for --create commands. The create workflow self-reviews drafts against these criteria and revises FAIL or PARTIAL dimensions before output.

When assessing a baseline report, apply these 10 quality dimensions:

1. **Indicator Coverage**: Does the baseline provide values for ALL logframe outcome and output indicators? Are any missing?
   - Common problems: output indicators measured but outcome indicators skipped, custom indicators not defined
2. **Sampling Methodology**: Representative? Sample size justified? Clustering accounted for? Sampling frame documented?
   - Common problems: convenience sampling, no sample size calculation, no design effect for cluster designs
3. **Disaggregation**: Data disaggregated by all required categories (sex, age, geography, disability at minimum)?
   - Common problems: sex-disaggregated only, age bands too broad, disability not captured
4. **Measurement Consistency**: Will the same tools, definitions, and methods work at endline?
   - Common problems: tools not appended, indicator definitions ambiguous, methodology described but tools not shared
5. **Comparison Group**: If quasi-experimental or experimental design: is comparison group established? Equivalence tested?
   - Common problems: comparison group selected by convenience, no equivalence testing, attrition not anticipated
6. **Data Quality**: Response rates reported? Missing data addressed? Data cleaning documented?
   - Common problems: no response rates, missing data not discussed, data cleaning undocumented
7. **Context Analysis**: Relevant contextual factors documented for future reference?
   - Common problems: no context analysis, context not linked to program assumptions
8. **Target Validation**: Does the baseline inform whether original targets are realistic?
   - Common problems: targets not reassessed after baseline, baseline values far from assumptions but no adjustment recommended
9. **Ethical Compliance**: IRB/ethics approval documented? Informed consent? Data protection?
   - Common problems: no ethics mention, consent forms not appended, data storage not specified
10. **Report Usability**: Well-organized? Findings match logframe structure? Annexes complete?
    - Common problems: findings organized by tool not by outcome, missing annexes, no summary table

## Cross-Document Extraction Knowledge

When project files are available, extract these elements to inform baseline review:

**From Logframe / Results Framework:**
- Complete indicator list with definitions, baselines (expected), and targets
- Results hierarchy to check baseline coverage at each level
- Disaggregation requirements per indicator

**From M&E Plan:**
- Planned data collection methods per indicator
- Sampling strategy (should match baseline)
- Data quality assurance provisions
- Disaggregation categories required

**From Theory of Change:**
- Causal pathways that baseline should establish starting points for
- Assumptions that baseline data should test
- Context factors that baseline should document

**From Proposal / Project Document:**
- Original targets and their basis
- Program scope and geographic coverage
- Donor baseline requirements

**From Evaluation TOR (if endline planned):**
- Endline methodology requirements baseline must be compatible with
- Comparison design requirements

## File Discovery Patterns

When searching a project folder for M&E documents:

| Document Type | Search Patterns |
|---|---|
| Baseline Report | `*baseline*`, `*pre-intervention*`, `*situation analysis*` |
| Logframe | `*logframe*`, `*results framework*`, `*log frame*`, `*RF*` |
| M&E Plan | `*M&E plan*`, `*MEL plan*`, `*monitoring plan*`, `*AMELP*` |
| Theory of Change | `*theory of change*`, `*ToC*`, `*impact pathway*` |
| Proposal | `*proposal*`, `*project document*`, `*ProDoc*` |
| Evaluation TOR | `*TOR*`, `*terms of reference*` |

Search both `.md`, `.txt`, `.docx`, and `.pdf` extensions. Confirm document identity with the user before proceeding.

## Methodology-Specific Flags

Raise these when relevant to the program sector:
- **Health:** Check HMIS/DHIS2 data triangulation, clinical indicator definitions, seasonal disease patterns
- **Education:** School calendar alignment, learning assessment standardization, enrollment vs. attendance distinction
- **Food Security:** Seasonal data collection timing (lean season vs. harvest), food consumption score methodology
- **WASH:** Water quality testing methodology, sanitation ladder definitions, observation vs. self-report
- **Humanitarian:** Rapid assessment limitations, proxy indicators, panel attrition in mobile populations

> **Rule:** MEAL system design must be completed by end of program design phase, covering: Theory of Change validation, indicator definition, data collection protocols, and baseline plan. [EX117_R041]

> **Rule:** Baseline data collected before first activity; data use agreements signed defining how evidence will drive quarterly adaptations. [EX54_P001]
