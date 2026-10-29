---
description: Check whether a proposal responds to all requirements in an RFP, with focus on M&E requirements
argument-hint: "[path to proposal and RFP/donor guidelines files]"
---

# /proposal--check-rfp: RFP Compliance Check

Compare a proposal against its RFP (or donor guidelines) to identify missed requirements, partial responses, and M&E-specific gaps. Produces a requirement-by-requirement coverage table with severity classification.

## Invocation

```
/me-workspace:proposal--check-rfp

[path to proposal and RFP files]
```

## Workflow

### Step 1: Identify Documents

Two documents needed:
- **Required:** Proposal (draft or final)
- **Required:** RFP / Call for Proposals / NOFO / Donor Guidelines

If `$ARGUMENTS` contains paths, use them. If a folder is given, search using the proposal skill's file discovery patterns. Confirm with the user.

**Optional context:** Logframe, M&E Plan, Budget, for verifying proposal claims.

### Step 2: Extract Requirements from RFP

Read the RFP systematically and extract ALL requirements, organized by category per the proposal skill's RFP requirement patterns:

**Administrative/Format requirements:**
- Page limits, formatting rules, required sections
- Required annexes
- Submission requirements

**Technical requirements:**
- Mandatory programmatic sections
- Required approaches or methodologies
- Geographic/thematic constraints
- Partnership requirements

**M&E-specific requirements:**
- Required indicators (standard and custom)
- Evaluation design requirements
- Baseline/endline requirements
- Disaggregation requirements
- Learning/CLA requirements
- Reporting frequency and format

**Budget requirements:**
- Budget ceiling or range
- Cost share / matching
- Allowed/disallowed costs

**Evaluation criteria** (if provided):
- Scoring sections and weights
- Pass/fail thresholds

Number each requirement for tracking (e.g., A1, A2 for admin; T1, T2 for technical; M1, M2 for M&E; B1, B2 for budget).

### Step 3: Map Proposal Against Requirements

Read the proposal and build a section map. For each extracted requirement:
1. Search the proposal for where it's addressed
2. Classify coverage: **Addressed** / **Partial** / **Missing** (per proposal skill's scoring criteria)
3. Note the proposal section and page/line where addressed
4. For Partial: explain what's missing

### Step 4: Deep-Dive on M&E Requirements

For M&E-specific requirements, go beyond surface coverage:

- **Required indicators:** Are they present? Properly defined? With baselines and targets?
- **Evaluation design:** Does the proposal commit to the required design? Is it feasible?
- **Disaggregation:** Does the M&E section (or logframe annex) show required disaggregation?
- **Reporting:** Does the proposal acknowledge the reporting schedule and format?
- **Learning/CLA:** Is there a genuine learning approach, or just boilerplate?

If logframe or M&E plan available as context files, cross-reference:
- Do proposal M&E claims match the logframe indicators?
- Does the M&E plan support the evaluation commitments made in the proposal?
- Is the M&E budget adequate for stated M&E activities?

### Step 5: Assess Competitive Positioning (if evaluation criteria available)

If the RFP includes scoring criteria:
- Map proposal strengths to high-weight sections
- Identify where the proposal is weakest relative to scoring weights
- Flag M&E scoring weight, donors typically allocate 10-25% to M&E

### Step 6: Classify Issues

For each gap or concern:
- **Critical (must fix)**: Would likely result in disqualification (mandatory requirement missing, format violation, over budget)
- **Important (should fix)**: Significantly weakens competitive score (weak M&E section, vague methodology, missing indicators)
- **Minor (nice to fix)**: Improvements for competitive edge (stronger CLA language, better disaggregation, clearer DQA)

### Step 7: Generate Output

## Output Format

```markdown
## RFP Compliance Check

**Proposal:** [filename]
**RFP:** [filename]
**Context files:** [list or "none"]

### Compliance Summary

| Category | Total Requirements | Addressed | Partial | Missing |
|---|---|---|---|---|
| Administrative/Format | [N] | [N] | [N] | [N] |
| Technical | [N] | [N] | [N] | [N] |
| M&E-Specific | [N] | [N] | [N] | [N] |
| Budget | [N] | [N] | [N] | [N] |
| **Total** | **[N]** | **[N]** | **[N]** | **[N]** |

### Overall Compliance: [N]% addressed, [N]% partial, [N]% missing

### Requirement Coverage Detail

#### Administrative/Format Requirements

| # | Requirement | Coverage | Proposal Section | Notes |
|---|---|---|---|---|
| A1 | [requirement text] | Addressed | Section 2.1 | |
| A2 | [requirement text] | Missing | - | [what's needed] |

#### Technical Requirements

| # | Requirement | Coverage | Proposal Section | Notes |
|---|---|---|---|---|

#### M&E-Specific Requirements

| # | Requirement | Coverage | Proposal Section | Notes |
|---|---|---|---|---|
| M1 | [requirement text] | Addressed | M&E Section, p.12 | |
| M2 | [requirement text] | Partial | M&E Section, p.13 | Mentions but doesn't specify method |

#### Budget Requirements

| # | Requirement | Coverage | Proposal Section | Notes |
|---|---|---|---|---|

### Critical Issues (Must Fix Before Submission)
1. [Issue, RFP requirement reference, specific fix]

### Important Issues (Should Fix)
1. [Issue, RFP requirement reference, specific fix]

### Minor Improvements
1. [Improvement, competitive rationale]

### M&E Section Assessment
[Focused analysis of M&E-specific requirements with cross-references to logframe/M&E plan if available]

### Competitive Positioning (if evaluation criteria available)
[Scoring weight analysis, where proposal is strong/weak relative to weights]
```

## Notes

- RFP compliance is binary for mandatory requirements, either you meet them or you risk disqualification. Be unambiguous about which requirements are mandatory vs. preferred.
- "Addressed" means the requirement is fully and clearly met, not just mentioned. A vague reference to "we will monitor and evaluate" does not address a requirement for "a detailed M&E plan with SMART indicators."
- When the RFP says "should" vs "must" vs "shall," distinguish between requirements (must/shall) and preferences (should). Flag all as requirements but note which are formally mandatory.
- Some RFPs embed requirements in narrative paragraphs rather than numbered lists. Read the full RFP carefully, requirements hidden in body text are still requirements.
- If the proposal exceeds page limits, flag this as Critical, many donors will not review over-length proposals.
