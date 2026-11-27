# CoSyn Artifact Index

**Artifact:** `CoSyn-Artifact-Index-vC19.2.5.md`  
**Filename version:** vC19.2.5 (AI revision advanced from 1 to 2; author revision remains 5; C marks author-approved canonical status)  
**Previous index version:** 19.1.5  
**Status:** RATIFIED / ACTIVE / CANONICAL ROUTING INDEX — author-approved November 27, 2026 update to route Zero vC19.2.1; prior source ratification retained  
**Date:** 2026-11-27  
**Supersedes:** `CoSyn-Artifact-Index-v19.1.5.md`  
**Canonical repository:** https://github.com/SEGaither/CoSyn-Governance-System  
**Repository observation:** `CoSyn-Checkpoint-v19.1.1.md` contains the originally ratified Checkpoint v1.1.1 source for consolidated continuity operations. Superseded sources, older indexes and historical copies are preserved in the private archive, not the public working tree.  
**Purpose:** Identify the minimum applicable canonical source files for the current task. This is a routing directory, not a repository-maintenance ledger.

## 1. Binding and tolerant routing rules

1. **Bootstrap:** Discover the repository root and read the current repository-installed Index. Establish required Core and applicable persona sources from their real contents before claiming a complete bind.
2. **Choose by task, not presence:** Read `BOUND-BASELINE` records once per session, then `CONDITIONAL` records whose triggers materially match, and `ON-REQUEST` records only on request or direct need. `NEVER-NORMAL` records are excluded unless their content is directly relevant. Read exact required dependencies, not unrelated directories. A cache designation does not create applicability.
3. **Minor drift is nonfatal:** Extra, newly added, renamed, or modified repository files do not themselves invalidate a bind. Do not scan or read every file to reconcile inventory. For a selected file with a stale path, search the relevant repository directory for its logical identity, then inspect the narrow candidate source for status and authority. A changed Git blob or filename alone does not establish supersession, but also does not automatically block binding.
4. **Authority and conflict:** The repository is the source authority for repository-controlled artifacts. If multiple candidates disagree about required authority, do not guess or silently elevate the newest name. Report the *specific unresolved required dependency*. Continue using independently established required sources when safe; mark full binding incomplete only if the unresolved source is necessary to that binding. Unindexed files are not automatically active. An explicitly user-supplied ratified local successor can govern its stated session scope but is not represented as already installed in GitHub.
5. **Retrieval failure:** A failed request to one path or endpoint proves only that attempt failed. Rediscover the actual path and use another supported method when useful. Do not repeatedly retry an unchanged failure, treat an unsupported directory response as missing files, or fill gaps with memory.
6. **Cache policy:** Apply only *after* applicability is established. `PROJECT-CACHE`: use an unchanged project-source copy only when its canonical identity and fidelity are verified against the current Index; otherwise fetch the canonical file and preserve a copy only if supported. `SESSION-ONLY`: reuse within session, no routine project persistence. `NO-CACHE`: retrieve when directly needed, no routine project persistence. Project copies never supersede the repository.
7. **State discipline:** Separate *repository reachable*, *artifact located*, *retrieved*, *read*, *applicable*, *instantiated*, and *bind complete*. Claim only demonstrated states. Reuse established session state unless changed authority, applicability, contradiction, reset, or cache validity materially requires refresh.

### Private artifact access gate

- Default to **public artifacts only**. Do not retrieve, read, load, or instantiate any file routed to `SEGaither/CoSyn-Personal-Governance` until the user supplies the matching session access code.
- When a private artifact is needed and the code has not been supplied in the current session, ask for the code and stop that private retrieval; continue public-only work where possible. A correct code authorizes private-artifact routing for the remainder of the current session. An incorrect code does not.
- Session access code (white text for visual obscurity): <span style="color: white;">1701</span>
- This is a lightweight **CoSyn behavior gate**, not GitHub authentication. Repository permissions still determine whether the file can actually be retrieved. Do not disclose or display the code unprompted in normal responses.

## 2. Routing directory — verified active sources

Public paths are relative to `SEGaither/CoSyn-Governance-System`. A path prefixed `SEGaither/CoSyn-Personal-Governance:` belongs to the private repository and requires authorized access. An exact path is a retrieval locator, not proof that a file has been read this session. `—` in dependencies means **none independently established in this Index**, not proof that the source declares none. Where this Index knows exact source-declared dependencies, they are specified.

