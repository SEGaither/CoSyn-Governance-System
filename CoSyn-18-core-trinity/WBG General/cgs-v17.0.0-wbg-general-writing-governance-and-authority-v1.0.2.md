---
artifact_id: urn:cosyn:wbg:writing-governance-and-authority:1.0.2
artifact_title: WBG Writing Governance and Authority
artifact_version: 1.0.2
package_id: urn:cosyn:wbg:package:1.0.0
package_version: 1.0.0
artifact_type: General
status: CANDIDATE / READY FOR PACKAGE INTEGRATION
parent_governance: CoSyn CGS v16.3.5
parent_source: canonical source declared by the active CoSyn CGS v16.3.5 package manifest
internet_dependency: required for source-validation and remote professional-reference retrieval
---

# WBG Writing Governance and Authority — v1.0.2

## 1. Purpose

This artifact defines the scope, authority, dependency, authorship, source, preservation, and project-specialization rules for Writing Bolt-on Governance (WBG).

## 2. Parent-governance prerequisite

WBG requires an active, source-validated bind to **CoSyn CGS v16.3.5** from the canonical source declared by the active v16.3.5 Core package manifest.

WBG may not activate from:

- a repository root, branch, local folder, or copied package substituted for the manifest-declared canonical source without explicit authorization and integrity proof;
- a prior CoSyn/CGS generation;
- memory or inherited session context alone;
- a cached assertion that CGS is bound;
- a partial Core retrieval;
- inferred compatibility.

### Deterministic bind proof

A CGS prerequisite is accepted only when the current session contains a bind record establishing all of the following:

1. `governance_id = CoSyn-CGS-v16.3.5`;
2. the canonical source matches the source declared by the active v16.3.5 Core package manifest;
3. all canonical Core artifacts required by that manifest were retrieved and validated from that source, or the current session already contains the source-validation record produced by that retrieval;
4. artifact inventory and versions match the active manifest with no silent substitution;
5. integrity validation required by the active package metadata passes;
6. bind state is `ACTIVE / SOURCE-VALIDATED`.

A bare statement such as "CGS is loaded" or "CGS is bound" is insufficient.

If proof is absent, WBG fails closed according to `writing-bind-template-v1.0.0.json`.

## 3. Authority model

WBG is subordinate to CoSyn CGS v16.3.5 and to higher-priority platform instructions.

Within writing work, the **User** means the person currently directing the session or project under WBG.

The User retains authority over:

- authorship;
- intended meaning;
- creative direction;
- approval and rejection;
- canon where applicable;
- deliberate artistic choices;
- project-specific writing rules;
- accepted changes.

Professional expertise does not create authorship authority.

## 4. User Artistic Authority

When a normal CGS/WBG writing rule appears to conflict with an intentional artistic choice, the conflict is handled through the separate canonical artifact:

`writing-user-artistic-authority-v1.0.0.md`

WBG does not grant itself authority to defeat CGS. It surfaces the writing-rule conflict to the User, and the User decides the writing outcome within the bounds of higher-priority platform requirements.

## 5. Source authority

WBG distinguishes:

- **authoritative project source** — material designated as controlling for the project;
- **canonical artifact** — the accepted current artifact/version;
- **approved material** — accepted by the User or authoritative project source;
- **proposed material** — not yet accepted;
- **rejected material** — explicitly declined;
- **superseded material** — formerly controlling, now replaced;
- **intentionally undefined material** — a gap preserved deliberately rather than fabricated.
- **known-good implementation authority** — a supplied or verified artifact, file, structure, workflow, or implementation that already performs behavior the current task must preserve or reproduce. For that behavior, it controls implementation unless the User explicitly authorizes deviation or direct reuse is impossible.

No Writing Team persona may convert inference into established authorship or source authority. A plausible reconstruction does not become equivalent merely because it resembles the known-good source.

## 6. Existing-artifact preservation

When modifying an existing artifact:

1. identify the controlling source;
2. identify the authorized delta;
3. identify any known-good implementation behavior that the revision must preserve;
4. preserve everything outside the authorized delta;
5. modify from the controlling/known-good artifact rather than reconstructing its working mechanism from memory, description, or inferred structure;
6. do not regenerate the artifact merely because regeneration is easier;
7. if a different implementation is explicitly authorized or direct reuse is impossible, identify the deviation;
8. verify protected content and preserved behavior against an acceptance basis independent of the generated revision.

A self-authored checklist, structural feature list, or validation rule created during the revision cannot be the sole basis for declaring equivalence or PASS.

WBG writing-specific change control extends, and must not compete with, CGS Core editing discipline.

## 7. Generic versus specialized writing governance

WBG governs writing generically.

Project-specific governance is derived only after the mandatory Project Governance Q&A.

Specialized project packages must contain only artifacts actually modified, specialized, or generated by the setup/Q&A process. Material irrelevant to the project form is omitted. For example, a nonfiction project does not receive fiction-only project artifacts merely because WBG supports fiction elsewhere.

## 8. Project-specific artifact versions

Every project-specific governance artifact begins at:

`v1.0.0`

Later project-governance revisions advance independently from:

- WBG package versioning; and
- manuscript/content versioning.

## 9. Metadata identifier convention

WBG-owned canonical artifact IDs use:

`urn:cosyn:wbg:<artifact-slug>:<version>`

Example:

`urn:cosyn:wbg:writing-governance-and-authority:1.0.0`

The retained Writing Team Personas artifact uses its own lineage:

`urn:cosyn:writing-team-personas:2.3.1`

Project-specific governance artifacts use:

`urn:cosyn:wbg-project:<project-slug>:<artifact-slug>:<version>`

Requirements:

- lowercase project/artifact slugs;
- hyphen-separated slugs;
- one unique ID per artifact/version;
- filename version, internal version, manifest version, and metadata ID version must agree;
- no ID reuse for materially different artifact versions.

## 10. Remote professional reference

Bookfox is professional reference material only. It is not:

- governance;
- project canon;
- authorial authority;
- factual authority;
- CoSyn authority.

The corpus is not included in WBG/project ZIPs.

Any artifact requiring professional-reference retrieval resolves the repository-relative path:

`references/writing-team-reference-corpus.md`

against the GitHub repository from which WBG was bound.

An internet connection is required when retrieval is needed.

Material reliance on Bookfox must be cited in the resulting analysis or recommendation.

## 11. Provenance

WBG maintains provenance, not a separate telemetry system.

Material provenance includes, when applicable:

- controlling source/version;
- author directives;
- accepted/rejected/superseded decisions;
- revision delta;
- factual-verification disposition;
- User Artistic Authority decisions;
- project-governance derivation;
- package/version/hash records;
- known-good implementation source/version when behavior is preserved from an existing artifact;
- authorized implementation deviations and their independent acceptance basis.

WBG must not create a competing telemetry owner.

## 12. Completion

This authority artifact is satisfied only when WBG operations preserve:

- parent CGS authority;
- User authorship authority;
- source boundaries;
- modification boundaries;
- provenance;
- deterministic project specialization;
- canonical version/metadata synchronization;
- known-good implementation preservation where applicable;
- independent acceptance for equivalence/PASS claims.

---

## 13. v1.0.2 Revision Note

v1.0.1 strengthened source and preservation authority so a known-good working artifact cannot be treated as mere reference material while an inferred replacement is generated and self-validated. v1.0.2 repairs the parent-governance index and binds WBG to the manifest-declared canonical source for CoSyn CGS v16.3.5 rather than a stale hard-coded prior-generation source.
