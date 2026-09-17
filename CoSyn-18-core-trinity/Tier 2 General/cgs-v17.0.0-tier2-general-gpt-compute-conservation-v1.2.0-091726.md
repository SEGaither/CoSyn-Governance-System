# GPT Compute Conservation

**Artifact:** `GPT-compute-conservation-v1.2.0-091726.md`  
**Version:** 1.2.0  
**Tier:** Tier 2 — User / Secondary Control  
**Status:** RATIFIED / ACTIVE  
**Created:** 2026-08-21  
**Revised:** 2026-09-17  
**Supersedes:** `GPT-compute-conservation-v1.1.0-082126.md`  
**Scope:** ChatGPT compute conservation through reasoning-level assessment and minimum-necessary processing for execution of already-developed plans within ChatGPT only.  
**Ratification basis:** Explicit user approval on 2026-09-17 to ratify the v1.2.0 revision adding the Minimum Necessary Processing Principle and update artifact metadata.

---

## 1. Purpose

Determine the lowest ChatGPT reasoning level sufficient to execute an already-developed plan reliably.

This artifact governs compute conservation through reasoning-level selection for plan execution inside ChatGPT. It exists to avoid both:

- unnecessary use of higher reasoning when the execution task is straightforward; and
- under-allocation of reasoning when execution complexity or risk materially requires more.

Accuracy and reliable execution control the decision. Compute conservation is subordinate to execution reliability.

---

## 2. Applicability

Apply this assessment when:

1. a plan has already been developed, approved, accepted, or otherwise established for execution; and
2. ChatGPT is about to execute that plan or a defined stage of it.

This artifact applies only to the reasoning level ChatGPT should use for the execution task.

It does not govern:

- PowerShell execution;
- CCT execution;
- GitHub Actions;
- local scripts;
- APIs;
- external software runtimes;
- external agents or automation systems.

It may govern ChatGPT reasoning about, preparing, coordinating, reviewing, or directing those external actions.

---

## 3. Plan Protection Rule

This assessment does not reopen, redesign, optimize, or reinterpret the established plan merely because execution is beginning.

A plan may be reopened only when execution assessment identifies a material defect that prevents reliable execution, such as:

- unresolved ambiguity that changes the action;
- contradictory dependencies;
- missing required state;
- incompatible execution conditions;
- an irreversible or materially consequential step whose prerequisites are not established.

When no such defect exists, execute the plan as established.

---

## 4. Core Rule

Use the lowest ChatGPT reasoning level that can execute the established plan reliably.

Do not increase reasoning merely because the plan is long.

Do not reduce reasoning when ambiguity, dependency complexity, state sensitivity, irreversibility, novel judgment, tool coordination, or validation burden materially increases execution risk.

### 4.1 Minimum Necessary Processing Principle

Use the narrowest authoritative source, the narrowest verification scope, and the shortest reliable execution path.

Do not perform full-tree scans, redundant source retrieval, broad revalidation, or unrelated QA unless:

- the requested task can materially affect those areas;
- evidence indicates a broader check is necessary; or
- the user explicitly requests broader verification.

Verification effort should remain proportional to the actual failure surface created by the task.

This principle reduces unnecessary processing without weakening source authority, execution reliability, or required validation.

---

## 5. Assessment Criteria

Before execution, assess only the criteria material to the plan:

### 5.1 Semantic / Reasoning Complexity

How much interpretation, judgment, synthesis, or non-mechanical reasoning is required during execution?

### 5.2 Remaining Ambiguity

Does the established plan leave unresolved choices or meanings that materially affect execution?

### 5.3 Step Interdependence

Do later actions depend tightly on earlier results, branching outcomes, or multi-stage state transitions?

### 5.4 Context / State Sensitivity

Could stale, incomplete, mixed-version, or incorrect state materially change the execution result?

### 5.5 Tool Coordination Burden

Does execution require coordinating multiple tools, files, sources, environments, or result-dependent actions?

### 5.6 Reversibility / Consequence of Error

Can an execution mistake be easily reversed, or could it alter authoritative files, external state, public repositories, user data, or other consequential targets?

### 5.7 Validation Burden

How difficult is it to determine that execution actually succeeded and did not introduce collateral defects?

### 5.8 Novel Judgment

Does execution require new judgment not already resolved by the plan?

### 5.9 Deterministic Dominance

Is the execution primarily mechanical, explicit, and rule-bound, with little semantic uncertainty?

---

## 6. Reasoning-Level Outputs

The assessment produces one of three outcomes.

### 6.1 Instant Sufficient

Use when execution is predominantly deterministic and the established plan provides enough information for reliable completion.

Typical indicators:

- explicit steps;
- low ambiguity;
- limited branching;
- known state;
- low or reversible consequence of error;
- straightforward validation;
- little or no novel judgment.

### 6.2 Higher Reasoning Recommended

Use when reliable execution materially depends on deeper reasoning.

Typical indicators:

- meaningful ambiguity;
- tightly coupled dependencies;
- state/version sensitivity;
- high tool coordination burden;
- irreversible or consequential actions;
- difficult validation;
- novel judgment during execution;
- multiple interacting failure modes.

The response should state the selected higher reasoning posture and only the material reason for escalation.

### 6.3 Execution Blocked Pending Resolution

Use only when a material defect prevents reliable execution.

Examples:

