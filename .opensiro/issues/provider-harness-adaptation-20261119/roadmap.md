# Capability Roadmap Receipt — Open Interpreter S4 prospective provider adaptation (2026-11-19)

## Identity and pins

- Original repository: openinterpreter/openinterpreter
- Original HEAD: 382f615b907279be1b6518156ac2754d3c235ff4
- Observed at: 2026-11-19
- Accepted Index assessment: https://github.com/opensiro/vsm-harness-index/blob/c2e43bf4750841277b3e58d8ba80314121734764/assessments/op/open-interpreter.md
- Accepted assessment blob SHA: e892024abc1206554838d6a7330e385acf863524
- Accepted review ref: f110a7a85f43efc343f936f5bc504e01eb262550
- Accepted reviewed at: 2026-09-15
- System in focus: one Open Interpreter Rust/Codex-derived configured session and first-party provider/harness routing, model selection, Goal/Guardian and optional agent tools; external model vendors and legitimate host/user policy outside.
- Index commit: c2e43bf4750841277b3e58d8ba80314121734764
- Accepted status: included
- Assessment age/freshness: Profile 0.2.1, Methodology 0.3.1, last historical check 2026-09-17; source older than 30 days, suggest Index re-assessment without automatic regrade.
- Catalog identity: harness_id open-interpreter, repository https://github.com/openinterpreter/openinterpreter, review_ref f110a7a85f43efc343f936f5bc504e01eb262550; source review revision resolves in original.
- Current original branch: main
- Fork: opensiro-contributions/openinterpreter, parent verified openinterpreter/openinterpreter, opensiro/meta owner ACTIVE/ALLOW.
- Receipt contract: proposal-gate
- Repository-wide source map: 9720-tree-entries structural directory screen (Rust core, extensions, provider/catalog/harness routing, app-server/ACP, SDK, tests/docs, user config, original issues/PRs, policies), direct pinned inspection of S1/2/3/3*/4/5 representative first-party source.
- Priority rationale: unlike S1 A, S2 C, S3 Goal/user-controlled and S3* C Guardian, current multiple source-reported external provider compatibility disturbances support a narrowly scoped hypothetical future-route S4 decision, with existing route and event substrate; S5 remains owner-reserved.
- Accepted VSM vector: S1=A · S2=C · S3=— · S3*=C · S4=— · S5=—
- S1 disposition: accepted A coding agent already chooses operational steps; no additional C evidence.
- S2 disposition: accepted C stable but opt-in MultiAgentV2 messaging/interrupt/status; native coordination is baseline.
- S3 disposition: accepted —, current Goals stable/default enabled and per-thread budgets/status/CAS, but no qualified new shared whole-system S3 actor need; no inferred current regrade.
- S3* disposition: accepted C, GuardianApproval stable/default enabled and distinct pre-action review, not a new S4 strategy.
- S4 disposition: accepted —, optional source-native prospective provider/harness adaptation actor proposed C using model/wire route, external facts, authorized choices and later feedback, not yet shipped.
- S5 disposition: accepted —, user/host/provider/legal authority remains ultimate; no new policy grant or autonomous change of credentials/budget.
- Target transition: S4=— -> S4=C
- P1 dependencies: native typed compatibility observation, opted-in route allowlist/host authority, future-turn apply bridge, subsequent real task feedback, original-native positive and fail-closed tests, baseline comparison.
- P2 optional: NONE
- Proposed C construction: first-party opt-in composer registers independent S4 actor allowed to stay/hold/select an already-approved future route after verified external compatibility change, host enforces selection, next task returns outcome to same actor for correction.
- C sufficiency falsifier: manual user choice or narrow native fixes achieve equal/better later task result at lower cost; no lawful and independently composed prospective actor can influence a future real route and receive verified feedback.
- Scenario basis: HYPOTHETICAL
- Proposal-stage decision: GO
- Research disposition: NEEDS_EVIDENCE
- Proposed validation: local #1982 reproduction plus legally available compatible alternate route and controlled later task; compare native manual/static-fix baseline, hold/veto/stale-fact negatives and after-run receipts.
- Validation state: NOT_RUN
- Proposal falsifier: unsupported route or absent approval blocks host change, no later task evidence or no improved operator result; returns NO_GO on such comparator.
- Result: NEEDS_EVIDENCE
- External issue: DRAFT — NOT PUBLISHED
- Cost status: NOT_MEASURED

