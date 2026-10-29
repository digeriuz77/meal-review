# M&E Workspace

File-integrated M&E document review, creation, and cross-referencing for Claude Code.

Point Claude at your project folder and it reads your logframe, M&E plan, proposal, progress reports, evaluation TOR, and evaluation report to cross-reference them, check consistency, identify gaps, and create new documents with source traceability.

Built by [M&E Studio](https://www.monitoringevaluationstudio.com/plugins).

## Job Skills

Each job skill does one task and writes an editable Markdown file. Start with [PILOT-START.md](PILOT-START.md) for the first eight and the three workflow packs, and [RESERVE-START.md](RESERVE-START.md) for the four newer ones.

| Job | Command |
|---|---|
| Frame evaluation questions | `/me-workspace:evaluation-questions` |
| Match questions to evidence and methods | `/me-workspace:question-method-alignment` |
| Draft an evaluation TOR | `/me-workspace:evaluation-tor-draft` |
| Document indicators | `/me-workspace:indicator-reference-sheets` |
| Assess measurement burden | `/me-workspace:measurement-feasibility` |
| Draft an M&E plan | `/me-workspace:me-plan-draft` |
| Check progress evidence | `/me-workspace:progress-evidence` |
| Turn findings into proposed actions | `/me-workspace:findings-to-actions` |
| Align a results chain across documents | `/me-workspace:results-chain-alignment` |
| Draft a sampling plan | `/me-workspace:sampling-plan-draft` |
| Plan a data quality assessment | `/me-workspace:data-quality-planning` |
| Plan a baseline | `/me-workspace:baseline-planning` |

Workflow packs in `workflows/` chain these jobs for evaluation planning, feasible measurement and reporting to action. Checked in Claude Code. Anthropic's help page says Free and paid plans can use uploaded skills once code execution is turned on; we checked browser upload on a paid plan only.

## What It Does

Unlike paste-and-review tools, M&E Workspace reads multiple files from your project folder and cross-references them. Three modes:

| Mode | Example | Output |
|------|---------|--------|
| **Compare** | "Does this M&E plan cover all logframe indicators?" | Alignment matrix + gap analysis |
| **Create** | "Write a TOR from our logframe, M&E plan, and proposal" | Draft document with source traceability |
| **Review** | "Review this progress report against the logframe" | Scored review with cross-reference findings |

## Skills (12 domains)

| Domain | Commands | What It Checks |
|--------|----------|---------------|
| **baseline-report** | `check-indicator-coverage`, `create-plan` | Baseline values for every indicator, baseline study plans |
| **data-quality** | `create-dqa-plan` | Data quality assessment plans |
| **eval-report** | `check-tor-compliance`, `create-response` | TOR question coverage, evidence chains, management response |
| **eval-tor** | `check-alignment`, `create` | Evaluation TOR quality, question-indicator alignment |
| **indicators** | `create-irs` | Indicator reference sheet generation |
| **logframe** | `check-narrative` | Logframe against the proposal narrative |
| **me-plan** | `check-coherence`, `create` | M&E plan completeness, logframe coverage, method appropriateness |
| **progress-report** | `check-coverage`, `check-trends` | Indicator coverage, data plausibility, narrative-data alignment |
| **project-audit** | `full-check` | Full M&E system audit across all documents |
| **proposal** | `check-rfp` | RFP compliance of the M&E section |
| **sampling-plan** | `check-methodology`, `create` | Sampling method and sample size, sampling plan drafts |
| **theory-of-change** | `check-logframe-alignment`, `create` | Theory of change against the logframe, theory of change drafts |

**19 commands total** (11 checks, 8 creates) across 12 M&E domains. Free under the MIT license.

## Requirements

- **Claude Code** (this plugin reads the documents in your project folder)
- Readable project documents. Our checks cover editable Markdown; other input formats need actual readability checks or a text export before analysis.

This folder-based plugin targets Claude Code. Separate individual browser-skill candidates use uploaded readable attachments instead of local folder access; their installation and execution remain unverified.

## Installation

Run these inside Claude Code. To load a local copy instead, use `claude --plugin-dir <path-to-me-workspace>`.

```
/plugin marketplace add mestudiohq/me-review
/plugin install me-workspace@me-review
```

On Claude Code 2.1.275 or later, one line does both:

```
/plugin install me-workspace --marketplace mestudiohq/me-review
```

If the install summary says `Run /reload-plugins to activate.`, run that too.

## How to Use

Tell Claude what you want to do and point it at your files:

**Review an M&E plan against a logframe:**
```
Review my M&E plan against the logframe. Check for missing indicators,
method-indicator mismatches, and frequency issues.

M&E Plan: ./project/me-plan.md
Logframe: ./project/logframe.md
```

**Check progress report indicator coverage:**
```
Check whether this progress report covers all logframe indicators.
Flag missing indicators, implausible values, and disaggregation gaps.

Report: ./project/year2-report.md
Logframe: ./project/logframe.md
```

**Run a full M&E system audit:**
```
Audit all M&E documents in this project folder for consistency.

./project/
```

**Create an evaluation TOR from project documents:**
```
Create an evaluation TOR using our logframe, M&E plan, and proposal.

Logframe: ./project/logframe.md
M&E Plan: ./project/me-plan.md
Proposal: ./project/proposal.md
```

## Output Format

All review commands produce:
- **Section scores** (PASS / PARTIAL / FAIL per quality dimension)
- **Overall rating** (Strong / Adequate / Needs Revision / Major Issues)
- **Issues classified by severity** (Critical / Important / Minor)
- **Cross-reference findings** when multiple documents are provided

Create commands produce draft documents with `[Source: document, section]` traceability tags.

The project audit produces a traffic-light dashboard (GREEN / YELLOW / RED) across 7 system dimensions.

## Companion Plugin

**[me-review](https://github.com/mestudiohq/me-review)** is the paste-and-review companion. Use it when you have a single document to review. Use me-workspace when you have a project folder with multiple related M&E documents.

## License

MIT
