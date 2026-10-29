---
name: measurement-feasibility
description: Assess whether proposed indicators and data collection plans are feasible with stated sources, staff, timing, and resources. Use when a measurement design may exceed available capacity.
---

# Measurement feasibility and burden

## Purpose and trigger
Identify measurement demands, constraints, risks, and practical options while preserving required information. This is a structured assessment, not a verified costing, sample-size calculation, or approval to remove an indicator.

## Minimum inputs
- Indicator list or measurement plan.
- Available data sources or collection approach, if known.
- At least one stated constraint such as staff, time, access, frequency, or budget. If none is supplied, describe what cannot be assessed.

Accept uploaded files or a user-designated folder and list. Upload mode uses attachments/text only. Folder mode inspects only that folder and lists the files used. Confirm ambiguous inputs. State intake mode.

## Starter prompt
> Use measurement-feasibility on the attached files [or folder: path]. Assess each stated measurement requirement against documented sources, staff, timing, frequency, and resources. Calculate workload only from supplied volumes and time assumptions. Separate evidence from design estimates and propose options without silently removing requirements.

## Procedure
1. Confirm intake mode, decision to support, indicator scope, and constraints. State which constraints are evidence and which are unknown.
2. Extract indicator definitions, population, disaggregation, source, tool, collection frequency, reporting frequency, roles, QA, and stated resources. Cite `filename#heading`, page, table, or row.
3. Build a demand inventory by data source and activity. Distinguish routine data already collected from new collection, extraction, cleaning, analysis, and reporting.
4. Assess each requirement as supported by evidence, plausible but unconfirmed, constrained, or unknown. Explain dependencies such as access, permissions, seasonality, data quality, sample design, language, or safeguarding.
5. Calculate workload only where both volumes and time per unit are supplied. Show formula and inputs. Label this arithmetic separately from design estimates. Never infer sample size or cost from indicator count alone.
6. Identify options to reduce burden, such as using an existing source, aligning collection windows, sampling where methodologically appropriate, or simplifying reporting. For each option state information lost, validity risk, equity effect, and required approval.
7. Preserve donor or approved measurement requirements as constraints unless the user authorizes a change. Do not claim a target is achievable or infeasible without supporting assumptions.
8. Return an editable demand matrix, summary, and decision list.

## Output structure
- Purpose, intake mode, and scope
- Evidence register and constraints
- Measurement-demand matrix: indicator/task; population or volume; source/tool; frequency; role; documented capacity; burden calculation (if supported); status; risk; evidence IDs
- Cumulative workload totals only when comparable periods and task units are supplied
- Options and tradeoffs, each labeled as proposed
- Unknowns and decisions required

## Feasibility dimensions
- **Data availability:** Is the source named, current, complete for the target population, and accessible? Unknown access is not availability.
- **Measurement validity:** Does the data capture the intended result, population, and period? Proxy measures need explicit limits.
- **Operational capacity:** Are collection events, locations, tools, roles, and review steps known? Mark absent volumes.
- **Time:** Check collection windows against seasons, deadlines, recall, and implementation stages where dates are supplied.
- **Equity and access:** Consider language, disability access, connectivity, safety, and populations likely to be missed.
- **Data quality:** Identify verification, completeness, consistency, and correction needs. Do not assume routine data are reliable.
- **Protection and ethics:** Identify sensitive data, consent, confidentiality, retention, safeguarding, and permissions that affect method choice.
- **Resource dependence:** Separate known staff time or budget from missing values. The plan is not costed unless quantities and costs are supplied.

## Burden calculation rules
Count each task once in the grand total. A call performed by the officer is already part of total calling time; do not add officer calling time again to an all-callers total. Use mutually exclusive role totals, or use activity totals with an explicit allocation across roles. An unallocated task is not extra work in addition to its later role allocation.
Do not equate a count of sessions with a count of active register weeks. A calendar quarter is not automatically twelve working weeks, and a month is not automatically four weeks. If exact activity dates/counts are absent, report the supplied weekly or per-event rate and a formula for the period total. A labeled hypothetical calendar scenario can illustrate a range, but must not become the central source-supported quarterly total or a confirmed capacity verdict. Preserve uncertainty across the burden table, plan and decisions.
Use transparent arithmetic such as `number of units × time per unit × frequency`. Include setup, collection, cleaning, validation, analysis, reporting, travel, and follow-up only when their inputs are supplied. Show the reporting period and whether totals are per cycle, month, or year. Do not add unlike tasks into one total unless their units and periods are compatible. If variability is known, show its range and source. An average is not a guaranteed time.

For each proposed simplification, state the requirement affected, evidence preserved and lost, likely validity or equity consequence, dependencies, and approval needed. Never describe an approved requirement as optional without authorization.

## Boundaries
Facts, assumptions, estimates, and recommendations must be visibly distinct. Avoid a single overall feasibility score unless the user supplies a scoring rule. Do not fabricate unit costs, staff availability, response rates, permissions, sample size, collection time, targets, or budget. Do not silently redefine or drop indicators. For any estimate, expose the formula, assumptions, period, and included tasks.

## Missing, conflicting, or unsuitable inputs
- No workload volumes or time data: describe burden drivers qualitatively and state that hours cannot be calculated.
- Unknown source access: classify it as unconfirmed and list verification needed.
- Conflicting frequency or population: show both versions and the consequence for the estimate.
- User asks to cut scope: propose options with tradeoffs and approval needed; do not present them as authorized changes.
- Non-M&E request: state the skill's boundary and stop.

## Completion checklist
- All supplied indicators and collection tasks are covered.
- Evidence and unknowns are distinguished.
- Calculations use supplied volumes and time only and show assumptions.
- Design estimates are separate from evidence-based arithmetic.
- Options explain information, validity, equity, and approval tradeoffs.
- No targets, budgets, roles, sample sizes, or commitments were invented.

## Interruption and resumption
If interrupted, preserve the actual assessment and calculations, evidence register with source filenames/versions or dates, assumptions, and unresolved decisions. Resume only from files and handover supplied for the resumed task. Check whether sources changed and flag differences. Record recalculations and edits. Never upgrade a proposal, assumption, or pending decision into an approved scope or resource decision.
