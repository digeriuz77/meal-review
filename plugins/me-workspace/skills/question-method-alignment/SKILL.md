---
name: question-method-alignment
description: Map evaluation questions to evidence, indicators, sources, and feasible collection methods, including limitations. Use when an evaluation needs an evidence or methods matrix.
---

# Evaluation question and method alignment

## Purpose and trigger
Build an editable question-to-evidence matrix and identify feasibility gaps. The matrix supports design decisions; it does not constitute a sampling plan, instrument, budget, or causal identification strategy.

## Minimum inputs
- Evaluation questions or a clear evaluation purpose.
- Program and population context.
- Known data sources, constraints, and timing, if available.

Accept explicitly uploaded files or a user-designated folder plus a candidate file list. Upload mode uses only attachments and supplied text. Folder mode inspects only the named folder and reports files selected. Confirm ambiguous file identities. State the intake mode.

## Starter prompt
> Use question-method-alignment on the attached files [or folder: path]. Map each evaluation question to the evidence needed, sources, collection methods, and limitations. Use only supplied facts; flag unknown sample size, access, timing, cost, or permissions. Return an editable Markdown matrix.

## Procedure
1. Confirm intake mode and extract the evaluation questions, purpose, population, geography, period, available data, and constraints.
2. Register evidence using `filename#heading`, page, table, or row. Mark unavailable locations rather than inventing citations. Separate supplied facts, assumptions, and proposed recommendations.
3. Check whether each question is descriptive, explanatory, comparative, or causal. Flag counterfactual claims that the described design cannot support. Pre/post difference alone does not establish attribution.
4. For each question, identify the minimum evidence required to answer it, including relevant indicators or constructs, unit of analysis, population, timeframe, and comparison if applicable.
5. Map evidence to existing sources first. Distinguish confirmed sources from possible sources. For new collection, describe a candidate method and why it fits the question, with likely limitations and ethical or access issues.
6. Select evaluation criteria by purpose; include only relevant criteria. Do not assume every OECD-DAC criterion is required.
7. Assess feasibility using stated access, staff, time, and data quality. Never calculate sample size without an explicit design and assumptions. If inputs permit a workload estimate, show the supplied volumes and time per task separately from an unverified design estimate.
8. Identify evidence gaps, triangulation needs, dependencies, and decisions required before methods can be finalized.
9. Return the matrix, assumptions, and bounded next steps.

## Output structure
- Purpose, intake mode, and scope
- Source register with evidence IDs
- Question-to-evidence matrix: question; evidence/construct; indicator or measure; population/unit; source (confirmed or candidate); method; timing; feasibility; limitations; evidence IDs
- Cross-cutting ethics, access, and data-quality considerations
- Evidence gaps and design decisions
- Assumptions and proposed recommendations

Use editable Markdown. Keep confirmed sources distinct from suggestions. Do not claim feasibility is confirmed unless evidence supports it.

## Method alignment checks
- **Question type:** Descriptive questions need measures of status or experience; explanatory questions need evidence about mechanisms and context; comparison questions require comparable groups or periods; causal questions require a credible identification strategy.
- **Unit of analysis:** State whether evidence concerns a person, household, facility, event, organization, or place. Do not mix units without explaining the mapping.
- **Measurement level:** A method should capture the construct in the question. Attendance data can confirm participation records but cannot establish changed knowledge or practice by itself.
- **Source quality:** Note who created each source, when, for what purpose, coverage, likely missingness, and known validation. If not supplied, list these as checks, not findings.
- **Triangulation:** Identify complementary sources that could corroborate a claim. Repeating one source through several formats is not independent corroboration.
- **Mixed methods:** Explain what each method contributes and how findings will be integrated. Do not list mixed methods as a quality marker without a reason.
- **Sampling:** Name a frame and selection approach only if supplied or authorized as a proposal. Sample size requires explicit population, design, precision or saturation assumptions, and nonresponse expectations.
- **Ethics and access:** Flag risks for sensitive populations, confidentiality, data permissions, language, and referral pathways when relevant. Do not claim approval or access.
- **Timing:** Match evidence to recall period, season, implementation stage, and decision date when known. Mark timing dependencies when unknown.
- **Feasibility:** Distinguish technical fit from confirmed operational feasibility. A sound method may still depend on staff, permissions, resources, or timing.

For each question, trace the wording to evidence, measure, population, source, method, timing, and limitation. A blank link is a design gap. If one source is expected to answer several questions, check it contains the needed measures for each.

## Evidence handling and limits
Tie facts to evidence IDs and preserve conflicting source statements. Label interpretations and recommendations. A method can be appropriate in principle yet infeasible locally; report both judgments. Do not invent sample sizes, response rates, access permissions, cost, staff time, donor rules, or source availability. Do not state that qualitative evidence is statistically representative. Avoid causal attribution from simple before/after comparisons.

## Missing, conflicting, or unsuitable inputs
- Questions absent: offer a short list of required clarifications or a provisional question set only if the user requests it.
- Data source availability unknown: label as candidate, not confirmed.
- Sample frame or design unknown: identify required decisions; no sample-size claim.
- Conflicting scope or population: show both versions and flag which alignment decisions depend on resolution.
- Non-M&E request: explain that the skill is for evaluation evidence design and offer a relevant direction.

## Completion checklist
- Every question has a traceable evidence path or a clearly stated gap.
- Existing sources and candidate sources are distinguished.
- Methods, limitations, population, and timing are explicit where known.
- Sample size, cost, access, and workload are not fabricated.
- Criteria are purpose-selected.
- Causal language matches the design.
- Facts, assumptions, recommendations, and conflicts are visible.

## Interruption and resumption
If interrupted, preserve the actual matrix, evidence register with source filenames/versions or dates, and unresolved design decisions. Resume only from files and handover supplied for the resumed task. Check whether sources changed and flag differences. Record edits made to the artifact. Never upgrade a proposal, assumption, or pending decision into an approved decision.
