---
name: baseline-planning
description: Plan baseline measurement, or check a baseline's indicator coverage against the framework, covering timing, source comparability, permissions and gaps without inventing starting values or targets. Use when a program needs a baseline plan or a coverage check before data collection.
---

# Baseline planning

**Status:** Checked in Claude Code. Anthropic's help page says Free and paid plans can use uploaded skills once code execution is turned on; we checked browser upload on a paid plan only.

## Purpose and trigger
Create a bounded plan for establishing baseline evidence against a supplied results framework or indicator set. The plan identifies what to measure, for whom, when, from which source, and what decisions or permissions are needed. It does not produce baseline values, approve targets, or guarantee causal attribution.

**Dates:** Never write today's date, the system date, or words such as "passed", "late" or "stale" about a supplied date in the artifact. Supplied dates govern; if a date's status matters, write "status unknown from supplied files".

## Minimum inputs
- A logframe, results framework, indicator list, or clearly identified set of measures.
- Program population and geographic scope, if known.
- Program start/exposure timing or an explicit statement that timing is unknown.

Useful context includes approved indicator definitions and versions, disaggregation, data sources, existing comparable evidence, planned endline or later measurement methods, sampling frame, collection permissions, ethics requirements, staff/resources, and decision deadlines.

## Intake modes
Accept files explicitly uploaded to this chat or a user-designated folder with a file list. Upload mode uses only attached files and supplied text. Folder mode inspects only the named folder, lists candidate files, and uses only selected files. Confirm ambiguous file identities and versions. State the intake mode and files reviewed. Do not imply access to unseen project material.

## Copyable starter
> Use baseline-planning on the attached files [or folder: path]. Map every supplied indicator to its population, operational definition/version, measurement window, source/tool, method, timing relative to program exposure, disaggregation, permission/access status, and comparability needs for later rounds. Identify prior evidence and gaps without inventing values or targets. Treat post-exposure recall as retrospective self-report, not a measured baseline. Return an editable Markdown plan with facts, assumptions, proposals, and decisions clearly separated.

## Reproducible procedure

**Choose the requested mode first.** Planning mode produces the nine-part plan below. Existing-report coverage mode requires a supplied baseline report and framework: map every framework indicator to the report's actual value or missing value, source/method, reference period, definition, population and disaggregation, then check comparability and unresolved decisions. Keep measured values as source-reported, with limitations. Return a coverage matrix and prioritized issues, not a replacement collection plan unless separately requested. If either report or framework is absent, state the limit and do not issue a complete coverage verdict.

1. Confirm intake mode, the planning purpose, program stage, start/exposure dates, decision deadline, and whether the request covers a new baseline, a delayed baseline, or review of an existing plan.
2. Inventory supplied sources with filename, type, version/date, and approval status if stated. Extract every indicator, including its exact wording, identifier, level label, operational definition, population, unit, observation window, disaggregation, baseline/target status, and source/tool. Record evidence IDs as `filename#heading`, page, table, row, or instrument item.
3. Preserve source-specific result levels and indicator definitions. Do not silently map “impact” to another label, rewrite an indicator, add a denominator, or treat a target as a baseline. If source versions conflict, show both and request an authority decision.
4. Define the target population for each measure using supplied eligibility rules, geographic boundary, unit of analysis, and time window. Mark missing or contradictory elements. Do not assume the logframe population matches the actual frame.
5. Map every indicator to a baseline measurement approach: existing administrative or secondary data; program records; primary quantitative collection; primary qualitative collection; direct observation or another stated method; or undecided. A source is only “available” when access and permission are documented.
6. Assess prior data for comparability: same or crosswalked construct/definition, population and eligibility, geography, unit, observation/recall window, method/tool, timing/season, disaggregation, and data quality. Report each material difference. Existing data are not automatically a baseline.
7. Establish timing relative to first program exposure and the relevant reference period. Plan prospective measurement before exposure when feasible. If exposure has already occurred, do not describe later collection or recalled pre-program conditions as a measured baseline. Label retrospective self-report separately and explain its recall and comparability limits.
8. Identify sampling design and sample-size decisions only to the extent supported by a population frame, intended estimates, design, precision/power or qualitative logic, expected response, and relevant assumptions. If these are absent, list decisions needed and do not invent a sample size. Keep design estimates separate from supplied facts.
9. Record permissions, ethics review, consent, safeguarding, data protection, source access, and tool-use permissions as confirmed, unconfirmed, or required. Do not imply that a named source can be reused without authorization.
10. Check planned measurements against likely later rounds. Preserve definitions, tools, modes, populations, disaggregation, and reference periods where comparability is intended. If a change is necessary, specify a versioned crosswalk or caveat as a proposal for review.
11. Return the output structure below. Leave baseline values blank or explicitly “Not yet measured.” Do not invent target revisions.

If an existing evaluation design includes comparison groups, multiple arms or a panel, map population/eligibility, exposure timing, matching or allocation, baseline tools/windows and follow-up/attrition needs for every arm. Identify differences that would compromise the intended comparison. Do not add a comparison group as an approved commitment, treat a comparator alone as causal identification or assume baseline equivalence. If causal estimation is requested without a design, propose a design decision with limitations rather than inventing one. A descriptive baseline does not require an unnecessary comparison group.

