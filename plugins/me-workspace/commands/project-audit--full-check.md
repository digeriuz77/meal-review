---
description: Run a comprehensive audit of the entire M&E document system checking coherence, consistency, and gaps across all project documents
argument-hint: "[path to project folder containing M&E documents]"
---

# /project-audit--full-check: Comprehensive M&E System Audit

Read all available M&E documents in a project folder and run a comprehensive system-level audit. Checks coherence across the entire document chain, identifies cross-document inconsistencies, and produces a health assessment with prioritized action items.

## Invocation

```
/me-workspace:project-audit--full-check

[path to project folder]
```

## Workflow

### Step 1: Discover and Classify Documents

Search the project folder using the project-audit skill's file discovery patterns. Present all candidates to the user:

```
I found these documents in your project folder:

M&E SYSTEM DOCUMENTS:
- [filename], appears to be a [Logframe / M&E Plan / etc.]
- [filename], appears to be a [...]

POSSIBLE ADDITIONAL DOCUMENTS:
- [filename], may be relevant (appears to be a [type])

NOT RECOGNIZED:
- [filename], could not classify

Which of these should I include in the audit? Are there any I'm missing?
```

Wait for user confirmation before proceeding. Read the first 50-100 lines of each candidate to verify its type.

### Step 2: Build Document Inventory

Create a document inventory showing what's present and what's missing:

| Document Type | Status | Filename | Notes |
|---|---|---|---|
| Theory of Change | Present / Missing / Partial | [name] | |
| Logframe | Present / Missing / Partial | [name] | |
| M&E Plan | Present / Missing / Partial | [name] | |
| Indicator Reference Sheets | Present / Missing / Partial | [name] | |
| Data Collection Tools | Present / Missing / Partial | [name] | |
| Proposal | Present / Missing / Partial | [name] | |
| Progress Report(s) | Present / Missing / Partial | [name] | |
| Evaluation TOR | Present / Missing / Partial | [name] | |
| Evaluation Report | Present / Missing / Partial | [name] | |
| Baseline Report | Present / Missing / Partial | [name] | |

### Step 3: Extract Key Elements from Each Document

Read each confirmed document and extract the elements needed for cross-checking. Build a consolidated reference for each cross-check item:

**Indicators:** Extract from every document that mentions indicators. Build a master comparison table.
**Geographic scope:** Extract from every document. Note discrepancies.
**Target populations:** Extract from every document. Note discrepancies.
**Timeline:** Extract from every document. Note discrepancies.
**Result statements:** Extract from every document. Note wording differences.

### Step 4: Run Audit Against 7 Dimensions

Assess each dimension per the project-audit skill's audit dimensions.

**Dimension 1: Design Coherence**
- Check ToC → logframe pathway alignment
- Verify IF-THEN logic at each logframe level
- Confirm assumptions are documented and testable
- Check that all results have indicators

**Dimension 2: Indicator System Quality**
- SMART-score a representative sample of indicators (all outcome/impact, sample of output)
- Check results level placement
- Verify baselines and targets
- Check disaggregation against requirements

**Dimension 3: Data Collection Alignment**
- Cross-check M&E plan methods against indicator types
- Verify frequency appropriateness
- Check data source accessibility
- Verify DQA procedures exist

**Dimension 4: Document Consistency**
- Run all cross-document consistency checks from the project-audit skill
- Build discrepancy tables for any inconsistencies found
- Prioritize by severity (target/scope discrepancies = Critical, wording differences = Minor)

**Dimension 5: Reporting Quality** (if progress reports available)
- Check indicator coverage against logframe
- Verify data plausibility
- Check narrative-data alignment
- Verify disaggregation

**Dimension 6: Evaluation Alignment** (if TOR/report available)
- Check question-to-logframe mapping
- Verify methodology leverages M&E plan data
- Check report answers all TOR questions
- Compare findings with monitoring data

**Dimension 7: Gap Analysis**
- Missing documents in the dependency chain
- Missing fields within documents
- Broken linkages between documents
- Missing quality assurance mechanisms

### Step 5: Assign Traffic Light Ratings

Rate each dimension per the project-audit skill's traffic light system:
- **GREEN:** 0 critical, max 2 important
- **YELLOW:** 0 critical + 3+ important, OR 1 critical resolved
- **RED:** 2+ critical issues
- **GREY:** Insufficient documents to assess

### Step 6: Calculate Overall System Health

Per the project-audit skill:
- **Healthy:** All GREEN or GREY
- **Manageable:** No RED, some YELLOW
- **At Risk:** 1 RED
- **Critical:** 2+ RED