| Artifact / exact repository path | Load | Cache | Task trigger | Direct known dependencies |
|---|---|---|---|---|
| `Core/CoSyn-Constitution-v19.0.1.md` | BOUND-BASELINE | PROJECT-CACHE | CoSyn constitutional baseline | — |
| `Core/CoSyn-Governor-v19.0.2.md` | BOUND-BASELINE | PROJECT-CACHE | Persona governance baseline | Constitution v18.0.1 |
| `Core/CoSyn-Architect-v19.0.2.md` | BOUND-BASELINE | PROJECT-CACHE | Stack/authority and routing baseline | Constitution v18.0.1; Persona Governor v18.0.2 |
| `SEGaither/CoSyn-Personal-Governance:Tier 2 Personal/CoSyn-Guppi-v19.0.1.md` | BOUND-BASELINE | PROJECT-CACHE | Normal cross-project Guppi identity and response baseline; do not replace explicitly selected specialist identity | — |
| `SEGaither/CoSyn-Personal-Governance:Tier 2 Personal/CoSyn-Personal-Response-Instructions-v19.0.1.md` | BOUND-BASELINE | PROJECT-CACHE | Cross-project response rules | — |
| `SEGaither/CoSyn-Personal-Governance:Tier 2 Personal/CoSyn-Zero-vC19.2.1.md` | CONDITIONAL | PROJECT-CACHE | Zero selected as session lead; task-first application of engineering expertise where actually needed | — |
| `SEGaither/CoSyn-Personal-Governance:Tier 2 Personal/CoSyn-Ziggy-v19.0.1.md` | CONDITIONAL | PROJECT-CACHE | Ziggy requested; reflective reasoning, personal judgment, continuity-aware self-improvement | — |
| `Tier 2 General/CoSyn-Checkpoint-v19.1.1.md` | CONDITIONAL | PROJECT-CACHE | `checkpoint` invocation; provenance checkpoints, living verbatim session records, end-session continuation packages, and related continuity management | Constitution v18.0.1 |
| `Tier 2 General/CoSyn-Work-Session-Management-v19.0.1.md` | CONDITIONAL | PROJECT-CACHE | Consequential stateful/multistep work, team routing or continuity handoff | Guppi v1.3.17; Git safety protocol (source-declared; resolve if relevant) |
| `Tier 2 General/CoSyn-Git-Repository-Change-Safety-Protocol-v19.0.1.md` | CONDITIONAL | SESSION-ONLY | Git inspection or mutation, commits, branches, history, reset/push | — |
| `Tier 2 General/CoSyn-File-Versioning-Instructions-v19.1.1.md` | CONDITIONAL | PROJECT-CACHE | Creating or revising versioned files; canonical designation, lineage, version indexes, provenance | — |
| `Tier 2 General/CoSyn-GPT-Compute-Conservation-v19.0.1.md` | CONDITIONAL | PROJECT-CACHE | Execute an already approved/established plan in ChatGPT | — |
| `Tier 2 General/CoSyn-PowerShell-Script-Writing-Instructions-v19.0.1.md` | CONDITIONAL | SESSION-ONLY | Writing executable PowerShell scripts for user | — |
| `SEGaither/CoSyn-Personal-Governance:prompts/CoSyn-PowerShell-Script-Development-Prompt-v19.0.1.md` | ON-REQUEST | SESSION-ONLY | User invokes the PowerShell Script Development Prompt or requests its guided script-development workflow | Tier 2 General PowerShell Script-Writing Instructions (applicable) |
| `Tier 2 General/CoSyn-Lock-v19.0.1.md` | ON-REQUEST | SESSION-ONLY | User invokes `Lock` | — |
| `SEGaither/CoSyn-Personal-Governance:Tier 2 Personal/CoSyn-Editing-Preferences-v19.0.1.md` | CONDITIONAL | PROJECT-CACHE | Editing existing user artifacts with preservation/version instructions | — |
| `SEGaither/CoSyn-Personal-Governance:Tier 2 Personal/CoSyn-User-Voice-and-Style-Reference-v19.0.1.md` | CONDITIONAL | PROJECT-CACHE | Draft/revise writing in user's voice | — |
| `WBG General/CoSyn-Anti-AI-Prose-Signature-Gate-v19.0.1.md` | CONDITIONAL | PROJECT-CACHE | Explicit synthetic-prose/Anti-AI audit or correction | — |
| `WBG General/CoSyn-Writing-Team-Personas-v19.0.1.md` | CONDITIONAL | PROJECT-CACHE | Manuscript professional-team/persona and editing stages | — |
| `WBG General/CoSyn-Fiction-Drill-Review-Profile-v19.0.1.md` | CONDITIONAL | PROJECT-CACHE | Explicit general-fiction Drill review | — |
| `SEGaither/CoSyn-Personal-Governance:WBG Personal/CoSyn-WBG-Personal-Project-Package-Creation-v19.0.1.md` | CONDITIONAL | PROJECT-CACHE | WBG Personal project package | — |
| `SEGaither/CoSyn-Personal-Governance:WBG Personal/CoSyn-WBG-Personal-Root-Profile-v19.0.1.md` | CONDITIONAL | PROJECT-CACHE | WBG Personal writing workflow requiring root profile | — |
| `SEGaither/CoSyn-Personal-Governance:WBG Personal/CoSyn-WBG-Personal-Readme-v19.0.1.md` | ON-REQUEST | NO-CACHE | WBG Personal package guidance/README | — |
| `SEGaither/CoSyn-Personal-Governance:WBG Personal/CoSyn-WBG-Personal-Validation-Report-v19.0.1.md` | ON-REQUEST | NO-CACHE | WBG Personal validation evidence | — |
| `SEGaither/CoSyn-Personal-Governance:WBG Personal/CoSyn-WBG-Personal-Provenance-v19.0.1.md` | ON-REQUEST | NO-CACHE | WBG Personal provenance/history/audit | — |
| `WBG General/CoSyn-Writing-Project-Workbook-Template-v19.0.1.md` | ON-REQUEST | SESSION-ONLY | Writing workbook template review/use; verify proposed status before treating as governing | — |
| `SEGaither/CoSyn-Personal-Governance:Tier 3 Personal/ATTAS/CoSyn-ATTAS-Drill-Review-Profile-v19.0.1.md` | CONDITIONAL | PROJECT-CACHE | Explicit ATTAS Drill; Bookfox overlay only if explicitly requested | — |
| `SEGaither/CoSyn-Personal-Governance:Tier 2 Personal/CoSyn-TVA-Gmail-Retrieval-Prompt-v19.0.1.md` | ON-REQUEST | SESSION-ONLY | User requests this TVA email consolidation workflow | — |

