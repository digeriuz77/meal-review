# Free M&E job skills and workflows

Use these eight job skills and three starter packs for evaluation planning, feasible measurement and reporting to action. Four newer skills are described in [RESERVE-START.md](RESERVE-START.md). The files are free, with no site signup or API backend.

## Choose a job

| Job | Skill | Output |
|---|---|---|
| Frame evaluation decisions | evaluation-questions | Prioritized evaluation questions |
| Match questions to feasible evidence | question-method-alignment | Question-method matrix |
| Prepare a commissioning draft | evaluation-tor-draft | TOR draft and unresolved decisions |
| Define how an indicator is measured | indicator-reference-sheets | Reference sheets |
| Assess collection workload | measurement-feasibility | Burden calculations and tradeoffs |
| Plan practical measurement | me-plan-draft | M&E plan and coherence check |
| Check reported evidence and comparisons | progress-evidence | Reconciled evidence review |
| Turn findings into proposed actions | findings-to-actions | Management response/action register |

Each skill folder includes SKILL.md, START.md, fictional inputs and an illustrative output. Examples are explanations, not test evidence. Choose a complete job from workflows/evaluation/START.md, workflows/measurement/START.md or workflows/reporting/START.md. Each pack names its required reviews from the separate me-review plugin.

## Delivery and access

In Claude Code, load this local plugin and invoke `/me-workspace:<skill>` with explicit readable file paths or a scoped folder. A local launch can use `claude --plugin-dir <me-workspace-folder> --plugin-dir <me-review-folder>`. The second plugin supplies the pilot document reviews. These packs write editable Markdown. They do not promise Word, PDF or spreadsheet rendering.

For browser custom skills, upload the individual skill ZIP, enable it, and upload the named documents. Browser files replace local folder access. Current [Claude documentation](https://support.claude.com/en/articles/12512180-use-skills-in-claude) lists custom skills on Free, Pro, Max, Team and Enterprise with file creation/code execution enabled; organization policy can restrict them. Checked in Claude Code. Anthropic's help page says Free and paid plans can use uploaded skills once code execution is turned on; we checked browser upload on a paid plan only. Copyable SKILL.md instructions are provided as a fallback, also awaiting separate browser testing.

Claude account usage and file limits apply. The free offering does not include a Claude subscription or guarantee completion within a Free-plan allowance. Code subscription access is [documented separately](https://support.claude.com/en/articles/11145838-use-claude-code-with-your-pro-or-max-plan). No API key is needed by these instructions.

Save actual intermediate artifacts and a short handover before pausing. In a new session supply the original input, saved artifacts and handover. Keep source facts, assumptions, proposals and approved decisions distinct. Human usability validation is pending; technical checks do not establish practitioner usability.
