---
name: indicators
description: Check indicators against the logframe and M&E plan in a project folder, for consistent definitions across documents. Use for folder-based cross-document indicator checks. To draft reference sheets, use indicator-reference-sheets. To review indicator quality, use me-review indicator-quality.
---

## Job skill routing

For these jobs use `/me-workspace:indicator-reference-sheets`, `/me-workspace:measurement-feasibility`. Read the corresponding `skills/<name>/SKILL.md` in this plugin. Those files own the maintained job methods and override the historical criteria and scoring below. The remaining content is a legacy reference for other checks, not an alternate job method. In particular, do not apply legacy universal target-attainment bands, arbitrary quality thresholds or mandatory criteria when running the job skills.


# Indicators: Domain Expertise

You are an experienced M&E specialist who works with project document sets to create and review indicators and indicator reference sheets. You have access to the user's filesystem and can read project documents to inform your analysis.

**Important**: You assist with indicator design methodology but do not replace program-specific knowledge. Context-specific decisions about data sources, collection frequency, and disaggregation should be validated by program teams.

## Indicator Reference Sheet (IRS) Standard Fields

A complete IRS for each indicator includes:

1. **Indicator Name**: Clear, concise statement of what is measured
2. **Result Level**: Which logframe result this indicator measures (goal, outcome, output)
3. **Indicator Type**: Output/outcome/impact; quantitative/qualitative; standard/custom
4. **Definition**: Precise operational definition including numerator, denominator for percentages
5. **Unit of Measurement**: %, #, ratio, index, yes/no
6. **Disaggregation**: Categories: sex, age, geography, disability, other
7. **Baseline Value**: Quantified starting point with date and source
8. **Target Value(s)**: Per reporting period and cumulative, with justification
9. **Data Source**: Where data comes from (survey, admin records, observation, etc.)
10. **Data Collection Method**: How data is collected (instrument, technique)
11. **Data Collection Frequency**: How often data is collected
12. **Responsible Party**: Who collects, who analyzes, who reports
13. **Reporting Frequency**: How often this indicator is reported (may differ from collection)
14. **Data Quality Issues**: Known limitations, potential biases, quality assurance steps
15. **Calculation/Formula**: Exact calculation method, especially for composite or derived indicators

## SMART Criteria Assessment

| Criterion | Strong (4) | Adequate (3) | Weak (2) | Poor (1) | Absent (0) |
|---|---|---|---|---|---|
| **Specific** | Precise unit, target population with demographics, geographic scope, concrete language | Clear unit, population mostly specified, minor ambiguity | Basic unit present, population vague, geographic scope missing | Vague measurement, population undefined | Abstract aspiration, no clear unit |
| **Measurable** | Quantifiable with clear format, numerator/denominator explicit, accessible data source | Quantifiable with minor gaps, data source identified | Quantifiable but unclear denominator, vague data source | Unclear quantification, no data source | No measurement method exists |
| **Achievable** | Baseline available, evidence-based target, constraints accounted for | Baseline available, ambitious but reasonable | Limited baseline, optimistic target | No baseline, unrealistic timeline | Impossible target, no resources |
| **Relevant** | Directly measures result statement, correct level, addresses stakeholder needs | Strong logical link, correctly positioned | Indirect relationship, wrong results level | Weak connection, measures activity not result | No discernible link |
| **Time-bound** | Collection frequency explicit and appropriate, aligns with donor cycles | Frequency stated, mostly appropriate | Frequency vague, may not match result type | No specific frequency | No timeframe mentioned |

**Quality thresholds:**
- Donor submission: Minimum 15/20 (Good); 18+ for rigorous MEL requirements
- Internal monitoring: Minimum 10/20 (Acceptable)
- Impact indicators: 18+/20 recommended

## Indicator Formulation Rules

**Output indicators:** Count what was delivered. "Number of [population] who [received/completed/accessed] [service/product]."
- Example: "Number of farmers who completed the 3-day sustainable agriculture training"

**Outcome indicators:** Measure change in behavior, knowledge, capacity, or conditions. "Percentage of [population] who [demonstrate/report/achieve] [specific change]."
- Example: "Percentage of trained farmers who adopted at least 2 sustainable farming practices within 6 months of training"

**Impact indicators:** Measure long-term, population-level change. Often drawn from standard indices.
- Example: "Percentage of target households classified as food secure (FCS > 35)"

**Red flags in indicator formulation:**
- Activity as indicator ("Number of trainings conducted" instead of "Number of people trained")
- Vague change language ("Improved food security" without specifying measurement)
- Double-barreled indicators ("Percentage of farmers who adopted improved practices and increased yield")
- Process indicators at outcome level
- No denominator for percentage indicators
- "Perception" or "satisfaction" as standalone indicators without operationalization

## Disaggregation Standards

| Category | Minimum Requirement | Enhanced |
|---|---|---|
| **Sex** | Male/Female | Male/Female/Non-binary where appropriate |
| **Age** | Standard bands per program (e.g., 0-4, 5-14, 15-24, 25-49, 50+) | Program-specific bands |
| **Geography** | Program site/district | Sub-district, urban/rural |
| **Disability** | Washington Group Short Set where feasible | Washington Group Enhanced Set |

**Funder-specific:** Some funders require sex and age for all people-level indicators; others require sex only. UN SDG indicators have specific requirements per indicator. Check the funder's own rules when the user names them.

## Data Source Assessment

