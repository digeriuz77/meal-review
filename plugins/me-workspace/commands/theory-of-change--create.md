---
description: Generate a structured Theory of Change from project documents with causal pathway validation and weighted QCM quality gates
argument-hint: "[path to project folder or program documents]"
---

# /theory-of-change--create -- Generate Theory of Change from Project Files

Create a complete Theory of Change through a structured pipeline: analyze program context, extract the causal logic, draft pathways with assumptions and evidence, validate structural integrity, score against a weighted quality rubric, and revise failing dimensions before delivering.

This workflow mirrors the production pipeline chain `mel-system/toc.json` and embeds its tested prompts, validation logic, and quality criteria.

## Invocation

```
/me-workspace:theory-of-change--create

[path to project folder, or list specific files]
```

---

## Workflow

### Step 1: DISCOVER

Search project folder using the theory-of-change skill's file discovery patterns. Present discovered files, confirm with user.

**Minimum required:** Proposal OR logframe (proposal preferred for problem analysis and program strategy).
**Useful but optional:** Logframe, M&E plan, baseline report, existing ToC (if updating).

Wait for user confirmation.

### Step 2: EXTRACT

**Behavioral guidance: Be precise. Extract, do not create. Stay faithful to source documents.**

Read each document and extract the program's core logic:

1. What is the ultimate **GOAL** (long-term change)?
2. What **OUTCOMES** (medium-term changes) contribute to the goal?
3. What **OUTPUTS** (direct deliverables) produce each outcome?
4. What **ACTIVITIES** generate each output?
5. What **ASSUMPTIONS** must hold for the causal chain to work?

Be specific to THIS program. Do not generate generic M&E content. Every element must trace directly to information in the documents.

**Evidence rules:**
- Extract SPECIFIC values, not approximations
- Note when information is missing vs. available
- Flag ambiguities or contradictions between documents
- Identify gaps in the causal logic that the ToC must address

Show extraction summary:

```
EXTRACTION SUMMARY:
- Results levels found: Goal ([N]), Outcomes ([N]), Outputs ([N]), Activities ([N])
- Assumptions extracted: [N] (from logframe/proposal)
- Problem analysis: [Found in proposal Section X / Not found]
- Evidence base: [What evidence exists for causal links]
- Gaps: [What is missing from source documents]
- Contradictions: [Any conflicts between documents]
```

### Step 3: CLARIFY

Ask guided questions:
- **Program theory:** What is the core "change hypothesis"? (e.g., "If we train health workers AND improve supply chains, maternal health outcomes will improve")
- **Multiple pathways:** Does the program have distinct pathways (e.g., supply-side vs. demand-side)?
- **Contribution vs. attribution:** Is the program the primary driver of change, or one contributor among many?
- **Known risks to causal logic:** Are there pathways the team is uncertain about?
- **Audience:** Who is the ToC for? (Internal team, donor, evaluation reference?)

Skip questions answered by documents. Wait for response.

### Step 4: DECOMPOSE

**Behavioral guidance: This is analytical. Map the structure before drafting.**

Break the ToC into its 8 required elements. For each, note what source material is available:

1. **Problem Statement** -- source: proposal needs assessment
2. **Target Population** -- source: proposal/logframe scope
3. **Causal Pathways** -- source: logframe results hierarchy + user's change hypothesis
4. **Assumptions** -- source: logframe assumptions column + identified risks
5. **Evidence Base** -- source: baseline report, cited research, program experience
6. **Preconditions** -- source: proposal context analysis
7. **Indicators** -- source: logframe indicators (what to measure at each level)
8. **Narrative** -- synthesized from all of the above

Flag any elements where source material is thin or absent.

### Step 5: DRAFT SECTIONS

**Voice rules:** Professional authority with specificity. Short declarative sentences. Authority from practice details, never from credentials.

**Evidence rules:** Never invent data or citations. Quote only traceable content. Mark unknowns as "[NEEDS USER INPUT]" or "Not specified in source documents." Where evidence is thin, be honest: "This link is based on program team experience rather than published evidence."

**Banned phrases:** 'unprecedented', 'groundbreaking', 'transformative', 'game-changing', 'robust M&E system', 'comprehensive framework', 'holistic approach'. Any sentence that could appear in any ToC with the program name swapped out is filler. Delete it.

**Sector-specific flags:** Apply the theory-of-change skill's methodology-specific flags when the program sector is identifiable (health: supply + demand pathways; education: long causal chains; governance: contribution vs. attribution; humanitarian: short chains acceptable).

---

#### Element 1: Problem Statement
Ground in data from the proposal's needs assessment. Include: what problem exists, who is affected, what causes it (root cause analysis), what evidence describes the scale. This is NOT a program description. It is the problem the program responds to.

#### Element 2: Target Population
From proposal/logframe: primary beneficiaries, secondary beneficiaries, geographic boundaries, demographic boundaries, temporal scope (when outcomes expected, when impact expected).

#### Element 3: Causal Pathways
The core of the ToC. For each pathway, present as:

```
PATHWAY [N]: [Name]
Activities: [list] --> Outputs: [list] --> Outcomes: [list] --> Impact contribution
Mechanism: [WHY does this causal link work? What is the change mechanism?]
Assumptions: [What must be true for this link to hold?]
Evidence: [What supports this causal claim?]
```

