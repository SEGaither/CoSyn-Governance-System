---
wbg_artifact:
  schema_version: "1.0.1"
  artifact_family_id: "wbg.project-package.creation-workflow"
  artifact_id: "urn:cosyn:wbg:project-package-creation-workflow:1.0.0"
  artifact_name: "WBG Project Package Creation Workflow"
  artifact_version: "1.0.0"
  filename: "WBG-Project-Package-Creation-Workflow-v1.0.0.md"
  artifact_class: "functional_extension"
  wbg_layer: "functional_extension"
  status: "RATIFIED"
  authority_ceiling: "urn:cosyn:wbg:wbg-root-authority:1.1.0"
  minimum_wbg_root: "1.1.0"
  required_parent_cgs: "16.3.3"
  capabilities_provided:
    - "writing.wbg.project-package-creation"
    - "writing.wbg.embedded-tier-package-structure"
    - "writing.wbg.package-integrity-validation"
  activation:
    - "creation or revision of a WBG Personal package"
    - "creation or revision of a project-specific WBG package"
    - "creation of a portable WBG package with embedded authority-layer folders"
  dependencies:
    - "family:wbg.root.authority"
    - "family:wbg.sync.registration-contract"
    - "family:wbg.bind.hierarchical-profile"
    - "family:wbg.base-artifact-registry"
  handoffs:
    - "project-specific package workflow derivative"
  conflicts: []
  supersedes_artifact_id: null
  integrity:
    method: "external_registry_sha256"
---

# WBG Project Package Creation Workflow — v1.0.0

**Status:** RATIFIED / CANONICAL  
**WBG release:** v1.2.1  
**Required parent:** CoSyn CGS v16.3.3  
**Purpose:** Govern creation of portable WBG Personal and project-specific WBG ZIP packages with explicit embedded authority-layer folders.

## 1. Scope

This workflow governs package construction, not substantive writing decisions.

It defines how to assemble, classify, validate, version, instantiate, ratify, and render a WBG package that carries its applicable governance dependencies and downstream specialization in an auditable directory structure.

It may be specialized downstream by WBG Personal and by project-specific WBG governance.

Downstream specializations may add stricter controls or project-specific directories. They may not weaken source integrity, authority separation, ratification boundaries, or validation requirements established here.

## 2. Core Packaging Principle

A package directory may physically contain multiple governance layers without changing the authority of the artifacts inside it.

Folder placement is packaging structure, not authority promotion.

A project-specific WBG package should make the distinction visible:

- `Tier-2/` contains applicable cross-project/user-level WBG governance and required persona/operational dependencies.
- `Tier-3/` contains project-specific governance, operational records, references, and templates.

Do not promote a Tier 3 artifact into Tier 2 merely because it is useful outside its original directory.

## 3. Entry Conditions

Before package construction:

1. Bind or validate the required parent CoSyn CGS version.
2. Bind the active canonical WBG release.
3. If applicable, bind the active WBG Personal release.
4. Identify the project-specific WBG control artifacts.
5. Identify applicable Tier 2 persona or operational dependencies.
6. Freeze the exact source set for the build.
7. Record the intended package name and version.
8. Resolve which artifacts are:
   - RATIFIED / ACTIVE;
   - INSTANTIATED / ACTIVE;
   - TEMPLATE / NOT YET EXECUTED;
   - PROPOSED / DRAFT;
   - SUPERSEDED;
   - reference-only.

Do not infer ratification from inclusion in the package.

## 4. Default Directory Framework

Unless a downstream specialization validly changes the structure, use:

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

Empty directories need not be emitted.

A package may use more specific subdirectories when that improves clarity without obscuring authority.

## 5. Tier 2 Selection Rule

Include only Tier 2 material that is applicable to the downstream package.

Typical Tier 2 contents may include:

- the active canonical WBG release or an exact dependency reference to it;
- the active WBG Personal release when the project uses it;
- applicable cross-project persona artifacts;
- applicable cross-project operational governance required to interpret or execute the project package.

Do not dump unrelated Tier 2 artifacts into the package merely because they exist.

## 6. Tier 3 Selection Rule

Tier 3 contains project-specific material.

Typical categories:

### Governance
Ratified project-specific controls, project bind records, source-authority rules, voice controls, or other project governance.

### Operational
Ledgers, working-state records, source maps, provenance records, execution records, and other project operational artifacts.

### Reference
Non-governing project references, credits, factual reference notes, or other supporting material.

### Templates
Instantiated shells intended for later execution.

Templates must be labeled as templates and must not be represented as completed work.

## 7. Source Integrity Rule

Every packaged source must come from an actual available source.

Do not:

- reconstruct missing canonical text from memory;
- replace a missing source with a paraphrase;
- silently use a similarly named older file;
- manufacture a canonical artifact from metadata alone;
- treat a file-search result title as proof that exact bytes are locally available.

If a required canonical source is missing:

1. fail closed for a claim of byte-complete packaging;
2. identify the exact missing artifact;
3. preserve any known expected hash or provenance;
4. do not fabricate the file;
5. either obtain the exact source or, if explicitly authorized, render a clearly labeled incomplete/candidate package.

A missing required source cannot be cured by a placeholder marker while still claiming the package is byte-complete.

## 8. Canonical Dependency Alternative

When an exact prior canonical package is an approved dependency, a later WBG package may use a layered update model instead of duplicating unchanged prior bytes.

The dependency lock must record:

- exact filename or package identity;
- exact version;
- exact SHA-256;
- whether it is embedded or externally required;
- which update-layer artifacts supersede members from the dependency;
- effective assembly order.

A layered package must not claim to be standalone if the dependency bytes are not embedded.

## 9. Ratification vs Instantiation

Use status according to function.

### Ratify
Ratify artifacts that establish governing authority, controlling workflow, or mandatory project rules.

### Instantiate
Instantiate operational artifacts, ledgers, references, and templates when they are created for use but do not themselves establish new governing authority.

### Template
A template may be instantiated without being executed.

### Package status
The package's status is distinct from member status.

A ZIP may contain ratified artifacts while the ZIP itself remains:

- PROPOSED;
- INCOMPLETE;
- READY FOR RATIFICATION;
- or RATIFIED / CANONICAL.

Do not allow member ratification to silently ratify the container.

## 10. Version and Lineage Control

Before rendering:

1. preserve unchanged artifact versions;
2. bump only artifacts whose governed behavior or material metadata changes;
3. record supersession explicitly;
4. preserve independently versioned persona or extension lineages;
5. update package-level README, manifest, integrity records, and provenance for the new package version;
6. do not overwrite the prior canonical package.

## 11. Manifest Requirements

The package manifest must identify at minimum:

- package name;
- package version;
- package status;
- creation date;
- required parent CGS;
- required canonical WBG;
- applicable WBG Personal version;
- authority-layer structure;
- every packaged member;
- relative path;
- artifact version where applicable;
- artifact status;
- role/classification;
- supersession if applicable;
- known external dependencies;
- known missing required sources, if any.

The manifest must not hide an unresolved source gap.

## 12. Integrity Requirements

Generate SHA-256 coverage for every packaged file except the checksum file itself.

At minimum validate:

- every manifest-listed local member exists;
- every local member has a checksum entry;
- no unexpected member exists outside the declared package framework;
- duplicate paths do not exist;
- ZIP archive test passes;
- source and packaged bytes match for copied artifacts;
- version strings and filenames agree where governed;
- superseded files are not accidentally presented as current;
- required source gaps are explicit.

If a package claims byte-complete canonical status, all required local/embedded source checks must pass.

## 13. Ratification Gate

Before marking a newly built package `RATIFIED / CANONICAL`:

1. source set complete or approved layered dependency model complete;
2. directory structure validated;
3. authority classification validated;
4. manifest validated;
5. SHA-256 coverage validated;
6. ZIP archive validated;
7. no unresolved capability collision;
8. no silent status promotion;
9. no missing mandatory source;
10. explicit User ratification/authorization obtained.

If any mandatory condition fails:

`WBG PACKAGE RATIFICATION — HOLD`

Do not convert HOLD to PASS by narrative judgment.

## 14. Downstream Roll-Down

### WBG Personal derivative
WBG Personal may create a Personal-layer derivative that specifies:

- which canonical WBG dependency form to use;
- which user-level Tier 2 artifacts are routinely included;
- Personal naming/version conventions;
- Personal package separation rules.

It inherits all canonical source-integrity and ratification requirements.

### Project-specific derivative
A project-specific WBG may create a project derivative that specifies:

- exact project folder names;
- exact project Tier 3 governance/operational/reference/template categories;
- project-specific personas;
- required project ledgers;
- project-specific package validation additions.

It inherits both the canonical workflow and any applicable WBG Personal specialization.

## 15. No-Promotion Rule

Packaging is not governance promotion.

A downstream artifact moves upward only through the applicable explicit promotion/refinement process.

Copying a Tier 3 file into a Tier 2 directory is not a valid promotion mechanism.

## 16. Completion Report

After successful rendering, report:

- package filename;
- package version/status;
- ZIP SHA-256;
- packaged member count;
- validation result;
- any external dependency;
- any intentionally excluded artifact;
- any unresolved issue.

Do not describe the package as complete when a required source or dependency is unresolved.

## 17. One-Line Standard

**Package the authority you actually have, preserve every layer's identity, and never fake completeness.**
