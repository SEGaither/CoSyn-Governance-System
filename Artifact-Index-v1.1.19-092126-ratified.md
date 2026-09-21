# Artifact Index

**Artifact:** `Artifact-Index-v1.1.19-092126-ratified.md`  
**Version:** 1.1.19  
**Status:** RATIFIED / ACTIVE / CURRENT  
**Purpose:** Deterministic reference for canonical artifact identity, location, status, explicit dependency relationships, supersession lineage, repository-cleanup disposition, and task-directed artifact routing.  
**Created:** 2026-09-03  
**Revised:** 2026-09-21  
**Supersedes:** `Artifact-Index-v1.1.18-092126-ratified.md`  
**Scope:** Current known CoSyn v18 / Tier artifact set established by ratified v1.1.18, plus ratified independent Voice and Style and Anti-AI prose-signature authorities. The unrelated local v1.1.16 index candidate remains unratified and is not promoted or incorporated by this revision.  
**Completeness:** Ratified operational successor with task-routing support. Unresolved source-level dependency, lineage, and ambiguous-authority items remain explicitly listed in Section 11.

## 1. Operating Rule

`Update one artifact -> update its index entry -> verify explicit dependents -> stop.`

An artifact update does not invalidate unrelated proven artifacts.

For repository cleanup:

`recon -> classify current / superseded / duplicate / unresolved -> update index -> approve cleanup plan -> execute bounded cleanup -> verify affected surface -> stop`

The index must not claim that a planned move, archival action, deletion, or repository mutation has occurred until execution evidence establishes it.

For task execution:

`classify task -> consult this index -> select only applicable ACTIVE artifacts -> load selected artifacts -> execute -> stop`

The index is the first routing reference. Physical presence in the repository does not make an artifact applicable to a task. Once an applicable artifact has been loaded and remains current for the session, do not reread it merely because another turn occurs.

## 2. Index Rules

1. `Depends on` and `Depended on by` contain exact artifact identities only.
2. Authority hierarchy, user instruction, platform rules, runtime evidence, and documentation sources are not artifact dependencies unless represented by an exact indexed artifact.
3. `Supersedes` and `Superseded by` record version lineage only. They are not dependency fields.
4. `Unknown` remains `Unknown` until source evidence establishes the value.
5. Historical and retired artifacts may remain indexed for resolution and lineage, but their status must make clear that they are not current canonical controlling artifacts.
6. A newer filename, date, or version number alone does not establish supersession when artifact status or function conflicts.
7. Exact duplicate bytes do not create additional canonical authority.
8. `Cleanup disposition` is a planned repository-placement classification and does not itself mutate repository state.
9. Current repository path means the path established by recon at the time of this revision, not a future planned Historical path.
10. Task routing must begin from the routing map in this index rather than from broad repository scanning.
11. Load only artifacts whose routing trigger materially matches the current task, plus any exact direct dependencies required by those selected artifacts.
12. `BOUND-BASELINE` means load once for the session when not already bound; reuse established state thereafter unless superseded, contradicted, reset, or materially changed.
13. `CONDITIONAL` means load only when the current task matches the stated trigger.
14. `ON-REQUEST` means do not load during normal routing unless the User requests it or the task specifically requires its evidence/function.
15. `NEVER-NORMAL` means historical, retired, duplicate, package, continuity, or evidence material is excluded from normal task routing unless history, provenance, recovery, audit, or comparison makes it directly relevant.
16. If no routing entry matches a task, inspect only the minimum index metadata needed to identify a candidate artifact; do not scan every artifact to discover applicability.
17. Cache policy is separate from load class. A cache designation never makes an artifact applicable and never authorizes loading it.
18. Cache policy applies only after an artifact has been legitimately selected by routing or direct task requirement.
19. A project-source cache is a verified working copy, not independent authority. Repository canonical authority controls if a conflict is discovered.
20. A cached artifact may be reused across sessions only after the current canonical Artifact Index confirms that the cached artifact identity remains current; refresh from canonical source when identity, version, status, completeness, or fidelity is uncertain.

## 3. Field Definitions

| Field | Meaning |
|---|---|
| Indexed canonical filename | Exact filename currently treated as canonical for the artifact |
| Path | Exact current repository path when established |
| Version | Current indexed artifact version |
| Status | Active / ratified / candidate / historical / retired / preserved / other source-defined state |
| Depends on | Exact direct artifact dependencies stated by source |
| Depended on by | Exact direct reverse dependencies established from source |
| Supersedes | Exact prior artifact identity directly superseded by this artifact |
| Superseded by | Exact successor artifact identity that supersedes this artifact |
| SHA-256 | Exact byte identity where independently established |
| Authority / scope | What the artifact is allowed to govern |
| Evidence status | Whether the record is fully established or partial |
| Cleanup disposition | Planned repository handling established by recon and lineage; execution still requires separate approval/script |
| Cache policy | Whether an already-applicable active artifact should be retained as a verified project-source cache for reuse across sessions |

## 4. Current Canonical / Active Records