**Quality checks per pathway:**
- No skipped levels (activities must not jump directly to impact)
- Each link has a stated mechanism (not just an arrow)
- Outcomes describe CHANGE in people/systems, not delivery of services (that is an output)
- Multiple pathways shown for multi-component programs
- Cross-pathway linkages identified where relevant

#### Element 4: Assumptions
For each assumption, classify:

| Assumption | Level | Likelihood (H/M/L) | Impact if False (H/M/L) | Monitoring Trigger | Contingency |
|-----------|-------|-------|-------|-------|-------|

Assumptions must be testable. "Stakeholders will cooperate" is not testable. "District health officers attend at least 3 of 4 quarterly review meetings" is testable.

#### Element 5: Evidence Base
For each causal link, state what evidence supports it:
- Published research (with citation if available in source documents)
- Prior program evaluations
- Program team experience (state this honestly)
- Theoretical frameworks
- "[No evidence identified]" where nothing supports the link

#### Element 6: Preconditions
What must be true BEFORE the program starts for the causal logic to work? (e.g., government policy supports community health workers; security situation allows field access; baseline data collected before activities begin)

#### Element 7: Indicators
Map indicators from the logframe to each results level of the ToC. Show which pathways are monitored and which have measurement gaps.

#### Element 8: Narrative
Write a coherent narrative explanation (500-800 words) that walks through the change logic: "This program addresses [problem] by [approach]. The theory is that if [activities] are delivered, they will produce [outputs], which will lead to [outcomes] because [mechanism]. This pathway depends on [assumptions]. The evidence supporting this logic includes [evidence]."

---

### Step 6: ASSEMBLE

**Behavioral guidance: Preserve content. Focus on coherence.**

Assemble the 8 elements into a cohesive document. Verify:
- Every outcome in the pathways can be traced to at least one output
- Every output can be traced to at least one activity
- Assumptions are present at each level transition
- Indicators cover all pathway levels (flag gaps)
- Narrative is consistent with the pathway tables

Add source traceability throughout.

### Step 7: MECHANICAL FIXES

Review the assembled draft and apply these fixes:

**Banned phrases (remove or rephrase):** 'unprecedented', 'groundbreaking', 'transformative', 'game-changing', 'revolutionary', 'paradigm shift', 'now more than ever', 'in today's rapidly changing landscape', 'it is imperative that', 'it bears mentioning', 'robust M&E system', 'robust monitoring', 'comprehensive MEL plan', 'comprehensive M&E', 'holistic approach', 'leverage cutting-edge', 'harness the power', 'unlock the potential'

**Credential phrases (remove entirely):** Any sentence starting with "As an expert...", "As an experienced...", "As a seasoned...", "With years of experience...", "Drawing on extensive expertise..."

**Formatting fixes:** Replace em-dashes with commas or restructure. Normalize list bullets (all use `- ` prefix). Ensure blank line before every heading. Collapse triple+ blank lines to double. Remove trailing whitespace.

### Step 8: QCM GATE

**Behavioral guidance: Score objectively. No leniency. Apply the rubric exactly.**

Quality Control check, scored against 5 weighted dimensions. Score each 0.00-1.00 in 0.05 increments:

| Dimension | Weight | Scoring Criteria |
|-----------|--------|-----------------|
| **LOGICAL_COHERENCE** | 0.30 | Each level causally follows from below. No skipped levels. No circular logic. Mechanisms stated. Multiple pathways for complex programs. |
| **ASSUMPTION_QUALITY** | 0.25 | Assumptions at each level. Testable. Risk-classified (likelihood x impact). Monitoring triggers specified. Distinct from risks. |
| **EVIDENCE_GROUNDING** | 0.20 | Causal links supported by evidence. Evidence relevant to context. Weak evidence acknowledged honestly. |
| **MEASURABILITY** | 0.15 | Each results level operationally defined. Indicators mapped from logframe. Measurement gaps flagged. |
| **COMPLETENESS** | 0.10 | All 8 elements present. Problem statement grounded in data. Narrative consistent with pathways. |

**Calculate:** OVERALL = 0.30*COHERENCE + 0.25*ASSUMPTION + 0.20*EVIDENCE + 0.15*MEASURABILITY + 0.10*COMPLETENESS

**Threshold:** >= 0.85 PASS, 0.70-0.84 REVISE, < 0.70 FAIL

Show quality scorecard.

### Step 9: REVISE (automatic, max 2 passes)

For failing dimensions: identify specific elements, state what is wrong, re-draft only those elements, re-score. Show what changed. Maximum 2 passes.

### Step 10: FINALIZE

Present final ToC with scorecard. Show pathway count, assumption count, evidence coverage. Ask for approval. On approval: clean output, save as markdown, offer DOCX conversion (conditional on environment).

---

## Notes

- A ToC is a thinking tool, not a compliance document. Draft for clarity of logic, not document length
- Multiple pathways are expected for multi-component programs. Do not force everything into one linear chain
- Where evidence is thin, be honest. "Based on program team experience" is acceptable; fabricated citations are not
- If the program already has a ToC that needs updating, read it first and build on it
- The QCM rubric weights LOGICAL_COHERENCE highest (0.30) because broken causal logic undermines everything else
