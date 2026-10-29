---
description: Use the maintained sampling-plan-draft method for this M&E job on supplied project files.
argument-hint: "[explicit files or scoped project folder]"
---

# sampling-plan--create

This compatibility adapter routes to the maintained method, not a second method. First read `${CLAUDE_PLUGIN_ROOT}/skills/sampling-plan-draft/SKILL.md`; apply it to the user's actual inputs and the targeted job below. `/me-workspace:sampling-plan-draft` is the candidate skill invocation when available.

Draft a prospective sampling plan, supported sizing calculations or calculation specification, selection/nonresponse rules, analysis limits and unresolved decisions. Do not claim actual selection.


Use explicit files or only the named folder; state which files were actually read. Browser users supply attachments instead of folders. Named sources do not need repeated approval. Missing or conflicting evidence yields a bounded note or draft and unresolved decisions. Unrelated input receives a suitability note, not an invented artifact. Separate supplied facts, assumptions and proposed choices.

If saving an artifact, write and inspect the actual Markdown file. Without file tools, return editable Markdown and state no download was created. A summary does not replace a promised file. For targeted checks retain exact standalone headings `## Critical Issues`, `## Important Issues` and `## Minor Improvements`, including None identified or Not assessable as needed. Severity reflects consequences for the intended use; do not invent a score or pass an unseen document.

Do not invent results, targets, budgets, references, approvals or commitments. Use US English and no em dashes. On resume verify inherited claims against original sources, preserving unknown status and recording changes.
