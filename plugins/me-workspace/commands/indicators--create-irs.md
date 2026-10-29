---
description: Use the maintained indicator-reference-sheets method for this M&E job on supplied project files.
argument-hint: "[explicit files or scoped project folder]"
---

# indicators--create-irs

This is a compatibility adapter, not a second method. First read `${CLAUDE_PLUGIN_ROOT}/skills/indicator-reference-sheets/SKILL.md` and apply that maintained method to the user's input. You may invoke `/me-workspace:indicator-reference-sheets` if available, but do not substitute a generic chat response or the legacy domain rubric.

Create reference sheets preserving each indicator ID and approved definition/target, with unknown fields explicit.

Use explicit files or only the named folder. List actual sources used; already named sources do not require another confirmation. Missing or contradictory evidence leads to a bounded draft/check with unresolved decisions. Unrelated input receives a suitability note, not an invented artifact. Supplied facts, assumptions and proposed choices remain separate.

When requested to save a file, write the actual Markdown artifact to that path and inspect it. The chat summary does not replace it. Retain source traceability and completion checks. For check commands, use these exact standalone headings, without numbering, abbreviation or extra text: `## Critical Issues`, `## Important Issues`, and `## Minor Improvements`. Keep each heading even when its content is None identified or Not assessable. Verify the actual file contains those headings before finishing. Do not fabricate results, targets, budgets, references, approvals or commitments. Use US English and no em dashes.
