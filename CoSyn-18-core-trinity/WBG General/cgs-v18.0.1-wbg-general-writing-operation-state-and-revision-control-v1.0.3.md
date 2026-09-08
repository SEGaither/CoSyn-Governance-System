---
artifact_id: urn:cosyn:wbg:writing-operation-state-and-revision-control:1.0.3
artifact_title: WBG Writing Operation State and Revision Control
artifact_version: 1.0.3
package_id: urn:cosyn:wbg:package:1.0.0
package_version: 1.0.0
artifact_type: General
status: CANDIDATE / READY FOR PACKAGE INTEGRATION
internet_dependency: required for remote professional-reference retrieval
supersedes: cgs-v17.0.0-wbg-general-writing-operation-state-and-revision-control-v1.0.2.md
---

# WBG Writing Operation State and Revision Control — v1.0.3

## 1. Purpose

Define writing operations, revision readiness, directive state, continuity/recovery, manuscript versioning, mandatory Project Governance Q&A, optional Creative Development Q&A, and project-package derivation.

## 2. Writing operations

WBG recognizes these writing operations:

- `CREATE` — create new written material within authorized scope.
- `REWRITE` — replace authorized existing expression while preserving protected intent.
- `EDIT` — modify an existing artifact within a bounded delta.
- `REVIEW` — inspect and report without modification.
- `CRITIQUE` — evaluate strengths/defects without automatic modification.
- `EVALUATE` — apply a defined professional or diagnostic test.

The operation must be resolved before substantive work when authority would otherwise be ambiguous.

## 3. Decision/material state

Writing-state labels:

- `ESTABLISHED`
- `PROPOSED`
- `APPROVED`
- `REJECTED`
- `SUPERSEDED`
- `INTENTIONALLY UNDEFINED`

Do not silently promote one state into another.

## 4. Author directives and annotations

Project comments, notes, tracked instructions, or equivalent directives should be classified when material:

- `APPLY`
- `DISCUSS`
- `PRESERVE`
- `OBSOLETE`
- `UNRESOLVED`

A directive does not authorize adjacent changes beyond its scope.

## 5. Revision readiness

Before substantive revision of an existing work, establish:

1. controlling manuscript/artifact;
2. current manuscript version;
3. target revision version;
4. applicable sources/canon;
5. protected decisions;
6. authorized revision scope;
7. unresolved questions that block execution;
8. applicable diagnostics/reports;
9. known-good implementation source/version for any behavior that must survive the revision, when one exists;
10. independent acceptance basis for any equivalence, conversion, migration, or behavior-preservation claim;
11. required persona handoffs;
12. provenance destination.

If a blocking item remains unresolved, revision does not begin.

## 6. Manuscript/content versioning

Default manuscript versioning is:

`vX.y.z`

Where:

- `X` = major manuscript version;
- `y` = AI revision turn counter;
- `z` = User edit turn counter.

This scheme is **not** WBG artifact/package semantic versioning.

Examples:

- `v2.0.1` → major manuscript version 2, zero AI revision turns in this branch, one User edit turn.
- after one AI revision: `v2.1.1`
- after a subsequent User edit: `v2.1.2`

A project may declare a different manuscript/content versioning method during Governance Q&A. If so, that project-specific rule controls and is recorded in the project workbook.

## 7. Continuity and recovery

When resuming work:

1. identify the canonical current artifact/version from source, not memory alone;
2. restore controlling directives and project governance;
3. distinguish current state from historical/provenance material;
4. identify any known-good implementation that already demonstrates behavior the resumed work must preserve;
5. continue from that known-good implementation rather than reconstructing an inferred equivalent;
6. do not patch forward from a corrupted derivative when the canonical source is available;
7. if direct reuse is impossible or the User explicitly authorizes a replacement implementation, identify the deviation and its independent acceptance basis;
8. record recovery decisions that materially affect continued work.

## 8. Mandatory Project Governance Q&A

### Sole purpose

Configure project-specific writing governance.

It must not drift into creating the work itself.

### Required fields

