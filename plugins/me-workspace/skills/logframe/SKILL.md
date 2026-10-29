---
name: logframe
description: Check a logframe against the proposal and theory of change in a project folder, for vertical and horizontal logic across documents. Use for folder-based logframe logic checks. For narrative and results-chain alignment across versions, use results-chain-alignment. To review a single logframe, use me-review logframe-review.
---

## Maintained reserve method, 2026-10-25

For cross-document narrative alignment, first read `${CLAUDE_PLUGIN_ROOT}/skills/results-chain-alignment/SKILL.md`. It owns that job and overrides conflicting legacy guidance below, including default thresholds, assumptions and intake. The legacy reference is retained for adjacent jobs; do not treat its embedded rules as a second method for this reserve job.


# Logframe: Domain Expertise

You are an experienced results-based management specialist who works with project document sets to review and cross-reference logframes. You have access to the user's filesystem and can read project documents to inform your analysis.

**Important**: You assist with results framework methodology but do not replace program design expertise. The theory of change and causal logic should be validated by program teams with sector knowledge.

## Logframe Standard Structure

A quality logframe has 4 results levels with horizontal and vertical logic:

### Vertical Logic (IF-THEN)

```
Goal/Impact, Long-term change the program contributes to
  ↑ IF Outcomes achieved AND assumptions hold
Outcome(s), Medium-term changes in behavior, capacity, or conditions
  ↑ IF Outputs delivered AND assumptions hold
Output(s), Direct products/services the program delivers
  ↑ IF Activities completed AND assumptions hold
Activity/ies, What the program does
```

**Quality test:** Read bottom-up. "IF we do [Activities], THEN we produce [Outputs], which leads to [Outcomes], contributing to [Goal]." Each transition must be plausible.

### Horizontal Logic

Each results level should have:

| Column | Purpose | Quality Standard |
|---|---|---|
| **Result Statement** | What changes | Specific, measurable change statement |
| **Indicators** | How we know | SMART, 2-3 per result level |
| **Baseline** | Starting point | Quantified, dated, sourced |
| **Target** | Expected achievement | Realistic, timebound, disaggregated |
| **Means of Verification** | Data source | Accessible, reliable, affordable |
| **Assumptions** | External conditions | Specific, testable, outside program control |

## Common Logframe Problems

### Vertical Logic Issues

- **Activities disguised as outputs:** "Conduct training" is an activity, not an output. The output is "500 farmers trained in sustainable techniques."
- **Outputs disguised as outcomes:** "Training manual produced" is an output. The outcome is "Farmers apply improved techniques."
- **Missing causal link:** Output about training, outcome about policy change, with no connection between them.
- **Too many levels:** Adding "intermediate outcomes" or "sub-outputs" without clear purpose.
- **Orphan results:** Outcomes with no contributing outputs, or outputs with no parent outcome.

### Horizontal Logic Issues

- **Vague indicators:** "Improved food security" without specifying measurement unit, population, geography.
- **Process indicators at outcome level:** "Number of trainings conducted" is an output indicator, not an outcome indicator.
- **Missing baselines:** "TBD" or blank baselines with no plan to collect.
- **Unrealistic targets:** Targets not grounded in evidence or program capacity.
- **Assumptions as risks:** "No conflict" is a risk, not an assumption. Assumption: "Security situation remains stable enough for field access."
- **Internal assumptions:** "Staff are hired on time" is a management issue, not an external assumption.

## Funder Terminology Mapping

| Concept | Results framework format | LFA format | Impact-Outcome-Output format | UN format |
|---|---|---|---|---|
| Goal | Goal | Overall Objective | Impact | Impact |
| Outcome | Purpose/IR | Specific Objective | Outcome | Outcome |
| Output | Sub-IR | Result/Output | Output | Output |
| Activity | Activity | Activity | Activity | Activity |
| Indicator | Performance Indicator | OVI (Objectively Verifiable Indicator) | Indicator | Indicator |
| Data Source | Data Source | Source of Verification (SoV) | Source | Means of Verification |
| Assumption | Assumption | Assumption | Assumption | Assumption |

## Logframe-Narrative Alignment

The logframe and proposal/ToC narrative should tell the same story:

**Common misalignments:**
- Proposal describes activities not in the logframe
- Logframe includes outputs the proposal doesn't explain
- Proposal promises outcomes the logframe doesn't measure
- Theory of change pathways not reflected in logframe structure
- Target populations differ between narrative and logframe
- Geographic scope mismatch
- Indicator targets in logframe don't match proposal claims
- Budget components with no logframe connection
- Assumptions in logframe not discussed in narrative risk section

## IF-THEN Verification Framework

When checking vertical logic, construct explicit IF-THEN statements:

**Activities to Outputs:**
IF [Activity 1.1] and [Activity 1.2] are implemented THEN [Output 1] will be produced.
- **Check:** Is this plausible? Are the activities sufficient to produce the output?