| Indexed canonical filename | Path | Version | Status | Depends on | Depended on by | Supersedes | Superseded by | SHA-256 | Authority / scope | Evidence status | Cleanup disposition |
|---|---|---:|---|---|---|---|---|---|---|---|---|
| `cgs-core-v18.0.1-constitution.md` | `CoSyn-18-core-trinity\Core\cgs-core-v18.0.1-constitution.md` | 18.0.1 | COMPLETE / RATIFIED / CURRENT | Unknown | `cgs-core-v18.0.2-persona-governor.md`; `cgs-core-v18.0.2-stack-architect.md` | Unknown | Unknown | `22FF2B087EDB3A16D8BD6EFAECFC08F1D955DBA876586DA60F119115D979FD7D` | Core constitutional governance | Current path established by recon; prior hash preserved from v1.0.9 evidence | KEEP ACTIVE |
| `cgs-core-v18.0.2-persona-governor.md` | `CoSyn-18-core-trinity\Core\cgs-core-v18.0.2-persona-governor.md` | 18.0.2 | RATIFIED / ACTIVE / CURRENT | `cgs-core-v18.0.1-constitution.md` | `cgs-core-v18.0.2-stack-architect.md` | `cgs-core-v18.0.1-persona-governor.md` | Unknown | `BE49AD49185ECED19D974B0494DAFE68BAB391E4D86AADB5E2710F9C8EA04B1A` | Persona governance; bounded per-turn enforcement | Ratification established; current local path recon-confirmed | KEEP ACTIVE |
| `cgs-core-v18.0.2-stack-architect.md` | `CoSyn-18-core-trinity\Core\cgs-core-v18.0.2-stack-architect.md` | 18.0.2 | RATIFIED / ACTIVE / CURRENT | `cgs-core-v18.0.1-constitution.md`; `cgs-core-v18.0.2-persona-governor.md` | Unknown | `cgs-core-v18.0.1-stack-architect.md` | Unknown | `BE49AD49185ECED19D974B0494DAFE68BAB391E4D86AADB5E2710F9C8EA04B1A` | Stack / authority architecture; selective per-turn routing | Ratification established; current local path recon-confirmed | KEEP ACTIVE |
| `Guppi-v1.3.17-091726-ratified.md` | `CoSyn-18-core-trinity\Tier 2 Personal\Guppi-v1.3.17-091726-ratified.md` | 1.3.17 | RATIFIED / ACTIVE / CURRENT | Unknown | `cgs-v18.0.1-tier2-general-work-session-management-team-persona-v1.1.1-091726.md` | `Guppi-v1.3.16-090326-ratified.md` | Unknown | `877767A1267319861A80136A3E935451FE667D01A82C483470189CBB9A1487F3` | Cross-project assistant identity, interaction character, response behavior; approved per-turn state reuse/task routing delta | Ratification established; current local path recon-confirmed; prior rendered hash preserved | KEEP ACTIVE |
| `Zero-v3.0.1-091726-ratified.md` | `CoSyn-18-core-trinity\Tier 2 Personal\Zero-v3.0.1-091726-ratified.md` | 3.0.1 | RATIFIED / ACTIVE / CURRENT | Unknown | Unknown | `Zero-v3.0.0-090826-ratified.md` | Unknown | Unknown | Software engineering / LLM programming persona; Direct-Path-First Execution | Explicit User ratification on 2026-09-17; successor rendered in-session | KEEP ACTIVE |
| `cgs-v18.0.1-tier2-personal-response-instructions-v1.3.md` | `CoSyn-18-core-trinity\Tier 2 Personal\cgs-v18.0.1-tier2-personal-response-instructions-v1.3.md` | 1.3 | RATIFIED / ACTIVE / CURRENT | Unknown | Unknown | `cgs-v18.0.1-tier2-personal-response-instructions-v1.2.md` | Unknown | `3666894A01E9EFB67EF2B2A4BC6CC330B85E5FC9D4CE764D53397C06E63CD9D4` | Cross-project response compactness, usable-path behavior, root-cause closure, and compact per-turn kernel | Ratification established; current local path recon-confirmed; prior rendered hash preserved | KEEP ACTIVE |
| `cgs-v18.0.1-tier2-general-work-session-management-team-persona-v1.1.1-091726.md` | `CoSyn-18-core-trinity\Tier 2 General\cgs-v18.0.1-tier2-general-work-session-management-team-persona-v1.1.1-091726.md` | 1.1.1 | RATIFIED / ACTIVE / CURRENT | `Guppi-v1.3.17-091726-ratified.md`; `git-repository-change-safety-protocol-v1.0.0-082126.md` | Unknown | `work-session-management-team-persona-v1.1.0-082626.md` | Unknown | `877767A1267319861A80136A3E935451FE667D01A82C483470189CBB9A1487F3` | Cross-project work-session management, established-state reuse, and selective specialist routing | Ratification established; current local path recon-confirmed; prior rendered hash preserved | KEEP ACTIVE |
| `git-repository-change-safety-protocol-v1.0.0-082126.md` | Unknown in current recon report | 1.0.0 | RATIFIED / ACTIVE | Unknown | `cgs-v18.0.1-tier2-general-work-session-management-team-persona-v1.1.1-091726.md` | Unknown | Unknown | Unknown | Git repository inspection/change safety | Source identity established; this recon report did not independently resolve the exact indexed path/hash | KEEP ACTIVE |
| `GPT-compute-conservation-v1.2.0-091726.md` | `CoSyn-18-core-trinity\Tier 2 General\cgs-v17.0.0-tier2-general-gpt-compute-conservation-v1.2.0-091726.md` | 1.2.0 | RATIFIED / ACTIVE | Unknown | Unknown | `GPT-compute-conservation-v1.1.0-082126.md` | Unknown | `CD9140BEE2D6F8A299ADCF8314CA0A397B92C8255B438E3C946078033AA44D39` | ChatGPT plan-execution compute conservation; lowest sufficient reasoning level; minimum necessary processing | Source content and repository presence verified 2026-09-17 | KEEP ACTIVE |
| `Zero-v3.0.0-090826-ratified.md` | `CoSyn-18-core-trinity\Tier 2 Personal\Zero-v3.0.0-090826-ratified.md` | 3.0.0 | SUPERSEDED / HISTORICAL CANDIDATE | `Zero-v3.0.1-091726-ratified.md` | Explicit User ratification of v3.0.1 establishes successor lineage | MOVE ONLY WHEN SEPARATELY AUTHORIZED |
| `cgs-v18.0.1-wbg-general-writing-project-workbook-template-v1.0.1.md` | `CoSyn-18-core-trinity\tier 3\General WBG Project Templates\cgs-v18.0.1-wbg-general-writing-project-workbook-template-v1.0.1.md` | 1.0.1 | PROPOSED / READY FOR USER REVIEW | Unknown | Unknown | `cgs-v17.0.0-wbg-general-writing-project-workbook-template-v1.0.0.md` | Unknown | `9A891BD976A5870ABA7F0B88F9202E8C51BEFE8A4603226F02F2BAE5FA5EB43E` | WBG Writing Project Workbook Template | Current path/status established by recon; prior hash preserved | KEEP; no supersession cleanup solely from date/version |
| `cgs-v18.0.1-wbg-personal-project-package-creation-workflow-v1.0.1.md` | `CoSyn-18-core-trinity\WBG Personal\cgs-v18.0.1-wbg-personal-project-package-creation-workflow-v1.0.1.md` | 1.0.1 | RATIFIED | Unknown | Unknown | Unknown | Unknown | `DB2BA19B376338430668937A639A2986F05E8E1271B4DFBB91117C8087BA52C3` | WBG Personal project-package creation workflow | Current path/status recon-confirmed; prior hash preserved | KEEP ACTIVE |
| `cgs-v18.0.1-wbg-personal-root-profile-v1.3.1.md` | `CoSyn-18-core-trinity\WBG Personal\cgs-v18.0.1-wbg-personal-root-profile-v1.3.1.md` | 1.3.1 | RATIFIED | Unknown | Unknown | Unknown | Unknown | `95829D5599BFC5546CB29EA8EA652583B2425A99470B389939808C488BBF6FAD` | WBG Personal root profile | Current path/status recon-confirmed; prior hash preserved | KEEP ACTIVE |
| `cgs-v18.0.1-wbg-personal-readme-wbg-personal-v1.3.2.md` | `CoSyn-18-core-trinity\WBG Personal\cgs-v18.0.1-wbg-personal-readme-wbg-personal-v1.3.2.md` | 1.3.2 | CURRENT SUCCESSOR — status field not resolved by recon | Unknown | Unknown | Unknown | Unknown | `A8207C489EBE926771AEE5E1E905CE0B26096025E85BF4DC51C967F3A17FC9DB` | WBG Personal README / package guidance | Current path recon-confirmed; prior hash preserved; exact source-defined status remains unresolved | KEEP |
| `cgs-v18.0.1-wbg-personal-validation-report-v1.3.2.md` | `CoSyn-18-core-trinity\WBG Personal\cgs-v18.0.1-wbg-personal-validation-report-v1.3.2.md` | 1.3.2 | CURRENT SUCCESSOR — status field not resolved by recon | Unknown | Unknown | Unknown | Unknown | `4499A0A615006B5EE3FC25B7677ABD09A352E0AAED5708CDD7A6E01BC23C879E` | WBG Personal validation evidence | Current path recon-confirmed; prior hash preserved; exact source-defined status remains unresolved | KEEP |
| `cgs-v18.0.1-wbg-personal-provenance-v1.3.2.md` | `CoSyn-18-core-trinity\WBG Personal\cgs-v18.0.1-wbg-personal-provenance-v1.3.2.md` | 1.3.2 | CURRENT SUCCESSOR — status field not resolved by recon | Unknown | Unknown | Unknown | Unknown | `AB94ADD8F2C78D75FA0BFA5EE2B3DB4330324F873FE6198DFFA292272E06847C` | WBG Personal provenance | Current path recon-confirmed; prior hash preserved; exact source-defined status remains unresolved | KEEP |
| `cgs-v18.0.1-tier2-personal-user-voice-and-style-reference-v1.2.0-092126-ratified.md` | LOCAL RENDERED ARTIFACT — repository installation not performed | 1.2.0 | RATIFIED / ACTIVE / CURRENT | Unknown | Unknown | `User_Voice_and_Style_Reference_v1.1.0-082126.md` | Unknown | `70A022F9B878352D02FA0117E7213AFDB03D43F780CDDEAB0A0E719598206DA4` | Tier 2 personal User voice/style definition and fidelity control; explicitly excludes Anti-AI diagnosis | Rendered and ratified by explicit User instruction on 2026-09-21; SHA-256 established from rendered artifact | KEEP ACTIVE LOCALLY; repository install only by separate authorization |
| `cgs-v18.0.1-wbg-general-anti-ai-prose-signature-gate-v1.1.0-092126-ratified.md` | LOCAL RENDERED ARTIFACT — repository installation not performed | 1.1.0 | RATIFIED / ACTIVE / CURRENT | Unknown | Unknown | `cgs-v18.0.1-wbg-general-writing-voice-style-and-naturalness-v1.0.1.md` (AA/naturalness capability) | Unknown | `DE1A13DB9B29790567763A4E54F5D8D39E073EC86994E52F4E2CB62EEAC18B0E` | General Anti-AI prose-signature diagnosis/correction gate; does not define authorial voice | Rendered and ratified by explicit User instruction on 2026-09-21 using the User-provided Wikipedia AI Writing Reference as a selective source basis | KEEP ACTIVE LOCALLY; repository install only by separate authorization |
| `attas-canon-v1.1.3-ratified.md` | LOCAL RENDERED ARTIFACT — repository installation not performed | 1.1.3 | RATIFIED / ACTIVE / CURRENT | Unknown | Unknown | `attas-canon-v1.1.2.md` | Unknown | `15079A4B0FB5FB1DC87CC552B2C9A4A0386A32C714BCBBB043C46CC1AA1EC9A3` | Authoritative ATTAS Book 1 and continuing-series story canon; preserves prior canon and adds the ratified Tanner diagnosed-ADHD, intellectual/problem-solving, generosity, and outward-misperception characterization | Rendered and ratified by explicit Author instruction on 2026-09-21; SHA-256 established from rendered artifact; GitHub repository not modified | KEEP ACTIVE LOCALLY; repository install only by separate authorization |
| `Artifact-Index-v1.1.19-092126-ratified.md` | LOCAL RENDERED ARTIFACT — repository installation not performed | 1.1.19 | RATIFIED / ACTIVE / CURRENT | Unknown | Unknown | `Artifact-Index-v1.1.18-092126-ratified.md` | Unknown | self-hash assigned after final byte generation | Canonical artifact index, cleanup basis, task-routing reference, and project-cache policy reference | Updated and ratified by explicit User instruction on 2026-09-21 to index independent VS and AA authorities; GitHub repository not modified | KEEP ACTIVE LOCALLY; repository install only by separate authorization |

