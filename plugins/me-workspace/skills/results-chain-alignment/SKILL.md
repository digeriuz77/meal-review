---
name: results-chain-alignment
description: Compare a theory of change, logframe, results framework, proposal or indicator register against each other for coverage, scope, indicator and causal-logic conflicts, preserving source versions and authority decisions. Use when results documents or their versions may disagree.
---

# Results-chain alignment

**Status:** Checked in Claude Code. Anthropic's help page says Free and paid plans can use uploaded skills once code execution is turned on; we checked browser upload on a paid plan only.

## Purpose and trigger
Compare supplied program-design artifacts and show where they tell a consistent story, diverge, or leave a link unsupported. This is a document alignment review, not a program redesign, validation of causal effects, or approval of a framework.

**Dates:** Never write today's date, the system date, or words such as "passed", "late" or "stale" about a supplied date in the artifact. Supplied dates govern; if a date's status matters, write "status unknown from supplied files".

## Minimum inputs
For a cross-document comparison, provide at least two distinct artifacts, including at least one results-chain or results-structure artifact: a theory of change (ToC), logframe, results framework, or program proposal/narrative that states results and pathways. The comparison is limited to the artifacts actually supplied. A single artifact can receive a preliminary extraction, but it cannot establish cross-document alignment.

Useful context includes indicator definitions and versions, scope/population, timeframe, assumptions, cited evidence, donor or organizational requirements, and whether any document is approved or locked. Do not assume a donor requirement from a document label.

## Intake modes
Accept either files explicitly uploaded to this chat or a user-designated folder with a file list. In upload mode, use only attached files and supplied text. In folder mode, inspect only the named folder, list candidate files, and use only the selected files. Confirm ambiguous identities or versions. State the intake mode and list the files reviewed. Do not imply access to other project files.

## Copyable starter
> Use results-chain-alignment on the attached files [or folder: path]. Compare the supplied ToC, logframe/results framework, and narrative. Preserve each source's wording, level labels, indicator definitions, assumptions, and version. Show matched elements, gaps, conflicts, and hypotheses versus demonstrated evidence. Do not choose a source authority or rewrite commitments. Mark facts, assumptions, and proposed recommendations separately, and return an editable Markdown alignment matrix.

## Reproducible procedure
1. Confirm intake mode, purpose, comparison scope, whether the review is diagnostic or intended to inform a revision, and which artifacts are supplied. List filename, stated type, date/version, and approval status where visible.
2. Extract each source independently before comparing it. Preserve exact result statements, level names, indicator wording and definitions, target population, geography, period, assumptions, and stated pathways. Record evidence IDs as `filename#heading`, page, table, row, or diagram label. Never invent a locator.
3. Build separate source inventories for: (a) activities and outputs, (b) intermediate and higher-level results, (c) pathways/mechanisms, (d) assumptions and contextual conditions, (e) indicators and definitions, and (f) scope, population, geography, and timing.
4. Keep source-specific level taxonomies. Do not automatically equate “impact” with “Goal,” merge outcome tiers, or map donor labels into another framework. If a crosswalk is needed, show the two labels and explain the proposed mapping as a question for the responsible team.
5. Compare in both directions: ToC/narrative elements to the results framework, and framework elements back to the ToC/narrative. Mark each relationship as aligned, partial, not found in supplied sources, conflicting, or not assessable. Similar wording alone does not prove the same construct.
6. Trace each stated causal link and distinguish: an asserted pathway or hypothesis; a rationale or cited evidence in the documents; observed implementation/results; and demonstrated causal effect. An assumption or plausible mechanism is not proof that the link operated. Pre/post movement alone does not establish attribution.
7. Compare indicators without rewriting them. Check exact wording/version, definition or construct, unit, population, observation window, result anchor, and source. A changed label is not necessarily a changed definition, and a shared label is not proof of equivalence. Record differences and ask for a crosswalk when needed.
8. Compare targets, population counts, locations, dates, and commitments across documents. Show conflicting values side by side with evidence IDs. Do not select a governing version from apparent recency, document type, or donor naming unless an explicit authority is supplied. When a signed or formally approved document conflicts with a later unsigned or unapproved one, treat the signed one as the working governing version, labeled proposed, and flag that the later document may govern if it was approved or supersedes it; the user decides.
9. Classify each issue by its observable document consequence, not an arbitrary numeric score. Distinguish an actual contradiction from information absent in the supplied set. Lack of a statement in one artifact does not prove the program lacks that logic.
10. Offer only clearly labeled proposals to resolve or investigate a conflict. Do not revise the results chain, change indicator commitments, invent a causal link, or mark a document approved.
11. Return the output structure below, including source limitations and decisions needed.

