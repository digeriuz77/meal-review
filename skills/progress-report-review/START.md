# Start progress-report-review

Use this review on a readable M&E document. All offering files are free; your Claude account's access and usage limits still apply. Checked in Claude Code. Anthropic's help page says Free and paid plans can use uploaded skills once code execution is turned on; we checked browser upload on a paid plan only. Code tests use the existing subscription. See SKILL.md for the full maintained criteria.

Browser: upload the document and any framework or definitions needed to verify its claims. Code: name the specific files or folder. For copy/paste, paste SKILL.md followed by your document. No site signup or API backend is required by the pack.

Starter: Use progress-report-review on my supplied document. Identify its type and limits, cite sources for material findings, preserve all three severity headings, and return an editable Markdown review. Separate facts, assumptions and proposals. Mark what cannot be assessed.

In Code invoke `/me-review:progress-report-review` with the same instruction and explicit files. In a browser name the enabled uploaded skill; local folder discovery is unavailable there.

Fictional example input: A community training program says 63 of 84 enrolled learners met its attendance rule this quarter. Its draft calls this an increasing employment impact, supplies no prior-period data, and proposes an unapproved evening-session pilot. A suitable review identifies the limits of those claims instead of inventing employment or trend evidence. For TOR or plan review, this extract alone supports only a preparation/gap note, not a full review.

Illustrative response: Attendance is 63/84 = 75% of enrolled learners [supplied extract]. No prior period or employment measure is supplied. Revise the claim to this period's attendance result. An evening-session pilot is a proposed option, with responsibility and approval unresolved. A full progress-report-review assessment requires the relevant document and definitions. This response is an illustration, not test evidence.