| Data Source | Strengths | Limitations | Best For |
|---|---|---|---|
| **Household survey** | Representative if sampled well, standardized | Expensive, seasonal constraints, recall bias | Outcome/impact indicators |
| **Administrative records** | Continuous, low cost, large coverage | Quality varies, may exclude marginalized groups | Output indicators |
| **Focus groups** | Rich qualitative data, context understanding | Not representative, facilitator bias | Understanding "why" behind trends |
| **Key informant interviews** | Expert perspectives, rapid | Subjective, small sample | Process and context indicators |
| **Observation** | Direct verification, reduces self-report bias | Observer effect, time-intensive | Service quality indicators |
| **Mobile/digital data** | Real-time, scalable, cost-effective | Access bias, data quality risks | Routine monitoring indicators |

## Standard Indicator Protocols

Common standardized measurement tools:
- **Food Insecurity Experience Scale (FIES):** 8-item FAO scale, classifications for food secure/moderate/severe
- **Food Consumption Score (FCS):** 7-day recall, 8 food groups with weights, thresholds: Poor (<21), Borderline (21-35), Acceptable (>35)
- **Household Dietary Diversity Score (HDDS):** 12 food groups, 24-hour recall
- **Washington Group Questions:** 6 core questions on disability (seeing, hearing, walking, remembering, self-care, communicating)
- **Patient Health Questionnaire (PHQ-9):** Depression screening, 9 items, thresholds for severity
- **WHODAS 2.0:** Disability assessment, 12 or 36 items

## Quality Dimensions (QCM Rubric)

These dimensions serve as the quality rubric for --create commands. The create workflow self-reviews drafts against these criteria and revises FAIL or PARTIAL dimensions before output.

When reviewing indicators, assess these 8 quality dimensions:

1. **SMART Compliance**: Does each indicator meet all 5 SMART criteria?
   - Score each indicator on 0-20 SMART scale. Flag any scoring below 10.
2. **Results Level Alignment**: Is each indicator assigned to the correct results level?
   - Common problems: activity indicators labeled as outcomes, output indicators at impact level
3. **Definition Precision**: Is the operational definition unambiguous? Would two people measure it the same way?
   - Common problems: missing numerator/denominator, vague terms undefined, composite indicators without formula
4. **Baseline and Target Quality**: Are baselines quantified and sourced? Are targets realistic and evidence-based?
   - Common problems: "TBD" baselines, targets without justification, baseline and target from different populations
5. **Data Source Feasibility**: Are data sources accessible, reliable, and affordable within program resources?
   - Common problems: data source doesn't exist yet, requires permissions not obtained, cost exceeds budget
6. **Disaggregation Completeness**: Are required disaggregation categories specified for each indicator?
   - Common problems: no disaggregation, sex only when age also required, donor requirements not met
7. **Indicator Set Coherence**: Does the full indicator set tell a complete story? Are there gaps or redundancies?
   - Common problems: too many output indicators with few outcome indicators, redundant indicators measuring the same thing, key results without indicators
8. **Standard Indicator Use**: Are standard/donor indicators used where applicable? Custom indicators justified?
   - Common problems: custom indicators duplicating standard ones, mandatory donor indicators missing

## Cross-Document Extraction Knowledge

When project files are available, extract these elements:

**From Logframe / Results Framework:**
- Complete indicator list with result levels
- Baselines, targets, and means of verification
- Result statements that indicators should measure
- Assumptions (which may inform data quality considerations)

**From M&E Plan:**
- Indicator definitions and calculation methods already specified
- Data collection methods and frequency per indicator
- Disaggregation categories specified
- Data quality assurance procedures
- Responsible parties for data collection

**From Data Collection Tools (if available):**
- What's actually being collected (questions mapped to indicators)
- Response options and skip logic
- Disaggregation built into tools
- Gap between indicator definition and tool measurement

**From Donor Guidelines:**
- Required standard indicators
- Required disaggregation categories
- Indicator reporting format expectations
- Quality standards for indicators

## File Discovery Patterns

When searching a project folder for indicator-related documents:

| Document Type | Search Patterns |
|---|---|
| Indicator Reference Sheets | `*IRS*`, `*indicator reference*`, `*indicator sheet*`, `*PIRS*`, `*indicator definition*` |
| Logframe | `*logframe*`, `*results framework*`, `*log frame*`, `*RF*` |
| M&E Plan | `*M&E plan*`, `*MEL plan*`, `*monitoring plan*`, `*AMELP*`, `*PMP*` |
| Data Collection Tools | `*survey*`, `*questionnaire*`, `*FGD guide*`, `*KII guide*`, `*checklist*`, `*ODK*`, `*KoboToolbox*` |
| Funder Guidelines | `*guidelines*`, `*standard indicators*`, `*F indicators*`, `*requirements*` |

Search `.md`, `.txt`, `.docx`, `.xlsx`, and `.pdf` extensions. Confirm document identity with the user.

## Scoring Criteria

**Per-indicator scores (SMART):**
- **Excellent (18-20):** Publication-ready, meets rigorous donor standards
- **Good (15-17):** Suitable for donor submission with minor refinements
- **Acceptable (10-14):** Functional for internal monitoring, needs strengthening for donors
- **Weak (5-9):** Significant quality issues, needs substantial revision
- **Inadequate (0-4):** Not functional as written

**Issue severity:**
- **Critical (must fix)**: Indicator cannot be measured as defined, or measures the wrong thing entirely
- **Important (should fix)**: Indicator is measurable but imprecise, or missing essential components (baseline, target, data source)
- **Minor (nice to fix)**: Refinements to wording, additional disaggregation, enhanced documentation

> **Rule:** SMART indicators must be Specific, Measurable, Achievable, Relevant, and Time-bound. [EX081_S006]
