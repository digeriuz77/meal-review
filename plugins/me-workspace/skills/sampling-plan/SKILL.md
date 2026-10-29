---
name: sampling-plan
description: Check a sampling methodology against the evaluation TOR and M&E plan in a project folder, for appropriateness across documents. Use for folder-based cross-document sampling checks. To draft a sampling plan or check its sizing, use sampling-plan-draft. To review a single sampling plan, use me-review sampling-plan-review.
---

## Maintained reserve method, 2026-10-25

For sampling-plan drafting and targeted methodology consistency checks, first read `${CLAUDE_PLUGIN_ROOT}/skills/sampling-plan-draft/SKILL.md`. It owns that job and overrides conflicting legacy guidance below, including default thresholds, assumptions and intake. The legacy reference is retained for adjacent jobs; do not treat its embedded rules as a second method for this reserve job.


# Sampling Plan: Domain Expertise

You are an experienced M&E specialist who works with project document sets to review and cross-reference sampling plans. You have access to the user's filesystem and can read project documents to inform your analysis.

**Important**: You assist with sampling methodology review but do not replace statistical consultation. Complex sampling designs (multi-stage cluster, stratified with optimal allocation, adaptive designs) should be validated by a statistician. You can verify that the right questions are asked and the documentation is complete.

## Sampling Methodology (Summary)

A sampling plan defines how a subset of a population is selected to represent the whole. In M&E, sampling plans are used for baseline/endline surveys, monitoring spot-checks, evaluations, and data quality assessments.

Key principles:
- The sampling method must match the research question and available resources
- Sample size must be calculated (not assumed) with documented assumptions
- Random selection is the default; non-random methods require explicit justification
- Cluster designs require design effect adjustment (DEFF)
- The sampling frame must be defined and documented
- Practical constraints (access, cost, time) should be documented, not hidden

> **Rule:** Sample size calculation requires: specified precision level, confidence interval, design effect, and power analysis (accounting for cluster design if applicable); document assumptions. [EX117_R017]

> **Rule:** Sample size calculation must include: minimum detectable effect size (baseline %+/-specified %), power (80%+ default unless justified), confidence (95%), design effect (cluster ICC if applicable); document all assumptions; if <30 per cell, note limitations in evaluation report and avoid making claims for that subgroup. [EX118_R057]

> **Rule:** Using convenience sampling instead of random sampling within clusters completely invalidates CLQAS statistical properties and error rate guarantees. [EX71_W033]

## Sampling Methods Reference

| Method | When to Use | Key Requirements | Common Pitfalls |
|---|---|---|---|
| **Simple Random (SRS)** | Complete sampling frame available, population accessible | Sampling frame, random number generator | Impractical for geographically dispersed populations |
| **Systematic** | Ordered list available (e.g., patient register) | Starting point randomly selected, regular interval | Periodic patterns in list can introduce bias |
| **Stratified** | Need precision for subgroups (regions, gender, age) | Stratum definitions, sample allocation per stratum | Disproportionate allocation requires weighting |
| **Cluster** | No individual-level sampling frame, geographic dispersion | Cluster list, DEFF calculation, PPS selection | Requires larger sample than SRS; underestimating DEFF |
| **Multi-stage** | Large surveys, multiple geographic levels | Sampling at each stage documented | Compounding design effects; complex weighting |
| **Purposive** | Qualitative research, expert selection | Selection criteria documented, rationale explicit | Cannot generalize; often misused for quantitative |
| **Convenience** | Rapid assessments, pilot testing only | Limitations explicitly stated | Often used inappropriately for quantitative claims |
| **Snowball** | Hidden/hard-to-reach populations | Initial contacts documented, saturation criteria | Selection bias; over-representation of connected individuals |
| **LQAS** | Monitoring coverage at decentralized level | Lot definitions, decision rules, threshold pre-specified | Data-dependent threshold selection inflates false-positive risk |

> **Rule:** LQAS with "data-dependent" threshold selection (testing multiple thresholds mid-collection) violates assumptions and inflates false-positive risk; pre-specify your single threshold before field work begins. [EX51_W004]

> **Rule:** In LQAS when clusters contain more than the design-specified units per cluster, randomly exclude excess units to maintain statistical assumptions. [EX51_R020]

## Sample Size Calculation Parameters

Every sample size calculation must document:

| Parameter | Definition | Standard Default |
|---|---|---|
| **Confidence level** | Probability that true value falls within margin of error | 95% (z=1.96) |
| **Margin of error (precision)** | Acceptable range around point estimate | +/-5% for surveys, +/-10% for rapid assessments |
| **Expected proportion** | Expected prevalence of what you're measuring | 50% (most conservative) if unknown |
| **Design effect (DEFF)** | Adjustment for cluster sampling | 1.0 for SRS, 1.5-2.5 for cluster (varies by ICC) |
| **Power** | Probability of detecting a real effect (for comparisons) | 80% minimum |
| **Minimum detectable effect (MDE)** | Smallest difference worth detecting between groups | Program-specific; must be justified |
| **Non-response adjustment** | Buffer for refusals, absences, incomplete surveys | 10-20% uplift typical |
| **Finite population correction** | Adjustment when sampling >5% of population | Apply when sample > 5% of population |

