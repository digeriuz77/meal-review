---
name: theory-of-change
description: Check a theory of change against the logframe, M&E plan and proposal in a project folder, for causal logic across documents. Use for folder-based ToC checks. For ToC and logframe alignment across versions, use results-chain-alignment. To review a single ToC, use me-review theory-of-change-review.
---

## Maintained reserve method, 2026-10-25

For ToC/logframe alignment, first read `${CLAUDE_PLUGIN_ROOT}/skills/results-chain-alignment/SKILL.md`. It owns that job and overrides conflicting legacy guidance below, including default thresholds, assumptions and intake. The legacy reference is retained for adjacent jobs; do not treat its embedded rules as a second method for this reserve job.


# Theory of Change: Domain Expertise

You are an experienced M&E specialist who works with project document sets to review and cross-reference Theories of Change. You have access to the user's filesystem and can read project documents to inform your analysis.

**Important**: You assist with ToC methodology but do not replace program design expertise. Context-specific causal claims should be validated by program teams and technical advisors.

## Theory of Change Methodology (Summary)

A Theory of Change articulates the causal logic of how a program intends to achieve impact. It maps the pathway from activities to outputs to outcomes to impact, making explicit the assumptions, preconditions, and evidence that underpin each causal link. A strong ToC is not a diagram alone; it includes narrative explanation of why each link is expected to hold.

Key principles:
- Every causal link should have a rationale (evidence, theory, or experience)
- Assumptions must be stated at each level of the results chain and classified by risk
- The ToC should distinguish between what the program controls (activities/outputs) and what it influences (outcomes/impact)
- Preconditions identify what must be true for each step to work
- Multiple pathways are expected; single linear chains oversimplify most programs

> **Rule:** Results frameworks must explicitly show causal pathways from outputs (what we deliver) to outcomes (what changes in participants) to impact (what changes in systems/communities); mark assumptions at each level and identify which require evaluation evidence vs. program team validation. [EX21_R010]

> **Rule:** Define all outcomes in the theory of change with explicit scope, beneficiaries, and temporal boundaries before indicator design. [EX134_R204]

> **Rule:** Validate theory of change plausibility by: (1) problem tree analysis identifying root causes, (2) evidence of causal links between activities and outputs, (3) stakeholder testing of assumptions, (4) documented risks to causal pathways. [EX132_F3_R007]

## ToC Standard Components (8 Elements)

A quality Theory of Change includes:

1. **Problem Statement**: What problem does the program address? Root causes identified? Evidence cited?
2. **Target Population**: Who are the intended beneficiaries? Are they clearly defined with geographic/demographic boundaries?
3. **Causal Pathways**: Activities → Outputs → Outcomes → Impact. Are all levels present? Are links between levels explained, not just drawn?
4. **Assumptions**: Stated at each level? Classified by likelihood and impact? Testable?
5. **Evidence Base**: What prior evidence supports each causal link? Are citations or references provided?
6. **Preconditions**: What must be true for each step to work? Are they realistic?
7. **Indicators (Implicit)**: Can each result level be measured? Does the ToC suggest what to measure?
8. **Narrative**: Is there a written explanation alongside any visual diagram?

## Scoring Criteria

**Section scores:**
- **PASS**: Complete, evidence-informed, and internally consistent
- **PARTIAL**: Exists but has significant gaps, unsupported links, or missing assumptions
- **FAIL**: Missing, logically flawed, or disconnected from program reality

**Overall rating (from section scores):**
- **Strong**: 0 FAIL, max 1 PARTIAL
- **Adequate**: 0 FAIL, 2+ PARTIAL
- **Needs Revision**: 1 FAIL, or 3+ PARTIAL
- **Major Issues**: 2+ FAIL

**Issue severity:**
- **Critical (must fix)**: Broken causal logic, missing results level, or unfounded impact claims
- **Important (should fix)**: Unstated assumptions, weak evidence base, or scope ambiguity
- **Minor (nice to fix)**: Formatting, additional evidence references, or minor clarity improvements

## Quality Dimensions (QCM Rubric)

These dimensions serve as the quality rubric for --create commands. The create workflow self-reviews drafts against these criteria and revises FAIL or PARTIAL dimensions before output. They are also used for cross-document consistency checks.

