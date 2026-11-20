# Open Interpreter — S3=C source-native constructor sufficiency

**Target transition:** S3=— -> S3=C
**Proposal-stage decision:** GO
**Research disposition:** NEEDS_EVIDENCE

**AI technical contract, not a second assessment table.** Human [issue.md](issue.md) · canonical [roadmap.md](roadmap.md). First-pass independent verdict was frozen before reading prior fork case; original HEAD 7a5509e307cc56d66f5c7413955bb387ab895815, historical included Index 308548ec89534590f948bc75dd61887e992a3756, protocol 28ea2cce06b517bc4550dceddb00210b1e0dc85c. The canonical receipt alone owns the historical vector and six-function dispositions.

## Function/authority boundary
System in focus is first-party runtime session and child threads. Disturbance = hypothetical competing current commitments/capacity under the same root, not mere agent-message collisions. S1 children execute; S2 transports and caps interference; S3 proposed supervisor owns a **developer-composed** live whole-session priority/resource decision and has a legitimate returned change; S3* Guardian retains independent approval and S5 parent retains ultimate policy; S4 prospective provider adaptation is out of scope.

At runtime today [LocalAgentControl](https://github.com/openinterpreter/openinterpreter/blob/7a5509e307cc56d66f5c7413955bb387ab895815/codex-rs/core/src/agent/control.rs) owns status and inspected token usage, agents may be interrupted, communication may trigger a turn, and [completion.rs](https://github.com/openinterpreter/openinterpreter/blob/7a5509e307cc56d66f5c7413955bb387ab895815/codex-rs/core/src/agent/control/completion.rs) feeds parent outcome. [execution.rs](https://github.com/openinterpreter/openinterpreter/blob/7a5509e307cc56d66f5c7413955bb387ab895815/codex-rs/core/src/agent/control/execution.rs) enforces static limits without choosing what the organization should prioritize. [budget.rs](https://github.com/openinterpreter/openinterpreter/blob/7a5509e307cc56d66f5c7413955bb387ab895815/codex-rs/core/src/agent/control/budget.rs) tracks fixed usage/reminders. These are reusable ports, not already a demonstrated autonomous S3 manager.

## Track A: native first-party coverage and overlap
| Status | Source and coverage | Limit for S3 |
| --- | --- | --- |
| SHIPPED | [V2 tool handlers](https://github.com/openinterpreter/openinterpreter/blob/7a5509e307cc56d66f5c7413955bb387ab895815/codex-rs/core/src/tools/handlers/multi_agents_v2.rs), spawn/list/communicate/wait | per-child communication and observation |
| SHIPPED | [agent-control](https://github.com/openinterpreter/openinterpreter/blob/7a5509e307cc56d66f5c7413955bb387ab895815/codex-rs/core/src/agent/control.rs), [execution limiter](https://github.com/openinterpreter/openinterpreter/blob/7a5509e307cc56d66f5c7413955bb387ab895815/codex-rs/core/src/agent/control/execution.rs) | deterministic capacity, status, interruptions but no independent whole-session policy decision |
| SHIPPED | [Guardian review](https://github.com/openinterpreter/openinterpreter/blob/7a5509e307cc56d66f5c7413955bb387ab895815/codex-rs/core/src/guardian/review.rs) and [root authorizations](https://github.com/openinterpreter/openinterpreter/blob/7a5509e307cc56d66f5c7413955bb387ab895815/codex-rs/core/src/agent/control/user_authorization.rs) | other decision rights; not a substitute S3 allocator |
| OPEN / NOT_SHIPPED | [PR #1973](https://github.com/openinterpreter/openinterpreter/pull/1973) @ 4d86fdf4b06a1b24b5884db5c56b9f5e2f79f6d7 | Goal CAS could help concurrency but no autonomous whole-session controller |
| OPEN / NOT_SHIPPED | [PR #1981](https://github.com/openinterpreter/openinterpreter/pull/1981) @ ed0e5147a6d770975a025a7f8461939706a7e4dc | broad Codex sync may change API shape |
| OPEN ISSUE | [#1926](https://github.com/openinterpreter/openinterpreter/issues/1926), [#1927](https://github.com/openinterpreter/openinterpreter/issues/1927) | distinct S1 task truth/completion defects |

## Track B: minimum complete C construction

1. **State and alternatives.** Root opts in, supplies enforceable policy envelope and shared-session scope. Collect a trusted versioned current-commitment view mapping child thread, assigned objective, status, quota and last returned outcome. Alternatives include keep, defer, reassign, or interrupt a lower-priority child. Avoid false atomicity: versions, retry and stale-target rejection must be explicit.
2. **Decisive actor and owner.** New pluggable session-scoped autonomous supervisory policy chooses among those alternatives based on observed current state; not static max_threads, not an S1 agent's ordinary prompt and not Guardian. An extension/crate with a minimal first-party checked control seam is preferred by [AGENTS.md](https://github.com/openinterpreter/openinterpreter/blob/7a5509e307cc56d66f5c7413955bb387ab895815/AGENTS.md).
3. **Lawful effect.** A capability-scoped root-approved action maps decision to existing checked agent-control send/followup/interrupt where possible, plus the minimum versioned commitment update needed to hold a choice. No unsanctioned cross-session mutation, no bypass of user approval, Guardian denial or hard budget limits. Do not infer a missing seam already exists.
4. **Return to operation.** Correlate action receipt to the next real child turn status and [terminal result](https://github.com/openinterpreter/openinterpreter/blob/7a5509e307cc56d66f5c7413955bb387ab895815/codex-rs/core/src/agent/control/completion.rs), mark whether effect actually occurred, and autonomously re-evaluate next time. Failed or absent feedback is a non-completion, not synthetic success.
5. **Optionality.** Off by default; default runtime/ACP/provider harness semantics and original control obligations unchanged. Root revocation immediately prevents further effect.

The **minimum missing work** is a first-party extension policy registration, versioned shared commitment state, scoped checked assignment/effect and outcome correlation; most low-level actor messaging/status/interrupt is already present. Source-native names are conceptual; no unimplemented Rust function or perfect atomicity is claimed as shipped.

## Alternative hypotheses and falsification
- Reconfigure native max_threads, budget rules or just add message-board priority: cheaper comparator but deterministic S2/enforcement, not independently composable S3=C.
- Current root model choosing each worker action manually: baseline and may be adequate to product owner, but not a separate source-native configurable S3 decision actor.
- Cross-provider routing: unrelated S4 hypothesis; not P0.
- Equivalent existing shipped autonomous S3 manager or inability to enact root-authorized change and observe a later child outcome would **falsify this GO**. First-party maintainers control adoption; native pending PRs and observed bug issues do not by themselves prove a permanent design intention.

## Unrun source-native acceptance and negative controls
- **Positive:** two child tasks collide over an operator-configured current quota; at identical starting state controller chooses one of two admissible global commitment policies, effects are applied, outcomes observed; a changed outcome leads to a different next choice.
- **Authorized but stale:** status or commitment revision moved; the action fails/re-evaluates rather than overwrite newer work.
- **Unauthorized/revoked:** non-root controller or wrong subtree cannot move a child's commitment; no S5 grant or Guardian privilege override; hard child limits still block excess work.
- **Failure/compatibility:** interrupted or missing child, failed message delivery, missing terminal outcome, ordinary no-supervisor default and ACP sessions remain safe.
- **Comparator:** static native limiter plus human/root messages on same tasks; measure correctness, effect, added complexity, token/runtime/cost. Use focused Rust integration tests then contributor-required just test on product implementation only.

**Tests:** NOT_RUN. **Implementation:** NOT_DONE. **Cost:** NOT_MEASURED. **Historical comparison:** earlier S3 NO_GO evaluated desirability/absence of observed conflict; neutral Wave 4 structurally justifies a hypothetical C construction and keeps old caution. **Publication:** DRAFT — NOT PUBLISHED.
