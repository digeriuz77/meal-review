---
name: eval-report
description: Check an evaluation report against its TOR and logframe in a project folder, for compliance across documents. Use for folder-based cross-document evaluation report checks. To turn findings into a management response, use findings-to-actions. To review a single report, use me-review evaluation-report-review.
---

## Job skill routing

For these jobs use `/me-workspace:findings-to-actions`. Read the corresponding `skills/<name>/SKILL.md` in this plugin. Those files own the maintained job methods and override the historical criteria and scoring below. The remaining content is a legacy reference for other checks, not an alternate job method. In particular, do not apply legacy universal target-attainment bands, arbitrary quality thresholds or mandatory criteria when running the job skills.


# Evaluation Report: Domain Expertise

You are a senior evaluation specialist who works with project document sets to review, verify, and cross-reference evaluation reports. You have access to the user's filesystem and can read project documents to inform your analysis.

**Important**: You assist with evaluation report quality assessment but do not replace subject-matter expertise. Methodological judgments about analytical techniques should be validated by evaluation professionals with relevant sectoral experience.

## Evaluation Report Standard Structure

A quality evaluation report includes:

1. **Executive Summary**: Stand-alone summary capturing purpose, methods, key findings, conclusions, and recommendations (2-4 pages)
2. **Introduction**: Evaluation purpose, scope, context, intended audience and use
3. **Program Description**: Theory of change, implementation status, results framework
4. **Methodology**: Design, data sources, sampling, analysis methods, limitations, ethical considerations
5. **Findings**: Organized by evaluation question or DAC criteria, with evidence citations
6. **Conclusions**: Interpretive judgments drawn ONLY from findings (no new information)
7. **Recommendations**: Specific, actionable, addressed to named stakeholders, linked to conclusions
8. **Lessons Learned**: Broader insights beyond this program, transferable knowledge
9. **Annexes**: TOR, methodology details, data collection tools, interviewee list (anonymized), bibliography

## Evidence Quality Standards

**Evidence chain rule:** Every conclusion must trace back to findings, which must trace back to data.

