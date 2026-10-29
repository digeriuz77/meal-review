---
name: evaluation-questions
description: Draft or improve prioritized evaluation questions from supplied program and decision context. Use when a user needs questions for an evaluation, inception process, or evaluation TOR.
---

# Evaluation question design

## Purpose and trigger
Turn an evaluation purpose and the decisions it must inform into a small, answerable set of prioritized questions. This skill drafts questions; it does not select methods in detail, promise causal attribution, or approve an evaluation design.

## Minimum inputs
- Evaluation purpose or reason for commissioning.
- Intended users and at least one decision or use, if known.
- Program, intervention, or policy being evaluated and its stage.
- Scope boundaries or constraints, if known.

Accept either files explicitly uploaded to this chat or a user-designated folder with a file list. For uploads, use only the attached files and text. For folder intake, inspect only the named folder and list candidate files before using them; do not assume access to a project workspace. Ask which files to use when multiple candidates are ambiguous. State the intake mode in the output.

## Starter prompt
> Use the evaluation-questions skill on the attached files [or the files in: folder path]. Draft a prioritized question set for [evaluation purpose]. The decisions or intended uses are [known uses, or “not yet specified”]. Preserve source evidence references, mark assumptions and open decisions, and return an editable Markdown artifact.

## Procedure
1. Confirm intake mode, evaluation type or stage, purpose, intended users, decisions, scope, timing, and known constraints. Separate stated facts from missing information.
2. Extract a short program and context summary with source evidence IDs. Use `filename#heading`, page, table, or row when available. Never invent an ID; label unlocatable evidence by filename and say the location is unavailable.
3. Identify the decisions questions must inform. If none are supplied, mark the decision link as unresolved and offer draft questions only as provisional options.
4. Select criteria that fit the purpose. OECD-DAC criteria may be relevant, but do not require every criterion. Explain why each selected criterion applies. Add non-DAC questions only when tied to a stated use.
5. Draft a concise set, normally three to five primary questions. Use subquestions only where they clarify scope. Ask one thing per question, avoid leading wording, and define population, geography, period, and comparison when supported.
6. For each question, check answerability against available or plausibly collectable evidence. Flag causal or counterfactual wording when the supplied design cannot support attribution. Do not convert association or pre/post change alone into causal attribution.
7. Prioritize questions by decision value, answerability, and fit with scope. Mark any ranking as a proposed recommendation, not a stakeholder decision.
8. Return the artifact structure below. Include unresolved inputs and a short validation checklist.

## Output structure
1. Purpose and intake mode
2. Source summary and evidence register
3. Stated facts, assumptions, and proposed recommendations
4. Prioritized evaluation-question matrix: priority; criterion or rationale; primary question; subquestions; decision/use; evidence needed; answerability note; evidence IDs
5. Questions deferred or excluded, with reason
6. Open decisions and validation checklist

Use Markdown tables that remain editable. Do not claim a question is approved. Label any unverified context. Markdown is the checked output format; other exports require separate verification.

## Question design checks
- **Relevance:** The question addresses a stated evaluation purpose, priority, or decision. If the connection is inferred, label the inference.
- **Answerability:** Ask about an observable result, experience, process, or relationship for which evidence can be identified.
- **Scope:** Name population, geography, and period when the source supports them. Avoid broad phrases such as “the community” when the intended group is narrower.
- **Neutrality:** Avoid wording that assumes the program worked, failed, or caused change.
- **Focus:** Split double-barreled questions if their parts need different evidence or support different decisions.
- **Proportionality:** Do not add questions simply because a criterion is familiar. More questions require more time and evidence.
- **Criterion fit:** Relevance concerns fit to needs or context; effectiveness concerns results; efficiency concerns use of resources; impact concerns broader effects; sustainability concerns continuation of benefits. Use concepts that match the evaluation.
- **Causal wording:** Reserve “caused,” “effect,” or attribution language for designs capable of supporting that inference. Otherwise ask what changed or what factors contributed.
- **Question hierarchy:** Keep each primary question answerable on its own. Use subquestions for dimensions that clarify the same decision.
- **Priority transparency:** Explain why a question is high priority, such as a direct decision link or major evidence gap. Do not imply a numeric score unless its rule was supplied.

Read the questions as a set. Look for duplication, missing decision needs, excessive breadth, and incompatible timeframes. If a question cannot be answered within known scope, mark it for revision rather than quietly broadening scope.

## Evidence and boundaries
Keep source statements distinct from interpretation. Link every extracted program fact and question rationale to evidence IDs. Preserve discrepancies as conflicts, with both source IDs and the consequence for question design. Do not infer budgets, targets, timeframes, stakeholder commitments, or methods. Do not use all DAC criteria by default. A small pre/post design supports a description of observed change, not a causal claim.

## If inputs are missing, conflicting, or unsuitable
- Missing purpose or decision: produce a bounded provisional question menu and mark the decision link unresolved; ask only the highest-impact clarification.
- Missing program or scope details: use explicit placeholders and identify which questions cannot yet be made specific.
- Conflicting sources: report both versions with evidence IDs; do not silently choose one.
- Too many questions: group overlaps and propose a smaller set, retaining a traceable list of candidates.
- Non-evaluation request: state that this skill is out of scope and suggest the closest M&E task in plain language. Do not fabricate an evaluation.

## Completion checklist
- Preserve the precision of source statements. If the user says "some reports," do not turn that into a count such as "two reports." Unspecified quantities, dates, file versions and response counts remain unspecified. Recheck each numeric statement against the source before delivery.
- Intake mode is explicit and source files are identifiable.
- Each primary question connects to a stated use or is labeled provisional.
- Criteria are selected for purpose, not treated as universally mandatory.
- Question wording is answerable, bounded, and non-leading.
- Causal claims match the supplied design and evidence.
- Facts, assumptions, and proposed recommendations are distinguished.
- Evidence IDs and unresolved conflicts are preserved.
- No targets, budgets, methods, approvals, or commitments were invented.

## Interruption and resumption
If work is interrupted, preserve the actual draft artifact, the evidence register with source filenames/versions or dates, and unresolved decisions. Resume only from files and handover supplied for the resumed task. Recheck whether sources changed and flag differences. Record what changed in the artifact. Never upgrade a proposal, assumption, or pending decision into an approved decision during resumption.
