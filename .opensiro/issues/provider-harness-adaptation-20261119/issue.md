# Open Interpreter — bounded provider/harness prospective adaptation (OpenSiro roadmap)

**PLAN_ONLY · proposal-stage GO · research NEEDS_EVIDENCE · DRAFT — NOT PUBLISHED**

**One-sentence proposal:** Reuse Open Interpreter's existing provider/harness selection and session mechanisms to let a developer compose one optional, narrowly delegated S4 actor that selects among *already approved compatible routes* following an independently verified provider-capability disturbance, and checks the next real run before retaining the new choice.

**Target transition:** S4=— -> S4=C
**Proposal-stage decision:** GO
**Research disposition:** NEEDS_EVIDENCE

[roadmap.md](roadmap.md) — canonical receipt · [constructor-sufficiency.md](constructor-sufficiency.md) — AI/developer contract. Fork `opensiro-contributions/openinterpreter`, `.opensiro/issues/provider-harness-adaptation-20261119/` on `opensiro/meta`. This is a complete unpublished fork Issue draft, **not** an original-maintainer publication.

## 1. OpenSiro purpose and accepted baseline

OpenSiro tests whether VSM-informed reusable organizational construction can reduce the total effort of building, integrating, testing and maintaining agent harnesses. VSM adoption is optional. No cost reduction is measured.