## Output structure
1. Planning purpose, stage, intake mode, and source/version register
2. Facts, assumptions, and proposed recommendations
3. Indicator coverage and measurement matrix: ID/exact wording; level as supplied; definition/version; population/unit; measurement window; source/tool; method; timing relative to exposure; disaggregation; permission/access; later-round comparability; status; evidence IDs
4. Prior evidence and comparability assessment by source and indicator
5. Sampling/design decisions and assumptions, comparison-arm/panel coverage when applicable, or explicit statement that sizing is not yet supportable
6. Data collection tools, quality assurance, ethics, protection, and permission decisions
7. Timing and responsibility plan, capacity/resource dependencies and unknown roles, effort or dates marked; proposals remain unapproved
8. Gaps, risks, and unresolved decisions
9. Completion checklist

Use editable Markdown only for this candidate. Do not output baseline values unless supplied as actual measurements with their source and timing. Do not assert that targets are achievable or causal effects can be measured unless design evidence supports that conclusion. When saving a file, write and inspect the actual artifact. A chat summary does not replace it. If file creation is unavailable, return editable Markdown and state that no download was created.

Only in existing-report coverage mode, add `## Critical Issues`, `## Important Issues` and `## Minor Improvements` after the coverage matrix, source register and scope limits. Critical issues prevent the intended comparison or make the supplied baseline claim misleading; important issues materially weaken interpretation or repeatability; minor improvements concern clarity without changing the conclusion. Retain each heading even when None identified or Not assessable. Planning mode keeps gaps/risks/decisions in its nine-part structure and requires no severity verdict. A missing report supports a bounded gap list, not a completed review of an unseen report.

## Measurement and comparability rules
- A baseline is an empirical measurement tied to a defined indicator, population, method, and period. It is not a target, estimate, assumption, or planned collection.
- Do not invent a baseline of zero for a new program. An output count may begin at zero only if the indicator definition and records support that value.
- Pre-existing administrative or survey data may be candidate baseline evidence only after comparability and access are assessed. Clearly label any proxy or source limitation.
- A post-exposure survey asking respondents to remember prior conditions is retrospective self-report, not a directly measured baseline. It may be proposed as supplementary evidence with limitations.
- Compare prior evidence and future measurement across construct/definition, population/frame, geographic scope, unit, time/season, tool/mode, recall window, disaggregation, and data quality. Numeric similarity alone is insufficient.
- Distinguish collection period from recall or observation window. A survey fielded in June may ask about a different period; record both.
- Maintain the indicator's supplied version. A proposed revision needs a dated change record and an explicit crosswalk decision where trend comparison matters.
- Define a sampling frame and eligible unit before sample design. Sample size depends on the intended estimate/design and explicit assumptions. Do not use a generic formula or guessed number as a completed design.
- Distinguish probability estimates from purposive qualitative evidence. Do not imply statistical representation from purposive samples.
- A baseline can establish starting conditions; it does not establish program attribution by itself. Simple pre/post difference is not causal proof.
- No permission, donor rule, ethics approval, staffing level, budget, or collection date may be presumed from absence of a contrary statement.

## Missing, conflicting, or unsuitable inputs
- **No indicator set:** return a bounded planning shell and identify the framework or indicator list required for coverage mapping.
- **Exposure/start timing unknown:** mark baseline timing as unresolved and ask for the actual first-exposure date and planned collection window.
- **Program exposure already occurred:** do not label a future survey or recall answer as a measured baseline. Offer clearly labeled options with limitations: valid pre-exposure administrative or monitoring records, a prospective baseline for a later cohort not yet enrolled, retrospective recall as supplementary evidence only, or labeling the first collection as a first measurement round rather than a baseline.
- **Prior data lack definitions or provenance:** classify them as candidate evidence with comparability unconfirmed; do not adopt their values as baseline.
- **Conflicting definitions, populations, or versions:** show each source and evidence ID, explain the effect on comparability, and request a governing decision. When a signed or formally approved document conflicts with a later unsigned or unapproved one, treat the signed one as the working governing version, labeled proposed, and flag that the later document may govern if it was approved or supersedes it; the user decides.
- **Sampling information absent:** map indicators and decisions, but do not calculate sample size or claim precision.
- **Access or permissions unclear:** mark source access unconfirmed and list permission steps; do not treat a public or partner-held dataset as authorized for use.
- **Non-M&E request:** state that this skill plans baseline measurement and stop or suggest an appropriate alternative.

## Interruption and resumption
If interrupted, preserve the actual plan and indicator matrix, evidence register with source filenames and versions/dates, assumptions, and unresolved decisions. Resume only from files and handover supplied for the resumed task. Recheck source versions and flag changed sources. Check inherited claims against original sources as confirmed, contradicted or unconfirmed. Record edits, revised measurement windows, and method decisions. Never upgrade a proposed baseline, source, permission, target, or design into an approved or measured fact.

## Completion checklist
- Every supplied indicator is mapped or explicitly identified as unassessable.
- Exact wording, definitions, versions, populations, units, and measurement windows are preserved or visibly unresolved.
- Timing relative to program exposure is explicit or marked unknown.
- Prior data are assessed for comparability and permission; no source is assumed available.
- Post-exposure recall is not called a measured baseline.
- Baseline values and targets are not invented or silently revised.
- Sampling claims expose assumptions or remain undecided.
- Facts, assumptions, proposals, conflicts, and required approvals are distinct.
- The plan names ethics, privacy, access, and later-round comparability decisions.