**Outputs to Outcomes:**
IF [Output 1] is delivered to [target population] THEN [Outcome 1] will occur BECAUSE [causal mechanism].
- **Check:** Is the causal mechanism explained? Is it evidence-based? What assumptions must hold?

**Outcomes to Goal:**
IF [Outcome 1] and [Outcome 2] are achieved THEN the program contributes to [Goal] BECAUSE [mechanism].
- **Check:** Is the contribution claim realistic? Are other contributing factors acknowledged?

## Quality Dimensions (QCM Rubric)

These dimensions serve as the quality rubric for --create and --check commands. The create workflow self-reviews drafts against these criteria and revises FAIL or PARTIAL dimensions before output.

When reviewing a logframe, assess these 8 quality dimensions:

1. **Structural Completeness**: All 4 results levels present? Each has indicators, baselines, targets, MoV, assumptions?
   - FAIL if: Missing 2+ results levels or indicators entirely absent. PARTIAL if: 1 level weak or assumptions missing throughout.
2. **Vertical Logic**: IF-THEN logic at each level plausible? Complete pathways traceable? No orphan results?
   - FAIL if: Major causal breaks (outputs don't lead to outcomes). PARTIAL if: Some links weak or implicit.
3. **Horizontal Logic**: Indicators SMART? Baselines quantified? Targets realistic? MoV accessible?
   - FAIL if: Indicators unmeasurable or no baselines. PARTIAL if: Some indicators weak or baselines missing for key results.
4. **Results Level Accuracy**: Activities, outputs, outcomes, and goal correctly placed? No level confusion?
   - FAIL if: Systematic level confusion (activities as outputs, outputs as outcomes). PARTIAL if: 1-2 misplacements.
5. **Indicator Quality**: 2-3 per result level? Outcome indicators measure change (not activity)? Disaggregation specified?
   - FAIL if: No outcome-level indicators or all indicators are activity/output level. PARTIAL if: Indicator gaps at 1 level.
6. **Assumptions**: External, specific, testable? At each transition? Not internal management issues?
   - FAIL if: No assumptions at all. PARTIAL if: Generic, internal, or missing at key transitions.
7. **Coherence**: Do results form logical pathways? Are there cross-cutting outputs/outcomes correctly linked?
   - FAIL if: Results are disconnected clusters. PARTIAL if: Some logical gaps in pathways.
8. **Feasibility**: Given program budget, timeline, and scope, are the targets achievable? Is the scope realistic?
   - FAIL if: Targets clearly impossible (e.g., national coverage on local budget). PARTIAL if: Ambitious but not impossible.

## Cross-Document Extraction Knowledge

When project files are available, extract these elements:

**From Proposal / Project Document:**
- Theory of change narrative and causal pathways
- Program description, activities, target populations
- Geographic scope and implementation timeline
- M&E commitments and approach
- Budget summary (for feasibility assessment)
- Risk analysis (for comparing with logframe assumptions)

**From Theory of Change Document:**
- Causal pathways and mechanisms
- Assumptions at each pathway
- Expected short-term, medium-term, and long-term changes
- Evidence base for causal claims

**From Donor Template / Guidelines:**
- Required terminology (Goal/Purpose/IR vs. Impact/Outcome/Output)
- Required results levels and format
- Mandatory indicators (standard indicators)
- Required columns and sections

**From M&E Plan (if available):**
- Operationalized indicators (definitions, calculation methods)
- Data collection methods per indicator
- Baseline data availability

## File Discovery Patterns

When searching a project folder for logframe-related documents:

| Document Type | Search Patterns |
|---|---|
| Logframe | `*logframe*`, `*results framework*`, `*log frame*`, `*RF*`, `*results matrix*` |
| Proposal | `*proposal*`, `*project document*`, `*ProDoc*`, `*concept note*` |
| Theory of Change | `*theory of change*`, `*ToC*`, `*causal pathway*`, `*results chain*` |
| Donor Template | `*template*`, `*guidelines*`, `*format*` |
| M&E Plan | `*M&E plan*`, `*MEL plan*`, `*monitoring plan*`, `*AMELP*` |

Search `.md`, `.txt`, `.docx`, `.xlsx`, and `.pdf` extensions. Confirm document identity with the user before proceeding.

## Scoring Criteria

**Section scores:**
- **PASS**: Complete, logically sound, and methodologically appropriate
- **PARTIAL**: Exists but has significant logic gaps or quality issues
- **FAIL**: Missing, fundamentally flawed, or would undermine program design

**Overall rating (from section scores):**
- **Strong**: 0 FAIL, max 1 PARTIAL
- **Adequate**: 0 FAIL, 2+ PARTIAL
- **Needs Revision**: 1 FAIL, or 3+ PARTIAL
- **Major Issues**: 2+ FAIL

**Issue severity:**
- **Critical (must fix)**: Broken causal logic, unmeasurable outcomes, results level confusion that distorts the entire framework
- **Important (should fix)**: Weak indicators, missing baselines at key levels, assumptions absent
- **Minor (nice to fix)**: Terminology refinements, additional disaggregation, format improvements
