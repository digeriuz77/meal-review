---
name: data-quality-planning
description: Plan a risk-based data quality assessment from supplied indicator, data-flow, risk, access and capacity information, with proposed checks, owners and timing. Use when a program needs a DQA plan. Does not claim completed verification.
---

# Data quality assessment planning

**Status:** Checked in Claude Code. Anthropic's help page says Free and paid plans can use uploaded skills once code execution is turned on; we checked browser upload on a paid plan only. The files are free; Claude account access and usage limits are separate. No API key or site signup is required by these instructions.

## Purpose and boundary
Create a prospective, risk-based plan for checking monitoring data and the systems that produce it. This skill plans checks. It does not verify records, report data-quality findings, certify data, approve a DQA, or replace authorized fieldwork. Never describe a planned procedure as completed evidence.

A completed-data-quality review is a different job. If asked to certify a result or state that data are accurate, explain that this plan cannot support that conclusion without completed checks and sufficient evidence.

**Dates:** Never write today's date, the system date, or words such as "passed", "late" or "stale" about a supplied date in the artifact. Supplied dates govern; if a date's status matters, write "status unknown from supplied files".

## Minimum inputs
Use what is supplied and preserve gaps:
- Indicator definitions, intended use, population, period, and reported values or report requirements, if available.
- Data flow from collection through entry, aggregation, review, and reporting, including systems, roles, and sites when known.
- Source records, tools, summaries, reports, prior concerns, or earlier DQA actions, if available.
- Known risks and constraints, including time, staff, access, permissions, privacy, safety, and approved standards or tolerance thresholds.

If there is no indicator or data stream to assess, ask for it. If flow, risks, or constraints are missing, offer only a bounded planning outline and mark these as decisions to resolve before field verification. Do not infer that unmentioned records, permissions, roles, or controls do not exist.

Accept explicitly attached files or a user-designated folder and candidate file list. In attachment mode, use only supplied attachments and text. In folder mode, inspect only the named folder and list files selected. Ask about ambiguous files. State the intake mode and evidence locations. Do not imply access to other folders or systems.

## Method
1. **Set purpose and boundary.** Identify the decision the data support, period, indicators, population, locations, reporting stage, and scope exclusions. Separate evidence from proposals.
2. **Map the data flow.** For each indicator, show source or observation, collector, entry, aggregation, review, and report. Mark each link confirmed, candidate, or unknown. Note versions, timing, permissions, and responsible roles only where supplied.
3. **Prioritize risk.** Use supplied decision importance, donor or management reporting use, known discrepancies, definition ambiguity, missing records, system changes, and vulnerable or hard-to-reach groups. Give each priority a stated rationale. Do not apply an invented numeric score, universal interval, fixed sample rule, or universal threshold.
4. **Plan dimension-specific checks.** Use the five lenses below where relevant. A dimension is a question for the planned assessment, not a result or score.
5. **Separate check types.** Specify which procedures examine completeness, internal reconciliation, source-record verification, accuracy/validity, reliability, timeliness, and integrity. Agreement between a report and the source used to produce it is reconciliation, not independent proof that the source reflects reality.
6. **Choose records and sites.** Prefer a defensible census when feasible. Otherwise state the selection frame, risk-based or probability method, selection rationale, and unresolved size after record volume and capacity are confirmed. A purposive or risk-based sample can locate exceptions but is not representative and cannot estimate population error rates. A probability sample needs an explicit design and assumptions before inference.
7. **Check safeguards and feasibility.** Confirm authorization, purpose limitation, minimum necessary data, secure handling, confidentiality, field safety, and any required consent or ethics review before access, contact, or site visits. Do not plan unauthorized respondent contact or access to identifiable data.
8. **Set decision rules.** Use only supplied approved thresholds. If none are supplied, show the counts, differences, and cases the team will review, and mark acceptance tolerances as a decision required. Any proposed trigger must be visibly labeled as a proposal and approved before use. Never import a fixed percentage tolerance as a universal quality standard.
9. **Define escalation and outputs.** Identify who must decide unresolved scope, access, threshold, or corrective action. If the proposed work encounters a privacy or safety risk, suspected deliberate alteration, or a material conflict, pause the affected check, preserve the record securely, and use the supplied escalation route. If no route is supplied, mark one for confirmation; do not accuse or adjudicate.
10. **Return a plan, not findings.** Provide planned procedures, evidence needed, responsibilities and timing only when supplied or proposed, limits, unresolved decisions, and a completion record for the future assessment team.

When prior DQA findings or action records are supplied, include planned follow-up for each relevant action: original issue, stated action/owner/due date, source of claimed closure, evidence needed to verify implementation and whether the issue recurs. A closure label is a claim to check, not proof of correction. Missing history is unknown; do not invent earlier failures or completed follow-up.