Also compare required disaggregation/equity groups across ToC, framework, indicator definitions and narrative. A population mentioned in the ToC but absent from a framework's measurement requirements is a coverage question, not permission to invent subgroup targets. Compare supplied resource, budget, staffing and implementation commitments with the activities/results they are expected to support; identify mismatched scope, units, totals or resource assumptions with both source references. Resource silence is an unknown, not proof of insufficiency; do not issue a costed feasibility judgment without quantities and assumptions.

## Output structure
1. Review scope, intake mode, and source/version register
2. Extraction summaries by source
3. Alignment matrix: element; source A wording/level/ID; source B wording/level/ID; match status; evidence and reasoning; consequence or uncertainty
4. Scope comparison: population, geography, timeframe, implementation stage, disaggregation/equity requirements, resource/budget/staffing alignment and commitments
5. Indicator identity/version matrix: source wording, definition, unit, population, period, anchor, differences, and crosswalk decision needed
6. Pathway and assumptions table: proposed link; stated mechanism; stated rationale/evidence; assumptions; what the documents demonstrate or do not demonstrate
7. Gaps, conflicts, and limitations, with source IDs
8. Facts, assumptions, and proposed recommendations
9. Decisions and source materials needed
10. Completion checklist

Use editable Markdown only for this candidate. Do not claim external validation or causal proof. When saving a file, write and inspect the actual artifact. A chat summary does not replace it. If file creation is unavailable, return editable Markdown and state that no download was created. For targeted check entry points retain `## Critical Issues`, `## Important Issues` and `## Minor Improvements` even when an item is None identified or Not assessable.

## Interpretation rules
- “Aligned” means the supplied documents describe compatible scope and result logic for the compared element. It does not mean that the pathway is empirically true.
- “Partial” means some shared content is present but important scope, population, timing, result level, or construct differs or is incomplete.
- “Conflict” means supplied statements cannot both govern the same scope as written, such as incompatible population sizes, target values, periods, definitions, or level assignments.
- “Not found in supplied sources” is limited to the files reviewed. Do not convert it into “does not exist.”
- “Not assessable” means document identity, source quality, or missing comparison context prevents a defensible judgment.
- Record each source's own taxonomy. Any mapping is a proposed crosswalk, never an automatic translation.
- A causal pathway in a ToC is a hypothesis about how change is expected to happen. Evidence cited for plausibility is distinct from program-specific evidence that the pathway operated and from evidence attributing outcomes to the program.
- Preserve approved commitments. Proposed reconciliation language must be shown separately from source wording and remain pending review.

## Missing, conflicting, or unsuitable inputs
- **Only one artifact:** provide a source-specific extraction and list what another artifact is required to compare. Do not issue an alignment verdict.
- **No identifiable result structure:** extract the claims present and mark result-level assessment as not assessable; do not invent a hierarchy.
- **Conflicting versions:** compare each version separately, retain date/version and both evidence IDs, and ask which version has authority. Do not choose from recency alone. If one version is signed or formally approved and a later one is not, use the signed one as the working version, labeled proposed, and flag that the later one may govern; the user decides.
- **Missing indicator definitions:** compare labels as labels only and request definitions before claiming construct alignment.
- **No causal evidence:** describe documented hypotheses and rationale, note evidence gaps, and make no attribution claim.
- **Ambiguous or inaccessible files:** ask the user to identify the intended file or upload it. Do not search beyond the named folder or claim access to unseen attachments.
- **Non-M&E request:** state that this skill compares M&E results-chain documents and stop or suggest the closest relevant task.

## Interruption and resumption
If interrupted, preserve the actual matrix and extraction notes, source filenames and versions/dates, evidence IDs, and unresolved decisions. Resume only from files and handover supplied for the resumed task. Recheck source versions, flag changed sources, and record edits. Check inherited claims against original sources as confirmed, contradicted or unconfirmed. Do not upgrade a hypothesis, proposal, or pending authority decision into a demonstrated link, approved crosswalk, or commitment.

## Completion checklist
- Intake mode, files, and versions are explicit.
- Each source was extracted before comparison, with traceable evidence IDs.
- Source-specific result labels and indicator definitions remain intact.
- Comparisons run in both directions and absence is limited to supplied sources.
- Hypotheses, supporting rationale, observed results, and demonstrated causal effects are distinguished.
- Conflicts show both versions and are not resolved by automatic source ranking.
- Facts, assumptions, and proposed recommendations are separate.
- No commitment or source document was silently rewritten or approved.
- Missing inputs, limitations, and decisions needed are visible.
