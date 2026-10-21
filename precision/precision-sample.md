# Precision sample

30 occurrences (definitions and references) drawn per project with a seeded pseudo-random generator (seed 42) from all occurrences the derived configuration extracts. Each was judged manually: correct means the occurrence denotes an element of the stated category, with the right ID and the right kind (definition or reference).

| Project | Correct | Precision |
|---|---:|---:|
| swift-secp256k1 | 30/30 | 100.0% |
| cache-data | 30/30 | 100.0% |
| oscar | 30/30 | 100.0% |
| sleap-roots | 30/30 | 100.0% |
| mssql-extension | 30/30 | 100.0% |
| caro | 29/30 | 96.7% |
| **Total** | **179/180** | **99.4%** |

## swift-secp256k1

| # | Correct | Kind | ID | Category | Location | Line text |
|---:|:---:|---|---|---|---|---|
| 1 | yes | reference | `User Story 1` | stories | `specs/001-spm-shared-code-plugin/tasks.md:241` | 3. **Phase 3**: Implement plugin (US1 - core functionality) |
| 2 | yes | reference | `User Story 2` | stories | `specs/001-spm-shared-code-plugin/tasks.md:81` | - [ ] T016 [US2] DEFERRED - Implement Windows file copy using robocopy or xcopy |
| 3 | yes | reference | `T030` | tasks | `specs/003-test-architecture/tasks.md:384` | - Verification tasks (T020, T026, T030, T035) confirm each story works before moving on |
| 4 | yes | reference | `User Story 2` | stories | `specs/003-test-architecture/tasks.md:71` | ## Phase 4: User Story 2 - Wycheproof Edge Case Vectors (Priority: P2) |
| 5 | yes | reference | `SM-003` | tests | `specs/003-test-architecture/tasks.md:161` | \| SM-003 \| ❌ Not exposed \| ⚠️ **Gap** \| `secp256k1_ecdsa_signature_normalize` not wrapped — **skip or add wrapper** \| |
| 6 | yes | reference | `User Story 1` | stories | `specs/003-test-architecture/tasks.md:54` | ## Phase 3: User Story 1 - BIP-340 Schnorr Test Vectors (Priority: P1) 🎯 MVP |
| 7 | yes | reference | `User Story 2` | stories | `specs/001-spm-shared-code-plugin/tasks.md:82` | - [ ] T017 [US2] DEFERRED - Add Windows CI job to verify build |
| 8 | yes | definition | `FR-007` | requirements | `specs/002-swift-version-compat/spec.md:86` | - **FR-007**: Bootstrap script MUST use binary search to efficiently find minimum Swift version |
| 9 | yes | definition | `IC-004` | tests | `Projects/README.md:74` | \| \| IC-004 \| Reject x-overflow (x=p+1) \| |
| 10 | yes | definition | `SC-007` | success | `specs/003-test-architecture/spec.md:140` | - **SC-007**: Test targets run successfully on all platform destinations defined in Projects/Project.swift |
| 11 | yes | definition | `T036` | tasks | `specs/003-test-architecture/tasks.md:229` | - [x] T036 [P] [US5] Add MuSig2VectorTests unit test target to `Projects/Project.swift` with sources from `Projects/Sources/TestShared/**` and `Projects/Sources/MuSig2VectorTests/**`, resources from ` |
| 12 | yes | reference | `User Story 2` | stories | `specs/004-swift-crypto-update/tasks.md:182` | \| **User Story 2 Tasks** \| 14 \| |
| 13 | yes | reference | `User Story 2` | stories | `specs/003-test-architecture/tasks.md:86` | **Checkpoint**: User Story 2 complete — Wycheproof edge case validation works independently |
| 14 | yes | reference | `FR-006` | requirements | `specs/002-swift-version-compat/workflow-schema.md:113` | - PR requires human approval before merge (FR-006) |
| 15 | yes | definition | `T015` | tasks | `specs/004-swift-crypto-update/tasks.md:84` | - [x] T015 [CHECKPOINT] **MANUAL VERIFICATION**: Confirm build succeeds before proceeding to tests |
| 16 | yes | definition | `T020` | tasks | `specs/003-test-architecture/tasks.md:65` | - [x] T020 [US1] **VERIFY**: Run `tuist test SchnorrVectorTests` and confirm all BIP-340 vectors pass with verbose output on any failure |
| 17 | yes | definition | `T014` | tasks | `specs/001-spm-shared-code-plugin/tasks.md:63` | - [x] T014 [US1] Implement SharedSourcesPlugin with `prebuildCommand` using rsync in `Plugins/SharedSourcesPlugin/Plugin.swift` |
| 18 | yes | reference | `User Story 1` | stories | `specs/003-test-architecture/tasks.md:348` | 2. Add US1 → BIP-340 Schnorr validation (MVP!) |
| 19 | yes | reference | `User Story 4` | stories | `specs/003-test-architecture/tasks.md:288` | \| US2 (P2) \| Phase 2 complete \| US1, US3, US4, US5 (after Phase 2) \| ✅ Complete \| |
| 20 | yes | reference | `User Story 1` | stories | `specs/003-test-architecture/tasks.md:287` | \| US1 (P1) \| Phase 2 complete \| US2, US3, US4, US5 (after Phase 2) \| ✅ Complete \| |
| 21 | yes | reference | `Phase 4` | phases | `.specify/memory/roadmap/phase-9.5-cli-tool.md:46` | 1. **Core CLI** — after Phase 4 encodings (address/npub output) |
| 22 | yes | definition | `T031` | tasks | `specs/003-test-architecture/tasks.md:209` | - [x] T031 [US4] Native test target `libsecp256k1Tests` configured in `Projects/Project.swift` as commandLineTool with subtree extraction for tests.c and precomputed tables |
| 23 | yes | reference | `User Story 3` | stories | `specs/003-test-architecture/tasks.md:287` | \| US1 (P1) \| Phase 2 complete \| US2, US3, US4, US5 (after Phase 2) \| ✅ Complete \| |
| 24 | yes | definition | `IC-001` | tests | `Projects/README.md:71` | \| **Invalid Curve Attack** \| IC-001 \| Reject truncated keys \| |
| 25 | yes | reference | `IC-002` | tests | `specs/003-test-architecture/tasks.md:168` | \| IC-001..IC-002 \| `sharedSecretFromKeyAgreement` \| ✅ \| Uses `secp256k1_ecdh` internally \| |
| 26 | yes | reference | `User Story 2` | stories | `specs/004-swift-crypto-update/tasks.md:99` | - [x] T017 [US2] Verify Linux build (Docker or CI) |
| 27 | yes | reference | `User Story 3` | stories | `specs/003-test-architecture/tasks.md:190` | **Checkpoint**: User Story 3 complete — Security regression coverage works independently |
| 28 | yes | definition | `T021` | tasks | `specs/001-spm-shared-code-plugin/tasks.md:99` | - [x] T021 [US3] Verified `Sources/P256K/` contains only `ASN1/` and `swift-crypto/` |
| 29 | yes | definition | `SC-003` | success | `specs/004-swift-crypto-update/spec.md:99` | - **SC-003**: Package builds successfully on Linux |
| 30 | yes | reference | `T001` | tasks | `specs/002-swift-version-compat/tasks.md:157` | \| 1 \| T001-T003 \| Setup verification \| |

## cache-data

| # | Correct | Kind | ID | Category | Location | Line text |
|---:|:---:|---|---|---|---|---|
| 1 | yes | definition | `Property 12` | properties | `.kiro/specs/1-3-9-appconfig-async-init-optimization/design.md:316` | ### Property 12: Selective Initialization |
| 2 | yes | definition | `Property 6` | properties | `.kiro/specs/1-3-8-security-fixes/design.md:485` | ### Property 6: Backwards Compatibility |
| 3 | yes | reference | `Property 11` | properties | `.kiro/specs/1-3-8-test-migration-phase-2/tasks.md:272` | - [x] 6.5 Create property test for Jest file naming convention (Property 11) |
| 4 | yes | definition | `2.1` | tasks | `.kiro/specs/1-4-0-property-test-generator-preconditions/tasks.md:117` | - [x] 2.1 Implement the audit over the registry |
| 5 | yes | reference | `Property 6` | properties | `.kiro/specs/1-3-10-test-migration-phase-5/tasks.md:326` | \| Property 6 \| Hash Function Determinism \| utils-property-tests.jest.mjs \| 5.5 \| |
| 6 | yes | definition | `X3` | plannedChanges | `.kiro/specs/1-4-0-cache-key-generation-docs/PLAN.md:178` | \| X3 \| Expose `useToolsHash` in `Cache.info()` \| Additive, low risk. Closes F4 \| |
| 7 | yes | definition | `Requirement 4` | requirements | `.kiro/specs/1-3-8-security-fixes/requirements.md:57` | ### Requirement 4: Security-Focused Testing |
| 8 | yes | definition | `Property 12` | properties | `.kiro/specs/1-3-10-validation-parameter-extraction-fix/design.md:349` | Property 12: Preservation - Single-Parameter Validation Interface |
| 9 | yes | definition | `1.4` | tasks | `.kiro/specs/1-3-10-new-response-format-method/tasks.md:34` | - [x] 1.4 Write property test: format() value preservation (Property 4) |
| 10 | yes | definition | `5.1` | tasks | `.kiro/specs/1-3-14-in-memory-only-cache-mode/tasks.md:70` | - [x] 5.1 Write property test: Relaxed initialization in memory-only mode |
| 11 | yes | definition | `2.7` | tasks | `.kiro/specs/1-3-15-powertools-integration/tasks.md:83` | - [x] 2.7 Write property tests for error resilience (Property 5) |
| 12 | yes | reference | `Property 2` | properties | `.kiro/specs/1-4-0-property-test-generator-preconditions/tasks.md:147` | - Tag `// Feature: 1-4-0-property-test-generator-preconditions, Property 2: Constructed ARNs are always accepted` |
| 13 | yes | reference | `Property 1` | properties | `.kiro/specs/1-3-10-clean-up-generic-responses/design.md:287` | - **Feature: 1-3-10-clean-up-generic-responses, Property 1: Factory structural completeness** — Generate random content type strings and body formatter functions, verify the returned module has all re |
| 14 | yes | definition | `Risk 6` | risks | `.kiro/specs/1-3-9-test-migration-phase-3/design.md:637` | ### Risk 6: Breaking Changes to APIs |
| 15 | yes | definition | `Requirement 4` | requirements | `.kiro/specs/1-3-17-node-26-support/requirements.md:56` | ### Requirement 4: Deprecation Notice Registry |
| 16 | yes | definition | `1` | tasks | `.kiro/specs/1-3-14-typescript-type-definitions/tasks.md:9` | - [x] 1. Set up TypeScript infrastructure and main entry point |
| 17 | yes | definition | `9.2` | tasks | `.kiro/specs/1-3-10-test-migration-phase-5/tasks.md:233` | - [x] 9.2 Verify property-based tests follow patterns |
| 18 | yes | reference | `Property 5` | properties | `.kiro/specs/1-3-8-api-request-pagination-retries-xray/tasks.md:100` | - **Property 5: Pagination Error Handling** |
| 19 | yes | reference | `Requirement 10` | requirements | `.kiro/specs/1-3-17-node-26-support/design.md:270` | ### Runbook trigger decision logic (Requirement 10) |
| 20 | yes | reference | `WS-3` | workstreams | `.kiro/specs/1-3-16-fully-implement-ssm-parameter-store-and-secrets-manager-sdk/requirements.md:378` | \| 9. Layer availability detection \| WS-3 \| Q11 heuristic then probe with override \| |
| 21 | yes | definition | `7.1` | tasks | `.kiro/specs/1-3-6-in-memory-cache/tasks.md:124` | - [x] 7.1 Add L0_Cache lookup before DynamoDB read |
| 22 | yes | definition | `Requirement 9` | requirements | `.kiro/specs/1-3-15-powertools-integration/requirements.md:135` | ### Requirement 9: Metrics Emission for Endpoint Operations |
| 23 | yes | reference | `WS-6` | workstreams | `.kiro/specs/1-3-16-fully-implement-ssm-parameter-store-and-secrets-manager-sdk/requirements.md:383` | \| 14. Secrets in configuration path \| WS-6 \| Q15 new key, Q6 nest, Q17 raw by default \| |
| 24 | yes | definition | `Requirement 3` | requirements | `.kiro/specs/1-3-10-new-response-format-method/requirements.md:39` | ### Requirement 3: error() Shortcut Method |
| 25 | yes | reference | `Property 1` | properties | `.kiro/specs/1-3-12-fix-cache-response-headers/tasks.md:4` | - **Property 1: Bug Condition** - Application-Set Cache Headers Overwritten by finalize() |
| 26 | yes | reference | `Property 5` | properties | `.kiro/specs/1-3-9-test-migration-phase-3/design.md:685` | - [ ] Implement Property 5: Round-Trip Serialization |
| 27 | yes | reference | `Property A2` | assertions | `.kiro/specs/1-3-16-fix-ssm-param-security/tasks.md:94` | - **Object.prototype guard**: every case above diffs `Object.getOwnPropertyNames(Object.prototype)` before and after and asserts no additions (Property A1, A2, Req 2.6) |
| 28 | yes | definition | `Requirement 6` | requirements | `.kiro/specs/1-3-10-test-migration-phase-6/requirements.md:103` | ### Requirement 6: Migrate Migration Validation Tests |
| 29 | yes | definition | `4.3` | tasks | `.kiro/specs/1-3-16-fully-implement-ssm-parameter-store-and-secrets-manager-sdk/tasks.md:105` | - [x] 4.3 Implement grouping via `ParameterKeySafety` |
| 30 | yes | definition | `1` | tasks | `.kiro/specs/1-3-9-improve-validations-object/tasks.md:11` | - [x] 1. Phase 1: Create Internal Classes (No Breaking Changes) |

