# AI/developer constructor — Open Interpreter future compatibility S4

**Target transition:** S4=— -> S4=C
**Proposal-stage decision:** GO
**Research disposition:** NEEDS_EVIDENCE

**Human roadmap:** [issue.md](issue.md). **Canonical source of truth:** [roadmap.md](roadmap.md). This is a PLAN_ONLY proposal, **not code**.

## 1. Source and decisive owner

Pinned original `openinterpreter/openinterpreter@382f615b907279be1b6518156ac2754d3c235ff4`; Index `c2e43bf4750841277b3e58d8ba80314121734764`, assessment blob `e892024abc1206554838d6a7330e385acf863524`, reviewed 2026-09-15, Profile 0.2.1/Methodology 0.3.1, included vector anchored in [roadmap.md](roadmap.md). Configured Open Interpreter Rust session via TUI, ACP or exec mode; do not infer feature parity across client modes. External providers and operator-controlled credentials are outside the autonomous owner. S4 prospective choices cannot grant S5 policy.

Current [feature flags](https://github.com/openinterpreter/openinterpreter/blob/382f615b907279be1b6518156ac2754d3c235ff4/codex-rs/features/src/lib.rs) show Goals stable/default enabled, MultiAgentV2 stable/default disabled, GuardianApproval stable/default enabled. [Core routing](https://github.com/openinterpreter/openinterpreter/blob/382f615b907279be1b6518156ac2754d3c235ff4/codex-rs/core/src/harness/routing.rs) selects a route by `WireApi` and `Harness` and validates unsupported combinations; [README](https://github.com/openinterpreter/openinterpreter/blob/382f615b907279be1b6518156ac2754d3c235ff4/README.md) documents `/model` and `/harness`. [Bundled catalog](https://github.com/openinterpreter/openinterpreter/blob/382f615b907279be1b6518156ac2754d3c235ff4/codex-rs/model-provider-info/src/bundled_provider_catalog.rs) and [generator](https://github.com/openinterpreter/openinterpreter/blob/382f615b907279be1b6518156ac2754d3c235ff4/codex-rs/scripts/write_provider_catalog.py) are provider metadata, **not** an autonomous prospective decision owner. Reported [#1982](https://github.com/openinterpreter/openinterpreter/issues/1982) is an observed user problem, not a live reproduction in this review.

## 2. Function-specific constructor and scope

Minimum first-party original-native change if further qualified:

1. **Observation / provenance:** a narrowly typed and redacted `compatibility_failure` event for unsupported tools/wire/harness in the actual configured runtime; preserve provider, model, harness, version, credential-free route identity and error-class provenance, treating catalog facts as fallible. Do not accept untrusted model output as compatibility proof.
2. **Developer-composed prospective decision:** an opt-in S4 decision actor registered against a developer-authored allowlist of already accessible `provider/model/harness` candidates and constraints. It may choose only `stay`, `hold`, or `switch-for-future-turn`, not create a credential, buy a model, change sandbox/Guardian or override owner constraints. This actor must make a context-dependent choice among alternatives; a hardcoded retry switch or plain config map is not C.
3. **Host-enforced operational effect:** validate chosen route against [native routing](https://github.com/openinterpreter/openinterpreter/blob/382f615b907279be1b6518156ac2754d3c235ff4/codex-rs/core/src/harness/routing.rs) and current session/config owner before changing a future turn. If a supported client cannot apply the change without new host work, *add the smallest original-native session override bridge* rather than claiming a present API exists. Preserve current turn's failed receipt; no silent replay of side-effecting tool calls. On rejected/unknown decision do nothing.
4. **Feedback to S4:** observe actual next applicable task/turn, successful relevant tool calls and explicit failures, attribute to source/decision/host-approval/route and feed it back to the same bounded S4 actor so it can revise or revoke subsequent choices. Do not treat a 200 HTTP response or a config write alone as task success.
5. **Safe fallback:** if no approved alternative, fact is stale/untrusted, or next operation fails, report HOLD/error to user and continue with normal native controls after human choice. Never claim independent S5 authority or automatic coverage of all providers.

The five steps describe **logical evidence and decision edges**, not existing interfaces or a required five-port schema. Code ownership is Open Interpreter-specific adapter, not modification of upstream Codex core unless accepted by the relevant owner. Native `S1/S2/S3/S3*/S5` dispositions are in Human and receipt; no second six-row rating here.

## 3. Track A vs Track B and required delta

- **SHIPPED:** [core harness routing](https://github.com/openinterpreter/openinterpreter/blob/382f615b907279be1b6518156ac2754d3c235ff4/codex-rs/core/src/harness/routing.rs), model/provider catalog, UI model and harness switching, goal budgeting, Guardian, extension lifecycle. Manual switch is best current simple counterfactual.
- **OPEN ISSUE:** [#1982](https://github.com/openinterpreter/openinterpreter/issues/1982) describes tool unsupported in Ollama + Qwen3.5:9b on 0.0.61; actual terminal/native reproduction not performed.
- **OPEN ISSUE with OPEN_PR:** [#1928](https://github.com/openinterpreter/openinterpreter/issues/1928) → [#1939](https://github.com/openinterpreter/openinterpreter/pull/1939) repairs exact Gemini JSON `store` request; [#1962](https://github.com/openinterpreter/openinterpreter/issues/1962) → [#1963](https://github.com/openinterpreter/openinterpreter/pull/1963) repairs catalog URL override precedence. They are **unmerged** at inspection, and narrow defects; do not call them shipped.
- **OPEN PR:** [#1981](https://github.com/openinterpreter/openinterpreter/pull/1981) upstream Codex sync; prohibit overlapping speculative core refactors. Native Goal PR [#1971](https://github.com/openinterpreter/openinterpreter/pull/1971) and [#1975](https://github.com/openinterpreter/openinterpreter/pull/1975) merged, are lifecycle/identity primitives, not S4 future-option choice.
- **On-top new delta:** optional lawful prospective choice and later observation across *already approved* routes; does not replace product-specific bug fixes or build another router. The exact provider/host interface must be validated with original tests and maintainers before implementation.

**Independent scenario basis: HYPOTHETICAL actor over source-reported failures.** Incremental operator outcome is fewer repeated manual compatibility interventions over multiple tasks while preserving strict permissions; not yet measured. Falsifier: the current manual/static-fix path performs equally well or better, route switch lacks rights, no repeatable later-work feedback, or the actor's decision cannot be composed inside the first-party supported mode.

## 4. P0, P1, P2

**P0:** bounded developer-composed S4 compatibility actor with choose/apply/observe next-run feedback, source-grounded plan-only GO.

**P1:** (a) prove actual native error-class-to-capability signal and allowlist/right semantics; (b) identify original-owned supported client switch-for-next-turn bridge without modifying inherited Codex behavior; (c) demonstrate a *real* two-route comparator and attributable subsequent task evidence; (d) focused regression/safety tests; (e) independent code review and operator agreement when required. These are future tests/dependencies, **not completed**.

**P2:** NONE. No mandatory extra S3 supervisor, independent S3* audit, S5 delegated policy or second function.

## 5. Future native acceptance / falsification (NOT RUN)

| Case | Observable success | Failure / invalid claim |
| --- | --- | --- |
| Reported Qwen tool mismatch + explicitly allowed compatible second route | Actor chooses future route only, native host applies authorized change, a later tool-dependent task succeeds and supplies evidence receipt | Just logging, repeating the failing tool, switching without proof or claiming success on config write |
| Same input with explicit `hold` | No mutation, action stops truthfully, preserved original failure | Silent fallback or future task executed on unauthorized provider |
| Repeated disagreement / stale catalog | Fact rejected, explicit uncertainty, next choice revised only from real run outcome | Catalog title or LLM assertion treated as trusted truth |
| Host veto, revoked allowance, unavailable credential, new billing | No external side effect, no new permission, no cross-user mutation | Unapproved model, hidden credential access, changed Guardian/sandbox |
| Original #1928 static protocol defect, with or without separate PR #1939 | Exact native fix/manual baseline preferred | New autonomous controller introduced solely to paper over JSON field |
| Later-run tool failure after apparently successful reroute | Receipt is failure and feeds next bounded S4 choice | Empty response/HTTP success treated as task completion |
| No S4 actor configured | Existing `/harness` and `/model` behavior unchanged | Normal workflows fail or falsely claim S4=C active |

Tests need real local Ollama and compatible alternative **only if legally/configurationally available**, plus unit fixtures and app-server/ACP+TUI integration. Do not claim a validated provider compatibility matrix, native test PASS, cost estimate, newly shipped C or Index state. All actual code tests **NOT_RUN**.

## 6. Rightful boundaries and historic comparison

The [original PR template](https://github.com/openinterpreter/openinterpreter/blob/382f615b907279be1b6518156ac2754d3c235ff4/.github/pull_request_template.md) directs generic Codex core changes upstream and reserves Open Interpreter-specific provider/harness for this repo. [License](https://github.com/openinterpreter/openinterpreter/blob/382f615b907279be1b6518156ac2754d3c235ff4/LICENSE) Apache-2.0; SEC disclosure for security bugs requires private original maintainer route. Do not copy external pack/source or publish without separate consent.

Previous [S3 current-resource NO_GO](https://github.com/opensiro-contributions/openinterpreter/blob/f98c5c04e944b8844f80a45c815bd3af61325bc0/.opensiro/issues/s3-current-commitments-20261119/roadmap.md) was inspected *only after* independent S4 proposal: different evaluation object, not contradictory proof. Keep it immutable. `ACTIVE/ALLOW` fork metadata authorizes case persistence only. No original issue, public fork issue, external PR, contributor record, product patch or reassessment has occurred. No future continuous monitoring was started.

**Cost status: NOT_MEASURED.**
