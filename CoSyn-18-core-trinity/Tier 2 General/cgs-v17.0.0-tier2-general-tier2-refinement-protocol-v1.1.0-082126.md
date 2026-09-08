# Tier 2 Refinement Protocol

**Artifact:** `tier2-refinement-protocol-v1.1.0-082126.md`  
**Version:** 1.1.0  
**Tier:** Tier 2 — User-specific governance refinement workflow control  
**Status:** RATIFIED / ACTIVE  
**Scope:** Cross-project evaluation, promotion, refinement, ratification lifecycle, and demotion of Tier 2 operational artifacts from direct project/session evidence  
**Created:** 2026-08-21  
**Revised:** 2026-08-21  
**Supersedes:** `tier2-refinement-protocol-v1.0.0-082126.md`  
**Ratification basis:** Explicit user instruction on 2026-08-21 to refine, ratify, and render this protocol.  
**Authority:** Subordinate to platform/system requirements, current explicit user instruction, CoSyn CGS, and applicable project-specific authority.

## Purpose

Define a disciplined method for converting demonstrated project/session lessons into durable Tier 2 refinements without overfitting one project, duplicating authority, or promoting local implementation detail into cross-project governance.

This protocol governs the refinement exercise and the Tier 2 artifact lifecycle rules that determine when prior user approval plus a later creation/render instruction authorizes ratification and activation.

## 1. Evidence Basis

Use direct operational evidence when evaluating Tier 2 refinement.

Valid evidence includes:

- current session behavior and results;
- directly accessible current artifacts;
- explicit user approvals, corrections, exclusions, and failure signals;
- executed tests and validation results;
- observed failures and successful recoveries;
- current provenance that can be tied back to the operational event.

Memory may be used as a discovery hint but not as inclusion or promotion evidence when authoritative source material can be retrieved.

Do not promote a rule because it merely sounds generally useful.

## 2. Mandatory Classification

Classify every candidate lesson into exactly one disposition:

1. **Adequately represented** — the active Tier 2 set already captures the lesson; no change.
2. **Refine existing Tier 2** — a current artifact is the correct authority location but its wording or control is incomplete.
3. **New Tier 2 justified** — the lesson is reusable across projects and has a distinct purpose that cannot be represented cleanly without overlap or authority confusion.
4. **Remain Tier 3** — the lesson is project/session-specific, insufficiently generalized, or insufficiently evidenced for Tier 2.

Do not leave a candidate lesson unclassified merely because its promotion decision is inconvenient.

## 3. Promote Mechanism, Not Local Values

When a project demonstrates a reusable mechanism, separate the mechanism from its implementation values.

Tier 2 may capture:

- control logic;
- decision criteria;
- validation patterns;
- failure handling;
- authority boundaries;
- reusable workflow invariants.

Keep in Tier 3 unless independently justified:

- project names;
- channel or repository targets;
- paths;
- filenames tied to one project;
- record counts;
- local taxonomy labels;
- one-project sorting rules;
- item IDs;
- project-specific schemas or business logic.

## 4. Existing-Artifact Preference

Prefer refining an existing Tier 2 artifact over creating a new one.

A new Tier 2 artifact is justified only when all are true:

1. the lesson is clearly reusable beyond the originating project;
2. it has a distinct operational purpose;
3. forcing it into an existing artifact would create overlap, ambiguity, scope distortion, or authority confusion;
4. its authority boundary can be stated cleanly;
5. its recurring benefit exceeds its recurring compliance cost.

Do not create an artifact merely to memorialize a successful session.

## 5. Cross-Project Evidence Threshold

Use the narrowest promotion justified by the evidence.

A strong field result may justify refinement of an already domain-specific Tier 2 artifact when the lesson is directly within that artifact's established scope.

Promotion from one project into a broader cross-domain Tier 2 rule should normally require one of:

- corroborating evidence from a materially different project;
- an independently testable invariant whose generality does not depend on the originating domain;
- explicit user authorization to promote despite the single-project evidence base.

When evidence is strong but generality remains uncertain, keep the rule provisional or Tier 3 rather than overpromoting it.

## 6. Regression Analysis

For every proposed Tier 2 change, identify what existing successful behavior it could accidentally constrain, slow, invalidate, or make more expensive.

Ask:

- Does this rule impose ceremony on trivial tasks?
- Does it reduce useful flexibility?
- Does it conflict with a faster valid path?
- Does it add recurring prompt/context burden?
- Could it make a domain-specific exception harder to express?

Narrow or reject a refinement whose cross-project regression cost exceeds its demonstrated benefit.

## 7. Interaction and Authority Analysis

Review the active Tier 2 set as a system, not only artifact by artifact.

For each proposed change, check:

- overlap;
- duplication;
- conflicting instructions;
- ambiguous precedence;
- scope leakage;
- authority inflation;
- version interaction;
- whether the rule belongs at Tier 2 at all.

A useful new rule must still live in the correct authority location.

## 8. Counterexample Test

Before promotion, identify at least one plausible project or task where the candidate rule could be wrong, wasteful, or harmful.

If a credible counterexample exists:

- narrow the rule;
- add an applicability condition; or
- keep it at Tier 3.

Do not convert a successful local pattern into an unconditional cross-project mandate without testing its boundary.

## 9. Testability Standard

Prefer operational rules with observable compliance conditions.

Where practical, define:

- trigger;
- required action;
- prohibited action;
- PASS condition;
- invalidation condition;
- failure behavior.

