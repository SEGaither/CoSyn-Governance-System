# CCT Prompt Building Directions

**Artifact:** `cct-prompt-building-directions-v1.2.0-082126.md`
**Version:** 1.2.0
**Tier:** Tier 2 — User-specific operational prompt-development control
**Status:** RATIFIED / ACTIVE
**Scope:** Cross-project Claude Code TUI (CCT) prompt design, refinement, debugging, model selection, and rendering
**Created:** 2026-08-21
**Revised:** 2026-08-21
**Supersedes:** `cct-prompt-building-directions-v1.1.0-082126.md`
**Revision basis:** Explicit user-approved refinement from CoSyn v16 v9 terminal-execution evidence: an otherwise read-only Git inspection appeared hung because Git opened an interactive pager.
**Authority:** Subordinate to platform/system requirements, current explicit user instruction, CoSyn CGS, and any applicable project-specific Tier 3 governance.

## Purpose

Define the user's standing rules for designing Claude Code TUI prompts across projects.

This artifact governs prompt architecture and prompt-production behavior. It does not define project-specific task logic, paths, repositories, schemas, source material, or execution state.

## 1. Context-Saturation Limit

Do not design monolithic CCT prompts expected to drive Claude Code beyond approximately 65% context saturation.

Prompt architecture must account for prompt size, expected tool output, expected source/code/document loading, intermediate reasoning burden, execution state required through completion, and final validation/reporting requirements.

If the expected workflow risks exceeding the limit, split it into serial prompts.

## 2. Standalone Serial-Prompt Rule

When a workflow is divided into serial prompts, every prompt must be independently executable.

Each serial prompt must carry all information required for its own execution, including as applicable:

- mission;
- scope;
- inputs;
- authoritative paths;
- required files or state;
- tool requirements;
- execution constraints;
- success criteria;
- failure gates;
- validation requirements;
- output contract.

Do not rely on hidden conversational residue, prior CCT context, unstated assumptions, memory of earlier prompt text, or undocumented execution state.

A serial prompt may consume artifacts created by an earlier prompt, but the dependency must be explicit and independently verifiable.

## 3. Optimization Priority

Prompt design priority is:

1. Accuracy.
2. Compute conservation.
3. Speed of render/execution.

Lower-priority goals must never degrade higher-priority goals.

## 4. Compute-Conservation Standard

Compute conservation is achieved through controlled linear execution.

Required defaults:

- linear processing;
- no parallel processing;
- no agents;
- no subagents;
- no agent teams;
- no unnecessary repeated reads;
- no broad context loading when bounded retrieval is sufficient;
- no redundant semantic re-analysis of facts already deterministically established.

Use specialized MCP capabilities when they materially reduce context load, repeated parsing, or unnecessary model reasoning.

### 4.1 Deterministic / Semantic Work Allocation

Assign work to the cheapest deterministic mechanism that can prove the requirement reliably.

Prefer deterministic local tooling for work such as:

- enumeration;
- parsing;
- file transformation;
- state persistence;
- reconciliation;
- counting;
- sorting;
- assembly;
- hash or schema validation.

Reserve model reasoning for work that genuinely requires semantic judgment, interpretation, classification, synthesis, or other non-deterministic reasoning.

Do not spend model context or semantic compute re-proving an invariant that a cheaper deterministic check can fully establish.

### 4.2 Non-Interactive Terminal Execution by Default

When a CCT prompt instructs terminal or shell execution, prefer a non-interactive command form when an equivalent form can complete the same task reliably.

The prompt should prevent avoidable hidden execution states such as:

- pagers that wait for a quit command;
- editors opened implicitly by a command;
- confirmation prompts that suspend unattended execution;
- credential or authentication prompts not anticipated by the workflow;
- other interactive modes that can make a valid command appear hung.

Where supported, use explicit non-interactive flags, environment settings, or command forms such as disabling a pager for bounded inspection commands.

Do not impose a blanket ban on interactive commands. If interaction is operationally required or materially safer, the prompt must state:

