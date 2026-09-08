# End-Session Package Prompt

**Artifact:** `end-session-package-prompt-v1.0.1-082626.md`  
**Version:** 1.0.1  
**Tier:** Tier 2 — User-specific operational workflow control  
**Status:** Rendered operational artifact  
**Scope:** Cross-project end-session continuity packaging  
**Created:** 2026-08-21  
**Revised:** 2026-08-26  
**Supersedes:** `end-session-package-prompt-v1.0.0-082126.md`  
**Authority:** Subordinate to platform/system requirements, current explicit user instruction, CoSyn CGS, applicable task-specific governance, and project-specific authority.  
**Revision basis:** Explicit user instruction on 2026-08-26 to ensure every rendered end-session ZIP physically includes a new-session prompt.

## Purpose

Define the standard user-level workflow for creating a compact, authoritative end-session continuation package that allows the next session to resume correctly without reconstructing project state from memory or rereading the full conversation.

This artifact standardizes packaging only. It does not independently ratify, promote, modify, or supersede project artifacts or governing authority.

## Required Package Contents

Create exactly these 6 files:

1. **Continuation State**
   - current project objective and scope;
   - current session state;
   - active governing authorities and bindings;
   - authoritative decisions;
   - current constraints and exclusions;
   - active artifacts and versions;
   - unresolved/open items;
   - anything required to resume safely.

2. **New-Session Resume Prompt**
   - concise startup instructions;
   - identify the continuation package as the controlling handoff;
   - establish project objective/scope as primary and session objective/scope as secondary;
   - instruct the next session to bind current governing authorities;
   - instruct it to read the continuation state and resume without reconstructing from memory;
   - preserve unresolved items;
   - end with readiness/standby instruction;
   - **MUST be physically included as a standalone file inside the rendered end-session ZIP**;
   - rendering the prompt only in chat does not satisfy this requirement.

3. **Full Session Provenance**
   - material decisions;
   - approvals and ratifications;
   - corrections;
   - substantive changes;
   - failures and recoveries;
   - artifacts created, revised, superseded, or rejected;
   - important reasoning outcomes that materially affected project state;
   - distinguish direct user authority from assistant recommendation or inference.

4. **Artifact Reference Ledger**
   - list current controlling/relevant artifacts;
   - filename;
   - version;
   - status;
   - tier/layer where applicable;
   - role/purpose;
   - whether physically included in this package or referenced only;
   - do not duplicate artifacts unless they must travel with the handoff.

5. **Package Manifest**
   - package name;
   - package version;
   - project;
   - closing session;
   - creation date;
   - purpose;
   - exact six-member inventory;
   - statement that the package is a continuity handoff, not a new ratification or authority promotion.

6. **SHA256SUMS**
   - SHA-256 hash for each of the other five package members.

## Packaging Rules

- Package must contain exactly 6 files.
- Keep the ZIP flat.
- The New-Session Resume Prompt is mandatory and must physically exist inside the ZIP before validation passes.
- Do not include manuscript baselines, ordinary deliverables, Tier 1/Core files, bolt-ons, or other project artifacts unless one must physically travel with the handoff to preserve continuity.
- Prefer references in the Artifact Reference Ledger over duplication.
- Preserve original artifact filenames when referencing existing artifacts.
- Do not modify, rename, rewrite, ratify, or promote source artifacts.
- End-session files may use clear purpose-based filenames containing the project/session identifier and current date.
- Preserve current project/session lineage exactly; do not correct historical filenames unless explicitly instructed.
- Current project objective and scope are the primary continuity frame. Session objective and scope are subordinate refinements.

## Validation

Before rendering the ZIP:

1. Verify all six required files exist.
2. Verify the New-Session Resume Prompt exists as a standalone package member.
3. Verify the package contains exactly six files.
4. Verify continuation state matches the current authoritative session state.
5. Verify open items are preserved.
6. Verify no superseded or historical-only artifact is represented as current.
7. Verify no existing project artifact was unnecessarily duplicated.
8. Verify manifest inventory matches actual ZIP contents.
9. Verify SHA-256 values against the rendered files.
10. Open/test the ZIP and verify all members are readable.
11. Recheck for continuity loss, authority drift, version confusion, source conflation, silent promotion, and omission of the new-session prompt.

## Output

Return:
- download link for the end-session ZIP;
- download link for the updated end-session workflow artifact when revised during the closing session;
- ZIP SHA-256;
- six-file inventory;
- validation result;
- unresolved continuity defects only if any remain.

## Operational Rules

- Use this artifact only for end-session closure, EOS packaging, or equivalent continuation handoff.
- Project objective and scope are primary; session objective and scope are subordinate.
- Existing project artifacts should be referenced rather than duplicated unless physical inclusion is required for safe continuity.
- A continuation package preserves state; it does not create new authority.
- Missing or unresolved state must remain visibly unresolved rather than reconstructed or guessed.
- The New-Session Resume Prompt is a mandatory physical member of the rendered ZIP.

## Amendment

Material changes require explicit user approval and a new indexed version.

## v1.0.1 Revision Note

v1.0.1 hardens an existing requirement already present in v1.0.0.

The New-Session Resume Prompt was already package member #2. This revision makes implementation explicit:

- the prompt must exist as a standalone file inside the rendered ZIP;
- rendering it only in chat does not satisfy the workflow;
- validation fails if the prompt file is absent.

The package remains flat and exactly six files.

---

*Document ID: end-session-package-prompt-v1.0.1 — Tier 2 operational workflow artifact.*
