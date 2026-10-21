# swift-secp256k1

- Repository: <https://github.com/21-DOT-DEV/swift-secp256k1> at commit `a0bb7c72577403945ea7e6ac744aabae5b852650`
- SDD approach: Spec Kit; coding agent(s): Devin
- Markdown: 120 files, 16,408 lines, 779 KB
- Agent run: 71 of 80 tool calls, 160 s
- Project model: 275 IDs, 279 definitions, 459 references, 151 IDs with an authored status (56% of the 272 defined IDs)
- Findings: 14 duplicate definitions, 9 unresolved references (listed in [findings.csv](findings.csv))
- Precision: 30/30 (100.0%), see [../../precision/precision-sample.md](../../precision/precision-sample.md#swift-secp256k1)
- Extraction time: 0.5 s

## Agent summary

Measured configuration for eight engineering-record categories: 279 definitions, 459 references, 159 mapped status occurrences with no status conflicts, and 55 dates. Remaining findings are documented source ambiguities and schema limitations.

## ID categories

| Category | IDs | Defs | Refs | With status | Status values | Agent rationale |
|---|---:|---:|---:|---:|---|---|
| Functional requirements (`requirements`) | 49 | 49 | 12 | 0 |  | Retains the existing requirements key and replaces the unused REQ convention with FR IDs. Four specs define 49 functional requirements in leading bold list items (e.g. specs/001-spm-shared-code-plugin/spec.md:124). IDs restart per specs/* feature; only spec.md defines them. |
| Success criteria (`success`) | 28 | 28 | 0 | 0 |  | SC IDs identify 28 measurable success criteria in spec.md lists. The pattern includes the authored SC-002a suffix (specs/001-spm-shared-code-plugin/spec.md:149); each feature has its own scope. |
| User stories (`stories`) | 16 | 16 | 228 | 1 | Done=1 | User Story N headings define 16 user stories in the four feature specifications. US1-style task annotations resolve through a numeric ID template to User Story 1. Definitions are restricted to spec.md so task-section repetitions remain references; 228 references resolve. |
| Tasks (`tasks`) | 135 | 140 | 67 | 133 | Done=128; Open=5 | T-number IDs identify checkbox tasks in specs/*/tasks.md. Feature scopes prevent cross-feature collisions, checkbox-only definitions prevent dependency lists from redefining tasks, and suffixes are retained. All 140 definition occurrences are actual tasks. Seven IDs genuinely repeat within the test-architecture feature; removed workflow tasks have stale references. |
| Rollback blockers (`blockers`) | 3 | 3 | 0 | 0 |  | BL-001 through BL-003 identify explicit rollback-trigger conditions in specs/004-swift-crypto-update/spec.md:83–85. Leading list definitions and feature scoping yield three clean records. |
| Security test cases (`tests`) | 27 | 26 | 63 | 0 |  | PV, SV, SM, ZS, DE, NS, and IC IDs identify security test cases, not protocol or type names. Projects/README.md:49–76 supplies 26 current coverage definitions in its ID column; task design and feasibility tables remain references via definitionPaths. SM-003 is an acknowledged skipped case absent from that canonical coverage table; its five unresolved mentions are retained. |
| Roadmap phases (`phases`) | 13 | 13 | 89 | 13 | Done=2; Future=2; Planned=8; In progress=1 | Phase N, including Phase 9.5, identifies 13 roadmap phases. Only level-one headings in .specify/memory/roadmap/*.md define phases. The shared .specify/mem* scope admits roadmap references while excluding unrelated workflow/template phases; all 89 references resolve. |
| Features (`features`) | 4 | 4 | 0 | 4 | In progress=1; Done=2; Draft=1 | Feature Specification: title headings identify four named features in specs/*/spec.md. Keyword definitions capture names rather than branch numbers or version tokens and provide the correct attachment point for feature status metadata. |

## Statuses

Enabled task-checkbox statuses and the authored COMPLETE heading suffix, plus a bounded Status: regex that reads contiguous values inside multi-line metadata paragraphs. Mapped Done/Complete/Implemented together and normalized decorated roadmap Planned, Future, and In Progress values. Evaluation maps all 159 occurrences: 140 checkboxes, 18 paragraphs, and one heading; no unmapped values or conflicts. All four features, 13 phases, and 133 distinct defined task IDs have statuses. No status is inferred for records lacking a supported authored status site.

## Dates

Retained actual ISO-date headings and Created, Ratified, and Date fields; enabled Last Updated and Last Amended as snapshots. Removed zero-hit status-date and list-entry rules. Excluded Vendor (30 files), .devin (18), and .specify/templates (5). Inspected every enabled rule: 18 heading dates, 8 Created, 1 Ratified, 12 Date, 15 Last Updated, and 1 Last Amended. The ambiguous 2025-12-08/09 heading is deliberately excluded rather than reduced to a partial date.

## Gaps reported by the agent

Conventions the agent found but could not express with the configuration language.

- Task IDs T031–T037 are reused for distinct tasks within one feature. File/folder scopes cannot disambiguate these same-file records or their bare references; 14 duplicate occurrences remain. Examples: `specs/003-test-architecture/tasks.md:182`, `specs/003-test-architecture/tasks.md:209`, `specs/003-test-architecture/tasks.md:230`.
- The skipped CI workflow removed T013–T023 definitions but left range references. Four unresolved endpoint occurrences are preserved rather than inventing definitions. Examples: `specs/002-swift-version-compat/tasks.md:70`, `specs/002-swift-version-compat/tasks.md:129`, `specs/002-swift-version-compat/tasks.md:160`.
- Security test definitions span incompatible ID and Test ID tables; the latter also repeats exact IDs in feasibility summaries in the same file. The single table-column/definition-path configuration cannot combine these cleanly. SM-003 remains unresolved because it is omitted from current coverage and marked skipped elsewhere. Examples: `specs/003-test-architecture/tasks.md:123`, `specs/003-test-architecture/tasks.md:161`, `Projects/README.md:116`.
- Completion marks and SKIP/DEFERRED qualifiers embedded in list-item descriptions are not supported status sites. Checkbox statuses remain literal Done/Open rather than guessing an override from prose. Examples: `specs/003-test-architecture/spec.md:109`, `specs/003-test-architecture/tasks.md:24`, `specs/001-spm-shared-code-plugin/tasks.md:81`.
- Status paragraphs in task-section summaries and spike reports cannot update a story/task defined in another file. They remain separate evidence rather than overriding canonical definitions. Examples: `specs/002-swift-version-compat/tasks.md:72`, `specs/001-spm-shared-code-plugin/tasks.md:74`, `specs/003-test-architecture/spike-native-tests.md:5`.
- Dates in inline metadata after another field, version-history tables, and non-date-leading log entries are outside supported date sites. Examples: `specs/002-swift-version-compat/plan.md:3`, `.specify/memory/roadmap.md:170`, `.specify/memory/constitution.md:347`.
- The abbreviated date range 2025-12-08/09 cannot be represented faithfully by a single captured ISO date. Examples: `specs/001-spm-shared-code-plugin/research.md:166`.
- Research decisions use ordinary topic headings plus Decision paragraphs, risks use descriptive table cells, and acceptance scenarios use repeated ordered-list positions without stable IDs. No selective convention identifies these records without also matching unrelated sections or lists. Examples: `specs/004-swift-crypto-update/research.md:17`, `specs/004-swift-crypto-update/research.md:80`, `specs/001-spm-shared-code-plugin/spec.md:46`.

## Files

- [configuration.json](configuration.json): the configuration the agent submitted (categories, rules, definition sites, status sites, statuses, dates).
- [categories.csv](categories.csv): the per-category breakdown above.
- [findings.csv](findings.csv): every duplicate definition and unresolved reference, with its line.
- [agent-run.json](agent-run.json): the agent run, including its step-by-step progress log, rationales, gaps and status/date metrics.
