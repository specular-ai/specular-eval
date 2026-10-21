# mssql-extension

- Repository: <https://github.com/hugr-lab/mssql-extension> at commit `d4cbe170265a535c3087f7b817296795fda30c5b`
- SDD approach: Spec Kit; coding agent(s): Claude Code
- Markdown: 589 files, 128,004 lines, 6,231 KB
- Agent run: 78 of 80 tool calls, 244 s
- Project model: 4,256 IDs, 4,236 definitions, 6,594 references, 2,368 IDs with an authored status (56% of the 4,234 defined IDs)
- Findings: 4 duplicate definitions, 40 unresolved references (listed in [findings.csv](findings.csv))
- Precision: 30/30 (100.0%), see [../../precision/precision-sample.md](../../precision/precision-sample.md#mssql-extension)
- Extraction time: 4.1 s

## Agent summary

Measured configuration for the project's Spec Kit records and numbered design notes: 4,236 definitions, 6,594 references, 2,368 mapped status occurrences, and 327 dates. Feature-local scopes and canonical definition paths exclude templates, technical tokens, and repeated summaries. Four duplicate occurrences and 40 unresolved references remain visible rather than being hidden with speculative rules.

## ID categories

| Category | IDs | Defs | Refs | With status | Status values | Agent rationale |
|---|---:|---:|---:|---:|---|---|
| Requirements (`requirements`) | 901 | 893 | 577 | 0 |  | Retains the existing requirements key and recognizes FR-/NFR- functional and nonfunctional requirements. Evidence: specs/001-attach-connection-validation/spec.md:86-95 and specs/045-named-instance-resolution/spec.md:124-127. IDs restart per feature; only canonical spec.md definitions and unordered requirement lists are used. 893 definitions; no duplicates. |
| Success criteria (`success`) | 394 | 391 | 386 | 0 |  | SC-nnn identifies measurable acceptance outcomes, e.g. specs/001-attach-connection-validation/spec.md:109-113. Feature scopes and spec.md definition paths prevent checklist and plan summaries from redefining outcomes. 391 definitions, no duplicates. |
| User stories (`stories`) | 264 | 261 | 3761 | 0 |  | User Story n headings identify user-facing scenarios, e.g. specs/001-attach-connection-validation/spec.md:10. US1 and US-001 forms normalize through an integer ID template. Most definitions belong in spec.md; task-phase headings are canonical in the observed 017, 047 and 068 exceptions. 261 definitions, no duplicates. |
| Tasks (`tasks`) | 2319 | 2317 | 1385 | 2280 | Done=1453; Open=825; Deferred=2 | Tnnn and suffix forms identify implementation tasks in tasks.md, e.g. specs/068-login-routing-unification/tasks.md:48 and :96. Checkbox-only list definitions preserve dependency mentions as references; heading definitions support specs/045-named-instance-resolution/tasks.md:30. File scopes exclude T1 test-case labels in other documents. 2,317 definitions, no duplicates. |
| Design decisions (`decisions`) | 143 | 139 | 367 | 7 | Done=6; Closed=1 | D-number, optional letter suffix, and Decision n headings identify decisions and design deliverables. Evidence includes specs/068-login-routing-unification/spec.md:70 and specs/001-attach-connection-validation/research.md:67. Explicit observed feature scopes avoid percent-encoded D0/D1 bytes; canonical spec/research sites plus the observed CI plan exception retain actual definitions. 139 definitions. |
| Research findings (`research`) | 144 | 144 | 113 | 0 |  | R-number headings identify research questions/findings, e.g. specs/068-login-routing-unification/research.md:11 and specs/001-mssql-transactions/research.md:6. Restricted to the 17 observed feature scopes with canonical research.md definitions, preventing SQL Server 2008 R2 and unrelated optimization labels from matching. 144 definitions, no unresolved references or duplicates. |
| Contracts (`contracts`) | 4 | 4 | 5 | 0 |  | C1-C4 identify the login-routing interface contracts in specs/068-login-routing-unification/contracts/tds_connection_routing.md:12, :40, :105 and :142. Scoped to that feature to exclude unrelated benchmark strategy C2. Four definitions and five resolved references. |
| Feature specifications (`features`) | 87 | 87 | 0 | 81 | Draft=60; Done=12; Closed=4; Ready=1; Proposed=1; In progress=2; Revised=1 | Each specs/<feature>/spec.md is a feature specification named by its folder, covering both Feature Specification headings and newer Spec nnn headings. Evidence: specs/001-attach-connection-validation/spec.md:1 and specs/068-login-routing-unification/spec.md:1. 87 derived records. |

## Statuses

Reads the leading contiguous authored status phrase from Status fields even when metadata shares a paragraph, avoiding captures across Markdown formatting. Enables explicit DONE/CLOSED heading tags and task checkbox markers x/X=Done, blank=Open, -=In progress, ~=Deferred. Observed Draft, Implemented, Complete, CLOSED, EXECUTED AND CLOSED, ready, PROPOSED, revised and in progress values map without ambiguity. Measurement: 2,368/2,368 occurrences mapped, zero conflicts; 81/87 feature specifications and 2,280/2,317 tasks have statuses. Missing-status samples include genuinely unmarked task headings; no status is inferred from priorities.

## Dates

Retains measured ISO dates in headings, dated list entries, Created and Date fields, and reads ISO dates immediately included in captured status phrases without requiring 'on'. Inspected matches include release headings, benchmark milestones and the 2026-10-08 Fabric probe entry. Counts: status 5, list entry 1, heading 91, Created 117, Date 113. Omits the zero-result Ratified rule and inactive Last Updated/Last Amended rules; excludes copied website/versioned_docs, tool skills, and templates. No active rule is empty.

## Gaps reported by the agent

Conventions the agent found but could not express with the configuration language.

- References qualified in prose by another spec number cannot select another feature's ID scope. Some unresolved references are cross-feature citations; others describe removed or renumbered requirements. Examples: `specs/044-codec-consolidation/plan.md:117`, `specs/067-dml-staging/spec.md:62`, `specs/052-thread-safe-catalog-entries/spec.md:15`.
- Historical original headings and completed updates repeat the same decision within one file. Definition paths cannot distinguish these sections; four duplicate occurrences for D3/D5 remain instead of silently suppressing history. Examples: `specs/059-staged-path-test-coverage/spec.md:166`, `specs/059-staged-path-test-coverage/spec.md:184`, `specs/059-staged-path-test-coverage/spec.md:242`.
- Mixed list-based design deliverables and prose summaries cannot be reliably separated with the available list definition site. A heading jointly defining D2 / D3 also cannot define both through a single named ID capture. Conservative heading-based decision recognition leaves these forms uncovered. Examples: `specs/056-chunk-analyzer-dictionary/spec.md:116`, `specs/084-metadata-query-shapes/spec.md:253`, `specs/064-columnar-write-gaps/spec.md:272`.
- Tasks written in fenced task-order blocks are ignored by the analyzer. Other spec-local T labels mix tests, investigations and tasks, so the task category is restricted to tasks.md. A combined checkbox item cannot define both task IDs. Examples: `specs/055-read-staging-and-batch-decode/spec.md:612`, `specs/058-read-framing/spec.md:84`, `specs/045-type-codec-consolidation/tasks.md:242`.
- Anonymous acceptance scenarios, risk bullets and quality-checklist items have no stable ID or keyword-heading identity. They are not approximated with generic numbered-list or arbitrary prose rules. Examples: `specs/001-attach-connection-validation/spec.md:20`, `specs/068-login-routing-unification/spec.md:166`, `specs/001-attach-connection-validation/checklists/requirements.md:10`.
- Dates in inline multi-field metadata, month-only dates, and status narrative beyond the safely captured contiguous status phrase are not all readable by the available sites. Snapshot Last Amended and Ratified share the Version line and yielded no field matches; no inaccurate approximation is proposed. Examples: `.specify/memory/constitution.md:148`, `feature-spec/refactoring-v0.2.md:5`, `specs/059-staged-path-test-coverage/spec.md:3`.
- Task-specific narrative dates embedded after checkbox status markers are not status dates: the checkbox supplies only the marker's mapped value. Examples: `specs/044-codec-consolidation/tasks.md:167`.

## Files

- [configuration.json](configuration.json): the configuration the agent submitted (categories, rules, definition sites, status sites, statuses, dates).
- [categories.csv](categories.csv): the per-category breakdown above.
- [findings.csv](findings.csv): every duplicate definition and unresolved reference, with its line.
- [agent-run.json](agent-run.json): the agent run, including its step-by-step progress log, rationales, gaps and status/date metrics.