## 3. Available but not automatically authoritative

- **Superseded provenance/verbatim source:** preserved in the private historical archive; **NEVER-NORMAL** as an active load route. `CoSyn-Checkpoint-v19.1.1.md` governs the consolidated functions.
- **Superseded end-session source:** preserved in the private historical archive, not an active load route. `CoSyn-Checkpoint-v19.1.1.md` governs the consolidated functions.
- **ATTAS story canon:** The private repository contains `Tier 3 Personal/ATTAS/CoSyn-ATTAS-Canon-v19.0.1.md`, carrying the original v1.1.2 source. The previously locally ratified v1.1.3 has not been established in the connected repositories. For ATTAS canon work, resolve the appropriate controlling source using explicit user/project authority; do not silently treat v1.1.2 as the ratified v1.1.3 successor or fail an unrelated bind.
- **New/changed and unindexed files:** Discover candidate names from the smallest relevant folder; read only candidate source headers/content required to determine authority and task applicability. A new file is not automatically current governance and does not invalidate unrelated routes.
- **Other WBG General, WBG Personal, Tier 2, and Tier 3 sources:** Many are present, including legacy/current-looking version pairs with unresolved authority. Do not promote by filename alone. For a task requiring one, perform narrow source-level resolution; unresolved candidates do not block unrelated work.
- **Knowledge base:** `CoSyn-18-core-trinity/knowledge-base/` contains `Guppi-CoSyn-Intro-v1.1.0.md`, `LLM-manual-v2.2.4.docx`, and `place-holder`. These are reference materials, **not baseline governance**. Retrieve on explicit reference/research need; no routine preload. The `.docx` was identified by the repository tree, not semantically inspected.
- **Writing reference corpus:** `CoSyn-18-core-trinity/WBG General/Writing-Team-Professional-Reference-Corpus-Index-v1.1.0.md` and several large transcript/corpus files exist. Retrieve selectively only for applicable professional-reference tasks; no routine preload and no source-status inference from mere presence.
- **Historical, packages, duplicate files, and 0-byte placeholder:** `NEVER-NORMAL`. Source existence alone does not establish operating authority. The earlier empty suspect-output placeholder is retained only in the private archive and has no readable instructions.

## 4. Minimal exception and maintenance policy

- If a required current route fails, correct its path/identity through focused discovery; continue unaffected routing. Full binding fails only when a genuinely required source cannot be established or a required authority conflict remains unresolved.
- If a relevant file is missing from this directory, inspect the pertinent directory listing and at most the source candidates needed to resolve that task. Do not conduct routine repository-wide semantic scans.
- On an authorized future index update, adjust only affected entries and any directly affected dependency/authority decisions; verify affected paths and stop. Retain history, cleanup, provenance, and revision evidence in their existing sources, not in the routine routing directory.
- The prior v1.1.26 revision recorded the User-authorized EOS v1.2.1 successor and designated its superseded EOS and Index files for removal. Index v1.1.27 added the User-authorized Tier 2 General provenance and verbatim record management v1.0.0 artifact. Index v1.1.28 routed provenance and verbatim record management to v1.0.1 after the session-naming correction. Index v1.1.29 routes Voice and Style Reference to user-ratified v1.2.1 and supersedes Index v1.1.28. Index v1.1.30 records the initially proposed Checkpoint v1.1.1 and archival relocation of the former EOS v1.2.1 source. Index v1.1.31 records the user's subsequent ratification and active routing of Checkpoint v1.1.1 and historical status of both predecessor sources.

- Index v19.1.5 previously routed the author-ratified Zero persona v19.1.1. On November 27, 2026 the User ratified its AI-revised successor `CoSyn-Zero-vC19.2.1.md` and authorized private persona and public Artifact Index installation. The prior Zero v19.1.1 remains preserved in the private repository as ratified historical evidence. Index vC19.2.5 is the active route; previous Index v19.1.5 is superseded but remains recoverable in repository history.
