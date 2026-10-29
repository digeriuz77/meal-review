---
name: indicator-reference-sheets
description: Draft or update indicator reference sheets from supplied indicator and program materials. Use when indicator definitions and collection procedures need a consistent editable record.
---

# Indicator reference sheets

## Purpose and trigger
Turn an approved or proposed indicator into a traceable, operational reference sheet. This skill documents decisions; it does not silently approve or change definitions, targets, or donor commitments.

## Minimum inputs
- Indicator name or result statement.
- Target population or result level, if known.
- Any available framework, source, collection method, baseline, target, or reporting requirement.

Accept explicitly uploaded files or a user-designated folder plus a file list. Upload mode uses only attachments/text. Folder mode inspects only that folder and reports files used. Confirm ambiguous documents. State intake mode.

## Starter prompt
> Use indicator-reference-sheets on the attached files [or folder: path]. Create one editable reference sheet per supplied indicator. Preserve existing approved wording and values, cite source evidence, and mark missing fields “Not supplied” or “Decision required.” Do not invent targets, owners, frequencies, or sources.

## Procedure
1. Confirm intake mode, indicator scope, and whether the task is draft, documentation, or update. Preserve approved wording unless the user explicitly authorizes revision.
2. Extract each indicator and its result-framework row, level, population, baseline, target, source, method, and stated requirements. Assign evidence IDs as `filename#heading`, page, table, or row.
3. Keep facts, assumptions, and proposed recommendations in separate fields. Record conflicting definitions or values with both evidence IDs and flag the change-control decision.
4. Review result-chain fit when enough context exists: Activities, Outputs, Immediate Outcomes, Outcomes, or Goal. Do not substitute another level or equate a delivered output with population change. Use “unclear” when result statement or anchor is missing.
5. Make the operational definition explicit. For percentages or ratios, specify numerator and denominator, inclusion/exclusion, unit, population universe, reference period, and calculation. Do not retrofit a denominator without evidence; propose it separately.
6. Check method, frequency, disaggregation, and source for fit and feasibility. Use conditional checks: source standards for greenfield or unfamiliar contexts; composite validation when a composite is proposed; disaggregation review when required; baseline/target review when values are new or under revision.
7. Complete the sheet fields below. Preserve all unknowns as “Not supplied,” “Not confirmed,” or “Decision required.”
8. Return one sheet per indicator plus a concise unresolved-decision list. Provide editable Markdown, keeping each indicator identifiable.

## Required reference-sheet fields
- Indicator name and stable source identifier
- Result statement, framework row, result-chain level, and rationale
- Indicator type and standard/custom status, with evidence
- Operational definition, including numerator, denominator, unit, population universe, and observation window
- Baseline value, date/period, source, and method
- Target value(s), timeframe, source/rationale
- Disaggregation categories and feasibility notes
- Data source, collection tool, collection method, frequency, and reporting frequency
- Responsible role for collection, analysis, reporting, and quality review
- Data quality risks, verification/QA steps, and known limitations
- Intended use, missing-data treatment, and change history/approval status
- Evidence IDs, assumptions, proposed recommendations, and decisions required

## Output and quality rules
Keep source facts separate from proposed fixes. Do not alter an approved definition or target silently. Do not claim a standard indicator or validated composite without traceable source evidence. Do not label an estimated value as a baseline. A missing frequency or owner remains missing. If collection workload is requested, calculate only from supplied task volumes and time per task; label all design assumptions separately from evidence.

## Operationalization checks
- A count states what is counted and how duplicate people or events are handled.
- A percentage or rate specifies numerator, denominator, eligibility, exclusions, unit, and period. The denominator must match the population universe.
- A composite names its source instrument, components, scoring rule, and validation evidence. Do not create a score by combining unrelated measures.
- A baseline names value, date, population, method, and source. An unavailable value is not zero.
- A target names value and timeframe, with source and approval status. A supplied target is not automatically endorsed.
- Collection and reporting frequency are separate fields. Do not infer one from the other.
- Disaggregation categories must be defined and tied to data the collection design can capture. Flag privacy and cell-size concerns where relevant.
- For qualitative indicators, specify the construct, source, coding or judgment approach, and how consistency will be supported.
- Responsible roles distinguish collection, verification, analysis, and reporting when functions differ.
- Quality checks should be repeatable, such as range checks, duplicate review, source reconciliation, or supervisory verification. Mark new checks as proposals.
- Missing-data rules must distinguish missing, not applicable, and zero.
- Change history preserves approved wording and identifies who authorized a revision if supplied.

Across sheets, look for duplicate constructs, inconsistent populations or periods, conflicting units, and results-chain coverage gaps. Report these as cross-sheet issues and do not modify indicators to force consistency.

## Missing, conflicting, or unsuitable inputs
- Incomplete indicator: provide a bounded sheet with visible gaps, not a guessed complete record.
- Conflicting definitions or targets: show both versions and request a governing decision in the output. If one version is signed or formally approved and a later one is not, use the signed one as the working version, labeled proposed, and flag that the later one may govern; the user decides.
- Composite without validation evidence: flag provenance as unconfirmed and avoid endorsing it.
- Population or result level missing: leave unresolved and explain what source would resolve it.
- Non-M&E request: say the skill covers indicator documentation and offer an appropriate direction.

## Completion checklist
- Preserve source wording and targets as supplied. "Existing" does not establish "approved," and missing approval evidence does not establish "unapproved" or "rejected." State approval status as not supplied unless a source confirms it. Apply the same distinction to roles, permission, tool readiness and commitments.
- Every supplied indicator is accounted for and source-linked.
- Numerator, denominator, unit, population, and period are explicit or flagged.
- Baseline, target, source, tool, frequency, role, QA, and use are captured or visibly missing.
- Disaggregation and result-level claims fit the evidence.
- No approved definition or target was changed silently.
- Facts, assumptions, proposals, and conflicts are distinguishable.

## Interruption and resumption
If interrupted, preserve the actual sheets, evidence register with source filenames/versions or dates, and unresolved definition or approval decisions. Resume only from files and handover supplied for the resumed task. Check whether sources changed and flag differences. Record edits and prior approved values. Never upgrade a proposal, assumption, or pending decision into an approved definition or target.
