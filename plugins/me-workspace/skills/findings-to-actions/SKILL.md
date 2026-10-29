---
name: findings-to-actions
description: Convert supplied evaluation or review findings into a traceable management response and action matrix. Use when evidence needs a proposed response, decision, or follow-up action.
---

# Findings to management actions

## Purpose and trigger
Translate documented findings into proposed management responses and trackable actions while preserving evidence and uncertainty. This skill does not approve findings, assign real owners, or make commitments for an organization.

## Minimum inputs
- Findings, recommendations, or issues with their source.
- Program or organizational context sufficient to interpret them.
- Existing response, action, owner, or deadline information if already decided.

Accept explicitly uploaded files or a user-designated folder and file list. Upload mode uses attachments/text only. Folder mode inspects only that folder and lists files used. Confirm ambiguous evidence files. State intake mode.

## Starter prompt
> Use findings-to-actions on the attached files [or folder: path]. Create a source-linked management response and action matrix. Separate finding, evidence, management decision, and proposed action. Label any suggested owner or deadline as a proposal, and do not present it as a commitment.

## Procedure
1. Confirm intake mode and the desired scope: findings only, response drafting, or action tracking.
2. Extract each finding, recommendation, evidence, confidence/limitation, and any existing organizational response. Cite `filename#heading`, page, table, or row.
3. Check that the finding answers a relevant evaluation question or stated concern when that link is available. Flag recommendation-only statements without supporting evidence; do not strengthen them.
4. Separate the evidence-based finding from management interpretation, acceptance/rejection/partial acceptance decision, response rationale, and proposed action.
5. For each action, state the observable deliverable or change, proposed timing, dependency, and evidence of completion. Only use named owners and dates when supplied. Otherwise mark “Owner to be assigned” and “Timing to be decided.”
6. Check that actions address the finding and are proportionate. Note feasibility, risks, resources, and monitoring needs only where supported; mark unknowns clearly.
7. Prioritize using a transparent rationale tied to risk, urgency, or stated decision criteria. If no rule is supplied, label prioritization as a proposal.
8. Return an editable response and action matrix, including unresolved management decisions.

## Output structure
- Purpose and intake mode
- Evidence register
- Finding-to-response matrix: finding; evidence IDs; evaluation question/link; limitation; management decision (supplied or pending); response rationale; proposed action; proposed owner; proposed due date; completion evidence; status
- Decisions requiring management input
- Risks, dependencies, and follow-up measures

Use editable Markdown. Preserve the difference between action proposal and assigned commitment. Do not create a fake status such as “in progress” when none was supplied.

## Response decision rules
- A finding states what evidence supports. A recommendation states what evaluators propose. Keep them separate.
- Management may accept, partially accept, reject, defer, or request clarification. Use only a supplied decision; otherwise mark it pending.
- A response explains management's position and evidence or feasibility rationale. Do not invent institutional agreement.
- An action describes an observable change or deliverable. “Strengthen coordination” alone is not trackable.
- A proposed owner must be a role or person supplied by the organization. Otherwise use “Owner to be assigned.”
- A due date must be supplied or marked “Timing to be decided.” Any proposed relative timing needs a label and basis.
- Dependencies, resources, approvals, and risks must be visible. Do not assume a budget exists.
- Completion evidence should state what can be checked, such as a revised procedure or dated review record, but label it as proposed until adopted.
- If evidence is mixed or limited, carry the limitation into the response and action.
- Prioritize using stated criteria. Without them, label priority as proposed.

For every row, trace evidence → finding → evaluation question or concern → management decision → response → action → completion evidence. Flag broken links. Do not create an action for an unsupported finding unless it is clearly an information-gathering proposal.

## Evidence and boundaries
Keep facts, evaluative judgments, management positions, assumptions, and proposals visibly distinct. Conflicting evidence remains visible. Recommendations do not become accepted actions automatically. Do not invent budgets, named owners, deadlines, completion evidence, or approval. If an action implies a policy, safeguarding, or resource decision, flag the approval needed rather than making it.

## Missing, conflicting, or unsuitable inputs
- Finding lacks evidence: include it as an unverified claim and ask for supporting source; do not draft a definitive response.
- No management decision: mark pending and offer clearly proposed response options if requested.
- Conflicting findings: show both evidence paths and identify the reconciliation decision.
- No owner or deadline: leave unassigned and undecided.
- Non-M&E request: state the skill supports evidence-to-action work and stop.

## Completion checklist
- Every action traces to a supplied finding or is labeled a proposal.
- Evidence, limitation, management decision, and response are separate.
- Owners, dates, budgets, and status are supplied or visibly unresolved.
- Actions are specific enough to verify when adopted.
- Conflicts, resource needs, and approval decisions are visible.
- Nothing is represented as an organizational commitment without source evidence.

## Interruption and resumption
If interrupted, preserve the actual response and action matrix, evidence register with source filenames/versions or dates, and unresolved management decisions. Resume only from files and handover supplied for the resumed task. Check whether sources changed and flag differences. Record edits and status changes. Never upgrade a proposal, assumption, or pending decision into an accepted response, assigned owner, deadline, or commitment.
