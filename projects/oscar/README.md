# oscar

- Repository: <https://github.com/grycap/oscar> at commit `af7c37e96b846ba06a0c4d93df5feddd3602103d`
- SDD approach: Spec Kit; coding agent(s): Codex
- Markdown: 126 files, 13,700 lines, 611 KB
- Agent run: 60 of 80 tool calls, 145 s
- Project model: 436 IDs, 436 definitions, 381 references, 223 IDs with an authored status (51% of the 436 defined IDs)
- Findings: 0 duplicate definitions, 0 unresolved references (listed in [findings.csv](findings.csv))
- Precision: 30/30 (100.0%), see [../../precision/precision-sample.md](../../precision/precision-sample.md#oscar)
- Extraction time: 0.4 s

## Agent summary

Recognize feature-scoped Spec Kit records across five features: 436 definitions and 381 references, with zero duplicates or unresolved references; 223 mapped task statuses and 18 dates. Exclude template examples and technical tokens.

## ID categories

| Category | IDs | Defs | Refs | With status | Status values | Agent rationale |
|---|---:|---:|---:|---:|---|---|
| Requirements (`requirements`) | 116 | 116 | 1 | 0 |  | Retains the existing requirements key. FR-nnn and NFR-nnn identify functional and non-functional requirements in specs/*/spec.md (e.g. metrics lines 101 and 149). Lists define them; specs/* folder scopes distinguish reused numbers. Measured 116 definitions and one resolved research reference. |
| Success Criteria (`success`) | 32 | 32 | 0 | 0 |  | SC-nnn identifies measurable success criteria in specification lists, e.g. metrics spec.md:229. Measured 32 definitions; restricted to feature scopes and definitionPaths specs/*/spec.md. |
| User Stories (`stories`) | 18 | 18 | 314 | 0 |  | User Story n headings define 18 stories in spec.md; US1-style task tags alias to User Story 1 using the numeric ID template. 314 references resolve. Definitions restricted to spec.md prevent task phase headings and checklist summaries from redefining stories; P1/P2/P3 are priorities, not IDs. |
| Tasks (`tasks`) | 223 | 223 | 66 | 223 | Done=218; Open=5 | T001-style IDs identify implementation tasks at the start of checkbox lists in specs/*/tasks.md, e.g. bucket quotas tasks.md:17. Checkbox-only definitions preserve dependency mentions as references. Measured 223 definitions and 66 resolved references, with per-feature scope. |
| Design Decisions (`decisions`) | 31 | 31 | 0 | 0 |  | Decision n headings identify numbered research decisions, e.g. bucket quotas research.md:3 and deployment research.md:19. Heading-only definitions and research definitionPaths avoid treating Decision prose fields as additional records. Measured 31 definitions. |
| Features (`features`) | 5 | 5 | 0 | 0 |  | Feature Specification: <name> top-level headings identify five feature specifications. Keyword headings extract authored feature names, restricted to specs/*/spec.md; templates are excluded through onlyInScopes. |
| Named Design Decisions (`named-decisions`) | 11 | 11 | 0 | 0 |  | Decision: <name> headings identify 11 federation design decisions, e.g. research.md:5 and :12. Keyword heading extraction preserves names containing inline code without partial-token references. This category complements numbered decisions. |

## Statuses

Enabled checkbox status extraction: x/X maps to Done and empty boxes to Open; 218 Done and 5 Open, no unmapped values, conflicts, or tasks without a status. Retained the standard Status: paragraph site after literal and regex experiments failed to attach the five feature Draft fields. No status is inferred for requirements, stories, criteria, or decisions that lack authored lifecycle values. Draft and In progress mappings remain available.

## Dates

Measured four dated Session headings, eight Created fields, five plan dates inside Branch metadata lines, and one constitution ratification date inside its Version line. Composite-field regexes specifically capture the Date or Ratified value. Removed unproductive default status/list-entry rules and disabled empty standalone Date/Ratified and constitution amendment rules. Templates are excluded; searches of docs/examples/root guidance found no further actual record date conventions or vendored date sources.

## Gaps reported by the agent

Conventions the agent found but could not express with the configuration language.

- Feature specifications state Status: Draft within the multi-line introductory metadata paragraph, but tested literal and regex paragraph sites attach no status to these keyword-defined features. Preserve this as an analyzer/configuration gap rather than infer statuses for child records. Examples: `specs/001-metrics-collection/spec.md:5`, `specs/006-volumes/spec.md:5`, `specs/007-bucket-quotas/spec.md:5`.
- The constitution's Last Amended snapshot shares a Version field line with Ratified. The additional snapshot rule produced zero dates alongside the ratification rule and is disabled; that separate date meaning remains unrepresented. Examples: `.specify/memory/constitution.md:76`.
- Validation dates embedded at the end of prose/list items are outside the available date sites: these are neither leading dated entries nor labelled fields, headings, or record statuses. Examples: `specs/006-volumes/quickstart.md:184`, `specs/006-volumes/quickstart.md:185`.
- Acceptance scenarios use ordered Given/When/Then lists whose numbering restarts under each story; they have no stable token IDs or keyword-named scenario headings. Do not turn ordinary ordered-list numbering into speculative record IDs. Examples: `specs/007-bucket-quotas/spec.md:41`, `specs/007-bucket-quotas/spec.md:77`.
- Quality checklists contain unnamed checkbox items rather than CHK IDs (CHK IDs occur only in templates). Checkbox statuses cannot be attached without defining stable records. Examples: `specs/006-volumes/checklists/requirements.md:10`.
- Task range notation resolves explicit endpoints but does not expand implicit interior IDs, such as T001-T003. Examples: `specs/001-metrics-collection/tasks.md:204`.

## Files

- [configuration.json](configuration.json): the configuration the agent submitted (categories, rules, definition sites, status sites, statuses, dates).
- [categories.csv](categories.csv): the per-category breakdown above.
- [findings.csv](findings.csv): every duplicate definition and unresolved reference, with its line.
- [agent-run.json](agent-run.json): the agent run, including its step-by-step progress log, rationales, gaps and status/date metrics.