Avoid replacing a testable session lesson with vague language such as `use good judgment` when the demonstrated behavior can be expressed deterministically.

## 10. Positive and Negative Evidence

Treat successful failures as evidence when they reveal a reusable control.

Examples include:

- a bounded preflight that stops a defect before scale;
- a validation gate correctly invalidated after code changes;
- a failed approach that exposes a scope or authority weakness;
- a recovery path that avoids repeating expensive work.

Preserve materially useful negative evidence when it prevents recurrence.

Do not promote incidental failures that have no cross-project lesson.

## 11. Cost-of-Compliance Test

Every Tier 2 rule creates recurring cost.

Evaluate:

- prompt length;
- context consumption;
- compute;
- execution time;
- user attention;
- artifact maintenance;
- cognitive friction;
- validation burden.

Promote only when the expected recurring reliability or usability benefit justifies that recurring cost.

## 12. Refinement Output Contract

For every recommended Tier 2 change, identify:

- target artifact;
- current version;
- proposed indexed version;
- amendment, clarification, replacement, or new artifact;
- exact refinement opportunity;
- direct evidence supporting it;
- cross-project benefit;
- regression/counterexample result;
- interaction/authority result;
- what remains explicitly Tier 3.

Prefer controlled deltas against canonical artifacts.

Do not rewrite unaffected artifacts merely to make the Tier 2 package look uniform.

## 13. Rollback, Narrowing, and Demotion

Tier 2 promotion is reversible.

Future evidence may justify:

- superseding a rule;
- narrowing its applicability;
- moving it to a more specific artifact;
- demoting it back to Tier 3;
- retiring an artifact whose purpose is absorbed cleanly elsewhere.

When later evidence materially contradicts a promoted rule, surface the conflict. Do not preserve the rule merely because it was previously ratified or successful.

## 14. Refinement Stopping Condition

The exercise is complete only when:

1. every candidate lesson has a disposition;
2. every proposed change has been checked for existing coverage;
3. regression and counterexample analysis are complete;
4. artifact interaction and authority placement are checked;
5. project-specific values remain excluded from Tier 2;
6. proposed new artifacts have distinct justified purposes;
7. the recurring cost of each change is justified;
8. another complete review at the stated reasoning level produces no further material cross-project gain.

If reasoning level is increased, the prior no-gain ceiling may be reopened.

## 15. Ratification Lifecycle

Preserve the distinction among:

- proposed;
- rendered;
- approved;
- ratified;
- active;
- superseded.

### 15.1 No Ratification Before Approval

Analysis, recommendation, drafting, or rendering does not by itself ratify a Tier 2 change when the user has not yet approved the design or content.

Do not infer approval merely because:

- an artifact was discussed;
- a draft was rendered;
- an assistant recommended it;
- the user continued to another topic;
- the artifact physically exists.

### 15.2 Prior Approval + Creation Command

When all of the following are true:

1. the user has explicitly approved the design, content, or proposed Tier 2 change;
2. that approval remains current and has not been withdrawn, superseded, or materially altered;
3. the user subsequently instructs the assistant to `create`, `render`, `instantiate`, `produce`, or otherwise materialize the indexed Tier 2 artifact;
4. the rendered artifact faithfully implements the approved design without material unapproved expansion; and
5. required validation succeeds;

the later creation/render instruction constitutes authorization to mark the resulting indexed artifact:

`RATIFIED / ACTIVE`

A second standalone command such as `ratify it` is not required.

### 15.3 Ratification Withheld

Do not ratify under Section 15.2 when the user explicitly requests or indicates:

- draft;
- proposed;
- pending review;
- for review only;
- do not ratify;
- approval withheld;
- another equivalent provisional status.

In those cases, preserve the provisional status exactly.

### 15.4 Material Change After Approval

If the rendered artifact materially departs from the approved design or introduces a substantive rule the user did not approve, prior approval does not automatically cover the new material.

Fail closed on the unapproved delta:

- preserve the artifact as proposed/draft as applicable;
- identify the material difference;
- obtain user approval before ratification.

Minor indexing, metadata, formatting, clarification, or mechanically necessary packaging changes that do not alter substantive meaning do not reopen approval.

### 15.5 Explicit Ratification Command

An explicit user instruction to `ratify`, `ratify and render`, or equivalent remains direct ratification authority for the requested scope, subject to successful rendering and validation.

### 15.6 Lifecycle Result

The default successful Tier 2 lifecycle after prior design approval is:

`design -> approval -> create/render -> validate -> RATIFIED / ACTIVE`

This lifecycle rule prevents redundant approval ceremonies while preserving fail-closed handling of unapproved substantive change.

## 16. v1.1.0 Revision Note

v1.1.0 adds the approved Tier 2 ratification lifecycle rule. When a Tier 2 design or content change has already been explicitly approved, a later instruction to create/render the indexed artifact authorizes ratification and activation after faithful implementation and successful validation, unless the user explicitly requests a provisional status or the render introduces material unapproved change.

This revision eliminates the redundant requirement for a second standalone ratification command after design approval while preserving explicit status distinctions and fail-closed handling of unapproved substantive deltas.

## One-Line Standard

Promote proven reusable mechanisms, not local values; refine existing Tier 2 before creating new authority; test every promotion for evidence, regression, interaction, counterexamples, cost, and reversibility; after explicit design approval, faithful creation/render plus successful validation completes ratification unless the user withholds it.
