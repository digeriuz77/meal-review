# Illustrative sampling draft: Orchard Training

Fictional, manually authored illustration of examples/input.md, not a Claude execution result. Draft only. No respondent selected and no consent or field permission confirmed.

## Scope and sources

Planning note v1, 2026-09-04 supplies a descriptive current-practice proportion for the January-June cohort, N=1,000 eligible adults, individual unit, no domain estimates and no causal claim. Its complete/current phone-frame statement is supplied, not independently verified. Check unique IDs, eligibility, duplicate records and contact coverage before selection.

## Proposed approach and arithmetic

Follow the requested single-stage SRS without replacement, conditional on frame verification. The supplied planning parameters are z=1.96, p=0.5, absolute e=0.05 and response fraction r=0.8. p and r are design assumptions, not measured results.

| Quantity | Substitution | Value |
|---|---|---|
| Infinite-population completions | 1.96^2 * 0.5 * 0.5 / 0.05^2 | 384.16 |
| Finite-population completions | 384.16 / (1 + 383.16/1,000) | 277.740825... |
| Required completions | ceil(277.740825...) | 278 |
| Invitations | ceil(278 / 0.8) | 348 |
| Invitation envelope | 360 - 348 | 12 invitations of headroom |

348 invitations fit the supplied count envelope. This is not a costed or staffed feasibility finding. Expected response is not a guarantee; achieved precision, nonresponse bias and the chosen confidence method need checking. There is no subgroup precision claim.

## Selection, contacts and analysis

Proposed: after permissions/frame checks, freeze the eligible frame and select 348 distinct IDs uniformly without replacement using a documented reproducible generator. Record actual seed, frame hash/version, date and selection code at execution; none exist yet. Do not publish personal identifiers in the report. Contact attempts, spacing and refusal/ineligibility dispositions require an agreed protocol. Do not substitute conveniently available trainees for refusals. Any reserve list must use a predeclared random order with preserved dispositions; more invitations cannot ensure absence of response bias.

Initial inclusion probability would be 348/1,000 and base invitation weight 1,000/348. Final respondent weights and any adjustments require actual dispositions and justified response assumptions; they are not simply evidence that respondents represent everyone. Report completed eligible n, item nonresponse and design-appropriate estimates/uncertainty after collection.

## Conditions before fieldwork

Confirm frame coverage/uniqueness, data access and consent; agree contact/withdrawal/retention rules; allocate actual staff and dates; pilot frame contactability and instrument interpretation. Proposed pilot criteria need the study lead's decision. If the frame claim fails, revisit scope and sizing instead of retaining the all-trainee inference. No new targets, costs, roles or approvals are asserted.

## Completion and change record

Calculation and invitation count independently checked for this illustration. Required source fields remain visible. This is one unapproved design draft; no previous version or field result is claimed. Handover would include the source note, this draft, pending decisions and the next task: frame/access verification.
