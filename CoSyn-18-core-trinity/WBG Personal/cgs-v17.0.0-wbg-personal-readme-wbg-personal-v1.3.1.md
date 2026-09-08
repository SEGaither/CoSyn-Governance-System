# WBG Personal v1.3.1

**Status:** RATIFIED / CANONICAL PERSONAL WBG  
**Version:** 1.3.0  
**Ratified:** 2026-08-22  
**Supersedes:** WBG Personal v1.2.0  
**Canonical WBG dependency:** WBG v1.2.1 — RATIFIED / CANONICAL LAYERED UPDATE  
**Canonical WBG update ZIP SHA-256:** `e85ffc9a003afcf5a14f18aecca9c3f90adea5b3eb4f725d72bd199f570ae987`  
**Underlying WBG v1.1.0 dependency SHA-256:** `ae33253dbbb6d2942715c389687466446c681775a7e47efd6af1b27e56342de6`  
**Required parent CGS through WBG:** CoSyn CGS v16.3.3

## Purpose

WBG Personal v1.3.1 is the reusable private User writing-governance baseline used to start and govern downstream writing projects.

It sits between canonical generic WBG and project-specific writing governance.

## Authority Position

`CoSyn CGS v16.3.3`
→ `WBG v1.2.1`
→ `WBG Personal v1.3.1`
→ `Project-Specific Writing Governance`
→ `Manuscript / Project Artifacts`

## v1.3.0 Change

This revision rolls the canonical WBG project-package creation capability down into the Personal layer.

Added:

`WBG-Personal-Project-Package-Creation-Workflow-v1.0.0.md`

The new artifact specializes the generic canonical workflow for the User's reusable writing-governance context.

It establishes Personal defaults for:

- embedded Tier 2 / Tier 3 package frameworks;
- exact WBG Personal inclusion/dependency handling;
- Personal/project separation during packaging;
- current-source/version verification;
- deterministic rebuild preference;
- no piecemeal ZIP surgery when a clean rebuild is safer;
- fail-closed handling of missing required sources;
- downstream project-specific package-workflow derivatives.

## Preserved Personal Governance

All substantive WBG Personal v1.2.0 writing rules remain active unless explicitly superseded.

No Adventures with G.U.P.P.I project-specific rule is promoted into WBG Personal by this revision.

## Package Entry Points

1. `WBG-Personal-Root-Profile-v1.3.0.md`
2. `WBG-Personal-User-Specialization-v1.3.0.md`
3. `WBG-Personal-Project-Initialization-Profile-v1.3.0.md`
4. `WBG-Personal-Refinement-and-Promotion-Protocol-v1.3.0.md`
5. `WBG-Personal-Project-Package-Creation-Workflow-v1.0.0.md`
6. `WBG-Personal-Bind-Profile-v1.3.0.json`
7. `WBG-Personal-Source-Classification-Ledger-v1.3.0.md`

## Canonical WBG Dependency

WBG Personal v1.3.1 requires an effective canonical WBG v1.2.1 bind.

Because WBG v1.2.1 is a layered update, that effective bind includes its exact WBG v1.1.0 dependency.

The generic canonical WBG bytes are not duplicated into this Personal ZIP.


## v1.3.1 Alignment Delta

This release preserves the v1.3.0 substantive Personal rules and updates only the active Guppi persona/index binding to `Guppi-v1.1.12-082326.md`.
