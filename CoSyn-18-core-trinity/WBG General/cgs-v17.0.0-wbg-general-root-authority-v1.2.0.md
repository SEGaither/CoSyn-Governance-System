---
wbg_artifact:
  schema_version: "1.0.1"
  artifact_family_id: "wbg.root.authority"
  artifact_id: "urn:cosyn:wbg:wbg-root-authority:1.2.0"
  artifact_name: "WBG Root Authority"
  artifact_version: "1.2.0"
  filename: "cgs-v17.0.0-wbg-general-root-authority-v1.2.0.md"
  artifact_class: "root_authority"
  wbg_layer: "root"
  status: "RATIFIED / ACTIVE"
  authority_ceiling: "CoSyn CGS v17.0.0"
  minimum_wbg_root: "1.2.0"
  required_parent_cgs: "17.0.0"
  capabilities_provided:
    - "writing.wbg.hierarchy"
    - "writing.wbg.extension-registration-authority"
    - "writing.wbg.cgs-v17-compatibility-authority"
  activation:
    - "successful WBG v1.2.x hierarchical bind under CoSyn CGS v17.0.0"
  dependencies:
    - "family:wbg.sync.registration-contract"
    - "family:wbg.bind.hierarchical-profile"
    - "family:wbg.compatibility.cgs-v17"
  supersedes_artifact_id: "urn:cosyn:wbg:wbg-root-authority:1.1.0"
  supersession_status: "RATIFIED — supersession is active and effective as of CoSyn v17.0.0 repository operationalization"
  integrity:
    method: "external_registry_sha256"
---

# WBG Root Authority — v1.2.0

**Status:** RATIFIED / ACTIVE
**Required parent:** CoSyn CGS v17.0.0
**Proposed supersession target:** urn:cosyn:wbg:wbg-root-authority:1.1.0
**Registered baseline:** WBG v1.0.0 RATIFIED / CANONICAL by external ratification provenance

This artifact is ratified as part of the CoSyn v17.0.0 repository operationalization.

## 1. Purpose

Establish WBG's internal hierarchy under CoSyn CGS v17.0.0, enable independently versioned writing capabilities to register without forcing unrelated WBG artifacts to be re-versioned, and define the bounded compatibility mechanism that permits preserved registered WBG source bytes to remain unchanged when exact-identity validation succeeds.

## 2. Authority Hierarchy

`Platform authority`
→ `CoSyn CGS v17.0.0`
→ `WBG Root Authority`
→ `registered WBG base governance`
→ `registered WBG functional extensions`
→ `project-specific writing governance`
→ `manuscript / project artifacts`

Lower layers may extend but may not weaken, fork, bypass, or compete with higher authority.

## 3. Baseline Preservation

The ratified WBG v1.0.0 11-artifact package remains the initial WBG base.

Its files are not rewritten for this hierarchy.

The baseline is registered through:

`WBG-Base-Artifact-Registry-v1.0.1.json`

The v1.0.0 package content fingerprint (SHA-256 of sorted filename:member_sha256 lines) is:

`37ff43471c8b21756319ff5d9c603654bc56780b87176817a031e6d7691c4b98`

This fingerprint is the registered baseline compatibility anchor.

## 4. Legacy Ratification Status Exception

The actual v1.0.0 member metadata still contains the pre-ratification marker `PROPOSED / READY FOR USER REVIEW`.

External WBG v1.0.0 provenance records the later explicit User ratification and controls package status.

The registry may therefore mark those exact verified baseline bytes as RATIFIED without rewriting them.

This exception applies only to the registered v1.0.0 baseline.

## 5. CGS v17.0.0 Compatibility

Some preserved WBG artifacts contain legacy parent-governance references to CoSyn CGS v16.3.3 or v16.3.5. These references are embedded source metadata, not re-authored content.

The proposed CGS-v17 Compatibility Profile (family: wbg.compatibility.cgs-v17) defines the exact bounded conditions under which such references resolve to CoSyn CGS v17.0.0 without modifying the source bytes.

**Compatibility does not modify source artifact semantics except for resolution of the registered legacy parent-governance metadata described by the ratified compatibility profile.**

Preserved registered WBG source bytes may remain unchanged when exact-identity compatibility validation succeeds under the profile's conditions.

The compatibility profile is ratified; this mechanism is active.

## 6. Root Ownership

This Root owns:

- WBG hierarchy;
- WBG layer precedence;
- extension-registration authority;
- WBG-level capability-conflict handling;
- WBG-level independent extension versioning;
- authority to define bounded CGS-version compatibility for preserved registered WBG artifacts.

It does not take over the substantive capabilities already owned by v1.0.0 base artifacts.

## 7. Registration Contract

New WBG artifacts conform to:

`WBG-Artifact-Registration-and-Sync-Contract-v1.0.1.md`

The contract preserves the existing WBG v1.0.0 identifier rule:

`urn:cosyn:wbg:<artifact-slug>:<version>`

A separate `artifact_family_id` supplies stable cross-version registration identity.

## 8. Binding

The existing `writing-bind-template-v1.0.0.json` continues to own **baseline WBG v1.0.0 binding**.

It is treated as preserved registered baseline material under the proposed hierarchical bind profile v1.1.0. Its source bytes are unchanged.

The proposed v1.2.x hierarchical wrapper is:

`cgs-v17.0.0-wbg-general-hierarchical-bind-profile-v1.1.0.json`

That profile:

1. validates/binds CoSyn CGS v17.0.0;
2. validates the exact registered v1.0.0 baseline content fingerprint;
3. loads this Root and the sync contract;
4. loads the proposed CGS-v17 Compatibility Profile and validates registered artifacts;
5. registers available extensions;
6. preserves the existing Project Governance handoff.

## 9. Self-Announcement

A WBG extension may announce its identity, capabilities, activation conditions, dependencies, and authority through its metadata when it is actually available to the session.

Self-announcement is not self-loading.

No artifact may claim it can inject itself into an unavailable model context.

## 10. Capability Ownership

One active governing capability has one active owner.

If two active artifacts claim the same capability and explicit supersession/precedence does not resolve the conflict:

`WBG CAPABILITY CONFLICT — FAIL CLOSED`

Advisory persona purview does not count as functional capability ownership.

## 11. Independent Versioning

Bump the Root only for hierarchy, authority, registration semantics, compatibility, or parent-governance changes.

Bump a functional artifact when its owned functional behavior changes.

Bump the Extension Index when discovery/integrity entries change.

Do not version-bump an unchanged base artifact merely because another artifact is added.

## 12. Project Governance

Project-specific writing governance remains downstream of WBG.

It may specialize WBG but may not:

- override this Root;
- take an already owned WBG capability;
- falsify provenance/source identity;
- convert a failed mandatory gate into a PASS.

## 13. Runtime Boundary

This hierarchy is interpreted governance/context.

It does not claim executable persistence, filesystem watching, automatic network loading, or independent host enforcement.

## 14. One-Line Standard

**Keep WBG authority stable under CoSyn CGS v17.0.0; let validated writing capabilities evolve independently; preserve registered source bytes when exact-identity compatibility succeeds.**
