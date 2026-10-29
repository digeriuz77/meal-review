---
name: sampling-plan-draft
description: Draft an M&E sampling plan, or check an existing one's sizing and selection, from purpose, population, frame and constraints, with transparent calculations and unresolved decisions. Use when a survey or evaluation needs a sample design.
---

# Sampling plan drafting

## Purpose and trigger

Use when a practitioner needs a prospective sampling plan for monitoring, a baseline, a survey or an evaluation. The output is an editable Markdown design draft, not a claim that respondents were selected or data collected. For a supplied plan, use the same method to check design consistency without replacing the user's approved choices. This file owns the method; supporting examples illustrate it.

**Status:** Checked in Claude Code. Anthropic's help page says Free and paid plans can use uploaded skills once code execution is turned on; we checked browser upload on a paid plan only. The files are free; Claude account access and usage limits are separate. No API key or site signup is required by these instructions.

**Dates:** Never write today's date, the system date, or words such as "passed", "late" or "stale" about a supplied date in the artifact. Supplied dates govern; if a date's status matters, write "status unknown from supplied files".

## Minimum input and intake

Supply the decision or study purpose, indicator or question, target population/unit and what is known about the sampling frame. Include precision or comparison requirements, proposed mode, geography/time, required subgroups, resources and access if available. A short description is acceptable; a complete TOR is not mandatory.

- Browser: upload readable source attachments. Do not request machine paths or search folders. If an attachment cannot be read, ask for accessible text and identify what remains unassessed.
- Code: use explicit files or the user's scoped folder. List candidate files when discovery is needed. Do not search unrelated folders; already named files need no repeated approval.
- Record filenames, versions/dates and page/section/table or row references. Show supplied facts, unresolved conflicts, assumptions and proposed design choices separately. Missing in the input does not mean nonexistent or unapproved elsewhere.
- No identifiable M&E sampling purpose: return a suitability note and stop. With purpose but missing population/frame, produce a bounded design outline and exact decisions needed; do not calculate a representative sample.

## Reproducible sequence

1. **Define the claim and population.** Name the estimand or qualitative question; eligibility/exclusions, counting and selection units, geography, reference dates and intended inference population. Distinguish enrolled people, households, records and encounters. State whether the job is descriptive estimation, comparison/change detection, causal evaluation or qualitative explanation. Random sampling alone does not identify a causal effect; causal identification and random assignment are different design questions.
2. **Assess the frame.** Describe its source/date, unique IDs, coverage, omissions, duplicates, eligibility errors, contactability and access. A larger sample cannot repair coverage bias. A phone list excludes people without listed working phones unless corrected. Offer frame repair or an explicitly narrower population as proposed options, not a silent scope change. Do not expose actual personal identifiers in the plan.
3. **Choose an approach with rationale.** Compare a census, simple random, stratified, systematic, cluster/multistage or nonprobability approach as relevant. Known nonzero inclusion probabilities and implementable selection are needed for design-based population inference. Probability sampling can start from area frames; a missing name list is not automatically a reason to use convenience sampling. Systematic selection needs random start, a valid interval/procedure and a periodicity check. Purposive qualitative selection needs explicit inclusion/variation/access logic; do not attach a survey margin of error to it. Census attempts can still have nonresponse and measurement error.
4. **Size only the applicable design.** Use the rules below and reproduce inputs, formula, substitutions, rounding, units and source of each parameter. Distinguish completed eligible responses from invitations/contacts. Independently recompute supplied and proposed arithmetic using an available calculator, or step-by-step manual substitution when none is available; state how it was checked and show discrepancies from the original. Do not merely repeat a supplied result. If a calculation cannot actually be verified, label it unchecked and leave the sizing verdict unresolved. Never fabricate a tool run or certified precision. Missing design inputs mean scenarios or a sizing specification, not a confirmed number.
5. **Specify selection and field rules.** Explain each selection stage, frame freeze/cleaning, reproducible randomization procedure and seed to be recorded at execution, without claiming it already happened. Define contact attempts/spacing, consent/refusal and ineligibility recording, no pressure to participate, and a predeclared reserve-list procedure if used. Do not replace refusals with whoever is available. Preserve original selection and disposition records. Distinguish invitation inflation, differential response and coverage; extra invitations do not remove response bias.
6. **Check analysis and feasibility.** Identify design weights and inclusion probabilities, nonresponse adjustment assumptions, survey-design-aware variance and required domain precision. Do not promise small subgroups are precise because total n is sufficient or because each exceeds 30. For clustered/panel designs name PSU/strata/repeated-unit effects and dependencies. Compare contacts, completed responses, cluster counts, timing and effort against supplied resources only. A budget cap can require redesign or reduced precision, not false certification of an underpowered design.
7. **Plan validation and handoff.** Propose a pilot/frame audit, what it would check, decision criteria and who must authorize changes. Label all proposed roles, dates, thresholds and permissions. Include limitations, alternatives, unresolved decisions, conditions before fieldwork and a change record. Do not report hypothetical pilot findings as observations.

## Sizing rules and boundaries

### Single proportion, simple random sampling without replacement

Only when the request is a two-sided approximate confidence interval for one proportion under simple random sampling:

`n0 = z^2 * p * (1-p) / e^2`

