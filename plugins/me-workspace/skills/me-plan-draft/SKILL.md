---
name: me-plan-draft
description: Draft an M&E or MEL plan from supplied program and indicator materials, or check an existing plan's coherence with its framework. Use when a program needs an operational monitoring, evaluation, learning and data-use plan.
---

# M&E plan draft

## Purpose and trigger
Draft a practical M&E plan that connects results, indicators, evidence collection, quality assurance, roles, learning, and use. The output is a proposal for program-team review, not an approved operating commitment.

## Minimum inputs
- Program summary or results framework.
- Indicator list or stated monitoring purpose.
- Any known reporting obligations, sources, or constraints.

Accept explicitly uploaded files or a user-designated folder and file list. Upload mode uses attachments/text only. Folder mode inspects only the named folder and lists files used. Confirm ambiguous files. State intake mode.

## Starter prompt
> Use me-plan-draft on the attached files [or folder: path]. Draft an operational M&E plan using the eleven components below. Link facts to source evidence, preserve approved indicators and targets, and mark assumptions, proposals, and decisions required. Do not invent budget, owners, frequencies, or commitments.

## Procedure
1. Confirm intake mode, intended audience, program stage, reporting horizon, and whether this is a new or revised plan.
2. Extract results logic, indicators, populations, targets, reporting requirements, existing sources, staffing, budget, timing, and data-use needs. Cite `filename#heading`, page, table, or row.
3. Keep facts, assumptions, and recommendations distinct. Preserve conflicts with both evidence IDs; do not resolve silently.
4. Preserve approved indicator wording, baselines, targets, and obligations. Flag gaps rather than changing them. Do not infer causal attribution from routine monitoring or simple pre/post values.
5. Draft the eleven components below. Tie each indicator to a source, collection method/tool, frequency, responsible role, quality checks, analysis, reporting, and use when supplied. Use explicit placeholders for unknowns.
6. Check alignment across result logic, indicators, collection and reporting schedules, disaggregation, data quality, roles, learning questions, and resources.
7. Assess workload or feasibility only to the extent supported. Calculate burden only from supplied volumes and time per task. Do not invent sample sizes, budgets, staffing, or targets.
8. Provide a prioritized list of decisions needed before adoption.

## Eleven plan components
1. Program context, results logic, and intended use
2. Monitoring and evaluation questions or learning agenda
3. Indicator matrix and definitions
4. Data sources, collection methods, and tools
5. Collection, reporting, and review schedule
6. Disaggregation and equity considerations
7. Data management, quality assurance, and protection
8. Analysis, interpretation, and limitations
9. Reporting, learning, and decision-use routines
10. Roles and responsibilities
11. Resources, risks, and implementation decisions

## Output structure
For a requested coherence check, use exact standalone headings `## Critical Issues`, `## Important Issues`, and `## Minor Improvements`, including None identified or Not assessable as appropriate. Do not abbreviate these to Critical, Important or Minor.
Return the eleven-section plan, an editable indicator and collection matrix, evidence register, assumptions and proposed recommendations, unresolved decisions, and coherence check. Use editable Markdown. State which components are drafts and which are directly documented facts.

## Matrix and operating checks
- For every status assertion such as approved, rejected, authorized or unapproved, cite the explicit status-bearing source statement. Otherwise write "approval/status not supplied." Approval of a target does not establish approval of indicator wording, a method, a role or the plan. Missing approved values in the supplied input does not prove that no approved values exist in the program. Preserve each supplied item without expanding its authority.
- Use one row per indicator or clearly linked measure. Keep its original identifier and wording visible.
- Distinguish routine monitoring, evaluation, learning, and compliance reporting. They may share data but answer different questions.
- Show collection frequency, analysis frequency, and reporting frequency separately when known.
- State who reviews data quality and what action follows a failed check. Mark any new workflow as a proposal.
- Include a data-management path from collection through storage, access, analysis, reporting, retention, and disposal where information is available.
- Connect learning questions to a scheduled review and a decision or use. A meeting is not an adaptive process unless its use is described.
- Show how external conditions and assumptions will be monitored when they affect interpretation. Do not label contextual change as program impact.
- State whether values are period or cumulative and how disaggregated totals relate to the headline indicator.
- Make missing values visible. Do not silently impute, convert missing to zero, or carry forward an old value.
- Separate approved framework content from suggested additions, including indicators or new tools.
- For a planned evaluation, identify timing, purpose, questions, and design status only as supported.
- Link role proposals to named functions, not fabricated individuals. Confirm workload before assigning responsibilities.

Trace results to indicators, indicators to sources and methods, methods to roles and schedule, and findings to decisions and use. Check that frequency and resources match the collection plan. Identify contradictions as decisions rather than editing them away. State when the plan cannot be judged because key sources were not supplied.

## Quality and evidence rules
Use methods appropriate to the question and indicator; qualitative data are not statistically representative by default. Select DAC criteria only when relevant to an evaluation purpose. A plan can describe contribution or observed change without claiming causal impact. A missing budget or responsible role remains a decision. Distinguish collection from reporting frequency. Proposed roles are not commitments. Do not include arbitrary gate scores or guarantees.

## Missing, conflicting, or unsuitable inputs
- No indicator list: draft the plan shell and identify decisions needed before an indicator matrix can be finalized.
- No resources or staffing: mark feasibility as unassessed; do not fill with benchmarks as facts.
- Conflicting framework and plan: show both and flag the governing source decision. If one version is signed or formally approved and a later one is not, use the signed one as the working version, labeled proposed, and flag that the later one may govern; the user decides.
- Insufficient evidence for a full plan: produce a bounded draft with visible placeholders.
- Non-M&E request: explain that this skill drafts monitoring and evaluation plans, then stop.

## Completion checklist
- Keep calendar uncertainty visible. Sessions, active weeks, calendar months and collection events are different units. Use source-supported rates and symbolic totals when dates/event counts are absent; optional assumed scenarios do not become established workload or capacity facts.
- All eleven components are present or explicitly marked unresolved.
- Indicators, sources, methods, frequency, disaggregation, QA, roles, reporting, and use align where known.
- Source evidence, assumptions, and proposals are distinguishable.
- Approved values and obligations were not changed silently.
- Workload calculations use supplied inputs only.
- Causal claims and feasibility statements are appropriately limited.
- Adoption decisions remain with the responsible program team.

## Interruption and resumption
If interrupted, preserve the actual plan draft and matrix, evidence register with source filenames/versions or dates, and unresolved decisions. Resume only from files and handover supplied for the resumed task. Check whether sources changed and flag differences. Record plan changes. Never upgrade a proposal, assumption, or pending decision into an approved plan element or commitment.