## 5. Superseded / Historical Cleanup Candidates

These records are no longer current controlling artifacts where explicit successor lineage is established. Their current repository presence is preserved here so Script 2 can move them to a dedicated Historical structure without treating the move as already executed.

| Artifact filename | Current path | Version | Status | Superseded by | Evidence status | Cleanup disposition |
|---|---|---:|---|---|---|---|
| `cgs-core-v18.0.1-persona-governor.md` | `CoSyn-18-core-trinity\Core\cgs-core-v18.0.1-persona-governor.md` | 18.0.1 | SUPERSEDED / HISTORICAL CANDIDATE | `cgs-core-v18.0.2-persona-governor.md` | Exact functional lineage and newer ratified successor established; current path recon-confirmed | MOVE TO `CoSyn-18-core-trinity\Historical\Core\` |
| `cgs-core-v18.0.1-stack-architect.md` | `CoSyn-18-core-trinity\Core\cgs-core-v18.0.1-stack-architect.md` | 18.0.1 | SUPERSEDED / HISTORICAL CANDIDATE | `cgs-core-v18.0.2-stack-architect.md` | Exact functional lineage and newer ratified successor established; current path recon-confirmed | MOVE TO `CoSyn-18-core-trinity\Historical\Core\` |
| `cgs-v18.0.1-tier2-personal-response-instructions-v1.2.md` | `CoSyn-18-core-trinity\Tier 2 Personal\cgs-v18.0.1-tier2-personal-response-instructions-v1.2.md` | 1.2 | SUPERSEDED / HISTORICAL CANDIDATE | `cgs-v18.0.1-tier2-personal-response-instructions-v1.3.md` | v1.3 is ratified active successor; current v1.2 path recon-confirmed | MOVE TO `CoSyn-18-core-trinity\Historical\Tier 2 Personal\` |
| `cgs-v17.0.0-tier2-general-work-session-management-team-persona-v1.1.0-082626.md` | `CoSyn-18-core-trinity\Tier 2 General\cgs-v17.0.0-tier2-general-work-session-management-team-persona-v1.1.0-082626.md` | 1.1.0 | SUPERSEDED / HISTORICAL CANDIDATE | `cgs-v18.0.1-tier2-general-work-session-management-team-persona-v1.1.1-091726.md` | v1.1.1 is ratified active successor; current General path recon-confirmed | MOVE TO `CoSyn-18-core-trinity\Historical\Tier 2 General\` |
| `Artifact-Index-v1.0.8.md` | `CoSyn-18-core-trinity\Artifact-Index-v1.0.8.md` | 1.0.8 | SUPERSEDED / HISTORICAL CANDIDATE | `Artifact-Index-v1.0.9.md` | v1.0.9 direct successor established; recon shows v1.0.8 at non-root local path | MOVE TO `CoSyn-18-core-trinity\Historical\Artifact Index\` |
| `Artifact-Index-v1.0.10.md` | repository root | 1.0.10 | SUPERSEDED / HISTORICAL CANDIDATE | `Artifact-Index-v1.1.11.md` | Explicit User ratification of v1.1.11 establishes successor lineage; no repository move performed by this artifact rendering | MOVE ONLY WHEN SEPARATELY AUTHORIZED |
| `Artifact-Index-v1.1.13-091726-ratified.md` | repository root | 1.1.13 | SUPERSEDED / HISTORICAL CANDIDATE | `Artifact-Index-v1.1.14-091726-ratified.md` | Explicit User instruction to update the canonical index with `attas-canon-v1.1.1.md` establishes successor lineage | MOVE ONLY WHEN SEPARATELY AUTHORIZED |
| `Guppi-v1.3.16-090326-ratified.md` | exact active-tree path unresolved by recon summary | 1.3.16 | SUPERSEDED / HISTORICAL CANDIDATE | `Guppi-v1.3.17-091726-ratified.md` | Direct supersession established by ratified successor; exact active-tree copy/path should be resolved before mutation | MOVE ONLY AFTER EXACT SOURCE PATH IS ESTABLISHED |
| `GPT-compute-conservation-v1.1.0-082126.md` | `CoSyn-18-core-trinity\Tier 2 General\cgs-v17.0.0-tier2-general-gpt-compute-conservation-v1.1.0-082126.md` | 1.1.0 | SUPERSEDED / HISTORICAL CANDIDATE | `GPT-compute-conservation-v1.2.0-091726.md` | Explicit supersession established by ratified v1.2.0 source; repository presence of both versions verified 2026-09-17 | MOVE ONLY WHEN SEPARATELY AUTHORIZED |
| `attas-canon-v1.1.1.md` | `CoSyn-18-core-trinity\tier 3\attas\attas-canon-v1.1.1.md` | 1.1.1 | SUPERSEDED / HISTORICAL CANDIDATE | `attas-canon-v1.1.2.md` | Explicit Author ratification of v1.1.2 establishes successor lineage | MOVE ONLY WHEN SEPARATELY AUTHORIZED |
| `Artifact-Index-v1.1.14-091726-ratified.md` | repository root | 1.1.14 | SUPERSEDED / HISTORICAL CANDIDATE | `Artifact-Index-v1.1.15-091826-ratified.md` | Explicit User instruction on 2026-09-18 establishes successor lineage | MOVE ONLY WHEN SEPARATELY AUTHORIZED |
| `attas-canon-v1.1.2.md` | `CoSyn-18-core-trinity\tier 3\attas\attas-canon-v1.1.2.md` | 1.1.2 | SUPERSEDED / HISTORICAL CANDIDATE | `attas-canon-v1.1.3-ratified.md` | Explicit Author ratification of v1.1.3 on 2026-09-21 establishes successor lineage; no repository move performed | MOVE ONLY WHEN SEPARATELY AUTHORIZED |
| `Artifact-Index-v1.1.15-091826-ratified.md` | repository root | 1.1.15 | SUPERSEDED / HISTORICAL CANDIDATE | `Artifact-Index-v1.1.17-092126-ratified.md` | Explicit User ratification of v1.1.17 on 2026-09-21 establishes successor lineage; GitHub repository not modified | MOVE ONLY WHEN SEPARATELY AUTHORIZED |
| `User_Voice_and_Style_Reference_v1.1.0-082126.md` | prior project/library source | 1.1.0 | SUPERSEDED / HISTORICAL SOURCE | `cgs-v18.0.1-tier2-personal-user-voice-and-style-reference-v1.2.0-092126-ratified.md` | Explicit User ratification of v1.2.0 on 2026-09-21 establishes successor lineage and removes AA overlap | PRESERVE; repository handling only by separate authorization |
| `cgs-v18.0.1-wbg-general-writing-voice-style-and-naturalness-v1.0.1.md` | prior WBG General source / repository identity previously recon-confirmed | 1.0.1 | SUPERSEDED FOR AA/NATURALNESS CAPABILITY | `cgs-v18.0.1-wbg-general-anti-ai-prose-signature-gate-v1.1.0-092126-ratified.md` | Explicit User ratification of the independent AA successor on 2026-09-21; generic voice/style authority is not carried into AA | PRESERVE; repository handling only by separate authorization |
| `Artifact-Index-v1.1.17-092126-ratified.md` | LOCAL RENDERED ARTIFACT — repository installation not performed | 1.1.17 | SUPERSEDED / HISTORICAL CANDIDATE | `Artifact-Index-v1.1.18-092126-ratified.md` | Explicit User ratification of v1.1.18 on 2026-09-21 establishes successor lineage; GitHub repository not modified | PRESERVE LOCALLY; repository handling only by separate authorization |
| `Artifact-Index-v1.1.18-092126-ratified.md` | LOCAL RENDERED ARTIFACT — repository installation not performed | 1.1.18 | SUPERSEDED / HISTORICAL CANDIDATE | `Artifact-Index-v1.1.19-092126-ratified.md` | Explicit User ratification of v1.1.19 on 2026-09-21 establishes successor lineage; GitHub repository not modified | PRESERVE LOCALLY; repository handling only by separate authorization |

## 6. Exact Duplicate / Misplacement Cleanup Candidates

Exact byte duplication does not create additional canonical authority. Recon found the following duplicates or misplaced copies. Script 2 may remove them from active paths or archive them only after exact source paths are confirmed immediately before mutation.

| File / group | Recon evidence | Canonical/current copy | Cleanup disposition |
|---|---|---|---|
| `Zero-v3.0.0-090826-ratified.md` duplicate group | Same SHA-256 appears at `Tier 2 General\Zero-v3.0.0-090826-ratified.md`, `Tier 2 Personal\Zero-v3.0.0-090826-ratified - Copy.md`, and `Tier 2 Personal\Zero-v3.0.0-090826-ratified.md` | `CoSyn-18-core-trinity\Tier 2 Personal\Zero-v3.0.0-090826-ratified.md` | KEEP canonical Personal copy; move duplicate General and ` - Copy` files to `Historical\Duplicates\` or delete only if separately approved |
| Work Session Management v1.1.0 duplicate | Same SHA-256 appears in `Tier 2 General` and `Tier 2 Personal` | Neither v1.1.0 copy is current; v1.1.1 is the active successor in Tier 2 General | Archive both v1.1.0 copies; mark Personal copy as misplaced duplicate |
| `cgs-v17.0.0-tier2-personal-guppi-v1.3.15-082726.md` | Exact duplicate exists in `archive\` and `Tier 2 Personal\` | Neither is current Guppi | Do not delete automatically; active-tree copy is a historical candidate, existing archive copy may satisfy preservation requirement after byte check |
| WBG Personal / WBG General voice-style file | Recon reports identical SHA-256 for `WBG General\cgs-v18.0.1-wbg-general-writing-voice-style-and-naturalness-v1.0.1.md` and `WBG Personal\cgs-v18.0.1-wbg-personal-writing-voice-style-and-naturalness-v1.0.1.md` | Functional authority differs by path/name despite identical bytes | NO AUTOMATIC CLEANUP; identical content alone is insufficient to establish duplicate authority |
| ATTaS v17/v18 pairs with identical bytes | Several v17/v18 ATTaS pairs share exact hashes | Status/authority not established by recon | NO AUTOMATIC CLEANUP solely from byte identity |
| Session/package/Zero-input-package duplicates | Many exact duplicates exist outside active tree | These are continuity/evidence/package surfaces, not active canonical slots | EXCLUDE FROM FIRST CLEANUP PASS unless separately approved |

## 7. Ambiguous Version-Pair Findings — Do Not Auto-Clean

The recon found multiple v17/v18 WBG and Tier 3 pairs where the newer file has `CANDIDATE / READY FOR PACKAGE INTEGRATION`, `PROPOSED / READY FOR USER REVIEW`, or another status that does not establish authority over an older ratified/current artifact.

These must not be classified as superseded merely from filename version or modification date.

Examples include:

- WBG General AI-use disclosure creator;
- anti-plagiarism check and gate;
- copyright-page creator;
- writing diagnostic/evaluation protocol;
- writing governance/authority;
- writing operation-state/revision control;
- writing-team personas;
- writing user artistic authority;
- writing voice/style/naturalness;
  - 2026-09-21 resolution note: the prior combined General WBG artifact is superseded for AA/naturalness by the ratified independent AA artifact; personal VS is separately governed by the ratified Tier 2 VS successor. This does not by itself resolve or delete any unrelated duplicate repository copy.
- Tier 3 General WBG Project Workbook Template;
- ATTaS v17/v18 pairs.

Disposition: `PRESERVE IN PLACE PENDING SEPARATE AUTHORITY REVIEW`.

## 8. Downloads Recon Result

The recon scanned `C:\Users\Magen\Downloads`.

Result:

`No supersession candidates were identified.`

Therefore this index revision does not introduce any repository successor from Downloads.

## 9. Historical / Preserved / Retired Indexed Records Preserved from v1.0.9

The following v1.0.9 historical records remain preserved and are not changed by the six-artifact cleanup classification:

| Artifact filename | Indexed status |
|---|---|
| `cgs-v17.0.0-wbg-general-writing-project-workbook-template-v1.0.0.md` | PRESERVED / SUPERSEDED SOURCE |
| `cgs-v17.0.0-wbg-personal-bind-profile-v1.3.1.json` | RETIRE |
| `cgs-v17.0.0-wbg-personal-integrity-manifest-v1.3.1.json` | RETIRE |
| `cgs-v17.0.0-wbg-personal-interaction-command-and-intensity-profile-v1.0.0.md` | CARRY_FORWARD/PRESERVE |
| `cgs-v17.0.0-wbg-personal-no-gain-refinement-report-v1.3.0.md` | CARRY_FORWARD/PRESERVE |
| `cgs-v17.0.0-wbg-personal-package-manifest-v1.3.1.json` | RETIRE |
| `cgs-v17.0.0-wbg-personal-project-initialization-profile-v1.3.0.md` | CARRY_FORWARD/PRESERVE |
| `cgs-v17.0.0-wbg-personal-ratification-record-v1.3.1.md` | CARRY_FORWARD/PRESERVE |
| `cgs-v17.0.0-wbg-personal-refinement-and-promotion-protocol-v1.3.0.md` | CARRY_FORWARD/PRESERVE |
| `cgs-v17.0.0-wbg-personal-sha256sums.txt` | RETIRE |
| `cgs-v17.0.0-wbg-personal-source-classification-ledger-v1.3.2.md` | CARRY_FORWARD/PRESERVE |
| `cgs-v17.0.0-wbg-personal-user-specialization-v1.3.0.md` | CARRY_FORWARD/PRESERVE |

Their prior v1.0.9 evidence, hashes, dependency unknowns, and preservation/retirement semantics remain unchanged unless a later source-specific review updates them.

## 10. Script 2 Cleanup Boundary Derived from This Index

The first cleanup script may operate only on records marked:

- `MOVE TO Historical...`;
- duplicate copies with an exact canonical survivor established;
- exact misplaced copies whose intended active location is established.

It must not:

- infer supersession for ambiguous WBG/Tier 3 pairs;
- delete continuity/session/package evidence;
- delete an artifact merely because another copy has identical bytes;
- modify active canonical artifact contents;
- change artifact semantics;
- stage, commit, or push unless separately authorized;
- touch GitHub directly unless separately authorized.

For every mutation Script 2 must:

1. establish exact source existence;
2. establish target absence or exact allowed collision state;
3. preserve byte identity on move;
4. verify the active canonical survivor remains present;
5. verify only the affected paths;
6. stop.

## 11. Unresolved Index Population Requirements

The following remain unresolved:

1. source-level direct dependency extraction for every indexed artifact;
2. reverse dependency reconciliation from those explicit direct dependencies;
3. exact supersession lineage for artifacts not covered by explicit successor evidence;
4. exact canonical status of ambiguous WBG/Tier 3 v17/v18 pairs;
5. exact active-tree path of the superseded Guppi v1.3.16 copy before cleanup;
6. final Historical destination paths until Script 2 is approved and executed;
7. post-cleanup verification and corresponding index path updates;
8. exact SHA-256 for this v1.1.11 ratified artifact is assigned after final byte generation and recorded with the rendered file.

## 12. v1.0.10 Revision Note

v1.0.10 is a recon-driven candidate successor of `Artifact-Index-v1.0.9.md`.

Changes:

- replaces `Unknown in repository` for the five newly ratified governing successors with exact local repository paths established by the 2026-09-17 recon;
- records exact current paths for Constitution v18.0.1 and canonical Zero v3.0.0;
- records Persona Governor v18.0.1, Stack Architect v18.0.1, Response Instructions v1.2, Work Session Management v1.1.0, and Artifact Index v1.0.8 as superseded/historical cleanup candidates where successor lineage is established;
- records the recon-confirmed duplicate Zero copies and duplicate Work Session Management v1.1.0 copy without treating duplicate presence as authority;
- records that no Downloads file was identified as a supersession candidate;
- explicitly blocks automatic cleanup of ambiguous WBG/Tier 3 v17/v18 pairs whose status does not establish supersession;
- establishes a bounded Script 2 cleanup boundary;
- preserves unrelated v1.0.9 records unless recon evidence materially updates path/status classification;
- does not claim that Historical moves or duplicate cleanup have been executed;
- does not update GitHub or the local repository.

v1.0.10 became controlling when explicitly adopted and installed; it is superseded by the ratified v1.1.11 successor.


## 13. Task Routing Map

### 13.1 Routing Objective

The index resolves applicability before source loading.

Normal execution must not begin by reading every artifact in the repository. The model identifies the task class, consults this routing map, and loads only the active artifacts whose triggers match the task plus exact dependencies required by those selected artifacts.

Repository presence is inventory evidence, not a load instruction.

Cache designation is persistence policy, not applicability. An artifact marked `PROJECT-CACHE` is cached only after normal routing selects it or the task directly requires it.

### 13.2 Load Classes

| Load class | Meaning |
|---|---|
| `BOUND-BASELINE` | Load once when needed to establish the active session baseline; reuse without rereading while identity and authority remain unchanged |
| `CONDITIONAL` | Load only when the current task materially matches the routing trigger |
| `ON-REQUEST` | Load only when specifically requested or when its evidence/function is directly required |
| `NEVER-NORMAL` | Exclude from ordinary routing; load only for history, provenance, recovery, audit, comparison, or another directly relevant exceptional purpose |

### 13.2A Cache Policies

Cache policy governs persistence only after an artifact is already applicable. It never triggers loading.

| Cache policy | Meaning |
|---|---|
| `PROJECT-CACHE` | When legitimately loaded for a project, preserve an unchanged verified copy in project source for reuse across sessions. Reuse only while the current Artifact Index confirms the same canonical identity; refresh from canonical source when identity or fidelity is uncertain. |
| `SESSION-ONLY` | Read and reuse within the current session when routed, but do not persist as a routine project-source cache unless the User explicitly directs otherwise. |
| `NO-CACHE` | Do not retain as a normal project-source cache. Retrieve only when directly required by routing or explicit request. |

Repository authority remains controlling. A cached copy does not become canonical merely because it is stored in project source.

### 13.3 Active Artifact Routing

| Artifact | Load class | Cache policy | Routing trigger / applies to | Normal exclusion |
|---|---|---|---|---|
| `cgs-core-v18.0.1-constitution.md` | `BOUND-BASELINE` | `PROJECT-CACHE` | Establishing or restoring the CoSyn constitutional baseline | Do not reread per turn after current identity is established |
| `cgs-core-v18.0.2-persona-governor.md` | `BOUND-BASELINE` | `PROJECT-CACHE` | Establishing or restoring persona/governance enforcement baseline | Do not reread per turn after current identity is established |
| `cgs-core-v18.0.2-stack-architect.md` | `BOUND-BASELINE` | `PROJECT-CACHE` | Establishing or restoring authority/routing architecture baseline; resolving a routing ambiguity not answerable from this index | Do not invoke merely because multiple artifacts exist |
| `Guppi-v1.3.17-091726-ratified.md` | `BOUND-BASELINE` | `PROJECT-CACHE` | Normal cross-project assistant identity, interaction behavior, established-state reuse, and task routing | Do not reread per turn after current identity is established |
| `cgs-v18.0.1-tier2-personal-response-instructions-v1.3.md` | `BOUND-BASELINE` | `PROJECT-CACHE` | Normal response compactness, usable-path behavior, root-cause closure, and compact per-turn execution | Do not reread per turn after current identity is established |
| `Zero-v3.0.1-091726-ratified.md` | `CONDITIONAL` | `PROJECT-CACHE` | Software engineering; LLM/API/agent engineering; scripts; debugging; repository work; Git-adjacent technical execution | Do not load for unrelated writing, general discussion, or nontechnical tasks |
| `cgs-v18.0.1-tier2-general-work-session-management-team-persona-v1.1.1-091726.md` | `CONDITIONAL` | `PROJECT-CACHE` | Consequential, stateful, multi-step, multi-file, multi-decision, continuity-sensitive, or session-handoff work | Do not load for ordinary simple turns |
| `git-repository-change-safety-protocol-v1.0.0-082126.md` | `CONDITIONAL` | `SESSION-ONLY` | Git inspection, staging, commit, branch/history manipulation, push/pull/fetch/reset/restore/clean/stash, or other repository-state mutation | Do not load for non-Git filesystem work merely because the files are inside a Git repository |
| `GPT-compute-conservation-v1.2.0-091726.md` | `CONDITIONAL` | `PROJECT-CACHE` | ChatGPT execution of an already-developed, approved, accepted, or otherwise established plan or defined execution stage | Do not load for plan creation, ordinary discussion, or work not executing an established plan |
| `cgs-v18.0.1-wbg-general-writing-project-workbook-template-v1.0.1.md` | `CONDITIONAL` | `PROJECT-CACHE` | Creating or using the WBG writing-project workbook/template | Do not load for unrelated writing tasks |
| `cgs-v18.0.1-wbg-personal-project-package-creation-workflow-v1.0.1.md` | `CONDITIONAL` | `PROJECT-CACHE` | Creating a WBG Personal project package | Do not load for ordinary writing or non-package work |
| `cgs-v18.0.1-wbg-personal-root-profile-v1.3.1.md` | `CONDITIONAL` | `PROJECT-CACHE` | WBG Personal work requiring the personal writing root profile | Do not load for non-WBG tasks |
| `cgs-v18.0.1-wbg-personal-readme-wbg-personal-v1.3.2.md` | `ON-REQUEST` | `NO-CACHE` | WBG Personal package guidance, package interpretation, or explicit README review | Do not load merely because WBG Personal is involved |
| `cgs-v18.0.1-wbg-personal-validation-report-v1.3.2.md` | `ON-REQUEST` | `NO-CACHE` | WBG validation evidence, validation review, or explicit evidence comparison | Do not load for execution tasks that do not require prior validation evidence |
| `cgs-v18.0.1-wbg-personal-provenance-v1.3.2.md` | `ON-REQUEST` | `NO-CACHE` | Provenance, history, audit, lineage, or explicit source-trace questions | Do not load for normal task execution |
| `cgs-v18.0.1-tier2-personal-user-voice-and-style-reference-v1.2.0-092126-ratified.md` | `CONDITIONAL` | `PROJECT-CACHE` | Drafting, revising, critiquing, or assessing text intended to preserve or reproduce the User's personal voice/style | Do not load solely for generic AA detection when personal voice is not material |
| `cgs-v18.0.1-wbg-general-anti-ai-prose-signature-gate-v1.1.0-092126-ratified.md` | `CONDITIONAL` | `PROJECT-CACHE` | Anti-AI audit, naturalness review, synthetic-prose diagnosis, or AA correction of writing | Do not use as a substitute for VS; do not load solely because prose is being written unless AA review is requested or materially required |
| `attas-canon-v1.1.3-ratified.md` | `CONDITIONAL` | `PROJECT-CACHE` | ATTAS story-canon, manuscript-development, continuity, character/worldbuilding, canon-protection, or canon-reconciliation work | Do not load for unrelated writing projects or non-ATTAS tasks |
| `Artifact-Index-v1.1.19-092126-ratified.md` | `BOUND-BASELINE` | `PROJECT-CACHE` | First routing reference for determining which artifacts apply | The index routes; it does not replace the instructions in selected artifacts |


### 13.4 Historical and Non-Active Routing

All records classified as superseded, historical, retired, duplicate, preserved source, continuity/package evidence, or unresolved ambiguous version pairs are `NEVER-NORMAL` for task routing.

Their presence does not authorize loading them during an ordinary task.

They may be loaded only when the task directly concerns:

- history or provenance;
- supersession or lineage;
- recovery or rollback;
- audit or comparison;
- unresolved authority determination;
- exact duplicate/collision investigation;
- another purpose that specifically requires that record.

### 13.5 Route Examples

| Task | Index-selected artifacts |
|---|---|
| Simple ordinary response | Bound baseline only; no additional artifact load |
| Software or repository diagnosis without Git mutation | `Zero-v3.0.1-091726-ratified.md`; add Work Session Management only if the task is consequential/stateful |
| Git staging/commit/push or repository-history work | `Zero-v3.0.1-091726-ratified.md` + `git-repository-change-safety-protocol-v1.0.0-082126.md`; add Work Session Management only when materially warranted |
| Execute an already-developed plan within ChatGPT | `GPT-compute-conservation-v1.2.0-091726.md`; add only other artifacts independently triggered by the task |
| WBG Personal writing project | Applicable WBG Personal active artifact(s) selected by the exact writing task; do not load unrelated Git, ATTaS, historical, or package evidence |
| User-voice drafting or revision | Current ratified VS artifact; add AA only when an Anti-AI/naturalness audit is requested or materially needed |
| Anti-AI prose audit | Current ratified AA artifact; add VS when the prose is intended to match the User or when AA correction could affect established voice |
| Provenance or historical comparison | Only the specific provenance/historical records needed for the question |
| No exact route found | Use index metadata first; load the minimum candidate source needed to resolve applicability; do not repository-scan |

## 14. v1.1.14 Ratified Revision Note

`Artifact-Index-v1.1.14-091726-ratified.md` is the User-ratified successor to `Artifact-Index-v1.1.13-091726-ratified.md`.

This revision preserves the v1.1.13 routing and inventory state and updates only the surfaces affected by installation of the ratified ATTAS canon v1.1.1.

Changes in v1.1.14:

- adds `attas-canon-v1.1.1.md` as RATIFIED / ACTIVE / CURRENT;
- records its canonical repository path under `CoSyn-18-core-trinity/tier 3/attas/`;
- routes ATTAS story-canon, manuscript-development, continuity, character/worldbuilding, canon-protection, and canon-reconciliation work to the canon artifact;
- records v1.1.14 as the current Artifact Index and v1.1.13 as superseded/historical;
- preserves unrelated inventory, routing, cleanup, and unresolved-state records unchanged;
- performs no unrelated repository cleanup or artifact mutation.

Ratification basis: explicit User instruction on 2026-09-17 to update the index with the newly installed canonical repository file `attas-canon-v1.1.1.md`.

---

## 15. v1.1.15 Ratified Revision Note

`Artifact-Index-v1.1.15-091826-ratified.md` is the User-ratified successor to `Artifact-Index-v1.1.14-091726-ratified.md`.

This revision updates only the surfaces affected by ratification of `attas-canon-v1.1.2.md`.

Changes in v1.1.15:

- indexes `attas-canon-v1.1.2.md` as RATIFIED / ACTIVE / CURRENT;
- records `attas-canon-v1.1.1.md` as superseded/historical;
- routes ATTAS canon work to v1.1.2;
- records the v1.1.2 SHA-256 established from the rendered artifact;
- records v1.1.15 as the current Artifact Index and v1.1.14 as superseded/historical;
- preserves unrelated inventory, routing, cleanup, and unresolved-state records unchanged;
- performs no unrelated repository cleanup or mutation.

Ratification basis: explicit User instruction on 2026-09-18 to update, ratify, index, and render the supplied canon and Artifact Index artifacts.

---

*Document ID: Artifact-Index-v1.1.15-091826-ratified — RATIFIED / ACTIVE / CURRENT.*

---

## 16. v1.1.17 Ratified Revision Note

`Artifact-Index-v1.1.17-092126-ratified.md` is the User-ratified successor to `Artifact-Index-v1.1.15-091826-ratified.md`.

An unrelated local `Artifact-Index-v1.1.16-092026-candidate.md` exists in PROPOSED / READY FOR USER REVIEW state. It was not ratified, promoted, incorporated, overwritten, or treated as controlling by this revision. Version 1.1.17 is used to avoid filename/version collision.

This revision changes only the surfaces required to index the newly ratified `attas-canon-v1.1.3-ratified.md`:

- indexes `attas-canon-v1.1.3-ratified.md` as RATIFIED / ACTIVE / CURRENT;
- records `attas-canon-v1.1.2.md` as superseded/historical;
- routes ATTAS canon work to v1.1.3;
- records the v1.1.3 SHA-256 established from the rendered artifact;
- records v1.1.17 as the current local Artifact Index and v1.1.15 as superseded/historical;
- explicitly preserves the unratified v1.1.16 candidate without promotion;
- preserves unrelated v1.1.15 inventory, routing, cleanup, historical, and unresolved state unchanged;
- performs no GitHub repository installation, commit, push, cleanup, or mutation.

Ratification basis: explicit User instruction on 2026-09-21 to update the ATTAS canon, ratify it, index it, render new Markdown artifact(s), and not update the GitHub repository.

---

*Document ID: Artifact-Index-v1.1.17-092126-ratified — RATIFIED / ACTIVE / CURRENT.*

---

## 17. v1.1.18 Ratified Revision Note

`Artifact-Index-v1.1.18-092126-ratified.md` is the User-ratified successor to `Artifact-Index-v1.1.17-092126-ratified.md`.

This revision changes only the index surfaces required to establish deterministic project-source caching behavior:

- adds cache policy as a routing dimension separate from load class;
- defines `PROJECT-CACHE`, `SESSION-ONLY`, and `NO-CACHE`;
- assigns a cache policy to every artifact already present in the active routing table;
- establishes that cache policy never creates applicability and never authorizes loading;
- establishes that project-source copies are verified working caches, not independent canonical authority;
- requires current Artifact Index identity confirmation before a cached artifact is reused across sessions;
- requires canonical refresh when cached identity, version, status, completeness, or fidelity is uncertain;
- records v1.1.18 as the current local Artifact Index and v1.1.17 as superseded/historical;
- preserves the unrelated unratified v1.1.16 candidate without promotion or incorporation;
- preserves all unrelated inventory, authority, dependency, cleanup, historical, ATTAS, and unresolved state;
- performs no GitHub repository installation, commit, push, cleanup, or mutation.

Ratification basis: explicit User instruction on 2026-09-21 to revise the Artifact Index for project-cache labeling, ratify the successor, index the filename, and render it as a Markdown artifact.

---

*Document ID: Artifact-Index-v1.1.18-092126-ratified — RATIFIED / ACTIVE / CURRENT.*


---

## 18. v1.1.19 Ratified Revision Note

`Artifact-Index-v1.1.19-092126-ratified.md` is the User-ratified successor to `Artifact-Index-v1.1.18-092126-ratified.md`.

This revision changes only the index surfaces required to establish independent but complementary Voice and Style and Anti-AI authorities:

- indexes `cgs-v18.0.1-tier2-personal-user-voice-and-style-reference-v1.2.0-092126-ratified.md` as RATIFIED / ACTIVE / CURRENT;
- indexes `cgs-v18.0.1-wbg-general-anti-ai-prose-signature-gate-v1.1.0-092126-ratified.md` as RATIFIED / ACTIVE / CURRENT;
- records VS v1.2.0 as successor to `User_Voice_and_Style_Reference_v1.1.0-082126.md`;
- records the AA gate v1.1.0 as successor to the AA/naturalness capability previously combined in `cgs-v18.0.1-wbg-general-writing-voice-style-and-naturalness-v1.0.1.md`;
- establishes VS as the authority for User voice fidelity and AA as the authority for synthetic-prose diagnosis;
- establishes that AA cannot redefine, compress, or override authorized voice/style;
- routes voice-sensitive drafting/revision to VS and AA audits to AA, loading both only when the task materially requires both;
- records rendered SHA-256 identities for both new artifacts;
- preserves unrelated inventory, routing, cache policy, cleanup, ATTAS, and unresolved state;
- performs no GitHub repository installation, commit, push, cleanup, or mutation.

Ratification basis: explicit User instruction on 2026-09-21 to update AA using the supplied AI-writing resource, remove VS/AA overlap, make them independent but complementary, update the indexed filenames, ratify, and render all affected artifacts.

---

*Document ID: Artifact-Index-v1.1.19-092126-ratified — RATIFIED / ACTIVE / CURRENT.*
