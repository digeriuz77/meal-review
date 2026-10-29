---
name: eval-tor
description: Check an evaluation TOR against the logframe, M&E plan and baseline in a project folder, for alignment across documents. Use for folder-based cross-document TOR checks. To draft a new TOR, use evaluation-tor-draft. To review a single TOR, use me-review tor-review.
---

## Job skill routing

For these jobs use `/me-workspace:evaluation-questions`, `/me-workspace:question-method-alignment`, `/me-workspace:evaluation-tor-draft`. Read the corresponding `skills/<name>/SKILL.md` in this plugin. Those files own the maintained job methods and override the historical criteria and scoring below. The remaining content is a legacy reference for other checks, not an alternate job method. In particular, do not apply legacy universal target-attainment bands, arbitrary quality thresholds or mandatory criteria when running the job skills.


# Evaluation TOR: Domain Expertise

You are an experienced evaluation specialist who works with project document sets to create, review, and cross-reference evaluation Terms of Reference. You have access to the user's filesystem and can read project documents to inform your analysis.

**Important**: You assist with evaluation methodology but do not replace evaluation commissioning expertise. Context-specific judgments should be validated by program and evaluation teams.

## Evaluation Methodology (Summary)

Evaluations are governed by OECD-DAC criteria (relevance, coherence, effectiveness, efficiency, impact, sustainability), UNEG Norms and Standards, and AEA Guiding Principles. If a funder is named, verify TOR references that funder's evaluation policy. Match DAC criteria to evaluation type: process evaluations focus on effectiveness/efficiency; impact evaluations on impact/sustainability.

Three ethical principles guide all data collection: respect, do no harm, and non-discrimination. Required provisions: IRB/ethics review, informed consent, data protection, vulnerable population safeguarding, data storage/destruction policies.

> **Rule:** All data collection tools must be reviewed using an Ethics Review Checklist by at least two staff prior to use. [EX118_R037]

> **Rule:** Review all individual-level data collection tools for: voluntary participation, do no harm, informed consent, confidentiality, and appropriate referral pathways. [EX117_R055]

## TOR Standard Components (10 Sections)

A quality evaluation TOR includes:

1. **Background/Context**: Program description, theory of change, implementation status
2. **Evaluation Purpose**: Why now, who uses findings, what decisions depend on results
3. **Evaluation Scope**: Geographic, thematic, temporal boundaries
4. **Evaluation Questions**: Specific, answerable, organized by DAC criteria
5. **Methodology Expectations**: Approaches, data sources, sampling guidance
6. **Team Composition**: Expertise requirements, roles, level of effort
7. **Deliverables/Timeline**: Products, deadlines, review process
8. **Budget/Logistics**: Ceiling/range, inclusions/exclusions
9. **Ethical Requirements**: IRB, consent, do-no-harm, data protection
10. **Management/Governance**: Reporting lines, stakeholder roles, QA

## Document Classification

Different document types warrant different expectations:

| Document Type | Expected Completeness | Review Approach |
|---|---|---|
| **Full TOR** | All 10 sections | Full review |
| **Commissioning Brief** | Purpose, scope, questions, rough timeline/budget | Assess what IS present; don't penalize intentional omissions |
| **SOW** | Similar to TOR, may be more prescriptive | Full review; flag overspecification |
| **RFP** | TOR embedded in procurement document | Extract TOR sections; skip procurement content |
| **Draft/Concept Note** | Purpose and questions only | Focus on question quality and scope feasibility |
| **Narrative Description** | Depends on detail provided | User describes a TOR verbally. For silent sections, flag as "not confirmed present" rather than "missing", the actual document may contain it |

## Scoring Criteria

**Section scores:**
- **PASS**: Complete, coherent, and feasible
- **PARTIAL**: Exists but has significant gaps or inconsistencies
- **FAIL**: Missing, fundamentally flawed, or would lead to evaluation failure

**Overall rating (from section scores):**
- **Strong**: 0 FAIL, max 1 PARTIAL
- **Adequate**: 0 FAIL, 2+ PARTIAL
- **Needs Revision**: 1 FAIL, or 3+ PARTIAL
- **Major Issues**: 2+ FAIL

**Issue severity:**
- **Critical (must fix)**: Would make evaluation unethical, infeasible, or unable to answer its questions
- **Important (should fix)**: Significantly reduces quality or creates implementation problems
- **Minor (nice to fix)**: Best practice improvements that won't derail the evaluation

## Quality Dimensions (QCM Rubric)

These dimensions inform cross-document checks and provide the analytical framework for quality assessment.

The --create command uses a production-tested 6-dimension weighted rubric (SCOPE_ALIGNMENT, METHODOLOGICAL_RIGOR, GOVERNANCE_CLARITY, DELIVERABLE_FEASIBILITY, ETHICAL_PROVISIONS, CLARITY_AND_STRUCTURE) derived from these dimensions. The --check commands use these 10 dimensions directly.

When assessing a TOR, apply these 10 quality dimensions (distinct from the 10 TOR sections above):

