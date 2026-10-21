# Specular: preliminary evaluation data

Extended results for a preliminary evaluation asking:

> Can the project map and cards adapt to projects built with different agentic programming approaches?

For each of six open-source projects, Specular's extractor agent derived a configuration (ID categories and recognition rules, plus status and date sites) from scratch. We then built each project model with that configuration and measured what it extracts.

## Projects

The projects come from SpecMine and use different SDD approaches and coding agents. The projects were selected at random, but requiring different coding agents and SDD approaches.

| Project | Repository (commit used) | SDD approach | Coding agent(s) | MD files | MD kLOC |
|---|---|---|---|---:|---:|
| [swift-secp256k1](projects/swift-secp256k1/README.md) | [21-DOT-DEV/swift-secp256k1](https://github.com/21-DOT-DEV/swift-secp256k1/tree/a0bb7c72577403945ea7e6ac744aabae5b852650) (`a0bb7c7`) | Spec Kit | Devin | 120 | 16.4 |
| [cache-data](projects/cache-data/README.md) | [63Klabs/cache-data](https://github.com/63Klabs/cache-data/tree/37c1f1fde6c791cea1b0c03658a996371ba471fc) (`37c1f1f`) | Kiro specs | Kiro | 249 | 70.9 |
| [oscar](projects/oscar/README.md) | [grycap/oscar](https://github.com/grycap/oscar/tree/af7c37e96b846ba06a0c4d93df5feddd3602103d) (`af7c37e`) | Spec Kit | Codex | 126 | 13.7 |
| [sleap-roots](projects/sleap-roots/README.md) | [talmolab/sleap-roots](https://github.com/talmolab/sleap-roots/tree/6394cb996a70e7e3f9ebe9c17150a0c423fc0e18) (`6394cb9`) | OpenSpec | Claude Code | 310 | 68.4 |
| [mssql-extension](projects/mssql-extension/README.md) | [hugr-lab/mssql-extension](https://github.com/hugr-lab/mssql-extension/tree/d4cbe170265a535c3087f7b817296795fda30c5b) (`d4cbe17`) | Spec Kit | Claude Code | 589 | 128.0 |
| [caro](projects/caro/README.md) | [wildcard/caro](https://github.com/wildcard/caro/tree/867323bf1e263194229bd3ebb46dbe53a2f2cb50) (`867323b`) | Spec Kit + Spec Kitty | Claude Code, Codex, Cursor, Copilot | 1,177 | 446.3 |

## Setup

- **Extractor agent:** Codex CLI with model gpt-6-astra at its default reasoning effort (low), run through Specular's agentic configuration discovery. Each project started from an empty configuration.
- **Agent environment:** a read-only sandbox with web search disabled and sub-agents off. The agent explores the project through Specular's tools: it surveys the files, reads them, proposes draft configurations, evaluates them against the whole project, and pages through matches, duplicates and unresolved references. It has a budget of 80 tool calls, and Specular submits the best draft evaluated during the run.
- **Measurement:** the submitted configuration ([`projects/<project>/configuration.json`](projects)) is applied to all Markdown files in the project with Specular's recognition pipeline. No human edited the configurations.

## Results

| Project | Cat./rules | IDs | Occ. (def/ref) | Status (%) | Duplicates | Unresolved | Precision | Time (s) | Agent calls / time (s) |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| swift-secp256k1 | 8/8 | 275 | 279/459 | 56 | 14 | 9 | 30/30 | 0.5 | 71 / 160 |
| cache-data | 11/14 | 1,952 | 1,943/800 | 62 | 4 | 13 | 30/30 | 1.8 | 71 / 205 |
| oscar | 7/7 | 436 | 436/381 | 51 | 0 | 0 | 30/30 | 0.4 | 60 / 145 |
| sleap-roots | 12/7 | 2,366 | 2,340/1,104 | 54 | 4 | 62 | 30/30 | 2.8 | 77 / 272 |
| mssql-extension | 8/8 | 4,256 | 4,236/6,594 | 56 | 4 | 40 | 30/30 | 4.1 | 78 / 244 |
| caro | 12/13 | 1,555 | 1,538/3,754 | 51 | 6 | 44 | 29/30 | 10.5 | 78 / 315 |
| **Total** | | **10,840** | **10,772/13,092** | | **32** | **168** | **179/180 (99.4%)** | | |

The machine-readable version, which has more columns, is in [results/summary.csv](results/summary.csv) and [results/summary.json](results/summary.json).

### Column definitions

- **Cat./rules:** ID categories and recognition rules in the derived configuration.
- **IDs:** distinct elements (category, ID and, for folder-local numbering, scope) that occur at least once.
- **Occ. (def/ref):** occurrences of those IDs, split into definitions (where an element is written down) and references (where it is cited).
- **Status (%):** the share of defined IDs with an authored status, i.e. one written in the documents (a checkbox, a `Status:` field, a status column), which their cards show. No status is inferred.
- **Duplicates / Unresolved:** occurrences reported as a second definition of the same ID, and references with no definition. Each one is listed in `projects/<project>/findings.csv`. Many are genuine authoring issues in the project, such as reused task numbers or citations of deleted tasks. The agent's own explanations are in the "Gaps" section of each project page.
- **Precision:** manually judged correct occurrences in a random sample of 30 per project. See [precision/](precision/precision-sample.md).
- **Time:** median of three runs of recognition over the in-memory documents (parsing, matching, indexing, statuses and dates), excluding file loading. Later changes are processed incrementally.
- **Agent calls / time:** tool calls used out of the budget of 80, and the wall-clock duration of the agent run.

## Contents

```
README.md                       this file
results/summary.csv|json        one row per project (the table above plus more columns)
precision/precision-sample.md   the 180 judged occurrences, with source line and verdict
precision/precision-sample.csv  the same, as a table
projects/<project>/
  README.md                     overview: categories with the agent's rationale, statuses, dates, gaps
  configuration.json            the configuration the agent derived
  categories.csv                per category: IDs, definitions, references, statuses, findings
  findings.csv                  every duplicate definition and unresolved reference
  agent-run.json                the agent run: progress log, rationales, gaps, status and date metrics
```

## Notes and limitations

- We measured precision, not recall: there is no ground truth of all the elements in these projects.
- The sample's only error is in caro: the row for sub-requirement `NFR-002.3` was read as a reference to its parent `NFR-002`.
- In caro, the prototype's 2,000-text-file explorer limit was reached, and two specification files that are not UTF-8 were skipped.
- Templates and the tools' own scaffolding (e.g., `.specify/templates`) are part of the repositories. The agents excluded them through scopes and definition paths, as described in each project's rationale.
