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

1. **State and alternatives (native-specific revision).** Root opts into a bounded MultiAgentV2 next-turn selection policy for child paths within one `SessionId`. Existing `list_agents` gives `AgentStatus`, not a reliable queued commitment. Propose the *smallest* revisioned pending-follow-up intent for a supported root/child path and explicit priority; the composed policy chooses which pending child to admit next or defer when V2 `max_threads` is contested. Direct goal reassignment or global cross-session budgets are out of the minimal P0 scope.
2. **Decisive actor and owner.** Proposed developer-composed session-root V2 turn-admission policy independently chooses a permitted *next* child turn (or hold) based on current V2 work; static `max_threads` only enforces a ceiling. An opt-in extension wired to existing `LocalAgentControl` is preferable to a generic second control plane; root authorization and Guardian remain distinct. Existing root context is not itself an authorization grant.
3. **Lawful effect.** Add a **proposed**, root-authorized and revision-checked V2 admission/permit seam *at the real turn start* (existing `agent/control/execution.rs`) before reusing `agent/control/delivery.rs` `TriggerTurn` to the selected child. Preserve `AgentPath` resolution, root restrictions, Guardian, static `max_threads` and rollout budget. Existing `send()` plus `DeliveryReceipt` is not an atomic commitment update or proof of child execution; no such interface is claimed shipped.
4. **Return to operation.** Track the submitted intent and verified subsequent child `AgentStatus` via `subscribe_status`, and a genuine terminal outcome through [completion.rs](https://github.com/openinterpreter/openinterpreter/blob/7a5509e307cc56d66f5c7413955bb387ab895815/codex-rs/core/src/agent/control/completion.rs) if observed. That parent notification is **best effort** and carries no proposed admission ID today: matching/recovery is new work. Missing delivery, rejected permit or uncorrelated completion => `UNKNOWN / NOT_APPLIED`, never a fabricated completed decision.
5. **Optionality.** Off by default; default runtime/ACP/provider harness semantics and original control obligations unchanged. Root revocation immediately prevents further effect.

The **minimum missing work** is a root-scoped opt-in V2 policy registration, revisioned pending-follow-up intent, **atomic** next-turn permit/decision integrated with `LocalAgentControl` and `execution.rs`, checked native delivery and correlated outcome/retry. This is **not** a new global scheduler, generic reassign API or second storage subsystem. These seams are proposed; current Rust source does not prove they exist or that effect/feedback is guaranteed.

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


## v0.18.1 native-specific critical review (same stable case)

This is a **post-v0.18.1 self-review**, not a fresh independent Wave 4 first attempt or a new Index assessment. [Patch protocol at 14973244](https://github.com/opensiro/upstream/commit/14973244a474cc643c01ce04d70913f51c714b74) recommends source-native details without a new score/gate. Original first-party `main@7a5509e3` and open #1973/#1981 heads remain the same. See [roadmap.md](roadmap.md) for the canonical narrowed P0/P1/P2 and full source mapping.

| Specific first-party seam | Actually shipped | Additional minimal proposed native contract |
| --- | --- | --- |
| `tools/handlers/multi_agents_v2/list_agents.rs` → `LocalAgentControl::list_agents` | V2 path-scoped agent names/statuses | Trusted pending-follow-up *intent*, including current priority and revision, is **not** present |
| `agent/control/execution.rs` | V2-subagent `max_threads`, `ensure_execution_capacity`, `execution_guard`; count/permit release | Checked **atomic** policy-picked admission at next real turn start; current `has_capacity` then `guard` alone does not prove a serialized selection |
| `agent/control/delivery.rs` | Resolves caller and agent path, `TriggerTurn` sends via native communication, returns submission receipt | Caller/root-authorized pending-intent selection + revision check; submission is not successful run/completion |
| `agent/control.rs` | `subscribe_status`, `get_status`, `interrupt_agent` and token usage info | Link the chosen child/turn to the V2 decision and revise **next** selection on actual result, not on textual prediction |
| `agent/control/completion.rs` | Best-effort terminal child notification to parent | Correlated outcome verification or explicit unknown/retry when an expected return is lost |
| `agent_message_board.rs` | Optional SQLite board for active sessions; does **not** wake idle children | Do not use it as an invented native scheduler or assume its notifications enact a turn |
| `agent/control/user_authorization.rs` / Guardian | Bounded root context and independent Guardian controls | Explicit opt-in root policy rights; no silent S5/Guardian privilege transfer |

**Concrete future user capability, if implemented:** Under MultiAgentV2 with `max_threads=1`, an authorized root can install a developer-composed policy that picks which of two pending child follow-ups runs next. Its priority choice must influence an actual subsequent turn, preserve the cap and forbidden actions, and receive outcome feedback that changes the following decision. This is a specific **root-session V2 admission** construction, not an all-purpose task manager.

**Native tests to write later (NOT_RUN):** same two child paths under V2; baseline direct parent follow-up and `AgentLimitReached` compared against opt-in priority A then B. Assert (1) priority can select two different lawful next turns without violating cap, (2) rival admissions cannot both acquire the same permit, (3) stale revision and revoked root action fail closed, (4) `DeliveryReceipt` alone is not treated as completed work, (5) missing best-effort terminal notice produces honest UNKNOWN and bounded recovery, (6) root/Guardian and ordinary mode remain unchanged. Native tests/implementation have **not** been performed; actual constructor sufficiency remains hypothesis-only.

**Verdict:** Keep proposal-stage `GO / NEEDS_EVIDENCE` as **architectural possibility** only, with the narrowed native-specific P0 and **P2 NONE**. If authorized effect or returned feedback cannot be made coherent in V2 without violating original constraints, the exact same case must be reconsidered as a scoped `NO_GO` or documented mandatory `BLOCKED`; this recommendation adds **no new metric or gate**. Product choices remain with the original maintainer.
