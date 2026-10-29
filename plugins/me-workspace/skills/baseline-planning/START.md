# Start: Baseline planning

**Status:** Checked in Claude Code. Anthropic's help page says Free and paid plans can use uploaded skills once code execution is turned on; we checked browser upload on a paid plan only.

Use it to plan measurement for every supplied indicator, including who/what is measured, definitions and versions, timing relative to exposure, sources, prior-evidence comparability, permissions, and open decisions. It plans measurement, not baseline values.

**Intake:** attach the framework and supporting files, or name a folder and ask the assistant to list candidate files before selecting them. It must state the intake mode and files used.

**Starter prompt:**

> Use baseline-planning on the attached files [or folder: path]. Map every supplied indicator to its population, operational definition/version, measurement window, source/tool, method, timing relative to program exposure, disaggregation, permission/access status, and comparability needs for later rounds. Identify prior evidence and gaps without inventing values or targets. Treat post-exposure recall as retrospective self-report, not a measured baseline. Return an editable Markdown plan with facts, assumptions, proposals, and decisions clearly separated.

See `examples/` for fictional input, incomplete, unsuitable, and output examples. These are illustrations only, not runtime or usability evidence.

## Delivery and access

Code candidate invocation: `/me-workspace:baseline-planning` with explicit readable files or a scoped folder. Browser candidates use uploaded readable attachments with the individual skill ZIP, or pasted SKILL.md; do not use machine paths. Checked in Claude Code. Anthropic's help page says Free and paid plans can use uploaded skills once code execution is turned on; we checked browser upload on a paid plan only. Save and inspect the actual Markdown artifact when file tools are available; otherwise state that no download was created.

These files are free with no site signup or API backend. They do not provide a Claude account or guarantee completion within provider limits. Save original sources, the actual output and a handover before pausing.
