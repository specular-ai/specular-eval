# sleap-roots

- Repository: <https://github.com/talmolab/sleap-roots> at commit `6394cb996a70e7e3f9ebe9c17150a0c423fc0e18`
- SDD approach: OpenSpec; coding agent(s): Claude Code
- Markdown: 310 files, 68,424 lines, 4,376 KB
- Agent run: 77 of 80 tool calls, 272 s
- Project model: 2,366 IDs, 2,340 definitions, 1,104 references, 1,261 IDs with an authored status (54% of the 2,338 defined IDs)
- Findings: 4 duplicate definitions, 62 unresolved references (listed in [findings.csv](findings.csv))
- Precision: 30/30 (100.0%), see [../../precision/precision-sample.md](../../precision/precision-sample.md#sleap-roots)
- Extraction time: 2.8 s

## Agent summary

Measured configuration for OpenSpec requirements/scenarios/capabilities/archived changes, checklist and plan tasks, design decisions, cross-cutting concerns, review findings, and risks. Best draft: 2340 definitions, 1104 references, 1261 mapped statuses with zero conflicts, and 33 dates. Four duplicate occurrences and 62 unresolved references remain visible rather than inventing identities.

## ID categories

| Category | IDs | Defs | Refs | With status | Status values | Agent rationale |
|---|---:|---:|---:|---:|---|---|
| Requirements (`requirements`) | 116 | 116 | 158 | 0 |  | Preserves the existing requirements key, replacing unused REQ prefix with authored level-3 Requirement: names. Evidence: openspec/specs/html-prediction-viewer/spec.md:10 and capability specs throughout. Capability scopes join current specs and change deltas; onlyInScopes excludes tool examples. 116 definitions, no duplicates or unresolved references. |
| Scenarios (`scenarios`) | 649 | 649 | 0 | 0 |  | Level-4 Scenario: headings identify behavioral acceptance examples, parented by requirement and scoped by capability. Evidence: html-prediction-viewer/spec.md:14,23,27. 649 definitions with no duplicates. |
| Capabilities (`capability`) | 14 | 14 | 0 | 0 |  | Fourteen openspec/specs/<capability>/spec.md files define capability names; verified derived records rather than class/type names. |
| Changes (`changes`) | 47 | 47 | 0 | 47 | Archived=47 | Proposal-bearing folders identify 47 archived engineering changes. Derivation is restricted to openspec/changes, excluding .claude/commands/openspec/proposal.md. Archive semantics preserve actual archived state. |
| Checklist tasks (`tasks`) | 1263 | 1263 | 1 | 1214 | Done=910; Open=304 | Numbered checkbox entries such as 1.1 and hierarchical numbered task headings identify work items within tasks.md. Evidence: 2026-02-11-add-html-prediction-viewer/tasks.md:2 and 2026-10-04-add-wheat-sorghum-pipeline-cards/tasks.md:45. Levels 3–6 capture heading tasks while level-2 6.5 scope-expansion heading remains a reference. 1263 definitions, no duplicates/unresolved. |
| Plan tasks (`plan_tasks`) | 23 | 23 | 11 | 0 |  | Task N and Task N.N headings in the two docs/superpowers/plans files identify implementation tasks. File scopes prevent collisions and exclude command documentation examples. 23 definitions, 11 resolved references. |
| Design decisions (`decisions`) | 198 | 173 | 531 | 0 |  | D1, D5b, Decision 1, and Decision D1 identify design decisions in scoped change/design documents. Heading regex recognizes optional Decision before D IDs; list sites support authored decision logs. definitionPaths keeps proposal/task mentions from defining decisions. Evidence: viewer/design.md:30, foundation/design.md:26,135, tier3c brainstorm:194. Remaining ambiguity is explicitly reported. |
| Cross-cutting concerns (`constraints`) | 10 | 10 | 367 | 0 |  | CC-1 through CC-10 are project-wide cross-cutting engineering concerns defined exclusively in docs/circumnutation/roadmap.md:26–123. definitionPaths prevents restatements elsewhere becoming definitions; all 367 references resolve. |
| Critical review findings (`reviews`) | 23 | 22 | 26 | 0 |  | CR-1 and CR2-1 style headings identify critical-review findings in superpowers design documents, not priority or lint tokens. Evidence: 2026-06-10 tier3c design:211,215. 22 definitions; one cross-document CR2-2 mention remains unresolved. |
| Numbered risks (`risks`) | 12 | 12 | 0 | 0 |  | R1.–R6. heading IDs identify twelve explicit engineering risks in the temporal-CWT and Tier-1 design files (e.g. lines 522 and 890). Start-and-dot syntax deliberately distinguishes these from reviewer labels and compound review codes. |
| Named risks (`named_risks`) | 3 | 3 | 0 | 0 |  | Risk: headings identify three named risks in fix-viewer-multi-timepoint/design.md:116,119,122. Keyword heading recognition is restricted to OpenSpec design files. |
| Pipeline design decisions (`pipeline_decisions`) | 8 | 8 | 10 | 0 |  | The June-14 pipeline brainstorm has D1–D8 heading definitions and repeats them in a list summary at lines 279–292. A separate scoped category uses heading-only definitions so all eight summary mentions resolve without duplicate definitions. |

## Statuses

Enabled checkbox statuses: 910 Done and 304 Open. Mapped the 47 archive-derived Archived statuses. All 1261 captured values map, with zero conflicts and zero unmapped values. Retained literal Status: paragraph/list and Status-column sites; these do not falsely propagate document-level statuses to child records. Inspected without-status matches: 49 heading-based tasks have no direct authored status. BLOCKING/IMPORTANT review tags are severity, not lifecycle status. Roadmap icon rules were measured but omitted because bare row numbers also match constants and malformed pipe tables misalign status cells.

## Dates

Retained measured heading (21), Created (1), and Date (10) rules; added Completed (1). Heading rule excludes Workstream title citations to an older design date. Removed empty status-date, dated-list-entry, and Ratified rules; Last Updated/Last Amended remain absent because no real values were found. Excluded .claude and .serena tool/copied workflow material. All four retained rules were inspected and find real dates; total 33.

## Gaps reported by the agent

Conventions the agent found but could not express with the configuration language.

- Decision references qualified by another PR or source document cannot be resolved reliably by file/folder scopes alone; merging scopes would conflate unrelated D1–D8 records. Some brainstorm decisions have no supported definition site. Examples: `openspec/changes/archive/2026-04-21-add-multiple-dicot-plate-pipeline/proposal.md:62`, `openspec/changes/archive/2026-06-29-add-circumnutation-cli/design.md:5`, `docs/superpowers/specs/2026-06-14-add-circumnutation-pipeline-design.md:275`.
- Repeated decision definitions within one file cannot be distinguished by definitionPaths: D7's later provisional note repeats its list definition, and two different plotting headings use D5. Four duplicate occurrences remain. Examples: `docs/superpowers/specs/2026-06-10-add-circumnutation-tier3c-traits-design.md:459`, `openspec/changes/archive/2026-06-23-add-circumnutation-plots/design.md:159`, `openspec/changes/archive/2026-06-23-add-circumnutation-plots/design.md:209`.
- Document-level and mixed-workstream Status paragraphs do not belong to a defined child decision or requirement. They are not propagated or collapsed into a misleading single status. Examples: `docs/superpowers/specs/2026-04-23-timelapse-diff-and-tip-kinematics-design.md:6`, `docs/circumnutation/investigations/2026-06-10-tier3c-traveling-wave/report.md:6`, `.serena/memories/execution_ready_plan.md:3`.
- Roadmap row-number IDs collide with numeric constants in the same file, and unescaped pipes shift the Status column in two rows. Omitted this category rather than recognizing constants as records or prose as status. Examples: `docs/circumnutation/roadmap.md:53`, `docs/circumnutation/roadmap.md:144`, `docs/circumnutation/roadmap.md:145`.
- Unnumbered checklist steps do not define stable record IDs, and their completion cannot be aggregated into the enclosing Task heading's status by current status sites. Examples: `docs/superpowers/plans/2026-04-24-metadata-layer.md:20`, `docs/superpowers/plans/2026-04-24-metadata-layer.md:29`.
- Review labels B1/I1/N1 recur across reviewers and rounds within the same file, requiring contextual identity beyond a simple file scope. Free-text Resolution/Addressed prose is not a reliable lifecycle status site. Examples: `openspec/changes/archive/2026-05-22-add-circumnutation-synthetic-generator/design.md:735`, `openspec/changes/archive/2026-05-22-add-circumnutation-synthetic-generator/design.md:748`.
- The updated date embedded after a primary Date field is a separate snapshot; the retained field rule reads the primary date only. Arbitrary prose dates and filename dates are not treated as record milestones. Examples: `docs/superpowers/specs/2026-04-23-timelapse-diff-and-tip-kinematics-design.md:3`.
- Bare R1–R6 references are ambiguous with reviewer/round labels in the same documents. Risk heading definitions are captured, but broad bare-R references are intentionally not inferred. Examples: `openspec/changes/archive/2026-05-27-add-circumnutation-temporal-cwt-machinery/design.md:39`, `openspec/changes/archive/2026-05-27-add-circumnutation-temporal-cwt-machinery/design.md:522`.

## Files

- [configuration.json](configuration.json): the configuration the agent submitted (categories, rules, definition sites, status sites, statuses, dates).
- [categories.csv](categories.csv): the per-category breakdown above.
- [findings.csv](findings.csv): every duplicate definition and unresolved reference, with its line.
- [agent-run.json](agent-run.json): the agent run, including its step-by-step progress log, rationales, gaps and status/date metrics.