## Rights and authority

Original [Apache-2.0](https://github.com/openinterpreter/openinterpreter/blob/382f615b907279be1b6518156ac2754d3c235ff4/LICENSE)/NOTICE, [SECURITY](https://github.com/openinterpreter/openinterpreter/blob/382f615b907279be1b6518156ac2754d3c235ff4/SECURITY.md), and [PR template](https://github.com/openinterpreter/openinterpreter/blob/382f615b907279be1b6518156ac2754d3c235ff4/.github/pull_request_template.md) inspected. Original PR template routes generic inherited Codex changes to openai/codex; Open Interpreter-specific provider/harness compatibility belongs here. CLA/DCO, third-party model/pack rights and any personal act unverified, not waived. Fork is verified `fork=true`, parent original, metadata `ACTIVE/ALLOW`, previous owner activation event `20261119T182226Z--owner-upstream58-active`. Internal case writes permitted; no public fork Issue/PR or original maintainer communication approval inferred. No default-branch/product source change.

## Existing work / overlap

| Track A source/status | Native scope | Track B on-top alternative and counterfactual |
| --- | --- | --- |
| [native README](https://github.com/openinterpreter/openinterpreter/blob/382f615b907279be1b6518156ac2754d3c235ff4/README.md) and [harness router](https://github.com/openinterpreter/openinterpreter/blob/382f615b907279be1b6518156ac2754d3c235ff4/codex-rs/core/src/harness/routing.rs) SHIPPED | Manual model/harness choice and static wire/harness routing | Reuse current native routes; only opt-in future-oriented delegated choice plus later real feedback, compare to manual |
| [provider catalog](https://github.com/openinterpreter/openinterpreter/blob/382f615b907279be1b6518156ac2754d3c235ff4/codex-rs/model-provider-info/src/bundled_provider_catalog.rs) SHIPPED | Curated/generated provider metadata | Redacted versioned facts with stale/trust control, not a verified result on their own |
| [#1982](https://github.com/openinterpreter/openinterpreter/issues/1982) OPEN original Issue | Ollama Qwen3.5:9b tool unsupported on 0.0.61 per reporter | Future compatibility change/hold among already authorized model/harness routes; native reproduction not run |
| [#1928](https://github.com/openinterpreter/openinterpreter/issues/1928) OPEN and [PR #1939](https://github.com/openinterpreter/openinterpreter/pull/1939) OPEN/UNMERGED | Gemini rejects `store` JSON payload; exact sanitizer fix under original PR | Preserve original issue/PR, not duplicate |
| [#1962](https://github.com/openinterpreter/openinterpreter/issues/1962) OPEN and [PR #1963](https://github.com/openinterpreter/openinterpreter/pull/1963) OPEN/UNMERGED | Catalog URL override precedence fix | Preserve static fix, no S4-grade upgrade from a generator patch |
| [#1981](https://github.com/openinterpreter/openinterpreter/pull/1981) OPEN/UNMERGED | Codex-main integration draft | Protect inherited upstream interfaces and owner boundary |
| [Goal PR #1971](https://github.com/openinterpreter/openinterpreter/pull/1971) and [#1975](https://github.com/openinterpreter/openinterpreter/pull/1975) MERGED | Current per-thread goal lifecycle and idempotent managed goals | Reuse budgets/owner checks, never infer new S3 or S4 decision from lifecycle persistence |
| [#1926](https://github.com/openinterpreter/openinterpreter/issues/1926) OPEN; [#1927](https://github.com/openinterpreter/openinterpreter/issues/1927) OPEN | Task verification truthfulness and SQL dialect-specific failure, not proof of current shared budget or S4 adoption | Separate native issue fixes; do not overload this adaptation actor |

Original source pinned current HEAD `382f615b907279be1b6518156ac2754d3c235ff4`. Old Index review_ref `f110a7a85f43efc343f936f5bc504e01eb262550` resolves to original, but historical grade is not current source reevaluation. The scenario is a reported user problem and proposed S4 loop is hypothetical.

## Function ownership

Main agent completes S1; optional MultiAgentV2 composes S2; Goals and user per-thread current status do not automatically form S3; Guardian is independent S3*; candidate S4 is prospective external provider compatibility, not a deterministic request retry. Its decision right is only scoped to allowlisted already authorized future routes and host-approved apply. The parent retains S5 policy and billing/credential decisions. No actor may bypass existing sandbox/Guardian nor silently create users, accounts or model spend.

## Parallel contribution-on-top review

- Evaluation object: one opt-in developer-composed S4 actor selecting a lawful future-turn route following a verified provider capability disturbance and learning from a later native task result.
- Existing-work overlap: native static routing and user selection, bundled provider catalog and exact original compatibility fixes under open PR #1939/#1963.
- Our on-top contribution: a first-party provenance-checked capability observation, configured composable decision owner with stay/hold/approved-select alternatives, host-validated return and later independent observed task outcome; no new generic model router/credentials.
- Incremental benefit: HYPOTHETICAL future decrease in repeated manual compatibility troubleshooting under #1982-like changes, strictly requiring a matched comparison against manual/native route.
- Decision scope: GO for this proposal-stage S4 construction hypothesis only; not an accepted implementation, present C grade, first-party test pass, PR or full project product judgment.

## Capability priority

P0 S4 accepted historical — to hypothetical developer-composable C, selected after all six functions. P1 native opt-in composition/permission/route bridge, typed compatibility facts, successful/failure after-run observation and comparator tests. P2 NONE. A user can still choose a model/harness manually; any proposed new S4 actor must show a materially distinct operational effect. No second function constructed by default.

## Implementation options

Use source-native [harness routing](https://github.com/openinterpreter/openinterpreter/blob/382f615b907279be1b6518156ac2754d3c235ff4/codex-rs/core/src/harness/routing.rs) and [model provider info](https://github.com/openinterpreter/openinterpreter/blob/382f615b907279be1b6518156ac2754d3c235ff4/codex-rs/model-provider-info/src/bundled_provider_catalog.rs); add only missing supported bridge for optional future route changes and an S4 decision lifecycle. Use extension turn/tool lifecycle where appropriate but do not assert a present public route-mutation API without native proof. Required positive later-effect test, parent veto/no-credential/sandbox negatives, trust/ambiguity fails closed. Native Rust, ACP, actual provider/model and cross-client checks NOT_RUN. No product implementation now.

## Specification and domain alternatives

No Profile/Skills semantic defect established. The distinct old [S3 case](https://github.com/opensiro-contributions/openinterpreter/blob/f98c5c04e944b8844f80a45c815bd3af61325bc0/.opensiro/issues/s3-current-commitments-20261119/roadmap.md) remains frozen as historical source: it rejected unfounded shared-budget allocation, and was consulted only after this S4 source-backed verdict. Original PR template requires placing inherited Codex changes upstream; source-specific integration must respect that. No independent domain fork needed.

## Cost experiment

NOT_MEASURED. Match actual original #1982-like tool workload, same privileges/available routes, native manual or exact PR fix versus optional S4 actor. Measure real task completion, approval/intervention, retries, billing/tokens, review, integration and maintenance; stop GO claim if native baseline is equal/better.

## Delivery and publication

[Human complete unpublished Issue](issue.md) ↔ [AI constructor](constructor-sufficiency.md) ↔ [README](README.md). This is a *new and different S4 object*; preserve old S3 proposal at its exact historic commit and stable case folder. Planned fork Issue title: Open Interpreter — bounded provider/harness prospective adaptation (OpenSiro roadmap). Destination if separately approved: https://github.com/opensiro-contributions/openinterpreter/issues . Current state **DRAFT — NOT PUBLISHED**. No original/fork public Issue/PR, implementation, Index re-assessment, external message, contribution record, native tests or measured benefit. AI-assisted source research. Fork authority `ACTIVE/ALLOW` is internal only.
