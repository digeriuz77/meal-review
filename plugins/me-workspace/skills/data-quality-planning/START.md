# Start: Risk-based DQA planning

Use this skill to plan a prospective assessment of specified monitoring data and the systems that produce them. It produces an editable Markdown plan only. It does not perform verification, write data-quality findings, or certify data.

**Minimum intake:** provide an indicator definition and intended use, data-flow information, known sources/risks, and constraints or access information when available. If some are missing, preserve them as unknown and limit the plan. If no indicator/data stream is identified, ask for it before drafting a plan.

**Intake mode:** attach the relevant files, or name one folder and ask the assistant to list candidate files before selecting them. State which mode was used and list the sources actually used. Do not assume access to another folder, system, respondent, or source.

**Starter:**

> Use data-quality-planning on the attached files [or the selected files in: folder path]. Plan a risk-based check of the supplied indicators and data flow for [period/decision, if known]. Separate completeness, reconciliation, source verification, validity/accuracy, reliability, precision, timeliness, and integrity procedures. Use only supplied thresholds and permissions. Mark any proposed sample or decision trigger as a proposal, preserve unknowns, and return an editable Markdown plan. Do not report findings or certify quality before checks are performed.

If a scope, access, threshold, or authority decision is required first, identify it and provide only the bounded plan that the current evidence supports. See `examples/` for fictional input and output illustrations; they are not test results.

## Delivery and access

Code candidate invocation: `/me-workspace:data-quality-planning` with explicit readable files or a scoped folder. Browser candidates use uploaded readable attachments with the individual skill ZIP, or pasted SKILL.md; do not use machine paths. Checked in Claude Code. Anthropic's help page says Free and paid plans can use uploaded skills once code execution is turned on; we checked browser upload on a paid plan only. Save and inspect the actual Markdown artifact when file tools are available; otherwise state that no download was created.

These files are free with no site signup or API backend. They do not provide a Claude account or guarantee completion within provider limits. Save original sources, the actual output and a handover before pausing.