1. that an interactive state is expected;
2. what the user or operator should see;
3. what input is required;
4. how to exit or continue safely; and
5. what condition indicates that execution is actually stalled rather than awaiting input.

This rule governs prompt execution ergonomics. It does not own repository safety, repository mutation policy, or project-specific Git logic.

Preferred MCP classes include, where appropriate:

- JCodeMunch;
- JCodeDoc;
- JCodeData;
- other fit-for-purpose MCPs with equivalent bounded retrieval or structured-processing capability.

## 5. MCP Availability Hard Gate

When a prompt depends on an MCP capability for acceptable accuracy or compute conservation:

1. Verify that the required MCP is available before substantive execution.
2. Verify the required operation is supported.
3. If the required MCP is unavailable or unusable, abort that prompt's mission.
4. Report the missing capability precisely.
5. Resolve the MCP/tooling issue before resuming.

Do not silently substitute broad manual context loading, agent-based processing, higher-compute fallback workflows, or less controlled retrieval methods.

A fallback may be used only when the prompt explicitly defines it and it preserves the governing accuracy and compute constraints.

## 6. Prompt Modularity

Partition work by coherent execution function rather than prompt length alone.

A useful prompt boundary should:

- produce a durable result or state transition;
- have a clear completion condition;
- be independently testable;
- minimize the state the next prompt must consume;
- avoid forcing later prompts to reconstruct prior reasoning.

Prefer deterministic artifacts and state files over conversational continuity.

## 7. Prompt Debugging Standard

Every CCT prompt must be iteratively debugged and refined to no further material gain before final rendering.

Each refinement pass should test for:

- ambiguity;
- contradictory instructions;
- hidden dependencies;
- unsupported assumptions;
- context-saturation risk;
- excessive compute;
- missing hard gates;
- unsafe or uncontrolled fallback behavior;
- serial-prompt dependency leakage;
- path ambiguity;
- state ambiguity;
- incomplete success criteria;
- incomplete failure criteria;
- weak validation;
- output-contract ambiguity;
- unnecessary repetition;
- model capability mismatch.

Continue refinement until another complete pass at the current reasoning level produces no meaningful improvement.

Record the total debug iteration count.

### 7.1 Debug Audit Integrity

Debug iteration counts must be auditable rather than decorative.

Required behavior:

1. A reported iteration counts only when a discrete review pass was actually performed.
2. Each pass must have an internal result: defects found and material corrections made, or zero material defects found.
3. Do not invent defects to justify an iteration count.
4. A zero-defect pass is valid evidence when no material issue is found.
5. `No further material gain` may be declared only after a complete subsequent pass produces zero material changes at the stated reasoning level.
6. If a later review at the same reasoning level finds a material defect that should have been discoverable under the same evidence/state, the earlier no-gain certification is invalidated.

### 7.2 Reasoning-Level Qualification

`No further material gain` is conditional on the reasoning level used for the review.

When reasoning level is known, certify the result as:

`No further material gain at [reasoning level].`

If reasoning level is increased, the previous ceiling is reopened. A higher-reasoning review may legitimately discover additional material defects without making the earlier lower-reasoning review fictitious.

Do not represent a lower-reasoning certification as proof that no higher-reasoning review could find more.

### 7.3 Stage-Gated Execution and Validation Binding

For long-running, expensive, destructive, stateful, or multi-item workflows, design staged release when practical:

`self-test -> bounded representative preflight -> full execution`

Do not impose this ceremony on trivial operations where it adds no meaningful reliability.

A validation PASS applies only to the implementation, authoritative inputs/state, material configuration, and relevant tool/runtime state actually tested.

Where practical, durable gate evidence should bind to:

- implementation identity, version, or content hash;
- authoritative input/state identity or hash;
- material configuration;
- relevant tool/runtime version.

A material change to a bound dependency invalidates that gate and any downstream gate that depends on it. Re-run the cheapest sufficient earlier validation before resuming downstream execution.

### 7.4 Systemic-Failure Circuit Breaker

For multi-item workflows, distinguish systemic implementation/runtime defects from legitimate item-specific or external outcomes.

