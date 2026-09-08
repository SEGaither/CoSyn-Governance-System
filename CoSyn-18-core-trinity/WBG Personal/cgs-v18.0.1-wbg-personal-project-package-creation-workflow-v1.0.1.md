---
wbg_personal_artifact:
  schema_version: "1.0.0"
  artifact_id: "urn:cosyn:wbg-personal:project-package-creation-workflow:1.0.0"
  artifact_name: "WBG Personal Project Package Creation Workflow"
  artifact_version: "1.0.0"
  filename: "WBG-Personal-Project-Package-Creation-Workflow-v1.0.0.md"
  artifact_class: "personal_operational_specialization"
  status: "RATIFIED"
  authority_ceiling: "WBG-Project-Package-Creation-Workflow-v1.0.0.md"
  required_wbg: "1.2.1"
  required_parent_cgs: "18.0.1"
  supersedes: null
---

# WBG Personal Project Package Creation Workflow — v1.0.0

**Status:** RATIFIED / ACTIVE PERSONAL SPECIALIZATION  
**Parent capability:** `WBG-Project-Package-Creation-Workflow-v1.0.0.md`  
**Required canonical WBG:** v1.2.1  
**Required parent CGS:** CoSyn CGS v18.0.1

## 1. Purpose

Specialize the canonical WBG project-package creation workflow for the User's reusable writing-governance layer.

This artifact governs how WBG Personal participates in creation of downstream project-specific WBG ZIP packages.

It does not replace or weaken the canonical workflow.

## 2. Inherited Controls

The following canonical requirements are inherited without modification:

- source-integrity control;
- authority-layer separation;
- Tier 2 / Tier 3 distinction;
- version and lineage control;
- package/member status separation;
- ratification vs instantiation distinction;
- manifest and SHA-256 coverage;
- missing-source fail-closed handling;
- no silent reconstruction of canonical bytes;
- explicit dependency locking;
- final ZIP validation;
- no-promotion-through-packaging rule.

If this Personal specialization conflicts with the canonical workflow, the canonical workflow controls.

## 3. Personal-Layer Package Default

For a project using WBG Personal, the preferred portable package framework is:

```text
<Project>-WBG-Project-Package-vX.Y.Z/
│
├── README.md
├── PACKAGE-MANIFEST.json
├── SHA256SUMS.txt
│
├── Tier-2/
│   ├── WBG-Canonical/
│   ├── WBG-Personal/
│   ├── Personas/
│   └── Other-Dependencies/
│
└── Tier-3/
    ├── Governance/
    ├── Operational/
    ├── Reference/
    └── Templates/
```

Folder placement communicates package structure only. It does not create or promote authority.

## 4. Default Tier 2 Selection

When applicable to the project, Tier 2 should contain or explicitly lock to:

1. the active canonical WBG release;
2. the active WBG Personal release;
3. only the cross-project personas needed by the project;
4. only other cross-project operational/governance dependencies needed to interpret or execute the project package.

Do not include unrelated Tier 2 material for completeness theater.

## 5. WBG Personal Inclusion Rule

The active WBG Personal package is the reusable User-level writing specialization.

A downstream project package may:

- embed the exact ratified WBG Personal package;
- embed its verified extracted members;
- or use an explicit dependency lock if the canonical workflow permits a layered package.

Whichever method is used must preserve exact version identity and integrity evidence.

## 6. Project-Specific Roll-Down

Each project may create a project-specific derivative of this workflow.

The project derivative may specify:

- exact project package name;
- exact Tier 3 governance files;
- exact operational ledgers;
- exact project references;
- exact project templates;
- required project personas;
- additional project-specific validation checks.

The project derivative may narrow or add structure.

It may not weaken inherited integrity, authority, ratification, versioning, or missing-source controls.

## 7. Personal / Project Separation

Project-specific files remain Tier 3 unless explicitly promoted through the WBG Personal refinement/promotion process.

Repeated inclusion in project ZIPs does not promote a project rule.

A project artifact does not become Personal merely because the Personal workflow packages it.

## 8. Source Currency Before Packaging

Before a project package is rendered:

- verify the current ratified canonical WBG version;
- verify the current ratified WBG Personal version;
- verify current applicable persona versions;
- verify current project-specific control versions;
- reject stale filenames when a superseding active artifact is known;
- preserve unresolved authority/status conflicts instead of silently resolving them.

## 9. User-Specific Robustness Rules

For this User:

- do not perform piecemeal patching of package structures when a deterministic rebuild is safer;
- prefer one complete validated render over iterative ad hoc ZIP surgery;
- surface any missing required source before claiming completion;
- preserve original filenames unless a versioned revision is intentionally created;
- do not overbuild the package beyond the approved framework;
- stop once the approved structure and integrity checks pass.

## 10. Ratification Gate

A project-specific ZIP may be ratified only after:

1. inherited canonical WBG package workflow checks pass;
2. WBG Personal dependency/version is current;
3. Personal/project separation is intact;
4. project-specific derivative requirements pass;
5. explicit User ratification is obtained where ratification is required.

If a required Personal or canonical source is missing, package status must remain incomplete/hold unless a valid layered dependency model applies.

## 11. Completion Standard

The final report should state:

- package name/version;
- package status;
- canonical WBG dependency;
- WBG Personal dependency;
- member count;
- ZIP SHA-256;
- validation result;
- any external dependency or unresolved source issue.

**Personal-layer standard:** carry the User's reusable writing governance into the package without confusing portability with promotion.
