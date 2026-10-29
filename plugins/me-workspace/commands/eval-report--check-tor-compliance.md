---
description: Check whether an evaluation report answers all TOR questions, follows the required methodology, and delivers all required outputs
argument-hint: "[path to evaluation report and evaluation TOR]"
---

# /eval-report--check-tor-compliance: TOR Compliance Check

Compare an evaluation report against its Terms of Reference to verify that all evaluation questions were answered, the methodology followed requirements, and all deliverables were produced.

## Invocation

```
/me-workspace:eval-report--check-tor-compliance

[path to evaluation report and evaluation TOR]
```

## Workflow

### Step 1: Identify Documents

- **Required:** Evaluation report
- **Required:** Evaluation TOR (or SOW/commissioning brief)
- **Optional but valuable:** Logframe (for verifying findings against targets)

If `$ARGUMENTS` contains paths, use them directly. If a folder is given, search using the eval-report skill's file discovery patterns and confirm with the user.

### Step 2: Extract TOR Requirements

Read the TOR and extract a complete requirements inventory:

**Evaluation questions:**
- Every question (numbered), with DAC criteria mapping
- Sub-questions if present
- Priority or weighting if specified

**Methodology requirements:**
- Required or suggested design (experimental, quasi-experimental, mixed methods)
- Required data sources or methods
- Sampling requirements
- Geographic/thematic scope requirements
- Gender and inclusion requirements

**Deliverables:**
- Every required product (inception report, data tools, draft report, final report, presentation, brief)
- Format requirements (page limits, sections, annexes)
- Quality standards specified

**Team requirements:**
- Required expertise
- National/local team member requirements
- Independence provisions

**Ethical requirements:**
- IRB/ethics review
- Informed consent
- Data protection
- Do-no-harm provisions

### Step 3: Extract Report Content

Read the evaluation report and build a section map:
- Map which report sections address which TOR requirements
- Extract the methodology description
- Extract findings organized by evaluation question
- Note deliverables mentioned or included as annexes
- Extract team composition (if described)
- Extract ethics provisions described

### Step 4: Build Compliance Matrix

For each TOR requirement, assess report compliance:

**Evaluation question compliance:**

| # | TOR Question | Report Section | Coverage | Evidence Quality | Rating |
|---|---|---|---|---|---|
| Q1 | [question text] | Findings 4.1 | Full answer with data | Strong (survey + KII) | ADDRESSED |
| Q2 | [question text] | Findings 4.3 | Partial, missing disagg. | Moderate (KII only) | PARTIAL |
| Q3 | [question text] | Not found | - | - | MISSING |

**Rating scale for questions:**
- **ADDRESSED**: Question fully answered with sufficient evidence
- **PARTIAL**: Question answered but with gaps (missing disaggregation, weak evidence, incomplete scope)
- **MISSING**: Question not addressed at all in the report

**Methodology compliance:**

| TOR Requirement | Report Description | Compliant? | Notes |
|---|---|---|---|
| Mixed methods | Survey + FGD + KII described | YES | |
| Minimum 400 HH survey | "385 households surveyed" | PARTIAL | Below target, justification provided |
| Gender analysis | Not mentioned in methodology | NO | No gender-specific analysis tools |

**Deliverables compliance:**

| Deliverable | Status | Notes |
|---|---|---|
| Inception report | Mentioned in timeline | Cannot verify from report alone |
| Final report | This document | Present |
| Executive summary | Pages 1-3 | Present |
| Presentation/brief | Not mentioned | MISSING |
| Data collection tools | Annex C | Present |

### Step 5: Assess Evidence Quality Per Question

For each evaluation question that was addressed, assess:
- **Data sources cited:** What evidence supports the answer?
- **Triangulation:** Were multiple sources used?
- **Sample adequacy:** Is the sample sufficient for the claim?
- **Disaggregation:** Is the answer disaggregated as the TOR required?
- **Depth:** Does the answer address the full scope of the question?

### Step 6: Classify Issues

For each finding, classify severity per the eval-report skill's framework:
- **Critical:** Evaluation question not answered at all, methodology requirement violated in a way that invalidates findings
- **Important:** Question partially answered, methodology deviation without justification, deliverable missing
- **Minor:** Minor scope gap, additional analysis that would strengthen the answer

### Step 7: Generate Output

## Output Format

```markdown
## TOR Compliance Check

**Evaluation Report:** [filename]
**Evaluation TOR:** [filename]
**Logframe:** [filename or "not provided"]

### Compliance Summary

- **Evaluation questions:** [N] total
- **Fully addressed:** [N] ([%])
- **Partially addressed:** [N] ([%])
- **Not addressed:** [N] ([%])
- **Methodology requirements met:** [N] / [N total]
- **Deliverables present:** [N] / [N required]

### Evaluation Question Compliance

| # | TOR Question | DAC Criterion | Report Section | Coverage | Evidence | Rating |
|---|---|---|---|---|---|---|
| Q1 | [abbreviated] | Effectiveness | 4.1 | Full | Strong | ADDRESSED |
| Q2 | [abbreviated] | Efficiency | 4.3 | Partial | Moderate | PARTIAL |
| Q3 | [abbreviated] | Impact | - | - | - | MISSING |

### Detailed Question Analysis

**Q1: [full question text]**
- **Report coverage:** [where and how it's answered]
- **Evidence quality:** [data sources, sample, triangulation]
- **Gaps:** [what's missing or weak, if anything]

**Q2: [full question text]**
- **Report coverage:** [where and how it's answered]
- **Evidence quality:** [data sources, sample, triangulation]
- **Gaps:** [specific missing elements]

[Repeat for each question]

### Methodology Compliance

| TOR Requirement | Report Compliance | Status | Notes |
|---|---|---|---|
| [requirement] | [what report says] | MET/PARTIAL/NOT MET | [explanation] |

### Deliverables Checklist

| # | Required Deliverable | Status | Notes |
|---|---|---|---|
| 1 | [deliverable] | Present / Missing | [notes] |

### Critical Issues (Must Fix)
1. [Issue, TOR requirement, report gap, impact on evaluation utility]

### Important Issues (Should Fix)
1. [Issue, TOR requirement, report gap, recommendation]

### Minor Improvements
1. [Improvement, rationale]

### Overall Assessment

[2-3 sentence summary: How well does this report meet its TOR? What are the most significant gaps? Is the evaluation useful for its intended purpose despite any gaps?]
```

## Notes

- TOR compliance doesn't equal quality. A report can address all questions but with weak evidence. This check focuses on coverage; the `/eval-report--review` command assesses quality depth.
- Some methodology deviations are justified (access constraints, budget changes, sampling challenges). Flag them, but note when the report provides adequate justification.
- If the TOR was amended during the evaluation (e.g., through an inception report), note this and assess against the amended scope. Ask the user if unsure.
- Missing deliverables can only be partially assessed from the report itself. The report may reference an inception report or presentation that was delivered separately.
- For questions rated PARTIAL, provide specific language about what's missing so the evaluator or commissioner knows exactly what to address.
