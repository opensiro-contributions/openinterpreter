# Capability Roadmap Receipt — Open Interpreter, neutral Wave 4 S3 case

## Identity and pins
- Receipt contract: proposal-gate
- Original repository: openinterpreter/openinterpreter
- Original HEAD: 7a5509e307cc56d66f5c7413955bb387ab895815
- Observed at: 2026-11-20
- Accepted Index assessment: https://github.com/opensiro/vsm-harness-index/blob/308548ec89534590f948bc75dd61887e992a3756/assessments/op/open-interpreter.md
- Accepted assessment blob SHA: e892024abc1206554838d6a7330e385acf863524
- Accepted review ref: f110a7a85f43efc343f936f5bc504e01eb262550
- Accepted reviewed at: 2026-09-15
- Accepted Index commit: 308548ec89534590f948bc75dd61887e992a3756
- Accepted VSM vector: S1=A · S2=C · S3=— · S3*=C · S4=— · S5=—
- Profile version: 0.2.1
- Assessment procedure version: 0.3.1
- Upstream protocol: https://github.com/opensiro/upstream/commit/28ea2cce06b517bc4550dceddb00210b1e0dc85c
- System in focus: First-party Open Interpreter Rust coding agent, subagent control, collaboration and Guardian; not external providers, Interpreter Workstation or maintainer policy.
- Repository-wide source map: README, AGENTS, docs/subagents, docs/harness, docs/auto-review, core tasks/agent-control/Guardian/tool handlers, configurations and tests, original Issues 1926 and 1927 and original open PRs 1973 and 1981. First-party source is distinct from adjacent inherited Codex and external provider governance.
- Evaluation object: Same existing stable S3 current shared-budget and commitment arbitration case; independent post-release first-pass verdict frozen locally before reading old case.
- Scenario basis: HYPOTHETICAL
- Result: NEEDS_EVIDENCE

## Rights and authority
- Fork: opensiro-contributions/openinterpreter (verified matching parent; opensiro/meta only).
- Owner control: ACTIVE / ALLOW at last readback; re-read immediately before write.
- Decisive proposed S3 authority: opt-in autonomous session-scoped supervisor, authorized by the root user/controller within configured objectives, capacity and priority envelopes, with no authority to change root permissions, Guardian decisions or parent S5.
- Effect boundary: **PROPOSED, NOT SHIPPED** root-authorized and revision-checked MultiAgentV2 turn-admission decisions at the session's existing agent-control boundary; current send/interrupt APIs are not a commitment transaction and cannot by themselves prove effect or complete feedback.
- External issue: DRAFT — NOT PUBLISHED
- Product source edit: NOT_DONE
- Native tests: NOT_RUN
- Cost status: NOT_MEASURED

