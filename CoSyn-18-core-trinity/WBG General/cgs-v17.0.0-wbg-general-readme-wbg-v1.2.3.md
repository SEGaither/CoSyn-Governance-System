# WBG General — v1.2.3 Ratified Repair Layer

**Status:** RATIFIED / ACTIVE
**Parent:** CoSyn CGS v17.0.0
**WBG Root:** 1.2.0
**Hierarchical Bind Profile:** 1.1.0
**Compatibility Profile:** 1.0.0

This update layer is the ratified WBG v17.0.0 compatibility repair. All v1.2.3 governance artifacts are RATIFIED / ACTIVE as of the CoSyn v17.0.0 repository operationalization.

## Purpose

Introduce the minimum WBG governance update required for full v17.0.0 parent compatibility without modifying any existing registered WBG source bytes.

## What v1.2.3 Proposes

**New Root Authority v1.2.0** — Establishes CoSyn CGS v17.0.0 as the required parent and defines the bounded v17 compatibility mechanism. Ratified successor to v1.1.0. Active as of the CoSyn v17.0.0 repository operationalization.

**New Hierarchical Bind Profile v1.1.0** — Updated bind sequence that incorporates the CGS-v17 Compatibility Profile validation step. Ratified successor to v1.0.0. The existing writing-bind-template-v1.0.0.json is treated as preserved registered baseline material, not replaced. Active as of the CoSyn v17.0.0 repository operationalization.

**New CGS-v17 Compatibility Profile v1.0.0** — Defines the exact conditions under which seven preserved WBG artifacts with embedded legacy parent references (v16.3.3 or v16.3.5) may resolve to CoSyn CGS v17.0.0 without source modification. Active as of the CoSyn v17.0.0 repository operationalization.

## Source Byte Preservation Rule

No existing registered WBG source artifact has been modified by this repair layer. The compatibility mechanism resolves the parent-governance reference only; all other artifact semantics remain unchanged.

## v1.2.2 Status

The existing v1.2.2 artifact contains a status discrepancy. This layer does not resolve, activate, or supersede v1.2.2. v1.2.2 is left in its current state. Version 1.2.3 is used to avoid collision.

## Ratification Status

All v1.2.3 governance has been ratified by the user as part of the CoSyn v17.0.0 repository operationalization. All v1.2.3 artifacts are RATIFIED / ACTIVE and govern WBG operation under CoSyn CGS v17.0.0.