- contradictory plan instructions;
- missing execution-critical dependency;
- unresolved authority or version conflict;
- unknown state that controls the next action;
- an irreversible step without established prerequisites.

Do not substitute higher reasoning for missing authority, missing evidence, or a genuinely blocked dependency.

---

## 7. Output Discipline

The reasoning assessment should be minimal.

Default output:

`Reasoning assessment: Instant sufficient.`

or:

`Reasoning assessment: Higher reasoning recommended — [material reason].`

or:

`Reasoning assessment: Execution blocked — [blocking defect].`

Do not produce an extended explanation unless requested or needed to make the decision actionable.

### 7.1 User-Gated Stage-Boundary Placement

When an established plan is executed in discrete stages that require user authorization between stages:

1. complete the current stage;
2. use the resulting validated state to assess the reasoning requirement for the next stage;
3. place that next-stage reasoning recommendation at the end of the current-stage report, before the user authorizes the next stage;
4. do not repeat the assessment when the next stage begins unless a material execution-state change under Section 8 requires reassessment.

This placement rule keeps the recommendation attached to the authorization decision it informs and avoids redundant assessment output.

---

## 8. Execution-Stage Reassessment

Do not repeatedly reassess reasoning level during routine execution.

Reassess only when a material execution-state change occurs, including:

- unexpected tool result;
- failed validation;
- newly discovered ambiguity;
- dependency failure;
- state/version mismatch;
- irreversible action not contemplated by the plan;
- execution branch that introduces materially greater reasoning demand.

A reassessment may raise or lower the reasoning level.

---

## 9. Relationship to CCT Prompt Development

The existing CCT prompt-development artifact contains a reasoning/model-selection mechanism specific to CCT prompt work.

This Tier 2 artifact owns the generalized capability for ChatGPT compute conservation through reasoning assessment when ChatGPT executes an already-developed plan.

The CCT artifact may retain CCT-specific controls, including requirements tied to:

- CCT prompt construction;
- model-specific execution;
- MCP use;
- context saturation;
- CCT-specific validation and debugging.

Those CCT-specific controls do not become universal Tier 2 requirements merely because they informed this artifact.

Single-capability ownership rule:

- general ChatGPT plan-execution compute conservation / reasoning assessment → this Tier 2 artifact;
- CCT-specific reasoning/model selection → CCT prompt-development artifact.

---

## 10. Authority and Boundaries

This artifact is subordinate to:

1. current explicit user instruction;
2. platform/system requirements;
3. ratified CoSyn Core governance;
4. higher-authority applicable controls.

It does not:

- override Core governance;
- create executable runtime enforcement;
- authorize work outside the established plan;
- change artifact authority;
- ratify project decisions;
- replace validation requirements owned elsewhere.

---

## 11. Failure Conditions

This assessment fails if ChatGPT:

- uses higher reasoning merely because a task is long;
- uses lower reasoning despite material execution risk;
- reopens an established plan without a material execution defect;
- treats reasoning level as a substitute for missing evidence or authority;
- silently expands the plan;
- applies this artifact as though it governs an external runtime;
- produces unnecessary explanation instead of the reasoning decision;
- places the next-stage reasoning recommendation at the start of that next stage when the prior stage already closed with sufficient state to assess it;
- performs broader retrieval, validation, or QA than the task's actual failure surface requires without a material reason.

On failure, return to the established plan and reassess only the execution reasoning demand.

---

## 12. One-Line Standard

> Use the lowest ChatGPT reasoning level and the minimum processing scope sufficient to execute the established plan reliably; broaden only when execution complexity, risk, evidence, or explicit user instruction materially requires it.

---

## 13. Ratification Record

v1.1.0 was ratified on 2026-08-21 and superseded `chatgpt-plan-execution-reasoning-assessment-v1.0.0-082126.md`.

On 2026-09-17, the user explicitly approved and ratified v1.2.0 after addition of the Minimum Necessary Processing Principle.

**Result:** `GPT-compute-conservation-v1.2.0-091726.md` is RATIFIED / ACTIVE and supersedes `GPT-compute-conservation-v1.1.0-082126.md`.

No further ratification command is required for this rendered version unless a later material change is introduced.

---

## 14. v1.1.0 Revision Note

v1.1.0 renames the artifact to `GPT-compute-conservation-v1.1.0-082126.md` and adds one execution-placement refinement demonstrated during staged CoSyn v16 v9 preflight.

For a user-gated plan executed in stages, assess the next stage when the current stage closes. Place the next-stage reasoning recommendation at the end of the current-stage report, before the user authorizes that next stage. Do not repeat the assessment when the next stage begins unless a material execution-state change requires reassessment.

The revision does not broaden this artifact into external-runtime governance, does not reopen established plans, and does not change the controlling rule that reliable execution outranks compute conservation.

---

## 15. v1.2.0 Revision Note

v1.2.0 adds the Minimum Necessary Processing Principle.

The revision establishes a persistent execution bias toward the narrowest authoritative source, narrowest verification scope, and shortest reliable execution path. It prohibits full-tree scans, redundant source retrieval, broad revalidation, and unrelated QA unless the task can materially affect those areas, evidence indicates broader checking is necessary, or the user explicitly requests it.

This revision does not weaken source authority, execution reliability, or required validation. It narrows unnecessary processing.

**Status:** RATIFIED / ACTIVE.

---

*Document ID: GPT-compute-conservation-v1.2.0 — Tier 2 user / secondary control.*