If a known finite eligible population N is relevant and the sampling fraction warrants correction, use `n = n0 / (1 + (n0 - 1)/N)`. Otherwise retain n0 and explain why. Round required completions up once after adjustment; then `invitations = ceil(required completions / r)` for a supplied or explicitly hypothetical response fraction r. These approximations assume the chosen confidence method is suitable; rare outcomes or boundary proportions may require another interval/design.

- z, p, absolute margin e, N and response fraction r need sources or explicit scenario labels. For example, e=0.05 means five percentage points, not five percent of p. p=0.5 maximizes p(1-p) for an absolute-margin single-proportion scenario; it is not a universal conservative setting for rare outcomes, relative precision, means or power.
- Do not silently use 95%, five percentage points, 80% power, a design effect or an 80% response rate as approved inputs. If the user asks for a scenario, label every assumed parameter and keep it separate from confirmed requirements. If the frame is unreconciled or a required design input (such as response rate, eligibility rate or intraclass correlation) is missing and the user did not ask for scenarios, present the calculation table as a checklist of required inputs and do not compute sample sizes.
- Validate 0<p<1, 0<e<1, 0<r<=1, positive z, integer N>0 and compatible units. An invitation count exceeding N is infeasible under a without-replacement eligible frame: report it and revise requirements/design, rather than quietly capping it and retaining the promised precision.
- This expression does not size a mean, rare-event detection, paired change, clustered comparison, impact study, LQAS classification or subgroup domain. Do not reuse it for those purposes.

### Other designs

- Comparison/power: require outcome type, comparison design, effect/MDE, variance or baseline rates, significance/test direction, power, allocation, repeated measures/attrition and clustering as applicable. Supply a design-specific calculation specification and seek statistical review where necessary; do not certify power from a generic proportion formula.
- Cluster/multistage: identify clusters, stages, selection probabilities and within-cluster correlation/design-effect evidence. A design effect is estimator/design specific. `1 + (m-1)*ICC` is a simplified equal-cluster approximation, not a universal formula. Unknown ICC, unequal sizes or too few feasible clusters remain design problems; multiplying n by an arbitrary default does not solve them. Finite corrections and nonresponse must be applied at the appropriate stage, with statistical review for complex designs.
- Stratified/domain estimates: size and allocate for the actual reporting domains and precision requirements. Proportional allocation can leave small domains unusable; oversampling changes weights. Report tradeoffs without inventing subgroup targets.
- Qualitative: specify purposive criteria, variation, recruitment, initial proposed range if requested, analysis-informed stopping/review rules and limits. Do not promise saturation at a fixed interview count or represent frequency as population prevalence.

## Output structure

For drafting mode, use the structure below. For an existing-plan consistency check, keep scope and source register, compare the supplied choices/calculations to the same design rules and return evidence-linked issues plus proposed corrections. Do not silently replace the plan or call proposed changes approved. A missing plan means no full check verdict.

Write one Markdown artifact with:
1. Scope, decision/use and status (draft, supplied approval or unresolved).
2. Source/evidence register, supplied facts and conflicts.
3. Population, frame quality, intended inference and exclusions.
4. Recommended approach and alternatives, explicitly proposed.
5. Calculation table or unresolved sizing specification; assumptions and verified arithmetic.
6. Stage-by-stage selection, contacts/nonresponse and data protection.
7. Analysis/weights/domain precision and limitations.
8. Feasibility, pilot, unresolved decisions and conditions before fieldwork.
9. Completion check and change record.

When checking an existing plan, additionally retain `## Critical Issues`, `## Important Issues` and `## Minor Improvements`, even when an item is None identified or Not assessable. Do not conflate this targeted consistency check with a completed independent review of every sampling criterion.

## Completion and resumption

- Every requested indicator/domain is covered or explicitly unresolved.
- Frame limitations and inference claims agree; sampling and causal identification are separate.
- Completions/invitations, periods, assumptions and arithmetic reconcile. No invented targets, observations, costs, references, permissions or commitments.
- Proposed selection can be implemented; privacy, access, nonresponse, weights and field validation are addressed or flagged.
- Inspect the actual saved artifact if file tools are available. A chat summary does not replace a promised file. Without file creation, return editable Markdown and state no downloadable file was created.
- On interruption save actual drafts, calculations, source/version register and a short handover listing next stage and decisions. On resume compare inherited claims against original sources; classify each as confirmed, contradicted or unconfirmed. Preserve unknown status instead of converting it into absence or approval. Recalculate affected results after any changed parameter and record the change.

## Public methodological context

This is a bounded design aid, not a replacement for design-specific statistical work. General sampling, frames and nonsampling error are covered in the UN Statistics Division's [Designing Household Survey Samples: Practical Guidelines](https://unstats.un.org/unsd/demographic-social/Standards-and-Methods/files/Handbooks/surveys/Series_F98-E.pdf). Complex survey analysis must reflect the design; see the CDC's [NHANES variance estimation tutorial](https://wwwn.cdc.gov/nchs/nhanes/tutorials/varianceestimation.aspx/SampleDesign.aspx). These references are background, not claims that a user's proposed design meets their requirements. Do not invent page citations or claim to have opened a source unless actually read.