### Step 7: Prioritize Actions

Create a prioritized action list. Group by urgency:

1. **Immediate (Critical issues):** Fix these before any reporting or evaluation
2. **Short-term (Important issues):** Fix within the next reporting period
3. **Medium-term (Minor issues):** Improve when opportunity arises
4. **Structural (Missing documents):** Create these to complete the M&E system

### Step 8: Generate Output

## Output Format

```markdown
## M&E System Audit

**Project folder:** [path]
**Documents audited:** [N]
**Audit date:** [date]
**Overall System Health:** [Healthy / Manageable / At Risk / Critical]

### Document Inventory

| Document | Status | Filename |
|---|---|---|
| Theory of Change | [Present/Missing] | [name or -] |
| Logframe | [Present/Missing] | [name or -] |
| M&E Plan | [Present/Missing] | [name or -] |
| Indicator Reference Sheets | [Present/Missing] | [name or -] |
| Data Collection Tools | [Present/Missing] | [name or -] |
| Proposal | [Present/Missing] | [name or -] |
| Progress Reports | [Present/Missing] | [name or -] |
| Evaluation TOR | [Present/Missing] | [name or -] |
| Evaluation Report | [Present/Missing] | [name or -] |
| Baseline Report | [Present/Missing] | [name or -] |

### System Health Dashboard

| Dimension | Rating | Critical | Important | Minor | Summary |
|---|---|---|---|---|---|
| Design Coherence | [GREEN/YELLOW/RED/GREY] | [N] | [N] | [N] | [one-line] |
| Indicator Quality | [GREEN/YELLOW/RED/GREY] | [N] | [N] | [N] | [one-line] |
| Data Collection | [GREEN/YELLOW/RED/GREY] | [N] | [N] | [N] | [one-line] |
| Document Consistency | [GREEN/YELLOW/RED/GREY] | [N] | [N] | [N] | [one-line] |
| Reporting Quality | [GREEN/YELLOW/RED/GREY] | [N] | [N] | [N] | [one-line] |
| Evaluation Alignment | [GREEN/YELLOW/RED/GREY] | [N] | [N] | [N] | [one-line] |
| Gap Analysis | [GREEN/YELLOW/RED/GREY] | [N] | [N] | [N] | [one-line] |

### Cross-Document Consistency Findings

| Check | Documents | Finding | Severity |
|---|---|---|---|
| Indicator targets | Logframe vs. Progress Report | Indicator 1.2 target differs (1000 vs. 1500) | Critical |
| Geographic scope | Proposal vs. M&E Plan | Proposal says 5 districts, M&E Plan says 3 | Critical |
| Baseline values | Logframe vs. IRS | Indicator 2.1 baseline differs (10% vs. 15%) | Important |

### Critical Issues (Fix Immediately)
1. [Issue, documents involved, specific discrepancy, recommended resolution]
2. [Issue, documents involved, specific discrepancy, recommended resolution]

### Important Issues (Fix This Quarter)
1. [Issue, documents involved, recommendation]

### Minor Issues (Improve When Possible)
1. [Issue, recommendation]

### Missing Documents

| Missing Document | Impact | Recommendation |
|---|---|---|
| [document type] | [what it affects] | [priority to create] |

### Priority Action Plan

| # | Action | Addresses | Documents to Update | Priority |
|---|---|---|---|---|
| 1 | [specific action] | [issue reference] | [document names] | Immediate |
| 2 | [specific action] | [issue reference] | [document names] | Short-term |
| 3 | [specific action] | [issue reference] | [document names] | Medium-term |

### Detailed Findings by Dimension
[Dimension-by-dimension analysis with evidence and document references]
```

## Notes

- This is the most comprehensive command in me-workspace. It orchestrates checks from all other domains. For targeted analysis, use domain-specific commands instead.
- The audit is only as good as the documents available. Many project folders will be incomplete. Rate missing dimensions as GREY, not FAIL.
- Document consistency is often the highest-value finding. Programs regularly have different indicator targets in the logframe vs. reports, or different geographic scope in the proposal vs. M&E plan. These inconsistencies are usually unintentional and easily fixed once identified.
- For large projects with many documents, read strategically: logframe and M&E plan first (core of the system), then reports and evaluations, then tools and guidelines.
- The traffic light dashboard is designed for senior management. The detailed findings are for the M&E team. Present both.
- Don't overwhelm the user. If you find 50+ issues, present the top 10 critical and important issues in the main output and offer to provide the complete list separately.
- If the project folder contains documents from multiple programs or time periods, clarify with the user which set to audit before proceeding.
