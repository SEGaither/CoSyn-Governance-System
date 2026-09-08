# Provenance Workflow

**Artifact:** `provenance-workflow-v1.1.0-082126.md`  
**Version:** 1.1.0  
**Status:** RATIFIED / ACTIVE  
**Tier:** Tier 2 — User-specific provenance workflow control  
**Scope:** Cross-project provenance record creation, maintenance, status-transition recording, and validation  
**Created:** 2026-08-21  
**Revised:** 2026-08-21  
**Supersedes:** `provenance-workflow-v1.0.0-082126.md`  
**Ratification basis:** Explicit user instruction on 2026-08-21 to refine, ratify, and render this workflow.  
**Authority:** Subordinate to platform/system requirements, current explicit user instruction, CoSyn CGS, applicable task-specific governance, and project-specific Tier 3 authority.

## 1. Purpose

Define the standard cross-project workflow for creating and maintaining provenance records.

This artifact governs:

`material event -> provenance trigger -> evidence collection -> classification -> provenance record -> validation`

Its primary function is provenance **creation and maintenance**.

It does not define how every downstream workflow must consume provenance. Other workflows may use validated provenance records as evidence when appropriate.

## 2. Provenance Definition

Provenance is a factual record of material project or session state changes and the evidence or authority that produced them.

Provenance is not:

- a transcript of the session;
- a narrative summary of everything that happened;
- a reconstruction from memory;
- an assistant interpretation presented as documentary fact;
- a mechanism for silently changing artifact status or authority.

A provenance record should preserve enough information to reconstruct the material decision and state-change history without unnecessary conversational detail.

## 3. Trigger

### 3.1 Explicit Trigger

When the user requests:

`provenance`

or an equivalent direct request, create a provenance record for the immediately relevant scope.

The requested scope controls.

Do not automatically expand a narrow provenance request into full-session or full-project provenance unless explicitly required.

### 3.2 Automatic Eligibility

The following events make provenance materially eligible:

- artifact creation;
- indexed revision;
- approval;
- ratification;
- supersession;
- rejection;
- material governance change;
- material project-state change;
- significant execution failure;
- correction or recovery that changes authoritative state;
- validation result that controls later execution;
- end-session closure when the active workflow requires provenance.

Eligibility does not automatically require rendering a separate provenance file.

Render one when:

- the user requests it; or
- another governing workflow explicitly requires it.

## 4. Source Discipline

Use only evidence that can support the provenance statement being made.

Valid sources include:

- current-session evidence;
- directly accessible current artifacts;
- explicit user decisions, approvals, corrections, exclusions, and ratifications;
- executed validation results;
- directly observed failures and recoveries;
- current controlling continuation state;
- authoritative provenance already validated for the relevant earlier state.

Memory may be used as a discovery hint only when authoritative evidence is available or expected.

Do not substitute memory for documentary evidence.

If a required fact cannot be supported, mark it unresolved or omit it rather than inventing or reconstructing it.

## 5. Classification

When materially relevant, distinguish among:

- **User decision** — explicit user instruction, approval, ratification, rejection, or scope decision.
- **Source fact** — fact directly supported by an authoritative artifact or observed execution result.
- **Assistant action** — work performed by the assistant.
- **Assistant recommendation** — proposed action or interpretation not yet adopted by the user.
- **Inference** — reasoned conclusion that is not itself documentary fact.
- **Artifact state change** — created, revised, approved, ratified, superseded, rejected, retired, or otherwise changed.
- **Validation result** — PASS, FAIL, limitation, invalidation, or other execution evidence.
- **Unresolved item** — material uncertainty or decision that remains open.

Do not collapse these classes merely to make the record read smoothly.

## 6. Required Provenance Record Content

A provenance record should contain the following when applicable:

### Identity

- title;
- date;
- project;
- session;
- scope;
- artifact type.

### Trigger

- what caused the provenance record to be created;
- explicit user request or governing workflow requirement.

### Authoritative Sources

- controlling artifacts;
- directly relevant source files;
- validation or execution evidence;
- explicit user decisions.

### Material Events

- significant decisions;
- substantive changes;
- failures;
- corrections;
- recoveries;
- validation outcomes.

### User Decisions and Authority Changes

Record explicit:

- approvals;
- ratifications;
- supersessions;
- rejections;
- scope changes;
- authority decisions.

### Artifact State Changes

For each materially affected artifact, identify as applicable:

- filename;
- version;
- prior status;
- resulting status;
- whether created, revised, approved, ratified, superseded, rejected, or otherwise changed.

### Validation

Record validation that materially controls the resulting state, including:

- what was tested;
- result;
- limitations;
- invalidation conditions when relevant.

### Resulting State

State the authoritative outcome produced by the recorded events.

### Open or Unresolved Items

Preserve material unresolved issues rather than silently resolving them.

## 7. Status and Authority Protection

Provenance records must preserve the exact distinction among:

- proposed;
- rendered;
- approved;
- ratified;
- active;
- superseded;
- rejected;
- historical.

Do not:

- promote `rendered` to `approved` without user authority;
- promote `approved` to `ratified` without explicit user authority or a governing lifecycle rule that already carries that authority;
- infer ratification from artifact creation when no prior approval or applicable lifecycle authorization exists;
- treat assistant recommendation as user decision;
- treat repetition as authority;
- treat physical presence as governing status;
- use provenance itself to create authority that did not already exist.

A provenance record documents authority changes. It does not independently cause them.

### 7.1 Recording Authorized Lifecycle Ratification

When an applicable governing workflow defines a lifecycle in which:

`prior explicit approval + later create/render instruction + successful validation = ratified/active`

the provenance record must record the resulting ratification as an authorized state transition, not as silent promotion.

For Tier 2 artifacts governed by the active Tier 2 Refinement Protocol, record:

- the earlier explicit user approval;
- the later creation/render instruction;
- successful validation;
- the resulting `RATIFIED / ACTIVE` status;
- any superseded prior version.

Do not require or fabricate a second standalone ratification command when the governing lifecycle rule already establishes ratification authority.

### 7.2 Withheld or Reopened Approval

If the user requests a provisional status, withholds ratification, or the rendered artifact contains material unapproved change, provenance must preserve that provisional or unresolved state.

Do not record `RATIFIED / ACTIVE` until the required authority condition is actually satisfied.

## 8. Compactness Rule

Record material state change, not conversational volume.

Exclude by default:

- routine acknowledgments;
- repeated explanations;
- ordinary conversational turns;
- abandoned tangents with no continuing effect;
- details already fully represented by a controlling artifact unless needed to explain a state transition;
- full artifact contents when a filename/version/status reference is sufficient.

Include negative evidence when it materially prevents recurrence, such as:

- a failed implementation that exposed a reusable defect;
- a contaminated source path that was abandoned;
- a validation failure that invalidated prior execution state.

## 9. Validation

Before delivering a provenance record, verify:

1. Every material claimed event is supported by available evidence.
2. Explicit user authority is distinguishable from assistant action, recommendation, or inference.
3. Artifact filenames, versions, and statuses are correct.
4. No status or authority was silently promoted; every ratification is supported by explicit user authority or an applicable governing lifecycle rule.
5. Memory was not substituted for available source evidence.
6. Material failures and recoveries affecting current state are preserved.
7. Resulting authoritative state is clear.
8. Material unresolved items remain unresolved.
9. Irrelevant conversational detail has not overwhelmed the record.
10. The provenance record is sufficient to reconstruct the material state-change history for its declared scope.

If validation fails, correct from the authoritative source evidence before delivery.

## 10. Relationship to Other Tier 2 Workflows

This artifact owns the generic provenance-creation workflow.

Specialized artifacts retain their own narrower provenance functions.

### End-Session Package Workflow

The end-session workflow may require a Full Session Provenance member.

When it does, use this provenance workflow as the general creation standard while preserving the end-session artifact's specific package requirements.

### Editing Preferences

Editing Preferences retains authority over revision-level provenance classification, color tracking, review marking, and revision ledgers.

This artifact does not replace those specialized editing controls.

### Tier 2 Refinement Protocol

The Tier 2 refinement workflow may consume validated provenance as operational evidence.

This artifact governs creation of the provenance record, not the later promotion decision.

## 11. File Naming

When rendering a standalone provenance file, use a clear indexable name tied to its scope.

Preferred pattern:

`[project-or-scope]-provenance-[YYYY-MM-DD].md`

When provenance itself is maintained as a versioned operational artifact, use normal indexed versioning.

Do not rename existing source artifacts merely to fit provenance naming.

## 12. Failure Handling

If provenance becomes contaminated by:

- version confusion;
- source conflation;
- unsupported reconstruction;
- incorrect status;
- invented authority;
- missing material state transitions;

do not patch the contaminated narrative from memory.

Return to the authoritative sources and rebuild the affected provenance scope.

## 13. Amendment

Material changes to this workflow require explicit user approval and a new indexed version.

## 14. v1.1.0 Revision Note

v1.1.0 aligns provenance status recording with the ratified Tier 2 lifecycle rule: when prior explicit approval plus a later create/render instruction and successful validation constitute ratification under the governing workflow, provenance records that transition as authorized rather than treating it as silent promotion.

The revision preserves fail-closed behavior when approval is withheld, absent, superseded, or reopened by material unapproved change.

## One-Line Standard

Create provenance from authoritative evidence of material state change; distinguish user authority, source fact, assistant action, inference, artifact status, validation, and unresolved state; record authorized lifecycle ratification when its governing conditions are satisfied; record enough to reconstruct what changed without turning provenance into a transcript.

---

*Document ID: provenance-workflow-v1.1.0 — Tier 2 provenance workflow artifact.*
