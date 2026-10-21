# cache-data

- Repository: <https://github.com/63Klabs/cache-data> at commit `37c1f1fde6c791cea1b0c03658a996371ba471fc`
- SDD approach: Kiro specs; coding agent(s): Kiro
- Markdown: 249 files, 70,946 lines, 3,084 KB
- Agent run: 71 of 80 tool calls, 205 s
- Project model: 1,952 IDs, 1,943 definitions, 800 references, 1,208 IDs with an authored status (62% of the 1,941 defined IDs)
- Findings: 4 duplicate definitions, 13 unresolved references (listed in [findings.csv](findings.csv))
- Precision: 30/30 (100.0%), see [../../precision/precision-sample.md](../../precision/precision-sample.md#cache-data)
- Extraction time: 1.8 s

## Agent summary

Measured configuration for Kiro engineering records: 1,943 definitions, 800 references, 1,208 mapped task statuses and 53 dates. Eleven categories; 4 duplicate occurrences and 13 unresolved references remain explicitly documented. Technical tokens, versions, runtime names and priorities are excluded.

## ID categories

| Category | IDs | Defs | Refs | With status | Status values | Agent rationale |
|---|---:|---:|---:|---:|---|---|
| Requirements (`requirements`) | 280 | 280 | 76 | 0 |  | Retains the existing requirements key. Requirement N headings define feature requirements, e.g. force-refresh-option/requirements.md. IDs restart per feature folder; definitionPaths prevents report summaries becoming definitions. Decimal acceptance-criterion citations are not truncated into whole requirement IDs. |
| Correctness Properties (`properties`) | 343 | 335 | 586 | 0 |  | Property N and dotted property citations identify correctness guarantees. design.md headings and colon-led paragraphs are definition sites (cache-bool-test-fix/design.md:74 and force-refresh-option/design.md:124). Feature scopes separate reused numbers; summaries in tasks/reports remain references. 335 definitions measured. |
| Tasks (`tasks`) | 1216 | 1216 | 0 | 1208 | Done=1192; Open=13; In progress=3 | Numbered checkbox items and numbered task headings define implementation work, e.g. force-refresh-option/tasks.md:9 and client-request-validation-fixes/tasks.md:5. File scopes and onlyInScopes prevent unrelated document section numbers becoming tasks. 1,216 definitions, zero duplicates or unresolved references. |
| Clarifying Questions (`questions`) | 28 | 28 | 1 | 0 |  | Qn and Qn.m identify clarification questions in SPEC-QUESTIONS.md and the Powertools recommendations file. Security-fixes/SPEC-QUESTIONS.md:15 uses Q1.1 in a colon-led paragraph. File scopes reflect local numbering; 28 definitions and one resolved reference. |
| Workstreams (`workstreams`) | 17 | 16 | 70 | 0 |  | WS-n identifies implementation workstreams in PLAN.md, with heading definitions in the SSM SDK plan:93 and list definitions in the Node 26 plan:90. Punctuated title forms define records; reference-only ID templates join other WS-n mentions without treating the implementation-order summary as new definitions. 16 definitions, no duplicates. |
| Remediations (`remediations`) | 7 | 7 | 9 | 0 |  | R1–R7 are recommended security remediations, not requirements or risk IDs, in the SSM SDK FINDINGS.md:170–245. Definition paths isolate the findings report while folder scope resolves PLAN.md references. Seven definitions, all references resolved. |
| Planned Changes (`plannedChanges`) | 11 | 11 | 11 | 0 |  | D1–D7 and X1–X4 identify proposed documentation changes and code fixes in cache-key-generation-docs/PLAN.md ID tables at lines 164 and 176. Restricted to that plan; 11 definitions and 11 resolved references. |
| Findings (`findings`) | 4 | 4 | 10 | 0 |  | F1–F4 identify empirically observed cache-key drift findings in cache-key-generation-docs/PLAN.md:32,57,63,68. Emphasized dash-led paragraphs define these records. Four definitions with ten resolved references. |
| Security Property Assertions (`assertions`) | 12 | 12 | 37 | 0 |  | Property A1–A12 identify security correctness assertions in fix-ssm-param-security/design.md:310–332. A1-style short references map to Property A1 with ID templates. Scoped to the security feature to avoid unrelated A tokens. Twelve definitions and 37 resolved references. |
| Risks (`risks`) | 20 | 20 | 0 | 0 |  | Risk N headings identify documented risks with impact, mitigation and detection sections, e.g. test-migration-phase-5/design.md:953. File scopes confined to design.md avoid numbering in other documentation. All 20 inspected definitions are risk records. |
| Scenarios (`scenarios`) | 14 | 14 | 0 | 0 |  | Scenario N headings identify error-handling and migration scenarios with problem/solution descriptions, e.g. test-migration-phase-4/design.md:303. Restricted to design files with independent file scopes. All 14 inspected definitions are scenario records. |

## Statuses

Enable checkbox status sites and map x/X to Done, blank to Open, and hyphen to In progress. Evaluation finds 1,192 Done, 13 Open and 3 In progress: all 1,208 values map, with zero conflicts. Eight heading-defined tasks have no authored status; inspected without-status matches and did not infer completion from child tasks. Keep literal Status paragraphs (including list fields) and Status table sites available; none attach to the selected records. No speculative mappings from prose or answer text.

## Dates

Retain ISO dates in headings (44) and Date fields (6); add Review Date (1) and Report Generated (2), each inspected with list_matches. Remove empty status-date, list-entry, Created, Ratified and Last Updated rules rather than enabling ineffective extraction. Imported GitHub issue copies are explicitly excluded. No vendored Markdown was identified. Total 53 real release/report/status-heading dates; natural-language dates and lifecycle table cells are documented as gaps.

## Gaps reported by the agent

Conventions the agent found but could not express with the configuration language.

- Acceptance criteria use ordered-list numbering beneath Requirement headings, with citations such as Requirements 1.1 or Req 1.2; the schema cannot synthesize hierarchical IDs from the enclosing requirement plus the ordered-list ordinal. Bugfix paragraphs also use bare decimal IDs without the required definition delimiter. These are not approximated as their parent requirement. Examples: `.kiro/specs/1-3-14-force-refresh-option/tasks.md:15`, `.kiro/specs/1-3-10-cache-bool-test-fix/bugfix.md:17`, `.kiro/specs/1-3-16-fix-ssm-param-security/design.md:310`.
- Some questions are bold paragraph titles using Q1. followed by prose, rather than a supported colon/dash definition site. PLAN.md and FINDINGS.md question sets are omitted rather than manufacturing definitions or merging independently numbered questions. Examples: `.kiro/specs/1-4-0-cache-key-generation-docs/PLAN.md:215`, `.kiro/specs/1-3-16-fully-implement-ssm-parameter-store-and-secrets-manager-sdk/FINDINGS.md:258`.
- Two correctness properties are repeated as paragraph summaries within the same design file, creating four duplicate occurrences. The schema cannot prefer heading definitions only in this file while retaining paragraph definitions used by other design files within the same category. Examples: `.kiro/specs/1-3-6-in-memory-cache/design.md:331`, `.kiro/specs/1-3-6-in-memory-cache/design.md:529`, `.kiro/specs/1-3-6-in-memory-cache/design.md:555`.
- Thirteen references name properties/workstreams from other feature scopes or pre-consolidation property numbers. Text does not provide a uniform scope-qualified ID convention, so these remain unresolved rather than linking to an unrelated local ID. Examples: `.kiro/specs/1-3-16-fix-ssm-param-security/design.md:324`, `.kiro/specs/1-3-9-appconfig-async-init-optimization/design.md:245`, `.kiro/specs/1-4-0-convert-aws-to-lazy-accessors/SPEC.md:99`.
- Document-level statuses and free-text answers do not state an individual selected record's lifecycle status. They cannot safely be propagated to all requirements/tasks or converted into a lifecycle state. Examples: `.kiro/specs/1-3-16-fully-implement-ssm-parameter-store-and-secrets-manager-sdk/PLAN.md:5`, `.kiro/specs/1-3-10-test-migration-phase-4/baseline-validation.md:4`, `.kiro/specs/1-3-15-powertools-integration/recommendations.md:234`.
- Natural-language calendar dates require normalization beyond regex capture; ISO-only rules leave these dates unrecognized. Examples: `.kiro/specs/1-3-10-test-migration-phase-4/final-validation-report.md:198`, `.kiro/specs/1-3-6-documentation-enhancement/COMPLETION-SUMMARY.md:196`.
- Runtime lifecycle dates and Last Checked snapshots live in table cells; the date schema has no table-column site, and some dates are explicitly approximate. They are not treated as heading or field dates. Examples: `.kiro/steering/cache-data-node-support.md:23`, `.kiro/steering/cache-data-node-support.md:24`.

## Files

- [configuration.json](configuration.json): the configuration the agent submitted (categories, rules, definition sites, status sites, statuses, dates).
- [categories.csv](categories.csv): the per-category breakdown above.
- [findings.csv](findings.csv): every duplicate definition and unresolved reference, with its line.
- [agent-run.json](agent-run.json): the agent run, including its step-by-step progress log, rationales, gaps and status/date metrics.