**Minimum cell size rule:** If any subgroup has <30 observations, note limitations and avoid making statistical claims for that subgroup.

## Sampling Plan Standard Components (7 Sections)

A quality sampling plan includes:

1. **Objective**: What the sample will be used for (survey, evaluation, DQA, monitoring)
2. **Target Population**: Who is being sampled, inclusion/exclusion criteria, geographic scope
3. **Sampling Frame**: Source of population list, completeness, currency, access
4. **Sampling Method**: Method selected with rationale, alternatives considered
5. **Sample Size Calculation**: Full calculation with all parameters documented
6. **Selection Procedure**: Step-by-step selection instructions (random number tables, PPS selection, stage-by-stage)
7. **Limitations & Mitigation**: Known constraints, their impact on representativeness, and mitigation strategies

## Scoring Criteria

**Section scores:**
- **PASS**: Methodologically sound, well-documented, appropriate for the research question
- **PARTIAL**: Exists but has gaps in documentation or methodological concerns
- **FAIL**: Missing, methodologically flawed, or would produce unrepresentative results

**Overall rating (from section scores):**
- **Strong**: 0 FAIL, max 1 PARTIAL
- **Adequate**: 0 FAIL, 2+ PARTIAL
- **Needs Revision**: 1 FAIL, or 3+ PARTIAL
- **Major Issues**: 2+ FAIL

**Issue severity:**
- **Critical (must fix)**: Would produce unrepresentative or biased results (e.g., convenience sampling claimed as random, no DEFF for cluster design)
- **Important (should fix)**: Reduces confidence in results or creates implementation problems
- **Minor (nice to fix)**: Documentation improvements that strengthen transparency

## Quality Dimensions (QCM Rubric)

These dimensions serve as the quality rubric for --create commands. The create workflow self-reviews drafts against these criteria and revises FAIL or PARTIAL dimensions before output.

When assessing a sampling plan, apply these 7 quality dimensions:

1. **Method Appropriateness**: Does the sampling method match the research question and practical constraints?
   - Common problems: cluster sampling for small population, SRS claimed but no sampling frame exists
2. **Sample Size Justification**: Is the calculation complete with all parameters documented?
   - Common problems: sample size asserted without calculation, no DEFF for clusters, no non-response buffer
3. **Sampling Frame Quality**: Is the frame defined, accessible, complete, and current?
   - Common problems: no frame documented, outdated population lists, incomplete geographic coverage
4. **Selection Procedure**: Are step-by-step instructions provided? Could someone else replicate the selection?
   - Common problems: "randomly select" with no procedure specified, PPS without probability calculation
5. **Disaggregation Feasibility**: Is the sample large enough to support required disaggregation?
   - Common problems: total sample adequate but subgroups too small, no power analysis for subgroup comparisons
6. **Practical Feasibility**: Can the sample be achieved within time, budget, and access constraints?
   - Common problems: sample requires visiting 200 villages in 2 weeks, no replacement procedure for inaccessible areas
7. **Limitations Transparency**: Are limitations stated honestly, and are mitigations proposed?
   - Common problems: no limitations section, limitations mentioned but dismissed without mitigation

## Cross-Document Extraction Knowledge

When project files are available, extract these elements to inform sampling plan work:

**From M&E Plan:**
- Planned data collection methods (which require sampling)
- Target population definitions
- Disaggregation requirements (determine minimum subgroup sizes)
- Data collection frequency and resources available

**From Logframe / Results Framework:**
- Indicators that require survey data (vs. routine monitoring)
- Target populations per indicator
- Geographic scope

**From Evaluation TOR:**
- Evaluation methodology requirements
- Comparison group requirements
- Required precision levels

**From Baseline Report:**
- Prior sampling methodology (for endline consistency)
- Achieved response rates (to calibrate non-response buffer)
- Lessons learned about access and logistics

**From Proposal / Project Document:**
- Budget allocated to data collection
- Target population size estimates
- Geographic coverage area

## File Discovery Patterns

When searching a project folder for M&E documents:

| Document Type | Search Patterns |
|---|---|
| Sampling Plan | `*sampling*`, `*sample size*`, `*survey design*`, `*methodology*` |
| M&E Plan | `*M&E plan*`, `*MEL plan*`, `*monitoring plan*`, `*AMELP*` |
| Logframe | `*logframe*`, `*results framework*`, `*log frame*`, `*RF*` |
| Evaluation TOR | `*TOR*`, `*terms of reference*`, `*SOW*` |
| Baseline Report | `*baseline*` |
| Proposal | `*proposal*`, `*project document*`, `*ProDoc*` |

Search both `.md`, `.txt`, `.docx`, and `.pdf` extensions. Confirm document identity with the user before proceeding.

## Methodology-Specific Flags

Raise these when relevant to the survey context:
- **Health:** Cluster immunization surveys (WHO 30x7 methodology), probability proportional to size (PPS) required
- **Food Security:** Seasonal timing critical (lean season vs. harvest); CARI/FCS methodology has specific sampling requirements
- **Education:** School-based vs. household-based sampling produces different results; account for absenteeism
- **Humanitarian:** Access constraints, mobile populations, rapidly changing denominators
- **Multi-country:** Harmonized sampling across countries requires consistent DEFF assumptions and comparable frames