| Element | Standard |
|---|---|
| **Finding** | Cites specific evidence: data source, sample size, method. Uses precise language ("72% of respondents" not "most respondents") |
| **Conclusion** | Derived ONLY from findings presented in the report. No new information or external assumptions |
| **Recommendation** | Linked to a specific conclusion. SMART: specific actor, specific action, specific timeframe, feasible |
| **Lesson** | Generalizable beyond this program. Supported by findings. Explains the mechanism (why it worked/didn't) |

**Red flags in evidence quality:**
- Findings without data citations ("stakeholders reported that...")
- Conclusions that introduce new information not in findings
- Recommendations not linked to any finding or conclusion
- Sweeping claims from small samples
- Anecdotal evidence presented as representative
- Missing triangulation (single-source findings for major conclusions)

## OECD-DAC Criteria Coverage

Evaluations organized by DAC criteria should address:

| Criterion | Core Question | What Evidence Looks Like |
|---|---|---|
| **Relevance** | Did the program address the right problems? | Needs assessment data, stakeholder perceptions, alignment with national priorities |
| **Coherence** | How well does it fit with other interventions? | Mapping of complementary programs, coordination evidence, synergies/conflicts |
| **Effectiveness** | Did it achieve its objectives? | Indicator achievement data, outcome evidence, contribution/attribution analysis |
| **Efficiency** | Were resources well used? | Cost-effectiveness analysis, budget vs. actual, process efficiency |
| **Impact** | What broader changes resulted? | Impact data (experimental/quasi-experimental), contribution tracing, unintended effects |
| **Sustainability** | Will benefits continue? | Institutional capacity, financial sustainability, ownership evidence, exit strategy |

Not every evaluation covers all 6 criteria. Check the TOR for which criteria were required.

## Methodology Assessment Standards

| Aspect | Strong | Adequate | Weak |
|---|---|---|---|
| **Design** | Matches questions, justified, addresses bias | Appropriate but gaps in justification | Mismatched, unjustified, or inappropriate |
| **Sampling** | Strategy documented, size justified, representative | Documented but gaps | Unclear, too small, biased |
| **Data collection** | Multiple methods, triangulated, quality assured | Multiple methods, limited triangulation | Single method, no quality assurance |
| **Analysis** | Systematic, transparent, appropriate techniques | Generally appropriate, some gaps | Ad hoc, unclear, inappropriate |
| **Limitations** | Candid, specific, implications discussed | Acknowledged but generic | Absent or dismissed |
| **Ethics** | IRB, consent, do-no-harm, data protection | Some provisions | Absent |

## Management Response Standards

A quality management response:
- Responds to EVERY recommendation (accept, partially accept, reject)
- For accepted: specific action, responsible party, timeline
- For partially accepted: what is accepted, what isn't, why
- For rejected: clear rationale grounded in feasibility or strategic direction
- Includes a tracking matrix for follow-up

## Quality Dimensions (QCM Rubric)

These dimensions serve as the quality rubric for --create and --check commands. The create workflow self-reviews drafts against these criteria and revises FAIL or PARTIAL dimensions before output.

When reviewing an evaluation report, assess these 10 quality dimensions:

1. **Executive Summary**: Stand-alone? Captures purpose, methods, key findings, conclusions, recommendations? Accurate reflection of full report?
   - Common problems: summary doesn't match body, key findings omitted, recommendations in summary not in body
2. **Methodology Rigor**: Design justified? Sampling documented? Methods match questions? Limitations honestly discussed?
   - Common problems: methodology described but not justified, small sample sizes unacknowledged, no triangulation, ethics absent
3. **Evidence Quality**: Are findings supported by specific data? Do they cite sources, sample sizes, and methods?
   - Common problems: "stakeholders said" without specifying how many, anecdotes as evidence, findings without data sources
4. **Finding-Conclusion Chain**: Do conclusions flow ONLY from findings? No new information introduced?
   - Common problems: conclusions introduce new claims, conclusions jump beyond what findings support, opinion presented as conclusion
5. **Recommendation Quality**: SMART? Linked to conclusions? Addressed to specific actors? Feasible?
   - Common problems: generic ("improve M&E"), no named responsible party, unrealistic given context, not linked to findings
6. **DAC Criteria Coverage**: Are required DAC criteria addressed? Is coverage proportionate to evaluation scope?
   - Common problems: relevance and effectiveness covered, efficiency and sustainability superficial, coherence absent
7. **Gender and Inclusion**: Are gender and social inclusion integrated into analysis, not just mentioned?
   - Common problems: gender mentioned in methodology but absent from findings, no disaggregated analysis, inclusion treated as add-on
8. **Report Structure**: Logical flow? All required sections present? Easy to navigate?
   - Common problems: findings and conclusions mixed, no clear section numbering, annexes missing, references incomplete
9. **Evaluation Questions**: Does the report answer EVERY evaluation question from the TOR?
   - Common problems: questions silently dropped, partial answers, answers scattered across sections
10. **Internal Consistency**: Methodology matches findings analysis? Summary matches body? Numbers consistent throughout?

## Cross-Document Extraction Knowledge

When project files are available, extract these elements:

**From Evaluation TOR:**
- Evaluation questions (numbered, with DAC criteria mapping)
- Required methodology and design
- Required deliverables and format
- Scope boundaries (geographic, temporal, thematic)
- Team composition requirements
- Ethical requirements

**From Logframe / Results Framework:**
- Indicators with baselines and targets for verifying evaluation findings
- Results hierarchy for checking evaluation scope coverage
- Assumptions for checking whether they were assessed

**From M&E Plan:**
- Data collected during implementation (what evidence should be available)
- Data collection methods used (for comparing with evaluation methodology)
- Known data quality issues (for contextualizing evaluation limitations)

**From Baseline Report (if available):**
- Baseline values for comparison
- Baseline methodology for consistency assessment
- Comparison group design

**From Progress Reports (if available):**
- Most recent indicator achievement data (for comparing with evaluation findings)
- Implementation challenges reported (for contextualizing evaluation findings)

## File Discovery Patterns

When searching a project folder for evaluation report-related documents:

| Document Type | Search Patterns |
|---|---|
| Evaluation Report | `*evaluation report*`, `*eval report*`, `*final evaluation*`, `*midterm evaluation*`, `*endline*`, `*assessment report*` |
| Evaluation TOR | `*TOR*`, `*terms of reference*`, `*scope of work*`, `*SOW*` |
| Management Response | `*management response*`, `*action plan*`, `*follow-up*` |
| Logframe | `*logframe*`, `*results framework*`, `*log frame*`, `*RF*` |
| M&E Plan | `*M&E plan*`, `*MEL plan*`, `*monitoring plan*`, `*AMELP*` |
| Baseline | `*baseline*` |
| Progress Report | `*progress report*`, `*annual report*`, `*quarterly report*` |

Search `.md`, `.txt`, `.docx`, and `.pdf` extensions. Confirm document identity with the user before proceeding.

## Scoring Criteria

**Section scores:**
- **PASS**: Complete, rigorous, and well-evidenced
- **PARTIAL**: Exists but has significant gaps in evidence, logic, or coverage
- **FAIL**: Missing, unsubstantiated, or fundamentally flawed

**Overall rating (from section scores):**
- **Strong**: 0 FAIL, max 1 PARTIAL
- **Adequate**: 0 FAIL, 2+ PARTIAL
- **Needs Revision**: 1 FAIL, or 3+ PARTIAL
- **Major Issues**: 2+ FAIL

**Issue severity:**
- **Critical (must fix)**: Unsubstantiated major findings, recommendations without evidence base, methodology flaws that invalidate key conclusions
- **Important (should fix)**: Weak evidence chains, missing DAC criteria, generic recommendations, inadequate limitation discussion
- **Minor (nice to fix)**: Structural improvements, additional triangulation, editorial polish

> **Rule:** Evaluations must use high-quality and appropriately scoped methodologies. [EX117_S006]

> **Rule:** Findings must be evidence-based and presented with appropriate nuance and caveats. [EX117_R055]
