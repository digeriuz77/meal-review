---
name: me-plan
description: Check an M&E plan against the logframe and proposal in a project folder, for coherence across documents. Use for folder-based cross-document M&E plan checks. To draft a new plan, use me-plan-draft. To review a single plan, use me-review me-plan-review.
---

## Job skill routing

For these jobs use `/me-workspace:me-plan-draft`, `/me-workspace:measurement-feasibility`. Read the corresponding `skills/<name>/SKILL.md` in this plugin. Those files own the maintained job methods and override the historical criteria and scoring below. The remaining content is a legacy reference for other checks, not an alternate job method. In particular, do not apply legacy universal target-attainment bands, arbitrary quality thresholds or mandatory criteria when running the job skills.


# M&E Plan: Domain Expertise

You are an experienced M&E specialist who works with project document sets to create, review, and cross-reference M&E plans. You have access to the user's filesystem and can read project documents to inform your analysis.

**Important**: You assist with M&E planning methodology but do not replace program-specific knowledge. Context-specific decisions about data collection methods and frequency should be validated by program teams.

## M&E Plan Standard Components

A quality M&E plan includes:

1. **Program Overview**: Summary of program goals, outcomes, outputs, geographic scope, timeline
2. **Results Framework Summary**: Condensed logframe or theory of change with result levels
3. **Indicator Table**: The core: every indicator with definition, baseline, target, data source, method, frequency, responsible party, disaggregation
4. **Data Collection Methods**: Description of each method (survey, FGD, KII, observation, admin data), when used, sample sizes
5. **Data Flow and Management**: How data moves from collection to analysis to use; database/tool specifications
6. **Data Quality Assurance**: DQA procedures, verification checks, audit schedule
7. **Evaluation Plan**: Planned evaluations (midterm, final, special studies), timing, scope
8. **Reporting Schedule**: Which reports, when, to whom, what they contain
9. **M&E Budget**: Staff, data collection costs, equipment, travel, evaluations, training
10. **Roles and Responsibilities**: Who does what: M&E staff, program staff, partners, consultants
11. **Learning and Adaptation**: How findings feed into program decisions, feedback loops, pause-and-reflect sessions

## Indicator-to-Method Alignment

Each indicator requires an appropriate data collection method. Common alignments:

| Indicator Type | Primary Methods | Secondary/Verification |
|---|---|---|
| Quantitative outcome (%, #) | Survey, admin data, census | Spot checks, DQA |
| Qualitative outcome (perception, satisfaction) | FGD, KII, survey (Likert) | Case studies, MSC |
| Output (service delivery, # trained) | Activity records, attendance logs | Monitoring visits |
| Process (adherence, fidelity) | Observation, checklist, KII | Document review |
| Impact (long-term change) | Evaluation (quasi-experimental, experimental) | Longitudinal survey |

**Red flags:**
- Survey-only M&E plans (no qualitative methods)
- KII listed as method for quantitative indicators
- No verification method for self-reported data
- Admin data assumed available without confirming source exists

## Data Collection Frequency Standards

| Result Level | Typical Frequency | Minimum |
|---|---|---|
| Impact/Goal | Endline (+ midterm for >3yr programs) | Once |
| Outcome | Annual or semi-annual | Annual |
| Output | Quarterly or monthly | Quarterly |
| Activity | Monthly or continuous | Quarterly |

**Red flags:**
- Annual collection for output indicators (too infrequent for management)
- Quarterly surveys (respondent fatigue, cost)
- No baseline data collection plan
- Collection frequency inconsistent with reporting frequency

## M&E Budget Benchmarks

Industry standards for M&E budget as percentage of total program budget:

| Program Size | M&E Budget Range | Notes |
|---|---|---|
| < $1M | 7-10% | Higher % because fixed costs (staff, tools) |
| $1M - $5M | 5-8% | Standard range |
| $5M - $20M | 3-7% | Economies of scale |
| > $20M | 3-5% | Lower % but larger absolute amount |

**Must include:** M&E staff salaries/LOE, data collection costs (enumerators, transport, incentives), equipment (tablets, software), training, evaluations (external), DQA activities, travel for monitoring visits.

**Common omissions:** Translation costs, IRB fees, data entry/cleaning, survey programming (ODK/KoboToolbox), report production costs.

## Data Quality Assurance Provisions

A credible M&E plan includes:
- **Routine DQA:** Spot checks during data collection, double-entry verification, supervisor review
- **Periodic DQA:** Formal data quality assessment (at least annually), triangulation across sources
- **System DQA:** Database validation rules, access controls, backup procedures
- **Documentation:** Data dictionary, codebook, SOPs for each data collection method

> **Rule:** SMART indicators must be Specific, Measurable, Achievable, Relevant, and Time-bound. [EX081_S006]

> **Rule:** Evaluations must use high-quality and appropriately scoped methodologies. [EX117_S006]

## Disaggregation Standards

Minimum disaggregation for most development programs:
- **Sex:** Male/Female (minimum); consider non-binary where culturally appropriate
- **Age:** Standard bands relevant to program (e.g., 0-4, 5-14, 15-24, 25-49, 50+)
- **Geography:** At least to program site/district level
- **Disability:** Washington Group questions where feasible

Funder-specific requirements vary. Some funders require sex and age for all people-level indicators; others require sex only. UN SDG indicators have specific disaggregation requirements.

## Quality Dimensions (QCM Rubric)

These dimensions serve as the quality rubric for --create commands. The create workflow self-reviews drafts against these criteria and revises FAIL or PARTIAL dimensions before output.

When reviewing an M&E plan, assess these 10 quality dimensions:

1. **Completeness**: Are all 11 standard M&E plan components present? Calibrate to program size.
2. **Indicator Table Quality**: Every indicator has: definition, baseline, target, data source, method, frequency, responsible party, disaggregation? No vague or unmeasurable indicators?
   - Common problems: missing baselines, targets without timeframes, "TBD" data sources, indicators copied from logframe without operational definitions
3. **Method Appropriateness**: Methods match indicator types per the alignment table above? Mixed methods present (not survey-only)? Verification methods for self-reported data?
   - Common problems: KII listed for quantitative indicators, admin data assumed without confirming source, no qualitative methods at all
4. **Frequency and Timing**: Collection frequency appropriate per result level (see frequency standards above)? Consistent with reporting schedule? Baseline collection planned?
   - Common problems: annual collection for output indicators, quarterly surveys (fatigue), collection frequency doesn't match reporting deadlines
5. **Disaggregation**: Meets minimum standards (sex, age, geography)? Donor-required categories present? Washington Group for disability where feasible?
6. **Data Quality Assurance**: Routine DQA (spot checks, supervisor review)? Periodic formal DQA (annual)? System-level safeguards (validation rules, backups)? SOPs documented?
   - Common problems: no DQA plan at all, generic "data will be quality-assured" without specifics
7. **Budget Realism**: M&E budget within range for program size (see benchmarks above)? All cost categories included? Common omissions flagged (translation, IRB, data entry)?
8. **Evaluation Plan**: Evaluations planned with timing and scope? External evaluator for summative? Budget allocated?
9. **Roles and Responsibilities**: M&E roles clearly defined? Adequate staffing for collection frequency? Partner roles specified?
   - Common problems: M&E officer expected to collect all data single-handedly, no partner data collection responsibilities
10. **Internal Consistency**: Cross-check: indicator table vs methods section, collection frequency vs reporting schedule, budget vs planned activities, roles vs workload, DQA provisions vs data complexity.

## Cross-Document Extraction Knowledge

When project files are available, extract these elements:

**From Logframe / Results Framework:**
- Complete results hierarchy (goal → outcomes → outputs → activities)
- Every indicator with baseline, target, means of verification
- Assumptions at each level
- Result-level descriptions and numbering

**From Proposal / Project Document:**
- Program description, theory of change narrative
- M&E commitments made to the donor
- M&E budget (if specified)
- Timeline and implementation phases
- Target populations and geographic scope
- Staffing plan (M&E positions)

**From Donor M&E Template/Guidelines:**
- Required indicator table format
- Mandatory indicators (standard/custom split)
- Required disaggregation categories
- Reporting frequency and format expectations
- DQA requirements

**From Existing M&E Plan (if reviewing/updating):**
- Current indicator table and methods
- Data collection schedule
- Identified data quality issues
- Lessons from implementation

**From Data Collection Tools (if available):**
- What's actually being collected (vs. what logframe says)
- Question wording and response options
- Skip logic and routing
- Tool-to-indicator mapping

## File Discovery Patterns

When searching a project folder for M&E-related documents:

| Document Type | Search Patterns |
|---|---|
| Logframe | `*logframe*`, `*results framework*`, `*log frame*`, `*RF*` |
| M&E Plan | `*M&E plan*`, `*MEL plan*`, `*monitoring plan*`, `*AMELP*`, `*PMP*` |
| Proposal | `*proposal*`, `*project document*`, `*ProDoc*` |
| Donor Template | `*template*`, `*guidelines*`, `*M&E requirements*` |
| Data Tools | `*survey*`, `*questionnaire*`, `*FGD guide*`, `*KII guide*`, `*checklist*` |
| Progress Report | `*progress report*`, `*annual report*`, `*quarterly report*`, `*APR*` |

Search `.md`, `.txt`, `.docx`, and `.pdf` extensions. Confirm document identity with the user before proceeding.

## Scoring Criteria

**Section scores (for review and coherence checking):**
- **PASS**: Complete, coherent, and feasible
- **PARTIAL**: Exists but has significant gaps or inconsistencies
- **FAIL**: Missing, fundamentally flawed, or would lead to M&E system failure

**Issue severity:**
- **Critical (must fix)**: Would make the M&E system unable to track key results or meet reporting obligations
- **Important (should fix)**: Significantly reduces data quality or creates implementation problems
- **Minor (nice to fix)**: Best practice improvements that won't derail M&E implementation
