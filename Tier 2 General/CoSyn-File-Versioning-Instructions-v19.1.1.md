# File Versioning Instructions

**Artifact:** `CoSyn-File-Versioning-Instructions-v19.1.1.md`  
**Version:** 19.1.1  
**Tier:** Tier 2 General — cross-project file versioning  
**Status:** RATIFIED / ACTIVE  
**Date:** 2026-11-25  
**Authority:** Subordinate to the CoSyn Core, applicable project controls, and current explicit user instructions.  
**Ratification basis:** User-approved independent-counter methodology, subsequent approved `vC` canonical designation, and explicit instruction to create and install this Tier 2 artifact.

## 1. Purpose and application

Provide a simple, traceable convention for human–AI collaborative file revisions. Apply to versioned work products unless a more specific, authorized project rule controls. Do not impose this convention retroactively on historical files or change existing filenames without an authorized reason.

## 2. Independent version counters

Use `vX.Y.Z` for ordinary versions:

- **X — major generation:** advance only when the author establishes a new major generation.
- **Y — AI revision counter:** advance when an AI actually modifies the file.
- **Z — author revision counter:** advance when the author actually modifies the file.

All three counters are independent. No counter resets solely because another advances. A request, instruction, review, or approval that does not itself modify the file does not advance a content-revision counter. Attribute revisions according to who made the actual content change, not merely who requested it.

Examples: AI revises `v2.3.4` to `v2.4.4`; author revises `v2.4.4` to `v2.4.5`. A major-generation change requires an author-established designation; do not infer it from the scale of an edit.

## 3. Canonical designation

Insert uppercase `C` immediately after `v` to designate the **author-approved canonical file**: `vC2.4.4`.

- `Manuscript-v2.5.5.md` is a noncanonical working revision.
- `Manuscript-vC2.4.4.md` is the explicitly approved canonical revision.
- The `C` is a status marker, **not** another counter and **not** a content revision.
- Only explicit author approval or an author-authorized approval procedure may assign or move `C`.
- Merely creating a newer file, importing a file, or observing a higher version does not make it canonical.
- When a new revision becomes canonical, ensure that only the currently designated version of the **same work and line** bears `vC` in its managed current set; retain the preceding version without its current-canonical designation. Preserve original source content and historical evidence.
- Do not rename or overwrite an archived source merely to alter a canonical marker. Manage canonical designation in the current working collection or through a documented, authorized transition.

A newer working version can coexist with an older canonical version. Approval without a content edit changes the canonical designation only; it does not advance X, Y, or Z.

## 4. Ordering, branches, and authority

Independent counters do not by themselves prove chronological order. Do not select the latest, parent, or canonical file by lexical filename order, maximum version components, modification time, or Git commit time alone.

For each managed revision, identify its immediate parent version and preserve any branch relationship. An index may identify the latest **working** file and the **canonical** file separately. The `vC` filename is the visible canonical marker; the index is a discovery and lineage aid, not a competing source of approval authority. If records conflict, stop source selection and resolve the conflicting evidence with the author rather than guessing.

## 5. Minimal version index and provenance

Maintain only the records needed to select and understand files reliably. For each managed revision, record:

- Exact filename, version, and repository/path location.
- Parent file/version, including branch origin when applicable.
- Actual modifier (author, AI, or identified contributors) and revision date.
- Brief description of what changed and why, with references to detailed review/decision records where they exist.
- Approval decision or working/rejected/superseded status when established; `vC` marks current canonical designation.
- File hash when available or required for integrity verification.

When a revision is accepted into a managed collection, update the revised file, minimal index entry, and applicable provenance together. Do not claim that any missing historical metadata is known. Keep substantive review, user decisions, and session artifacts as separate referenced provenance where useful; do not duplicate them in the index.

## 6. Source protection and verification

Start revisions from the actual controlling source, not memory or reconstructed text. Preserve unapproved content unchanged, and make only authorized edits. Verify the resulting file and the changed scope before advancing a version or claiming completion. Retain superseded revisions according to the project's history policy; never overwrite originals merely to simplify versioning.

A version label or index entry is not proof of approval, content fidelity, or successful implementation. Record actual outcomes and explicitly identify unverifiable gaps.

## 7. Minimal operating sequence

1. Locate the controlling source and determine whether the work is a content revision or a canonical-status change.
2. Apply the correct independent counter only for actual content changes.
3. Preserve the parent relationship and original file.
4. Verify the output against the intended change.
5. Update the minimal index and provenance; assign or move `vC` only with author authority.

Do not add separate approval ceremonies, databases, or elaborate controls when the filename, minimal index, and provenance are sufficient. Applicable higher-authority and project-specific controls continue to govern.

## 8. Adoption and amendment

This instruction establishes a cross-project default, not a mandate to rename or reclassify existing historical repositories. Project-specific exceptions require explicit authority and must not be silently generalized. Future substantive changes require the applicable Tier 2 refinement and approval process.
