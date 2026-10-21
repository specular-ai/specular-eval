# caro

- Repository: <https://github.com/wildcard/caro> at commit `867323bf1e263194229bd3ebb46dbe53a2f2cb50`
- SDD approach: Spec Kit + Spec Kitty; coding agent(s): Claude Code, Codex, Cursor, Copilot
- Markdown: 1177 files, 446,281 lines, 13,936 KB
- Agent run: 78 of 80 tool calls, 315 s
- Project model: 1,555 IDs, 1,538 definitions, 3,754 references, 776 IDs with an authored status (51% of the 1,535 defined IDs)
- Findings: 6 duplicate definitions, 44 unresolved references (listed in [findings.csv](findings.csv))
- Precision: 29/30 (96.7%), see [../../precision/precision-sample.md](../../precision/precision-sample.md#caro)
- Extraction time: 10.5 s

## Agent summary

Measured discovery across 1,177 Markdown files: 12 categories, 1,538 definitions, 3,754 references; 777 mapped status occurrences, no unmapped statuses or status conflicts, and 519 date occurrences. Feature/file scopes exclude templates and technical tokens. Six duplicate definition occurrences are genuine ADR number collisions; 44 references remain unresolved.

## ID categories

| Category | IDs | Defs | Refs | With status | Status values | Agent rationale |
|---|---:|---:|---:|---:|---|---|
| Requirements (`requirements`) | 401 | 396 | 238 | 0 |  | Retains the existing requirements key; FR/NFR (including qualified IDs) identify functional and nonfunctional requirements. Evidence: kitty-specs/002-unquoted-cli-arguments/spec.md:105 and specs/005-caro-vscode-extension/spec.md:94. IDs restart by feature; spec.md/PRD.md are definition sources. |
| Success Criteria (`success`) | 55 | 55 | 100 | 0 |  | SC IDs identify measurable success criteria, e.g. kitty-specs/002-unquoted-cli-arguments/spec.md:128. Feature scopes and specification definitionPaths prevent contract/quickstart restatements from duplicating definitions. |
| User Stories (`stories`) | 31 | 30 | 57 | 0 |  | User Story N headings define feature stories, e.g. kitty-specs/002-unquoted-cli-arguments/spec.md:10. US1/US-001 aliases normalize to User Story 1 with integer ID templates in the folders using this naming convention. |
| Tasks (`tasks`) | 709 | 695 | 1984 | 653 | Done=319; Open=334 | Tnnn identifies implementation subtasks. Checkbox definitions in kitty-specs/002-unquoted-cli-arguments/tasks.md:33 and heading definitions in specs/004-implement-ollama-and/tasks.md:29 are supported. Canonical task lists and deferred work detail files define records; prompt repetitions are references. |
| Work Packages (`packages`) | 81 | 81 | 965 | 9 | Planned=8; Deferred=1 | WPnn identifies work packages in feature task-list headings, e.g. kitty-specs/002-unquoted-cli-arguments/tasks.md:26 and kitty-specs/008-caro-web-hub/tasks.md:33. Restricting definitions to tasks.md avoids prompt-file duplicates. |
| Architecture Decisions (`decisions`) | 20 | 23 | 212 | 15 | Proposed=11; Accepted=3; Rejected=1 | ADR-nnn identifies architectural decisions, defined only by level-one headings under docs/adr, e.g. ADR-019-autoharness-harness-hygiene.md:1. External summaries are references. Actual number collisions are preserved as diagnostics. |
| Risks (`risks`) | 12 | 12 | 0 | 12 | Mitigated=3; Open=6; Accepted=1; Closed=2 | RISK-nnn identifies release risks in .claude/releases/v1.1.0-beta-risk-register.md:44 onward; file-local scope and Status paragraphs support 12 risks. |
| Test Cases (`tests`) | 19 | 19 | 16 | 0 |  | TC-nnn identifies QA cases in docs/qa/i18n-test-cases.md:24 and specs/006-intelligent-prompt-generation/test_cases.md:5. Definition paths exclude task-list summaries; unrelated TC technical constraints in another feature are excluded by scope. |
| ID User Stories (`shortstories`) | 40 | 40 | 5 | 0 |  | Other specifications define US-001, US-1, or US1 directly, e.g. specs/002-implement-tdd-green/spec.md:28 and kitty-specs/027-issue-281-add/spec.md:16. These retain their authored identity in separate feature scopes. |
| Shell Integration Stories (`shellstories`) | 100 | 100 | 28 | 0 |  | S1.1.1-style IDs identify implementation stories in the Story column of specs/007-caro-shell-integration/milestones.md:17. Scope is limited to that feature; 100 definitions and 28 references resolve without duplicates. |
| Broken Windows (`backlog`) | 71 | 71 | 14 | 71 | Open=45; Fixed=18; Done=1; Mitigated=1; Claimed=5; Not reproducing=1 | BW-nnn identifies handoff/backlog records headed in .claude/memory/broken-windows.md:22 onward. Word/path boundaries avoid interpreting a branch-name fragment as a record; 71 definitions have statuses. |
| Work Packages (registers) (`package_tables`) | 16 | 16 | 135 | 16 | Done=8; Planned=8 | Features 018 and 020 use ID-column registers with authored statuses, e.g. kitty-specs/018-issue-10-implement/tasks.md:14 and kitty-specs/020-machine-resource-assessment/tasks.md:23. Separate sites preserve table statuses while treating repeated headings as references. |

## Statuses

Checkbox markers yield 653 task statuses. Paragraph regex reads Status fields even within multiline metadata paragraphs, captures contiguous authored lifecycle text without crossing Markdown formatting, and handles the bold deferred phrase. Table statuses remain authoritative for work-package registers. Common values and decorations map to Done, Open, Planned, Proposed, Accepted, Rejected, Mitigated, Closed, Fixed, Claimed, Deferred, and Not reproducing. Final evaluation maps all 777 occurrences, with zero conflicts. Missing status examples and unmapped/conflict lists were inspected; no inferred completion from acceptance checkboxes or feature-level Draft fields.

## Dates

Retains measured ISO dated entries (10), headings (67), Created fields (69), and Date fields (123); enables Last Updated snapshots (179) and Found milestones (71). All active rules have real matches inspected with list_matches. Removes zero-yield status-date/Ratified/Last Review rules; leaves unsupported textual dates as gaps. Excludes copied agent skills, plugins, prompt/template trees. Next Review is omitted because it is a scheduled review rather than evidence of an event.

## Gaps reported by the agent

Conventions the agent found but could not express with the configuration language.

- ADR numbers 001, 002, and 004 are reused for different documents. Bare IDs cannot distinguish these decisions; six duplicate definition occurrences remain rather than hiding legitimate records. Examples: `docs/adr/001-llm-inference-architecture.md:1`, `docs/adr/ADR-001-enterprise-community-architecture.md:1`, `docs/adr/ADR-004-skills-extension-system.md:1`.
- FR-NEW requirements restart independently in backend contracts, while task references depend on contextual backend meaning. A single feature-scoped ID cannot faithfully resolve those references. Examples: `specs/004-implement-ollama-and/contracts/ollama-backend.md:428`, `specs/004-implement-ollama-and/contracts/vllm-backend.md:520`, `specs/004-implement-ollama-and/tasks.md:211`.
- Task ranges and mixed plain-list/table definitions cannot all be covered by the chosen category-wide sites without also defining summary/dependency occurrences. Remaining task references are left unresolved. Examples: `kitty-specs/025-llm-evaluation-harness/future_work/WP10-multi-backend.md:156`, `kitty-specs/025-llm-evaluation-harness/tasks.md:474`, `specs/004-implement-ollama-and/tasks.md:616`.
- Malformed Markdown heading ###User Story 1 is not a heading definition. Examples: `kitty-specs/008-caro-web-hub/spec.md:10`.
- Vertical metadata tables put Status in a header/key cell rather than beside an ID definition; current status sites cannot attach these values to the ADR. Examples: `docs/adr/ADR-005-hayagriva-bibliography-integration.md:3`.
- Work-package lane/history YAML precedes the Markdown definition and is not a supported status/date site. Examples: `kitty-specs/025-llm-evaluation-harness/future_work/WP10-multi-backend.md:16`, `kitty-specs/025-llm-evaluation-harness/future_work/WP10-multi-backend.md:23`.
- Month-name or month-only dates did not yield normalized dates. They are not approximated as ISO dates. Examples: `.claude/releases/v1.1.0-beta-risk-register.md:75`, `.claude/releases/v1.1.0-beta-decision-record.md:13`, `docs/adr/ADR-005-hayagriva-bibliography-integration.md:5`.
- Quoted automation metadata and unnamed research-decision table rows are not supported by the configured definition/status sites. Examples: `.claude/automation/specs/AUTOMATED_DEV_FLOW_DRS.md:5`, `kitty-specs/002-unquoted-cli-arguments/research.md:16`.
- Status prose may contain several historical dates and linked/inline-code fragments; the configuration captures the lifecycle phrase only and cannot safely assign every mentioned date as a status transition. Examples: `.claude/memory/broken-windows.md:55`, `.claude/memory/broken-windows.md:238`.

## Files

- [configuration.json](configuration.json): the configuration the agent submitted (categories, rules, definition sites, status sites, statuses, dates).
- [categories.csv](categories.csv): the per-category breakdown above.
- [findings.csv](findings.csv): every duplicate definition and unresolved reference, with its line.
- [agent-run.json](agent-run.json): the agent run, including its step-by-step progress log, rationales, gaps and status/date metrics.