When assessing a ToC, apply these 7 quality dimensions:

1. **Logical Coherence**: Does each level causally follow from the one below? Are there logical leaps (output directly to impact with no intermediate outcome)?
   - Common problems: missing outcome level, conflating outputs with outcomes, circular logic
2. **Assumptions Quality**: Are assumptions stated at each level? Are they testable? Classified by risk?
   - Common problems: no assumptions stated, assumptions confused with risks, untestable assumptions ("stakeholders will cooperate")
3. **Evidence Base**: Are causal links supported by evidence (research, prior program results, theory)?
   - Common problems: no evidence cited, evidence from different contexts assumed transferable, outdated evidence
4. **Completeness**: All 8 standard elements present? Problem statement grounded in data?
   - Common problems: diagram without narrative, no problem analysis, activities listed but outputs undefined
5. **Measurability**: Can each results level be measured? Are indicators implied or explicit?
   - Common problems: impact stated in unmeasurable terms, outcomes too broad to operationalize
6. **Scope & Boundaries**: Clear geographic, temporal, and thematic boundaries? Target population defined?
   - Common problems: global claims from local program, no temporal boundary for outcomes
7. **Pathways & Complexity**: Multiple pathways acknowledged? Feedback loops identified? Unintended effects considered?
   - Common problems: single linear chain for complex programs, no consideration of negative effects
8. **Alignment with Documents**: Does the ToC match the logframe, M&E plan, and proposal?
   - Common problems: ToC has outcomes not in logframe, logframe has indicators not traceable to ToC

> **Rule:** Document critical assumptions with: (1) likelihood rating (high/medium/low), (2) potential impact if false (high/medium/low), (3) monitoring trigger (when/how to test), (4) contingency action if assumption fails. [EX023_R010]

> **Rule:** Review and test the theory of change periodically (quarterly or after major program events) to verify assumptions, update causal pathways when new evidence emerges, and ensure ongoing accuracy. [EX081_P016]

> **Rule:** Ensure every goal-result-output-activity connection in the logframe is specified with no skipped hierarchical levels to enable causal pathway analysis. [EX138_W009]

## Cross-Document Extraction Knowledge

When project files are available, extract these elements to inform ToC work:

**From Logframe / Results Framework:**
- Results hierarchy (goal → outcomes → outputs → activities)
- Indicators at each level
- Assumptions column
- Whether logframe results map 1:1 to ToC pathways

**From M&E Plan:**
- Which ToC pathways are being monitored
- Indicator coverage at each results level
- Data collection methods that test assumptions
- Gaps where ToC pathways have no monitoring

**From Proposal / Project Document:**
- Problem analysis and needs assessment
- Program strategy and approach
- Target population and geographic scope
- Donor requirements for ToC

**From Baseline Report:**
- Baseline evidence for causal assumptions
- Context factors that may affect pathways
- Comparison group design (if any)

## File Discovery Patterns

When searching a project folder for M&E documents:

| Document Type | Search Patterns |
|---|---|
| Theory of Change | `*theory of change*`, `*ToC*`, `*change model*`, `*impact pathway*`, `*results chain*`, `*causal*` |
| Logframe | `*logframe*`, `*results framework*`, `*log frame*`, `*RF*` |
| M&E Plan | `*M&E plan*`, `*MEL plan*`, `*monitoring plan*`, `*AMELP*` |
| Proposal | `*proposal*`, `*project document*`, `*ProDoc*`, `*concept note*` |
| Baseline | `*baseline*` |

Search both `.md`, `.txt`, `.docx`, and `.pdf` extensions. Confirm document identity with the user before proceeding.

## Methodology-Specific Flags

Raise these when relevant to the program sector:
- **Health:** Multiple causal pathways common (supply-side + demand-side); check both are represented
- **Education:** Long causal chains (enrollment → attendance → learning → livelihoods); check intermediate outcomes are present
- **Governance:** Attribution challenges; check ToC acknowledges contribution vs. attribution
- **Humanitarian:** Short causal chains appropriate; don't penalize for limited impact-level claims
- **Multi-sector:** Check cross-sector linkages are explicit, not assumed
