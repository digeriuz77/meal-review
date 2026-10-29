# Start: Results-chain alignment

**Status:** Checked in Claude Code. Anthropic's help page says Free and paid plans can use uploaded skills once code execution is turned on; we checked browser upload on a paid plan only.

Use it to compare two or more supplied ToC, logframe/results framework, and program narrative artifacts. To assess cross-document alignment, include at least one results structure and another artifact. The review preserves each source's terminology and commitments, and flags conflicts for a responsible person to resolve.

**Intake:** attach files directly, or name a folder and ask the assistant to list candidate files before using them. It must say which intake mode and files it used.

**Starter prompt:**

> Use results-chain-alignment on the attached files [or folder: path]. Compare the supplied ToC, logframe/results framework, and narrative. Preserve each source's wording, level labels, indicator definitions, assumptions, and version. Show matched elements, gaps, conflicts, and hypotheses versus demonstrated evidence. Do not choose a source authority or rewrite commitments. Mark facts, assumptions, and proposed recommendations separately, and return an editable Markdown alignment matrix.

See `examples/` for fictional input, incomplete, unsuitable, and output examples. They show the intended artifact shape, not a live invocation, runtime pass, or usability result.

## Delivery and access

Code candidate invocation: `/me-workspace:results-chain-alignment` with explicit readable files or a scoped folder. Browser candidates use uploaded readable attachments with the individual skill ZIP, or pasted SKILL.md; do not use machine paths. Checked in Claude Code. Anthropic's help page says Free and paid plans can use uploaded skills once code execution is turned on; we checked browser upload on a paid plan only. Save and inspect the actual Markdown artifact when file tools are available; otherwise state that no download was created.

These files are free with no site signup or API backend. They do not provide a Claude account or guarantee completion within provider limits. Save original sources, the actual output and a handover before pausing.
