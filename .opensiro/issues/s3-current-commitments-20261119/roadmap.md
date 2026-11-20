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
- Effect boundary: checked child-status and commitment-version action through first-party agent-control methods; never arbitrary cross-session control or implicit rights expansion.
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
- P0: optional current-commitment supervisor (session-root, bounded goals and max-capacity).
- P1 dependencies: versioned shared-commitment snapshot, legitimate actor identity/consent, checked cross-child assign/defer/interrupt effect seam, verifiable action/outcome correlation, native overlap and authority tests.
- P2 optional: low-noise UI status/read-only per-commitment provenance after P0 is validated; no new autonomous governance.
- Proposal-stage decision: GO
- Research disposition: NEEDS_EVIDENCE
- Decision scope: proposal-stage constructibility only; no product endorsement, implementation permission or current Index grade.
- Proposed C construction: opt-in developer-composed supervisor observes current child commitments, capacities, token usage and outcomes, chooses preserve/reassign/defer/interrupt among lawful alternatives, applies via checked first-party agent-control actions, receives later child status/terminal outcome and recomputes; an authorized parent establishes policy bounds and retains S5/Guardian rights.
- C sufficiency falsifier: equivalent first-party autonomous session-wide S3 decision/authority/effect/feedback already proven in shipped code, or no lawful checked assignment/effect/returned outcome seam exists under this source-native runtime.
- Proposed validation: matched two-child contention task, current static limiter/manual parent baseline versus opt-in supervisor; verify two alternative decisions, authorized effect, later feedback-driven change, revocation/stale target and denied privileged action, default-mode nonregression.
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