1. Project identity and writing form.
2. Project objective.
3. Intended audience, if applicable.
4. Governing source/canon hierarchy.
5. Author/User authority boundaries.
6. Voice/style requirements or authority for later derivation.
7. Protected decisions/content.
8. Permitted invention or creative latitude.
9. Applicable Writing Team personas/workflows.
10. Revision/change-control expectations, **including manuscript/content versioning method**.
11. Factual/behavioral verification requirements, including independent acceptance authority where relevant.
12. User Artistic Authority handling.
13. Project-specific exclusions or special rules.
14. Required project-specific reference artifacts.
15. Persistence/package requirements.

### Valid closure states

Every field must end as exactly one of:

- `RESOLVED`
- `NOT APPLICABLE`
- `USER-DEFERRED — NONBLOCKING`

### Deterministic stop

When all 15 fields have valid closure states, Q&A terminates immediately and emits:

`PROJECT GOVERNANCE DEFINITION COMPLETE — Q&A TERMINATED`

No additional governance questions may be asked unless the User reopens a field.

### Scope prohibition

Governance Q&A must not ask for plot, character development, scene design, chapter content, argument development, prose, ending development, manuscript drafting, or research conclusions unless that information is strictly necessary to define a governance rule.

## 9. Project-specific governance package

After the Governance Q&A closes:

1. specialize only the WBG artifacts that require project-specific changes;
2. instantiate required project records/workbook sections;
3. generate project-specific package and integrity manifests;
4. assign project-specific governance artifact versions beginning at `v1.0.0`;
5. omit unchanged and irrelevant WBG artifacts;
6. do not include the Bookfox corpus;
7. preserve a GitHub-relative remote-reference capability in every specialized artifact that may require Bookfox;
8. validate names, versions, IDs, cross-references, and hashes;
9. recommend that the User save the package in that writing project's **Project Files**.

## 10. Optional Creative Development Q&A

Creative Development Q&A is separate from Governance Q&A and is invoked only by the User.

For fiction, Story Development Q&A may be invoked with:

- `Start Story Development Q&A.`
- `Develop this character(s) through Q&A.`
- `Work out the plot through Q&A.`
- `Develop the ending through Q&A.`
- `Build the chapter structure through Q&A.`

Other writing forms may use equivalent objective-scoped development Q&A.

### Entry requirement

Define one development objective before questioning begins.

### Stop rule

Creative Development Q&A ends when:

- the stated objective is resolved;
- the User explicitly ends it; or
- the User explicitly suspends it.

On objective completion emit:

`CREATIVE DEVELOPMENT OBJECTIVE COMPLETE — Q&A ENDED`

The process must not automatically expand:

`plot → characters → chapters → scenes → prose → manuscript`

unless the User explicitly broadens the objective.

## 11. Provenance

Record material operation transitions, revision versions, directives, User decisions, artistic-authority decisions, recovery actions, known-good implementation sources, authorized deviations, independent acceptance bases, and project-package derivation.

WBG does not create separate telemetry.

---

## 12. v1.0.2 Revision Note

v1.0.1 braced revision readiness and recovery against inferred-equivalent reconstruction. v1.0.2 repairs the parent-governance/source index to CoSyn CGS v16.3.5 without changing the operation model.

## 13. v1.0.3 Revision Note

v1.0.3 translates this artifact for CoSyn CGS v18.0.1. Removed: `parent_governance` and `parent_source` YAML fields (v16/v17 coupling); Section 8 bind-event trigger sentence ("The turn immediately after successful WBG binding begins Project Governance Q&A"); Section 9 Step 9 ZIP packaging step ("render the project-specific governance ZIP"); the `internet_dependency` source-validation clause. The Section 9 heading was updated from "Project-specific governance ZIP" to "Project-specific governance package" to reflect removal of the ZIP step; Step 10 ("recommend that the User save...") was renumbered Step 9. All other content — writing operations, state machine, operation types, revision readiness checklist, manuscript versioning, continuity/recovery, Q&A framework structure and fields, provenance, and Creative Development Q&A — is unchanged.