**Accepted historic Index (not a current-HEAD regrade): `S1=A · S2=C · S3=— · S3*=C · S4=— · S5=—`.** [Immutable included assessment](https://github.com/opensiro/vsm-harness-index/blob/c2e43bf4750841277b3e58d8ba80314121734764/assessments/op/open-interpreter.md), Index `c2e43bf4750841277b3e58d8ba80314121734764`, blob `e892024abc1206554838d6a7330e385acf863524`, review `f110a7a85f43efc343f936f5bc504e01eb262550` (2026-09-15, last checked 2026-09-17); Profile 0.2.1 / Methodology 0.3.1. Current original `main@382f615b907279be1b6518156ac2754d3c235ff4`, observed 2026-11-19, is a newer Rust/Codex-derived system. Historical assessment age exceeds 30 days; an Index-owned reassessment is advisable, but this roadmap does not change grades.

**Boundary:** one configured Open Interpreter session/runtime with its native provider/harness catalog and supported ACP/TUI/SDK modes, optional multi-agent and Goal controls, sandbox/Guardian authorization. External model vendors, inherited upstream Codex governance, original maintainer organization and user-held policy rights are outside the S4 owner's authority. We screened the repository tree, Rust core/extension APIs, bundled provider catalog, routing, tests, user controls, root instructions, license, original Issues/PRs and security/PR policy, not a deployed live-provider session.

| Function / role | Historical Index state | Pinned current source and decisive owner | Independent priority |
| --- | --- | --- | --- |
| **S1 · Operations** | A | Agent executes file/tool work and checks within [core runtime](https://github.com/openinterpreter/openinterpreter/blob/382f615b907279be1b6518156ac2754d3c235ff4/codex-rs/core/src/harness/mod.rs) and sandbox; model/agent chooses work steps | NOT_SELECTED: no demonstrated additional C task-owner need |
| **S2 · Coordination** | C | Optional stable/default-disabled [MultiAgentV2](https://github.com/openinterpreter/openinterpreter/blob/382f615b907279be1b6518156ac2754d3c235ff4/codex-rs/core/src/tools/handlers/multi_agents_v2.rs) offers messaging, status, interrupts, follow-up | NOT_SELECTED: task coordination is already a composable option |
| **S3 · Inside-and-now** | — | [Goal extension](https://github.com/openinterpreter/openinterpreter/blob/382f615b907279be1b6518156ac2754d3c235ff4/codex-rs/ext/goal/src/extension.rs) handles per-thread goal/status/budget/continuation and [agent control](https://github.com/openinterpreter/openinterpreter/blob/382f615b907279be1b6518156ac2754d3c235ff4/codex-rs/core/src/tools/handlers/multi_agents_v2/list_agents.rs) exposes statuses, not proven whole-organization shared priorities | DEFER: no evidence for new shared-budget autonomy; simpler current Goal/user control |
| **S3* · Independent audit** | C | [Guardian](https://github.com/openinterpreter/openinterpreter/blob/382f615b907279be1b6518156ac2754d3c235ff4/codex-rs/core/src/guardian/mod.rs) supplies separate approval reviews and binding denials under host policies | NOT_SELECTED: distinct S3* reviewer already exists; not task-outcome auditor by assumption |
| **S4 · Outside-and-then** | — | [Provider catalog](https://github.com/openinterpreter/openinterpreter/blob/382f615b907279be1b6518156ac2754d3c235ff4/codex-rs/model-provider-info/src/bundled_provider_catalog.rs), [harness routing](https://github.com/openinterpreter/openinterpreter/blob/382f615b907279be1b6518156ac2754d3c235ff4/codex-rs/core/src/harness/routing.rs) and user `/model` / `/harness` choices; no demonstrated *agent-composed prospective adaptation-and-feedback* | **P0:** bounded C capability using these native surfaces |
| **S5 · Identity and policy** | — | Human/configured host decides allowed models, credentials, spending, sandbox and ultimate policy; [PR/governance boundary](https://github.com/openinterpreter/openinterpreter/blob/382f615b907279be1b6518156ac2754d3c235ff4/.github/pull_request_template.md) remains external | NOT_SELECTED: do not delegate new authority |

These are ownership categories, not a score ladder. No deliberate refusal to implement S4 is inferred from historical `—`. Maintainer interest in **this** proposal: NOT_STATED. A recorded user failure is not approval to implement.

## 2. Observed scenario, proposed change, minimal user outcome

**Scenario basis:** a user reports on Open Interpreter 0.0.61 that [Ollama Qwen3.5:9b rejects tool calls](https://github.com/openinterpreter/openinterpreter/issues/1982) with the native harness. Older [Gemini JSON-body failure #1928](https://github.com/openinterpreter/openinterpreter/issues/1928) and [provider catalog URL drift #1962](https://github.com/openinterpreter/openinterpreter/issues/1962) show different compatibility modes. These are *reported*, not re-executed here. They do **not** show that every model has a legal fallback or that S4 is already operating.

A developer wants a **strictly opt-in** source-native adaptation component for a configured project/session with at least two pre-approved usable provider/harness routes. When an authenticated compatibility observation arrives, it could choose **stay**, **hold**, or **one allowed route change for future work**, enforce the choice through existing host configuration/approval, then observe whether a *later* real task works. No new credentials, hidden model purchases, blanket retry loops or bypass of required tool review. A manual `/model` or `/harness` switch remains the baseline.

**P0:** `S4=— -> S4=C` optional prospective provider/harness compatibility adaptation, with a developer-selected decision actor and closed future-outcome feedback. The *complete minimum path* is: redacted source-pinned external capability signal + current route/candidate context → an independently composed S4 selector exercising permitted alternatives → host-validated session/future-turn route selection or hold → subsequent native task evidence → revised subsequent S4 choice. This is a design, not a shipped API or proven model capability.

## 3. Parallel original-native Track A vs on-top Track B

| Track A: native shipped / pending | Track B: minimum original-owned contribution on top | Incremental benefit / falsifier |
| --- | --- | --- |
| SHIPPED: [routing.rs](https://github.com/openinterpreter/openinterpreter/blob/382f615b907279be1b6518156ac2754d3c235ff4/codex-rs/core/src/harness/routing.rs) and [README harness/model UI](https://github.com/openinterpreter/openinterpreter/blob/382f615b907279be1b6518156ac2754d3c235ff4/README.md) | Reuse routing and existing selection; add scoped prospective decision/feedback only, never another router | Current path supports manual selection. Distinct benefit only if validated future adaptation avoids repeated user troubleshooting at acceptable cost |
| SHIPPED: generated [provider catalog](https://github.com/openinterpreter/openinterpreter/blob/382f615b907279be1b6518156ac2754d3c235ff4/codex-rs/model-provider-info/src/bundled_provider_catalog.rs) | Reuse vetted capabilities as claims but require live/verified compatibility receipts before changed decision | Catalog entries alone are not reliable proof a particular local model can call tools |
| OPEN original [#1982](https://github.com/openinterpreter/openinterpreter/issues/1982) | On specific unsupported-tool failure, selector considers already allowed compatible fallback, or explicit HOLD | Falsifier: simple permanent provider fix or manual model switch achieves same future task |
| OPEN original [PR #1939](https://github.com/openinterpreter/openinterpreter/pull/1939) for [#1928](https://github.com/openinterpreter/openinterpreter/issues/1928) | Let the original exact JSON-body correction land separately; do **not** replace its request sanitizer | A new controller must solve later changing capability choices beyond this specific fixed field |
| OPEN original [PR #1963](https://github.com/openinterpreter/openinterpreter/pull/1963) for [#1962](https://github.com/openinterpreter/openinterpreter/issues/1962) | Reuse explicit catalog-override precedence when accepted, not duplicate it | Static source URL correction is not a dynamic S4 option/feedback loop |
| OPEN original [PR #1981](https://github.com/openinterpreter/openinterpreter/pull/1981) Codex sync; merged native Goal [#1971](https://github.com/openinterpreter/openinterpreter/pull/1971)/[#1975](https://github.com/openinterpreter/openinterpreter/pull/1975) | Preserve parent/upstream compatibility and per-thread budget/scope; do not miscast Goal automation as S4 | New extension must not duplicate Goal CAS or invent S5 powers |

**Distinctness:** Track A solves individual static compatibility defects and lets the user pick routes. Track B is only interesting if *independent future-facing choice with alternate legal actions and verified later feedback* proves better than those minimal existing solutions. The reported original issues support investigation; economic and downstream operational gain remain hypothetical.

## 4. Priorities, minimal sufficiency and decision

**P0:** optional S4 prospective compatibility selector with restricted actual route choices and later-run corrective feedback, selected ahead of S3 (no witnessed shared budget collision), S3* (existing separate auditor), S1/S2 (already operating/composable), S5 (legitimate human owner). **P1:** native observation/decision attachment and host-validated configuration bridge; allowlist and explicit authority; truthful later-run receipts; isolated native control and negative tests, plus comparison against manual/user routing. **P2:** NONE. No extra new VSM function.

**C sufficiency is a proposal, not established implementation.** The current original already has core native parts (route selection and runtime outcome visibility), but the developer-composable **S4 independent prospective decision** and **returned later outcome** need to be built/verified. This GO means the bounded *construction hypothesis* is worth native validation, not that it is available. The strongest falsifier is a same-task test where a static compatible route, a simple original bugfix or manual selection gives equal or better outcome at lower total cost.

## 5. Acceptance and stop

**Proposed positive test:** Pin a first-party failure in issue #1982's local-provider mode; two routes are explicitly approved and one is known to support the required task/tool contract. Without crossing a user permission boundary, the installed S4 actor identifies the present compatibility failure, chooses the allowed future route, the host applies it for a later turn, and a real later tool-dependent task succeeds with an attributable source/decision/approval/result receipt. Test alternate allowed HOLD and restored route. Compare with manual route selection.

**Negative tests:** unsupported alternative, stale/untrusted catalog, unavailable model, missing credential, ambiguous cause, user veto, revoked allowlist, accidental paid provider, or mismatched task → HOLD/no mutation, no fake success. A different user/project cannot be affected. A normal static bug like #1928 must still be fixed in the existing native request path, not masked by a new fallback.

**Validation:** NOT_RUN. Proposed verification is conditional and requires real original native tests/host/provider access; no model/agent run, cost savings or implementation performed.

## 6. Independent paths and cost

The original's [PR template](https://github.com/openinterpreter/openinterpreter/blob/382f615b907279be1b6518156ac2754d3c235ff4/.github/pull_request_template.md) reserves Open Interpreter-specific provider/harness adaptation for this repository, while generic Codex runtime changes should go to `openai/codex`. This proposed work remains *design-only*; no original issue/PR or public fork Issue is opened. Profile/Skills or domain-fork changes: NONE established.

Compare actual user intervention, success of future tasks, time, tokens, retries, model billing, engineering complexity and later maintenance against the manual/simple-fix comparator. **Cost status: NOT_MEASURED**.

## 7. Historical comparison (only after independent decision)

A previous, separate [S3 shared-current-budget NO_GO](https://github.com/opensiro-contributions/openinterpreter/blob/f98c5c04e944b8844f80a45c815bd3af61325bc0/.opensiro/issues/s3-current-commitments-20261119/roadmap.md) explored a supervisor with no witnessed resource conflict. This new object addresses **S4 external-provider compatibility over time**, not S3 allocation. Therefore **old S3 NO_GO is preserved**, and it is not rewritten or reported as an S4 verdict. The current #58 re-run chooses an alternative source-grounded P0, `S4=— -> S4=C` **GO / NEEDS_EVIDENCE**.

## 8. Rights, publication and handoff

Original Apache-2.0 [LICENSE](https://github.com/openinterpreter/openinterpreter/blob/382f615b907279be1b6518156ac2754d3c235ff4/LICENSE), NOTICE, [security policy](https://github.com/openinterpreter/openinterpreter/blob/382f615b907279be1b6518156ac2754d3c235ff4/SECURITY.md) and [original PR template](https://github.com/openinterpreter/openinterpreter/blob/382f615b907279be1b6518156ac2754d3c235ff4/.github/pull_request_template.md) were reviewed; no claim that inherited Codex/third-party provider rights or CLA/DCO personal formalities are cleared. Fork metadata `ACTIVE/ALLOW` permits OpenSiro case writes only. A public GitHub Issue, original maintainer message, external PR, implementation or grade change requires separate authorization/review. Prepared with AI assistance; no first-party tests or human independent reviewer pass claimed.