A prompt should define a bounded circuit breaker when repeated systemic failure could poison state or waste substantial compute.

When the threshold is reached:

1. stop further propagation;
2. diagnose the shared defect;
3. repair the implementation or execution contract;
4. re-run any invalidated self-test or preflight;
5. retry affected items;
6. resume only after the governing gate passes.

Do not convert a programming defect into many item-level final failures.

## 8. Recommended CCT Model Rule

Every rendered CCT prompt must identify the lowest-compute Claude Code model that has sufficient capability to execute the prompt reliably.

Model selection must account for reasoning complexity, coding complexity, tool use, repository/document scale, context requirement, debugging burden, and validation burden.

Do not default to the strongest available model.

Do not reduce model capability below the level required for reliable execution.

Accuracy remains the controlling priority.

## 9. ChatGPT Render Contract for CCT Prompts

When ChatGPT renders a completed CCT prompt, the response must contain, outside the paste-ready code box:

- **Purpose:** concise statement of what the prompt does.
- **Debug iterations:** total refinement/debug pass count.
- **Recommended CCT model:** lowest-compute model with sufficient capability.

Inside the code box:

- the complete paste-ready CCT prompt;
- no omitted dependencies;
- no reliance on surrounding commentary;
- no metadata that belongs outside the code box unless the prompt itself operationally requires it.

The prompt itself must always be placed in a code box.

## 10. Completion Test

A CCT prompt is ready to render only when:

- expected context load remains within the design limit;
- serial dependencies are explicit and standalone-safe;
- accuracy requirements are preserved;
- compute is conserved without reducing reliability;
- deterministic work is not needlessly assigned to semantic model reasoning;
- avoidable terminal interactivity is suppressed, and required interactivity is explicitly signposted with safe continuation/exit instructions;
- required MCP/tool capability is gated;
- failure behavior is deterministic;
- staged validation is used when the workflow materially benefits from it;
- durable PASS gates are bound to the state they actually proved and have explicit invalidation behavior when applicable;
- systemic failures cannot silently propagate across a multi-item run;
- validation is sufficient;
- output contract is precise;
- debug iteration counts are auditable;
- another complete debug pass at the stated reasoning level yields no material gain;
- the recommended model is the lowest-compute model that can reliably execute it.

## One-Line Standard

Build bounded, standalone, accuracy-first CCT prompts; assign deterministic work to deterministic tools; prefer non-interactive terminal forms unless interaction is required and explicitly explained; conserve compute through linear execution and specialized MCPs; use bound stage gates and circuit breaking where scale warrants them; debug with auditable passes to no further material gain at the stated reasoning level; render the complete prompt in a code box with purpose, debug count, and lowest-sufficient-model metadata outside it.


## v1.1.0 Revision Note

v1.1.0 incorporates cross-project-worthy controls demonstrated by the Transcript Scraping workflow through successful bounded preflight:

- auditable debug iteration counts;
- no invented defects;
- reasoning-level-qualified no-gain certification;
- deterministic-versus-semantic work allocation;
- staged self-test/preflight/full release when warranted;
- validation-gate binding and invalidation;
- systemic-failure circuit breaking and repair/retest/resume behavior.

Project-specific transcript paths, counts, taxonomy rules, and local implementation details remain excluded.

## v1.2.0 Revision Note

v1.2.0 adds a narrow cross-project terminal-execution reliability control demonstrated during CoSyn v16 v9 Git preflight.

When an equivalent reliable form exists, CCT prompts should use non-interactive terminal commands so pagers, editors, confirmation prompts, or similar hidden states do not make execution appear hung. When interaction is genuinely required, the prompt must announce the expected interactive state and explain how to continue or exit safely.

This refinement does not make CCT Prompt Building Directions the owner of Git repository safety. Repository-state discovery, mutation isolation, staging controls, protected-reference handling, and push validation are owned separately by `git-repository-change-safety-protocol-v1.0.0-082126.md`.

**Ratification:** Explicitly approved and ratified by the user on 2026-08-21.