## oscar

| # | Correct | Kind | ID | Category | Location | Line text |
|---:|:---:|---|---|---|---|---|
| 1 | yes | reference | `User Story 2` | stories | `specs/001-metrics-collection/tasks.md:105` | - [X] T018 [US2] Extend sources with per-user execution counts in pkg/metrics/sources.go |
| 2 | yes | definition | `T038` | tasks | `specs/007-bucket-quotas/tasks.md:187` | - [X] T038 [US4] Persist updated per-user bucket count and |
| 3 | yes | reference | `User Story 3` | stories | `specs/007-bucket-quotas/tasks.md:157` | - [X] T033 [US3] Keep quota responses focused on machine-readable MinIO quota |
| 4 | yes | reference | `User Story 1` | stories | `specs/002-deployment-status-logs/tasks.md:211` | 3. US3 begins once US1 and US2 behaviors are stable enough to correlate summary and logs. |
| 5 | yes | reference | `User Story 1` | stories | `specs/002-federation/tasks.md:135` | - **User Story 3 (P3)**: Can start after Foundational (Phase 2) - Independent of US1/US2 but benefits from federation definitions |
| 6 | yes | reference | `User Story 1` | stories | `specs/002-deployment-status-logs/tasks.md:197` | 3. Complete Phase 3: User Story 1. |
| 7 | yes | definition | `T039` | tasks | `specs/007-bucket-quotas/tasks.md:190` | - [X] T039 [US4] Ensure lowered bucket count limits block only new |
| 8 | yes | definition | `Service Deployment Visibility` | features | `specs/002-deployment-status-logs/spec.md:1` | # Feature Specification: Service Deployment Visibility |
| 9 | yes | definition | `T005` | tasks | `specs/001-metrics-collection/tasks.md:42` | - [X] T005 Add shared request validation helpers in pkg/handlers/metrics.go |
| 10 | yes | definition | `T031` | tasks | `specs/002-deployment-status-logs/tasks.md:127` | - [X] T031 Validate the deployment visibility quickstart scenarios against specs/002-deployment-status-logs/quickstart.md |
| 11 | yes | definition | `T009` | tasks | `specs/002-federation/tasks.md:55` | - [x] T009 [P] [US1] Integrate federation expansion into service updates in `pkg/handlers/update.go` |
| 12 | yes | reference | `User Story 1` | stories | `specs/007-bucket-quotas/tasks.md:317` | 2. Implement US1 bucket count enforcement for OSCAR-controlled creation. |
| 13 | yes | reference | `User Story 1` | stories | `specs/002-federation/tasks.md:53` | - [x] T007 [US1] Implement mesh topology expansion in `pkg/utils/federation.go` |
| 14 | yes | reference | `T006` | tasks | `specs/002-deployment-status-logs/tasks.md:157` | - Foundational backend helper tasks `T006` and `T007` can run in parallel after `T004` and `T005`. |
| 15 | yes | definition | `SC-006` | success | `specs/006-volumes/spec.md:251` | - **SC-006**: In validation runs, 100% of service-created volumes with |
| 16 | yes | definition | `FR-007` | requirements | `specs/002-federation/spec.md:130` | - **FR-007**: System MUST support delegation policies `static`, `random`, and |
| 17 | yes | definition | `T051` | tasks | `specs/001-metrics-collection/tasks.md:144` | - [X] T051 Document Prometheus metrics configuration in docs/api.md |
| 18 | yes | reference | `User Story 2` | stories | `specs/007-bucket-quotas/tasks.md:116` | - [X] T024 [US2] Apply configured `storage_per_bucket` after successful |
| 19 | yes | reference | `T023` | tasks | `specs/006-volumes/tasks.md:226` | - `T023` and `T024` can run in parallel for US3 tests. |
| 20 | yes | reference | `T011` | tasks | `specs/006-volumes/tasks.md:222` | - `T005`, `T007`, `T008`, `T009`, `T010`, and `T011` can run in parallel once |
| 21 | yes | definition | `FR-023` | requirements | `specs/007-bucket-quotas/spec.md:274` | - **FR-023**: The system MUST handle MinIO read/count failures by failing quota |
| 22 | yes | definition | `T004` | tasks | `specs/002-federation/tasks.md:36` | - [x] T004 Align replica/federation structs with new semantics in `pkg/types/replica.go` |
| 23 | yes | reference | `T004` | tasks | `specs/006-volumes/tasks.md:223` | `T004` starts the shared model transition. |
| 24 | yes | definition | `T002` | tasks | `specs/001-metrics-collection/tasks.md:30` | - [X] T002 Create metrics aggregation package files in pkg/metrics/aggregators.go and pkg/metrics/sources.go |
| 25 | yes | reference | `T020` | tasks | `specs/002-federation/tasks.md:159` | - T016 and T020 can be implemented in parallel (`pkg/types/service.go` vs `pkg/handlers/status.go`) |
| 26 | yes | reference | `T006` | tasks | `specs/007-bucket-quotas/tasks.md:282` | - `T006`, `T008`, `T010`, `T012`, and `T014` can run in parallel with helper |
| 27 | yes | reference | `User Story 3` | stories | `specs/006-volumes/tasks.md:146` | **Checkpoint**: User Story 3 should preserve retained volumes and clean up |
| 28 | yes | definition | `T052` | tasks | `specs/001-metrics-collection/tasks.md:152` | - [ ] T052 Add benchmark for breakdown CSV export generation in pkg/handlers/metrics_test.go |
| 29 | yes | definition | `FR-008` | requirements | `specs/006-volumes/spec.md:158` | - **FR-008**: The system MUST automatically provision and attach a new volume |
| 30 | yes | reference | `User Story 2` | stories | `specs/002-deployment-status-logs/tasks.md:93` | - [X] T022 [US2] Update deployment log contract details in specs/002-deployment-status-logs/contracts/deployment-visibility.openapi.yaml and Swagger comments in pkg/handlers/deployment.go |