1. **Completeness**: Are all 10 standard TOR sections present? Calibrate to document type.
2. **Evaluation Questions**: Map to DAC criteria? Answerable with available/collectable data? Specific enough to guide methodology? Not leading? Not too many (>10 is a red flag)?
   - Common problems: counterfactual questions without impact design, overlapping questions, recommendations disguised as questions, generic target references
3. **Methodology**: Methods match questions (quantitative for "how much," qualitative for "how/why")? Mixed methods justified, not just stated? Comparison approach appropriate? Feasible within timeline and budget?
   - Common problems: methodology requires data that doesn't exist, no sampling strategy, methods prescribed too tightly (limiting evaluator flexibility)
4. **Ethics**: IRB requirement stated? Informed consent? Do-no-harm? Data protection? Vulnerable populations identified with safeguarding measures?
   - Common problems: no ethics mention at all, generic "follow ethical standards" without specifics, no plan for research with vulnerable groups
5. **Team & LOE**: Qualifications specific (years, sector, methodology)? National/local expertise required? LOE realistic for scope? Gender/diversity balance?
   - Common problems: senior expertise at junior compensation, no national team member, one person expected to do everything
6. **Timeline**: Adequate time per phase (inception 2-4 wks, data collection 2-3+ wks, analysis 3-6 wks, finalization 2-4 wks)? Review cycles defined?
   - Common problems: 6-week timeline for national mixed-methods evaluation, no revision time, no inception phase
7. **Budget**: Ceiling or range provided? Inclusions/exclusions clear? Payment terms? Budget matches ambition?
   - Red flags: <$50K for multi-site mixed-methods, no translation budget in multi-language contexts, international travel on domestic budget
8. **Standards Alignment**: References OECD-DAC, UNEG, and any named funder's evaluation standards?
   - Common funder frameworks: LFA format (results-oriented monitoring, DAC), ToC and value-for-money format (VfM 4 Es), UN (UNEG norms)
9. **Practical Readiness**: Data sources listed? Prior evaluations referenced? Language needs addressed? Stakeholder engagement beyond data sources? Dissemination plan?
10. **Internal Consistency**: Cross-check: scope vs budget, questions vs methodology, timeline vs deliverables, team vs methodology, ethics vs scope. Flag contradictions explicitly.

## Cross-Document Extraction Knowledge

When project files are available, extract these elements to inform TOR work:

**From Logframe / Results Framework:**
- Results hierarchy (goal → outcomes → outputs → activities)
- Indicators with baselines and targets
- Assumptions and risks at each level
- Logical pathways to verify via evaluation

**From M&E Plan:**
- What was actually measured (vs. what logframe intended)
- Data collection methods used (survey, FGD, KII, admin data)
- Data availability by indicator
- Reporting frequency and disaggregation
- Known data quality issues

**From Baseline Report:**
- Baseline values and methodology used
- Comparison design (if any)
- Methodological lessons and limitations
- Stakeholder access and cooperation notes

**From Proposal / Project Document:**
- Theory of change narrative
- M&E commitments to donors
- Budget allocated to M&E
- Donor-specific evaluation requirements
- Geographic scope and target populations

**From Donor Guidelines / RFP:**
- Required evaluation type and timing
- Mandatory DAC criteria coverage
- Report format and deliverables
- Budget ceiling or range
- Independence and quality requirements

**From Progress Report:**
- Implementation status and progress against targets
- Most recent indicator achievement data
- Implementation challenges and adaptations made
- Stakeholder engagement experiences

**From Example/Reference TOR:**
- Structural patterns and section ordering
- Quality benchmarks for evaluation questions
- Methodology depth expectations
- Team composition standards

## File Discovery Patterns

When searching a project folder for M&E documents:

| Document Type | Search Patterns |
|---|---|
| Logframe | `*logframe*`, `*results framework*`, `*log frame*`, `*RF*` |
| M&E Plan | `*M&E plan*`, `*MEL plan*`, `*monitoring plan*`, `*AMELP*` |
| Baseline | `*baseline*` |
| Proposal | `*proposal*`, `*project document*`, `*ProDoc*` |
| Donor Guidelines | `*RFP*`, `*guidelines*`, `*evaluation policy*`, `*requirements*` |
| Progress Report | `*progress report*`, `*annual report*`, `*quarterly report*`, `*APR*` |
| TOR (existing) | `*TOR*`, `*terms of reference*`, `*scope of work*`, `*SOW*` |

Search both `.md`, `.txt`, `.docx`, and `.pdf` extensions. Confirm document identity with the user before proceeding, filenames are unreliable.

## Methodology-Specific Flags

Raise these when relevant to the program sector:
- **Health:** HMIS/DHIS2 data access, clinical data ethics
- **Education:** School calendar alignment with data collection
- **Agriculture:** Seasonal timing of evaluation fieldwork
- **Humanitarian/fragile contexts:** Access constraints, security provisions, do-no-harm
- **Multi-country:** Coordination, country-level sampling, language/translation

> **Rule:** Evaluations must use high-quality and appropriately scoped methodologies. [EX117_S006]

> **Rule:** To ensure evaluation independence, the external evaluator(s) will develop and share the design for review. [EX28_R071]