## Five quality lenses
- **Validity:** Does the operational definition measure the intended result for the stated population and period? Compare definitions across tools and reports. Do not infer outcome validity from tidy records.
- **Reliability:** Would another trained person applying the same instructions obtain a consistent result? Plan a repeat or independent re-abstraction where appropriate. A small purposive repeat does not estimate system-wide reliability.
- **Precision:** Is the unit and level of detail adequate for the intended decision? Check denominators, units, rounding, resolution, and uncertainty. Do not invent margins of error or precision claims without an appropriate design and inputs.
- **Integrity:** Are access, changes, approvals, and handoffs documented and protected from unauthorized alteration? Missing audit evidence is a control gap to investigate, not proof of misconduct.
- **Timeliness:** Are collection, entry, review, and reporting dates suitable for the decision? Compare with supplied due dates or explicitly request them. Do not impose a universal DQA calendar.

## Check types and limits
- **Completeness:** Compare expected submissions, fields, periods, or records with received items only when the expected set is known. State the denominator and exclusions.
- **Reconciliation:** Recompute or compare totals between stages and record differences, formulas, and versions. Reconciliation establishes consistency between records, not truth.
- **Source verification:** Trace selected reported values to their originating records using authorized access. Recount consistently defined items and retain an audit trail. State selection limits.
- **Accuracy and validity:** Compare with independent, authoritative evidence or approved direct observation where permitted. If no independent evidence exists, identify the limit rather than calling a cross-check “accuracy verification.”
- **Reliability:** Plan duplicate abstraction, repeat measurement, or inter-rater checks only when the method and resources are defined. Report what was repeated and for which cases.
- **Timeliness and integrity:** Trace dates, roles, approvals, changes, and system handoffs. Do not infer intent from a discrepancy or missing log.

## Output format
Return editable Markdown with these sections:
1. **Plan status and purpose:** State “Draft DQA plan; checks not yet performed,” intake mode, decision, period, and boundaries.
2. **Evidence register:** Source ID, supplied fact, location/version/date, and limitation. Identify facts, unknowns, and proposals separately.
3. **Indicator and risk selection:** Indicator, use, population/period, data-flow status, priority, evidence-based rationale, excluded items and rationale.
4. **Planned check matrix:** Indicator/site or stage, check type and quality lens, evidence or procedure, selection method (where capacity and risks are supplied, propose a risk-based selection that fits the supplied capacity, labeled proposed), responsible role (propose from roles named in the inputs, labeled proposed; unresolved only when none is named), timing (a proposed phase or date inside the supplied calendar, such as before or after a stated freeze or review, and a proposed split of any supplied staff-day cap across checks, all labeled proposed; unresolved only when none is supplied), permissions/safeguards, threshold rule, and limits.
5. **Selection and feasibility:** Frame, census/sample decision, capacity and dependencies. State whether any sample is nonrepresentative. Do not invent sample size, field days, costs, or workload.
6. **Unresolved decisions and approvals:** Missing definitions, access, thresholds, team, schedule, privacy/ethics, escalation route, and who must decide if known.
7. **Conditional escalation:** Describe what would pause a check and what supplied authority should be contacted; do not create a finding or make an allegation.
8. **Completion record for later use:** Blank fields for actual dates, cases checked, evidence, exceptions, limitations, decisions, and assessor sign-off. Leave blank until the assessment is performed.

Use source IDs such as `filename#heading`, page, table, row, or record ID. If a location cannot be identified, give the filename and say the location is unavailable. A result can be marked “not assessable from supplied material”; do not turn absence from the submitted files into a claim about the real program. Only editable Markdown is in scope. When saving a file, write and inspect the actual artifact. A chat summary does not replace it. If file creation is unavailable, return editable Markdown and state that no download was created.

## Missing, conflicting, or unsuitable inputs
- No indicator/data stream: ask what data should be assessed; do not invent an assessment scope.
- Missing definitions, flow, or risks: record each as unresolved and limit the plan to supported desk checks.
- Missing access or permissions: make the check conditional; do not assume it can proceed.
- Conflicting definitions, values, dates, or standards: preserve both versions and explain which design decisions depend on resolution.
- No thresholds: do not pass/fail, score, or certify data against an invented tolerance.
- Request to prove accuracy or produce findings before checks: explain the boundary and offer the prospective plan only.
- Non-DQA request: state the scope and stop; do not fabricate DQA content.

## Completion checklist
- Every selected indicator is tied to an intended use, definition, population, period, and data flow or an explicit gap.
- Risk priorities have evidence-based reasons and no hidden weights or universal rules.
- Planned checks distinguish completeness, reconciliation, verification, validity/accuracy, reliability, precision, timeliness, and integrity as appropriate.
- Selection limits prevent nonprobability checks from being presented as representative.
- Thresholds, permissions, roles, schedule, sample size, budget, and workload are supplied, explicitly proposed, or unresolved.
- Privacy, safety, consent, access, and conditional escalation are addressed.
- No assessment result, certification, approval, or commitment is invented.

## Interruption and resumption
If interrupted, preserve the actual draft plan, evidence register with source names/versions or dates, selection frame and rationale, safeguards, and unresolved decisions. Resume only from files and handover supplied for the resumed task. Check for changed sources and flag differences. Check inherited claims against original sources as confirmed, contradicted or unconfirmed. Record plan changes. Never treat a planned check as completed or upgrade a proposal into approval.