## sleap-roots

| # | Correct | Kind | ID | Category | Location | Line text |
|---:|:---:|---|---|---|---|---|
| 1 | yes | definition | `Module-level imports are accurate` | requirements | `openspec/specs/example-correctness/spec.md:93` | ### Requirement: Module-level imports are accurate |
| 2 | yes | definition | `Tier 2 ψ_g trait emission API / psi_g.compute rejects invalid cadence_s value with ValueError naming the field` | scenarios | `openspec/specs/circumnutation/spec.md:1489` | #### Scenario: psi_g.compute rejects invalid cadence_s value with ValueError naming the field |
| 3 | yes | reference | `CC-8` | constraints | `openspec/changes/archive/2026-06-03-add-circumnutation-tier1-derr-faithful/proposal.md:5` | Theoretical foundation: `theory.md` §7.2 (Tier 1 trait table — 5 traits anchored to BM2016 §"Temporal linear variation of ψ_g" + Derr 2025 pilot); `theory.md` §7.6 (QC tier — `is_nutating = band_power |
| 4 | yes | reference | `CC-6` | constraints | `docs/superpowers/specs/2026-06-05-add-circumnutation-tier2-psi-g-design.md:545` | (r3); spec-delta MODIFIED+ADDED split; CC-3/CC-6/CC-9 all pass (r3); no |
| 5 | yes | reference | `Series.sample_uid SHALL provide a cross-scan stable identity` | requirements | `openspec/changes/archive/2026-05-06-add-sample-uid-timepoint-metadata/specs/series-metadata/spec.md:3` | ### Requirement: `Series.sample_uid` SHALL provide a cross-scan stable identity |
| 6 | yes | reference | `Task 3.1` | plan_tasks | `docs/superpowers/plans/2026-04-24-metadata-layer.md:668` | **Note**: `self.sample_uid` is referenced but not yet defined as an attrs field — that lands in Task 3.4. The tests in Task 3.1 don't pass a `sample_uid` kwarg; they rely on a default. To unblock thes |
| 7 | yes | definition | `Tier 2 ψ_g trait emission API / psi_g.compute is deterministic across runs and across OSs` | scenarios | `openspec/specs/circumnutation/spec.md:1510` | #### Scenario: psi_g.compute is deterministic across runs and across OSs |
| 8 | yes | definition | `6.17` | tasks | `openspec/changes/archive/2026-05-07-add-tracked-tip-pipeline/tasks.md:103` | - [x] 6.17 Add `test_track_id_values_match_inst_track_name` — synthetic .slp with custom track names `["alpha", "beta"]` → `set(row["track_id"] for row in result["tracks"]) == {"alpha", "beta"}`. |
| 9 | yes | definition | `5.3` | tasks | `openspec/changes/archive/2026-02-11-add-external-image-mode/tasks.md:47` | - [x] 5.3 Test `generate(embed=True)` does not create images directory |
| 10 | yes | definition | `7.2` | tasks | `openspec/changes/archive/2026-05-22-add-circumnutation-synthetic-generator/tasks.md:328` | - [ ] 7.2 Update `docs/circumnutation/roadmap.md` row PR #4 → ✅ with the GitHub issue and PR numbers. |
| 11 | yes | definition | `2.2` | tasks | `openspec/changes/archive/2026-06-10-add-circumnutation-tier3b-spatial-cwt/tasks.md:32` | - [x] 2.2 GREEN: define `ResampleResult`. |
| 12 | yes | reference | `CC-3` | constraints | `openspec/specs/circumnutation/spec.md:1932` | The function SHALL emit only these 6 columns; the `L_gz`/`L_c`-dependent traits (`L_gz_estimate`, `L_c_estimate`, `B_balance_number`, `L_gz_steady_state_residual`, `L_gz_resolvable`) and the growth-zo |
| 13 | yes | reference | `CC-3` | constraints | `docs/superpowers/specs/2026-06-10-add-circumnutation-tier3c-traits-design.md:368` | honest" correct; MAD computed about the median; all 6 column suffixes correct; CC-3/CC-1 honored; |
| 14 | yes | definition | `Real-fixture integration tests SHALL ship with the change / No-CSV path defaults sample_uid and timepoint` | scenarios | `openspec/specs/tracked-tip-pipeline/spec.md:476` | #### Scenario: No-CSV path defaults sample_uid and timepoint |
| 15 | yes | definition | `2.2` | tasks | `openspec/changes/archive/2026-06-29-add-circumnutation-cli/tasks.md:29` | - [x] 2.2 Implement `sleap_roots/circumnutation/adapters.py::series_to_inputs(...) -> tuple[CircumnutationInputs, dict]` to pass 2.1: returns the inputs + the identity-provenance dict (`metadata_csv_p |
| 16 | yes | definition | `6.1` | tasks | `openspec/changes/archive/2026-06-03-add-circumnutation-tier1-derr-faithful/tasks.md:297` | - [ ] 6.1 Stage files: `git add sleap_roots/circumnutation/_constants.py sleap_roots/circumnutation/_geometry.py sleap_roots/circumnutation/_noise.py sleap_roots/circumnutation/nutation.py sleap_roots |
| 17 | yes | definition | `4.6` | tasks | `openspec/changes/archive/2026-04-21-add-multiple-dicot-plate-pipeline/tasks.md:139` | - [x] 4.6 Implement `compute_batch_plate_traits(all_series, write_csv=False, write_json=False, output_dir=".", csv_name="plate_batch_traits.csv", json_name="plate_batch_traits.json")`. Loop over serie |
| 18 | yes | reference | `D9` | decisions | `openspec/changes/archive/2026-06-03-add-circumnutation-tier1-derr-faithful/design.md:995` | - Add **6** new module-level constants per D9 + S2 round-1 reconciliation: `RIDGE_CONTINUITY_FILTER_WINDOW=5`, `NOISE_FLOOR_OUT_OF_BAND_FACTOR=5.0` (S7: kept at CC-8 verbatim, GREEN-phase may revisit) |
| 19 | yes | reference | `CC-2` | constraints | `openspec/changes/archive/2026-05-27-add-circumnutation-temporal-cwt-machinery/design.md:18` | Cross-cutting concerns touched: **CC-6 (determinism, including across OSs)**, CC-2 (constants), CC-3 (pure-pixel emission — preserved by the bool COI mask + complex-amplitude scaleogram; no calibrated |
| 20 | yes | reference | `CC-6` | constraints | `openspec/changes/archive/2026-05-22-add-circumnutation-synthetic-generator/specs/circumnutation/spec.md:124` | **Determinism contract (CC-6).** `random_state` SHALL accept `int`, `np.random.Generator`, or `None`. A single internal call to `np.random.default_rng(random_state)` handles all three idiomatically. S |
| 21 | yes | definition | `3.1` | tasks | `openspec/changes/archive/migrate-to-uv/tasks.md:196` | #### 3.1 Update Claude Commands |
| 22 | yes | definition | `8.2` | tasks | `openspec/changes/archive/2026-06-09-add-circumnutation-tier3a-midline/tasks.md:55` | - [x] 8.2 GREEN-phase: cross-tier acceptance — primary ROBUST invariant `arc_length_px[-1] ≤ L` per track (`L = Σ‖diff(xy)‖`, recovered/recomputed via `kinematics`; SG smoothing never lengthens the pa |
| 23 | yes | reference | `D11` | decisions | `openspec/changes/archive/2026-05-22-add-circumnutation-synthetic-generator/tasks.md:83` | - [ ] 2.B.5 Test `noise_zero_short_circuits_rng` (design.md D11): assert `generate_trajectory(noise_sigma_px=0, random_state=None, ...)` and `generate_trajectory(noise_sigma_px=0, random_state=42, ... |
| 24 | yes | definition | `3.4` | tasks | `openspec/changes/archive/2026-02-11-add-external-image-mode/tasks.md:29` | - [x] 3.4 Test `is_h5_video()` returns True for H5-backed video |
| 25 | yes | reference | `D1` | decisions | `openspec/changes/archive/2026-05-14-add-circumnutation-tier0-kinematics/design.md:13` | - Emit per-track scalar kinematic traits matching `theory.md` §7.1 — expanded from the doc's 7 listed traits to **9 + 1 flag** as explained in D1 below. |
| 26 | yes | reference | `D4` | decisions | `openspec/changes/archive/2026-06-23-add-circumnutation-plots/design.md:473` | - **MINOR (design labels):** duplicate `### D5` headers and dangling `D4`/`D7` |
| 27 | yes | reference | `CC-6` | constraints | `openspec/changes/archive/2026-05-22-add-circumnutation-synthetic-generator/design.md:25` | - Honor the determinism contract (CC-6 / D5): `random_state` accepts `int \| np.random.Generator \| None`; same int seed → bit-identical `tip_x` / `tip_y` across runs AND across OSs on 64-bit platforms. |
| 28 | yes | definition | `4.2` | tasks | `openspec/changes/archive/2026-05-06-add-sample-uid-timepoint-metadata/tasks.md:46` | - [x] 4.2 Add `get_metadata(self, column, plant_id=None)` method. The `_warned_missing_plant_id_column` flag is initialized in `__attrs_post_init__` (Section 2.2) — DO NOT declare it as an `attrs.fiel |
| 29 | yes | definition | `3.6` | tasks | `openspec/changes/archive/2026-06-18-add-circumnutation-per-genotype-aggregation/tasks.md:95` | - [x] 3.6 Implement the `_iqr_or_nan` wrapper (module-qualified `scipy.stats.iqr`; |
| 30 | yes | definition | `sleap_roots/metadata.py SHALL provide CSV builder helpers / build_metadata_csv returns the written Path` | scenarios | `openspec/specs/series-metadata/spec.md:202` | #### Scenario: `build_metadata_csv` returns the written Path |

## mssql-extension

| # | Correct | Kind | ID | Category | Location | Line text |
|---:|:---:|---|---|---|---|---|
| 1 | yes | reference | `User Story 2` | stories | `specs/013-table-scan-filter-refactor/tasks.md:210` | - US2 (Functions/CASE): Can start after Foundational, benefits from US1 completion |
| 2 | yes | reference | `User Story 5` | stories | `specs/007-catalog-integration/tasks.md:157` | - [ ] T044 [P] [US5] Create MSSQLPreparedStatement class in `src/include/pushdown/mssql_prepared_statement.hpp` |
| 3 | yes | reference | `User Story 1` | stories | `specs/049-fix-partitioned-table-catalog/tasks.md:172` | - **Phase 3 (US1 fix)**: T003-T005 can run in parallel (independent string literals). T006-T007 after all three. |
| 4 | yes | reference | `User Story 3` | stories | `specs/032-fedauth-token-provider/tasks.md:118` | - [ ] T037 [P] [US3] Add test case for expired token error message format in test/cpp/test_jwt_parser.cpp |
| 5 | yes | reference | `T034` | tasks | `specs/042-integrated-authentication/tasks.md:163` | - Phase 4: T031 → T032 → T033 → T034 |
| 6 | yes | reference | `User Story 7` | stories | `specs/031-connection-fedauth-refactor/tasks.md:187` | - [ ] T054a [US7] Add state transition guards to `TdsConnection::TransitionState()` in `src/tds/tds_connection.cpp` (FR-011) |
| 7 | yes | reference | `User Story 6` | stories | `specs/007-catalog-integration/tasks.md:186` | - [ ] T057 [US6] Generate CONVERT(varchar(max), @pN) COLLATE <collation> for VARCHAR filters in `src/pushdown/mssql_filter_translator.cpp` |
| 8 | yes | definition | `SC-004` | success | `specs/010-extension-documentation/spec.md:194` | - **SC-004**: Type mapping table covers all 20+ supported SQL Server types |
| 9 | yes | definition | `SC-011` | success | `specs/001-tds-fedauth-integration/spec.md:203` | - **SC-011**: Fabric Warehouse basic operations (SELECT, catalog) documented and working |
| 10 | yes | definition | `T020` | tasks | `specs/025-bcp-improvements/tasks.md:84` | - [ ] T020 [US2] Add connection state validation before release in src/copy/copy_function.cpp |
| 11 | yes | definition | `038-fix-datetime2-uri-parsing` | features | `specs/038-fix-datetime2-uri-parsing/spec.md:1` | # Feature Specification: Fix datetime2(0) Truncation and URI Password Parsing |
| 12 | yes | reference | `D0` | decisions | `specs/080-dml-pushdown/spec.md:848` | - Synapse (MERGE in preview there; D0). |
| 13 | yes | reference | `User Story 5` | stories | `specs/033-fix-catalog-scan/tasks.md:212` | ## Parallel Example: User Story 5 |
| 14 | yes | reference | `T002` | tasks | `specs/028-ansi-connection-options/tasks.md:254` | - User Story 1 (P1/MVP): 5 tasks (T002-T006) |
| 15 | yes | definition | `T004` | tasks | `specs/049-fix-partitioned-table-catalog/tasks.md:59` | - [ ] **T004** [P] [US3] Fix `BULK_METADATA_SCHEMA_SQL_TEMPLATE` in the same file (line ~79-105). Same replacement. Required so `mssql_preload_catalog` and `MSSQLTableSet::Scan` work on partitioned ta |
| 16 | yes | definition | `SC-006` | success | `specs/031-connection-fedauth-refactor/spec.md:203` | - **SC-006**: CTAS operations trigger 3 or fewer connection acquires for cached tables (currently 9+) |
| 17 | yes | definition | `User Story 2` | stories | `specs/006-split-tls-build/spec.md:87` | ### User Story 2 - Loadable Extension With Full TLS (Priority: P1) |
| 18 | yes | reference | `T046k` | tasks | `specs/047-process-state-cleanup/tasks.md:282` | T001 → T002 → T003 → T004 → T005 → T006 → T007 → T008 → T009 → T010 → T011 → T012 → T013 → T014 → T020 → T021 → T022 → T023 → T024 → T025 → T026 → T027 → T028 → T028a → T029 → T032 → ... → T046k → T04 |
| 19 | yes | reference | `User Story 4` | stories | `specs/045-type-codec-consolidation/tasks.md:245` | - [X] T095 [US4] `GEN=ninja make test && GEN=ninja make integration-test` — all green (unit: 109 cases / 3385 assertions, integration: 34+16 cases / 1076+304 assertions). See T106. |
| 20 | yes | reference | `FR-026` | requirements | `specs/045-type-codec-consolidation/tasks.md:120` | - [X] T040 [P] [US5] Wrote `test/cpp/codec/test_string_codec.cpp`: 7 test groups covering FormatSqlLiteral byte-identity (Filter == InsertValues), single-quote escape contract (N'...' doubles `'`), Fo |
| 21 | yes | reference | `User Story 4` | stories | `specs/001-tds-fedauth-integration/tasks.md:258` | - US4-US7: Depend on US1, can proceed in parallel or sequentially by priority |
| 22 | yes | definition | `User Story 3` | stories | `specs/036-azure-token-docs/spec.md:48` | ### User Story 3 - Primary Key Update Limitation Notice (Priority: P3) |
| 23 | yes | reference | `User Story 5` | stories | `specs/045-type-codec-consolidation/tasks.md:137` | - [X] T054 [US5] Captured post-fix wire bytes evidence in `specs/045-type-codec-consolidation/issue_91_repro.md`: full reproduction of the new client-side `InvalidInputException` (verbatim REPL output |
| 24 | yes | definition | `User Story 1` | stories | `specs/001-tds-fedauth-integration/spec.md:20` | ### User Story 1 - Connect with Azure Authentication (Priority: P1) |
| 25 | yes | reference | `T001` | tasks | `specs/043-refactoring-foundation/tasks.md:142` | - [ ] T036 [P] Update the spec's `Status` field in `specs/043-refactoring-foundation/spec.md` from `Draft` to `Implemented` once T001..T035 complete. |
| 26 | yes | reference | `D2` | decisions | `specs/060-target-types-and-ddl-options/spec.md:225` | source by the catalog** (D2), which is the case that needs no user input at |
| 27 | yes | reference | `T035` | tasks | `specs/044-codec-consolidation/tasks.md:200` | - **US5 (Phase 7)**: T033-T035 (microbenchmark) depends on US3's rename pass (T024) because the `tds::encoding::testing::LegacyUtf16LE*` re-export only exists post-rename. T036-T037 (e2e script) is bu |
| 28 | yes | definition | `SC-005` | success | `specs/007-catalog-integration/spec.md:274` | - **SC-005**: All pushed predicates use `sp_executesql` with bound parameters (verifiable via SQL Server profiler). |
| 29 | yes | definition | `T001` | tasks | `specs/045-type-codec-consolidation/tasks.md:23` | - [X] T001 Create directories `src/codec/` and `src/include/codec/` at repo root |
| 30 | yes | reference | `User Story 1` | stories | `specs/026-varchar-nvarchar-conversion/tasks.md:51` | ## Phase 3: User Story 1 - Query Tables with Extended ASCII (Priority: P1) 🎯 MVP |

## caro

| # | Correct | Kind | ID | Category | Location | Line text |
|---:|:---:|---|---|---|---|---|
| 1 | yes | reference | `WP07` | package_tables | `kitty-specs/018-issue-10-implement/plan.md:181` | - WP07: Progress UI (indicatif integration) |
| 2 | yes | reference | `WP03` | packages | `kitty-specs/017-issue-9-add/tasks/WP03-config-benchmarks.md:56` | - 2026-01-08T13:39:55Z – claude – shell_pid=1505 – lane=doing – Started WP03 implementation |
| 3 | yes | reference | `T046` | tasks | `specs/002-implement-tdd-green/tasks.md:830` | - T046: Integration complete (80 tests - GOAL) |
| 4 | yes | reference | `T004` | tasks | `kitty-specs/025-llm-evaluation-harness/tasks/WP01-project-setup.md:9` | - T004 |
| 5 | yes | reference | `T014` | tasks | `kitty-specs/025-llm-evaluation-harness/tasks.md:405` | \| T014 \| Unit test: malformed TOML \| WP02 \| P0 \| [P] \| |
| 6 | yes | reference | `WP05` | packages | `kitty-specs/022-issue-135-build/tasks.md:300` | **Deferred to Phase 2**: WP05 (POSIX), WP06 (backends), WP07 (advanced reporting) |
| 7 | yes | reference | `T027` | tasks | `kitty-specs/017-issue-9-add/tasks/WP04-context--logging-benchmarks.md:5` | subtasks: [T022, T023, T024, T025, T026, T027, T028, T029, T030, T031] |
| 8 | yes | definition | `T067` | tasks | `kitty-specs/025-llm-evaluation-harness/tasks.md:279` | - [x] T067 Assert safety accuracy = 1.0 |
| 9 | yes | definition | `T029` | tasks | `kitty-specs/004-add-internationalization-i18n/tasks.md:246` | - [ ] T029 Create `.github/scripts/translate.js` Node.js translation script |
| 10 | yes | definition | `FR-021` | requirements | `specs/005-caro-vscode-extension/spec.md:114` | - **FR-021**: System MUST block critical-risk commands with explanation |
| 11 | yes | definition | `T020` | tasks | `specs/010-nimble-cve-pipeline/tasks.md:25` | - [ ] T020 `[P2]` Create `src/dogma/mod.rs` (module stub, pub re-exports) |
| 12 | **no** | reference | `NFR-002` | requirements | `specs/008-functiongemma-intent-router/PRD.md:342` | \| NFR-002.3 \| Safety pattern coverage \| > 80 patterns \| |
| | | | | | | *Note:* The row is sub-requirement NFR-002.3 (under `#### NFR-002: Reliability`); the rule `\b(?:FR\|NFR)-(?:[A-Z]+-)?\d+\b` stops at the dot, so it is read as a reference to the parent NFR-002. Right element family, truncated ID. |
| 13 | yes | reference | `T028` | tasks | `kitty-specs/025-llm-evaluation-harness/tasks/WP04-safety-posix-validators.md:155` | ### T028-T032 – Unit Tests |
| 14 | yes | reference | `WP06` | packages | `kitty-specs/022-issue-135-build/tasks/WP06-backend-comparison.md:175` | - [ ] `tasks.md` updated with WP06 completion status |
| 15 | yes | reference | `SC-004` | success | `kitty-specs/002-unquoted-cli-arguments/tasks/WP05-validation-and-help-display.md:32` | **Goal**: Validate prompts and show help for empty/whitespace input (FR-004, SC-004). |
| 16 | yes | definition | `S3.1.2` | shellstories | `specs/007-caro-shell-integration/milestones.md:162` | \| S3.1.2 \| M \| Build pattern database in `src/shell/fixit/patterns.rs` \| |
| 17 | yes | definition | `T067` | tasks | `kitty-specs/018-issue-10-implement/tasks.md:381` | - [ ] T067: Document HF_TOKEN usage and authentication |
| 18 | yes | reference | `T021` | tasks | `specs/002-implement-tdd-green/tasks.md:347` | - **Commit Message**: `[T021] Define CommandGenerator async trait` |
| 19 | yes | reference | `T046` | tasks | `kitty-specs/026-llm-evaluation-harness/tasks.md:463` | \| T046 \| Implement JSON output format \| WP06 \| P1 \| Yes \| |
| 20 | yes | reference | `T019` | tasks | `kitty-specs/026-llm-evaluation-harness/tasks.md:436` | \| T019 \| Implement EvaluationHarness struct \| WP03 \| P1 \| No \| |
| 21 | yes | reference | `T028` | tasks | `kitty-specs/004-add-internationalization-i18n/tasks.md:268` | - T030, T031, T032, T033 must be sequential (building on T028/T029 foundation) |
| 22 | yes | definition | `FR-052` | requirements | `specs/008-magic-link-terminal/spec.md:187` | - **FR-052**: Preflight check MUST clearly indicate this is a preview and Caro will run full validation locally |
| 23 | yes | reference | `T024` | tasks | `kitty-specs/026-llm-evaluation-harness/tasks.md:441` | \| T024 \| Implement result aggregation \| WP03 \| P1 \| No \| |
| 24 | yes | definition | `T015` | tasks | `kitty-specs/004-add-internationalization-i18n/tasks.md:78` | - [ ] T015 Create `website/src/i18n/index.ts` to export all translation objects |
| 25 | yes | reference | `WP06` | packages | `kitty-specs/025-llm-evaluation-harness/tasks.md:439` | \| T048 \| Implement calculate_posix_compliance_rate() \| WP06 \| P1 \| [P] \| |
| 26 | yes | reference | `T014` | tasks | `specs/004-implement-ollama-and/tasks.md:402` | **Dependencies**: T014 |
| 27 | yes | reference | `T041` | tasks | `kitty-specs/026-llm-evaluation-harness/tasks/WP05-test-dataset-creation.md:55` | ### T041-T042 – Validation & Documentation |
| 28 | yes | definition | `T024` | tasks | `kitty-specs/020-machine-resource-assessment/tasks.md:163` | - [x] T024: Implement `--recommendations-only` flag |
| 29 | yes | reference | `T002` | tasks | `kitty-specs/002-unquoted-cli-arguments/tasks/WP01-cli-argument-parsing-setup.md:97` | ### Subtask T002 – Add trailing_args field to CliArgs |
| 30 | yes | reference | `T017` | tasks | `kitty-specs/022-issue-135-build/tasks/WP03-correctness-evaluation.md:299` | ### T017 – Implement correctness scoring (0.0-1.0) |