## Existing work / overlap
- Shipped V2 coordination: [multi-agents tools](https://github.com/openinterpreter/openinterpreter/blob/7a5509e307cc56d66f5c7413955bb387ab895815/codex-rs/core/src/tools/handlers/multi_agents_v2.rs), [list_agents](https://github.com/openinterpreter/openinterpreter/blob/7a5509e307cc56d66f5c7413955bb387ab895815/codex-rs/core/src/tools/handlers/multi_agents_v2/list_agents.rs), [message board](https://github.com/openinterpreter/openinterpreter/blob/7a5509e307cc56d66f5c7413955bb387ab895815/codex-rs/core/src/agent_message_board.rs). These perform communication and status observation; they do not document an independent repeatedly choosing whole-session priority/budget owner.
- Shipped local limiter: [agent execution](https://github.com/openinterpreter/openinterpreter/blob/7a5509e307cc56d66f5c7413955bb387ab895815/codex-rs/core/src/agent/control/execution.rs) limits child turn concurrency; [budget](https://github.com/openinterpreter/openinterpreter/blob/7a5509e307cc56d66f5c7413955bb387ab895815/codex-rs/core/src/agent/control/budget.rs) enforces configured usage; neither is a composable current shared-commitment S3 actor.
- Action/feedback substrate: [agent control](https://github.com/openinterpreter/openinterpreter/blob/7a5509e307cc56d66f5c7413955bb387ab895815/codex-rs/core/src/agent/control.rs) exposes inspect, subscription, token usage and interrupts; [delivery](https://github.com/openinterpreter/openinterpreter/blob/7a5509e307cc56d66f5c7413955bb387ab895815/codex-rs/core/src/agent/control/delivery.rs) applies allowed communication, [completion](https://github.com/openinterpreter/openinterpreter/blob/7a5509e307cc56d66f5c7413955bb387ab895815/codex-rs/core/src/agent/control/completion.rs) returns terminal results.
- Original PR [#1973](https://github.com/openinterpreter/openinterpreter/pull/1973) OPEN @ 4d86fdf4b06a1b24b5884db5c56b9f5e2f79f6d7: typed Goal CAS, not shipped nor a sufficient multi-agent supervisor. Original PR [#1981](https://github.com/openinterpreter/openinterpreter/pull/1981) OPEN @ ed0e5147a6d770975a025a7f8461939706a7e4dc: upstream Codex sync, not shipped.
- Original [Issue #1926](https://github.com/openinterpreter/openinterpreter/issues/1926) OPEN: unverified claimed task completion. Original [Issue #1927](https://github.com/openinterpreter/openinterpreter/issues/1927) OPEN: SQL adaptation. Both are S1 defect hypotheses, not S3 ownership/closure.
- Old historical case: previous NO_GO / NO_USEFUL_CHANGE at original 382f615b907279be1b6518156ac2754d3c235ff4 was grounded in absent demonstrated incremental product benefit, conflict and lawful owner. The independent Wave 4 first-pass was saved before this comparison. The 2026-11-20 neutral rule assesses architectural constructibility, not presumed maintainer intent, demonstrated demand or costs. The old caution remains valid for product adoption. This is the SAME evaluation object (not a distinct S4 or new case); preserved commit history and append-only event.

## Function ownership
- S1 disposition: A historical; native agent task/exec and tools execute primary work; no C proposal needed. Source https://github.com/openinterpreter/openinterpreter/blob/7a5509e307cc56d66f5c7413955bb387ab895815/codex-rs/core/src/tasks/regular.rs.
- S2 disposition: C historical; active optional collaboration, message board, capacity guard and status tools. Native coordination is a reused prerequisite rather than separate S3 ownership. Source https://github.com/openinterpreter/openinterpreter/blob/7a5509e307cc56d66f5c7413955bb387ab895815/codex-rs/core/src/agent_message_board.rs.
- S3 disposition: — historical; static shared caps and root ad-hoc commands differ from a developer-composed autonomously repeated whole-session commitment choice with checked effect and returned result; P0 proposed C. Source https://github.com/openinterpreter/openinterpreter/blob/7a5509e307cc56d66f5c7413955bb387ab895815/codex-rs/core/src/agent/control.rs.
- S3* disposition: C historical; Guardian approval and independent review supported. Keep authority separate from S3. Source https://github.com/openinterpreter/openinterpreter/blob/7a5509e307cc56d66f5c7413955bb387ab895815/codex-rs/core/src/guardian/review.rs.
- S4 disposition: — historical; providers and harness modes provide compatibility options but do not prove prospective external signals-to-decision-and-return loop. No current priority. Source https://github.com/openinterpreter/openinterpreter/blob/7a5509e307cc56d66f5c7413955bb387ab895815/docs/harness.md.
- S5 disposition: — historical; root user policy/permissions and contributor rules are parent governance, not local S5 C. No construction without new owner grant. Source https://github.com/openinterpreter/openinterpreter/blob/7a5509e307cc56d66f5c7413955bb387ab895815/codex-rs/core/src/agent/control/user_authorization.rs.

## Capability priority
- Target transition: S3=— -> S3=C
- Priority rationale: One bounded session-level, first-party composable S3 policy actor could choose and correct competing child commitments using existing agent control, observation and return paths, without inferring product demand from a missing Index grade. Architectural GO is falsifiable but not implementation authority.
- P0: optional root-authorized **MultiAgentV2 next-turn admission arbiter** for competing current child commitments within one session, implemented at the existing `LocalAgentControl`/V2 execution boundary; no general-purpose supervisor service.
- P1 dependencies: root-authorized opt-in policy/actor identity; revisioned pending follow-up intent linked to `SessionId`/`AgentPath`; atomic permit/decision integration with `agent/control/execution.rs`; checked V2 `delivery.rs` trigger/interrupt action under existing caps; observed status plus terminal feedback correlated to intent; native concurrency/revocation/rollback tests.
- P2 optional: NONE for this revised minimal native-specific construction; existing `list_agents` status remains available, and no new UI/reporting layer is proposed.
- Proposal-stage decision: GO
- Research disposition: NEEDS_EVIDENCE
- Decision scope: proposal-stage constructibility only; no product endorsement, implementation permission or current Index grade.
- Proposed C construction: root opts into a developer-composed current-work policy for V2 child turns; the actor observes `list_agents`/status and bounded pending follow-up intent, chooses **which child follow-up to admit next vs defer/hold** when capacity is contested, effects a checked `AgentControl::send` `TriggerTurn` only after a version/permit decision, and observes later child status/completion for its next selection. `interrupt_agent` is an existing possible root-authorized intervention, **not** a proven atomic reassign primitive. No cross-session manager, new global budget engine, S5 delegation or automatic Guardian override.
- C sufficiency falsifier: equivalent first-party autonomous session-wide S3 decision/authority/effect/feedback already proven in shipped code, or no lawful checked assignment/effect/returned outcome seam exists under this source-native runtime.
- Proposed validation: same session with two V2 child paths and `max_threads=1`; compare current parent-driven follow-up / `AgentLimitReached` baseline with opt-in admission actor selecting child A or B by explicit priority. Prove atomic capacity admission at actual turn start (not mere `DeliveryReceipt`), status/terminal outcome correlation, opt-out baseline, stale/revoked-root rejection, Guardian preservation and no cross-session effect. All tests **NOT_RUN**.
- Validation state: NOT_RUN
- Proposal falsifier: accepted native tests demonstrate that the actor cannot alter a current cross-child commitment under bounded root authority or cannot receive verifiable later outcome; or equivalence with an already shipped C actor.

## Parallel contribution-on-top review
- Existing-work overlap: static max_threads, token budget reminders, status tools, Goal CAS proposal and current Guardian; all are useful substrates, none by themselves show an independent S3 whole-session choice loop.
- Our on-top contribution: source-native optional narrow policy/decision extension + versioned commitment/action receipt + feedback recheck, using existing agent-control transport, not second communication subsystem.
- Incremental benefit: structural autonomy and repeatable trace of current cross-child resource choices versus manual parent decisions; actual task improvement and cost remain hypothetical.
- Track A: original source and open PRs inspected as listed above; PR 1973 may supply conditional state revision but is unmerged, so proposed controller must not claim reliance on shipped CAS.
- Track B alternative A: static message-board priority flags or new max_threads rules are S2/deterministic enforcement, do not qualify as S3 C.
- Track B alternative B: prospective provider-selection heuristics are S4 research only with missing external feedback, out of this evaluation object.
- Historical comparison: old NO_GO rested on unavailable product-demand/cost and unproven authority; Wave 4 GO is narrower, allowing a hypothetical but source-mapped autonomous constructor. Historical negative research conclusions are preserved, not rewritten as 2026-11-19 GO.

## Implementation options
- Minimal native route: separate small core extension/crate per AGENTS.md (avoid generic core bloat) registering session-scoped supervisor under explicit configuration; reference thread ID/path ownership checks and existing state/communication events. Enforce through existing agent control with a narrow atomic commitment effect and idempotent receipt; the missing seam is proposed, not shipped.
- Alternative: no source change, manual root messages and existing limiter. This is the matched native baseline; absent autonomous repeated S3 choice it is not a C-equivalent.
- Negative tests: no root or rejected owner, stale commitment revision, terminal or unloaded child, exceeded resource policy, override attempt on Guardian/user approvals, failed delivery or lost feedback => no false completion.
- No source-code implementation is part of this plan-only request.

## Specification and domain alternatives
- No Profile/Skills redefinition or Index reassessment; S3 already has defined semantics. If native hooks are impermissible, the status becomes a falsified design rather than writing unrelated product code. No inferred maintainer desire.
- Developer owner selects whether to pursue the plan; no public fork/original GitHub Issue or PR is authorized by this research.

## Cost experiment
- Test identical bounded concurrent workloads under native manual Goal/threads/limits and opt-in controller. Observe accepted task completion, missed commitments, variance, token cost, extra moving parts, review/maintenance burden. Costs and user adoption have not been measured.
- Cost status: NOT_MEASURED

## Delivery and publication
- Human issue: [issue.md](issue.md)
- AI contract: [constructor-sufficiency.md](constructor-sufficiency.md)
- Canonical receipt: roadmap.md
- Research reviewed: YES / independent first pass, source pinned.
- Fork-local metadata persistence: subject to exact HEAD/state check and structural validator.
- Original product code: NOT_MODIFIED
- External issue: DRAFT — NOT PUBLISHED
- Native tests: NOT_RUN
- Publication to original or public fork GitHub Issue/PR: NOT_PUBLISHED


## v0.18.1 source-native specificity review — 2026-11-20 (same case, not a fresh independent rerun)

**Protocol:** [Upstream v0.18.1 patch (merged PR #87)](https://github.com/opensiro/upstream/commit/14973244a474cc643c01ce04d70913f51c714b74), with [reporting hygiene (merged PR #89)](https://github.com/opensiro/upstream/commit/ae7a8a6d32b4da1c5fd97c6862821460503bf9e2). This is a subsequent critical self-review of the historical Wave 4 first-pass, not an additional candidate, new Index assessment, retroactive v0.18.0 conclusion or third-party publication. Accepted original HEAD remains `7a5509e307cc56d66f5c7413955bb387ab895815`; original `main` and cited PR #1973/#1981 heads were rechecked unchanged on 2026-11-20.

**What was over-general:** The old phrase "shared commitment supervisor / reassign / feedback" could be copied to AG2 or Strands with mostly new names. Open Interpreter does **not** ship an authoritative cross-child commitment ledger, a guaranteed acknowledgement that a queued message ran, or an atomic "reassign commitment" API. The old outline under-described this gap. Narrow P0 to an actual MultiAgentV2 control seam rather than inventing a platform-wide resource scheduler.

**Actual first-party native surfaces (SHIPPED at pinned original):**

- [`multi_agents_v2/list_agents.rs`](https://github.com/openinterpreter/openinterpreter/blob/7a5509e307cc56d66f5c7413955bb387ab895815/codex-rs/core/src/tools/handlers/multi_agents_v2/list_agents.rs) returns `agent_name` and `AgentStatus`, **not** a trusted priority/commitment queue.
- [`agent/control.rs`](https://github.com/openinterpreter/openinterpreter/blob/7a5509e307cc56d66f5c7413955bb387ab895815/codex-rs/core/src/agent/control.rs) has `list_agents`, `subscribe_status`, `get_agent_token_usage_info`, `send_inter_agent_communication`, `interrupt_agent`; these are observation/transport controls, not a complete independent S3 policy.
- [`agent/control/delivery.rs`](https://github.com/openinterpreter/openinterpreter/blob/7a5509e307cc56d66f5c7413955bb387ab895815/codex-rs/core/src/agent/control/delivery.rs) resolves target within allowed agent paths and sends `MessageDeliveryMode::TriggerTurn` via `send_inter_agent_communication`; its `DeliveryReceipt` contains a submission ID, **not** terminal task proof, and follow-up to root is rejected.
- [`agent/control/execution.rs`](https://github.com/openinterpreter/openinterpreter/blob/7a5509e307cc56d66f5c7413955bb387ab895815/codex-rs/core/src/agent/control/execution.rs) gates V2 subagent turns with an active-count `max_threads` permit. It currently uses separate `has_capacity` and `guard` methods; an atomic admission/priority claim is **not shown**, and no concurrency failure is claimed without a test.
- [`agent/control/completion.rs`](https://github.com/openinterpreter/openinterpreter/blob/7a5509e307cc56d66f5c7413955bb387ab895815/codex-rs/core/src/agent/control/completion.rs) delivers captured child terminal outcome to parent **best effort**; it does not correlate an S3 decision ID or guarantee delivery.
- [`agent_message_board.rs`](https://github.com/openinterpreter/openinterpreter/blob/7a5509e307cc56d66f5c7413955bb387ab895815/codex-rs/core/src/agent_message_board.rs) explicitly does not start or restore idle agents and is therefore **not** a substitute for authoritative next-turn admission. [`user_authorization.rs`](https://github.com/openinterpreter/openinterpreter/blob/7a5509e307cc56d66f5c7413955bb387ab895815/codex-rs/core/src/agent/control/user_authorization.rs) exposes bounded root authorization context; it is **not** a new delegation grant.

**Minimal original-specific Track B (PROPOSED only):** For an opt-in V2 root with two child paths and one available execution slot, expose a bounded root-authorized pending-follow-up view (revision, intended task/child, priority, scope) *in or immediately adjacent to* `LocalAgentControl`; allow a developer-composed actor to choose which currently waiting child gets next lawful turn; integrate its checked decision with the actual V2 admission/permit path and existing `send`/follow-up tool rather than a second scheduler or service. Correlate the action with status and captured terminal outcome; if delivery, effect, version or ownership cannot be verified, report UNKNOWN/NOT_APPLIED rather than success. No default behavior change and no implicit increase of `max_threads` or rights. Direct reassigning an active agent's objective is **out of the minimal P0 scope** unless a separate supported checked source path is proven.

**Native A/B falsification (NOT_RUN):** With the **same** two child paths and hard `max_threads=1`, baseline is parent-driven `list_agents` and follow-up/limit behavior. Proposed B must show at least two different lawful priorities leading to different *actual next child turns*, successful release/retry at terminal, version-conflict denial, revoked-root denial, unchanged Guardian and ordinary default path. A mere message receipt, fixed first-in-first-out selector, best-effort parent completion message, model-written priority text or synthetic test stub **does not close S3=C**. No native tests or implementation are claimed.

**Revised scoped outcome:** Proposal-stage **GO / NEEDS_EVIDENCE**, unchanged as a structural *hypothesis*, but now specifically tied to first-party MultiAgentV2 turn control; **P2 NONE**. Actual enforceability, return-to-policy and consumer need remain unresolved. If the missing legal/atomic effect+return seam cannot be constructed with supported native surfaces, reopen this same case as `NO_GO` or `BLOCKED` under the actual reason. This patch supplies **no extra metric, specificity grade or new qualification gate**. Product adoption remains the original maintainer's decision; external/public fork issues/PRs **NOT_PUBLISHED**.
