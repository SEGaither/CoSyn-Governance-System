# CoSyn Artifact Index

**Artifact:** `artifact-index-v1.1.24.md`  
**Version:** 1.1.24  
**Status:** RATIFIED / ACTIVE / CURRENT — installed in canonical GitHub repository  
**Date:** 2026-10-24  
**Supersedes:** `artifact-index-v1.1.23.md`  
**Canonical repository:** https://github.com/SEGaither/CoSyn-Governance-System  
**Repository observation:** `main` recursive Git tree `13a5665f9a9af715fc1a503577cff935d84c77cc`; tree not truncated. This is a point-in-time observation, not a continuing guarantee.  
**Purpose:** Identify the minimum applicable canonical source files for the current task. This is a routing directory, not a repository-maintenance ledger.

## 1. Binding and tolerant routing rules

1. **Bootstrap:** Discover the repository root and read the current repository-installed Index. Establish required Core and applicable persona sources from their real contents before claiming a complete bind.
2. **Choose by task, not presence:** Read `BOUND-BASELINE` records once per session, then `CONDITIONAL` records whose triggers materially match, and `ON-REQUEST` records only on request or direct need. `NEVER-NORMAL` records are excluded unless their content is directly relevant. Read exact required dependencies, not unrelated directories. A cache designation does not create applicability.
3. **Minor drift is nonfatal:** Extra, newly added, renamed, or modified repository files do not themselves invalidate a bind. Do not scan or read every file to reconcile inventory. For a selected file with a stale path, search the relevant repository directory for its logical identity, then inspect the narrow candidate source for status and authority. A changed Git blob or filename alone does not establish supersession, but also does not automatically block binding.
4. **Authority and conflict:** The repository is the source authority for repository-controlled artifacts. If multiple candidates disagree about required authority, do not guess or silently elevate the newest name. Report the *specific unresolved required dependency*. Continue using independently established required sources when safe; mark full binding incomplete only if the unresolved source is necessary to that binding. Unindexed files are not automatically active. An explicitly user-supplied ratified local successor can govern its stated session scope but is not represented as already installed in GitHub.
5. **Retrieval failure:** A failed request to one path or endpoint proves only that attempt failed. Rediscover the actual path and use another supported method when useful. Do not repeatedly retry an unchanged failure, treat an unsupported directory response as missing files, or fill gaps with memory.
6. **Cache policy:** Apply only *after* applicability is established. `PROJECT-CACHE`: use an unchanged project-source copy only when its canonical identity and fidelity are verified against the current Index; otherwise fetch the canonical file and preserve a copy only if supported. `SESSION-ONLY`: reuse within session, no routine project persistence. `NO-CACHE`: retrieve when directly needed, no routine project persistence. Project copies never supersede the repository.
7. **State discipline:** Separate *repository reachable*, *artifact located*, *retrieved*, *read*, *applicable*, *instantiated*, and *bind complete*. Claim only demonstrated states. Reuse established session state unless changed authority, applicability, contradiction, reset, or cache validity materially requires refresh.

## 2. Routing directory — verified active sources

All paths are relative to the repository root. An exact path is a retrieval locator, not proof that a file has been read this session. `—` in dependencies means **none independently established in this Index**, not proof that the source declares none. Where this Index knows exact source-declared dependencies, they are specified.

| Artifact / exact repository path | Load | Cache | Task trigger | Direct known dependencies |
|---|---|---|---|---|
| `CoSyn-18-core-trinity/Core/cgs-core-v18.0.1-constitution.md` | BOUND-BASELINE | PROJECT-CACHE | CoSyn constitutional baseline | — |
| `CoSyn-18-core-trinity/Core/cgs-core-v18.0.2-persona-governor.md` | BOUND-BASELINE | PROJECT-CACHE | Persona governance baseline | Constitution v18.0.1 |
| `CoSyn-18-core-trinity/Core/cgs-core-v18.0.2-stack-architect.md` | BOUND-BASELINE | PROJECT-CACHE | Stack/authority and routing baseline | Constitution v18.0.1; Persona Governor v18.0.2 |
| `CoSyn-18-core-trinity/Tier 2 Personal/Guppi-v1.3.17-091726-ratified.md` | BOUND-BASELINE | PROJECT-CACHE | Normal cross-project Guppi identity and response baseline; do not replace explicitly selected specialist identity | — |
| `CoSyn-18-core-trinity/Tier 2 Personal/cgs-v18.0.1-tier2-personal-response-instructions-v1.3.md` | BOUND-BASELINE | PROJECT-CACHE | Cross-project response rules | — |
| `CoSyn-18-core-trinity/Tier 2 Personal/Zero-v3.0.1-091726-ratified.md` | CONDITIONAL | PROJECT-CACHE | Zero requested; software, LLM/API/agents, code, debugging, repository engineering | — |
| `CoSyn-18-core-trinity/Tier 2 Personal/persona-tier2-personal-ziggy-v1.3.4-ratified.md` | CONDITIONAL | PROJECT-CACHE | Ziggy requested; reflective reasoning, personal judgment, continuity-aware self-improvement | — |
| `CoSyn-18-core-trinity/Tier 2 General/cgs-v18.0.1-tier2-general-work-session-management-team-persona-v1.1.1-091726.md` | CONDITIONAL | PROJECT-CACHE | Consequential stateful/multistep work, team routing or continuity handoff | Guppi v1.3.17; Git safety protocol (source-declared; resolve if relevant) |
| `CoSyn-18-core-trinity/Tier 2 General/cgs-v17.0.0-tier2-general-git-repository-change-safety-protocol-v1.0.0-082126.md` | CONDITIONAL | SESSION-ONLY | Git inspection or mutation, commits, branches, history, reset/push | — |
| `CoSyn-18-core-trinity/Tier 2 General/cgs-v17.0.0-tier2-general-gpt-compute-conservation-v1.2.0-091726.md` | CONDITIONAL | PROJECT-CACHE | Execute an already approved/established plan in ChatGPT | — |
| `CoSyn-18-core-trinity/Tier 2 General/cgs-v17.0.0-tier2-general-end-session-package-prompt-v1.1.1-100726.md` | CONDITIONAL | PROJECT-CACHE | End-session/continuation packages | — |
| `CoSyn-18-core-trinity/Tier 2 General/cgs-v17.0.0-tier2-general-powershell-script-writing-instructions-v1.1.1-082626.md` | CONDITIONAL | SESSION-ONLY | Writing executable PowerShell scripts for user | — |
| `CoSyn-18-core-trinity/Tier 2 General/cgs-v17.0.0-tier2-general-lock-v1.0.0.md` | ON-REQUEST | SESSION-ONLY | User invokes `Lock` | — |
| `CoSyn-18-core-trinity/Tier 2 Personal/cgs-v17.0.0-tier2-personal-editing-preferences-v1.3.md` | CONDITIONAL | PROJECT-CACHE | Editing existing user artifacts with preservation/version instructions | — |
| `CoSyn-18-core-trinity/Tier 2 Personal/cgs-v18.0.1-tier2-personal-user-voice-and-style-reference-v1.2.0-092126-ratified.md` | CONDITIONAL | PROJECT-CACHE | Draft/revise writing in user's voice | — |
| `CoSyn-18-core-trinity/WBG General/cgs-v18.0.1-wbg-general-anti-ai-prose-signature-gate-v1.1.0-092126-ratified.md` | CONDITIONAL | PROJECT-CACHE | Explicit synthetic-prose/Anti-AI audit or correction | — |
| `CoSyn-18-core-trinity/WBG General/Writing-Team-Personas-v2.4.1-ratified.md` | CONDITIONAL | PROJECT-CACHE | Manuscript professional-team/persona and editing stages | — |
| `CoSyn-18-core-trinity/WBG General/cgs-v18.0.1-wbg-general-fiction-drill-review-profile-v1.3.0-092526-ratified.md` | CONDITIONAL | PROJECT-CACHE | Explicit general-fiction Drill review | — |
| `CoSyn-18-core-trinity/WBG Personal/cgs-v18.0.1-wbg-personal-project-package-creation-workflow-v1.0.1.md` | CONDITIONAL | PROJECT-CACHE | WBG Personal project package | — |
| `CoSyn-18-core-trinity/WBG Personal/cgs-v18.0.1-wbg-personal-root-profile-v1.3.1.md` | CONDITIONAL | PROJECT-CACHE | WBG Personal writing workflow requiring root profile | — |
| `CoSyn-18-core-trinity/WBG Personal/cgs-v18.0.1-wbg-personal-readme-wbg-personal-v1.3.2.md` | ON-REQUEST | NO-CACHE | WBG Personal package guidance/README | — |
| `CoSyn-18-core-trinity/WBG Personal/cgs-v18.0.1-wbg-personal-validation-report-v1.3.2.md` | ON-REQUEST | NO-CACHE | WBG Personal validation evidence | — |
| `CoSyn-18-core-trinity/WBG Personal/cgs-v18.0.1-wbg-personal-provenance-v1.3.2.md` | ON-REQUEST | NO-CACHE | WBG Personal provenance/history/audit | — |
| `CoSyn-18-core-trinity/tier 3/General WBG Project Templates/cgs-v18.0.1-wbg-general-writing-project-workbook-template-v1.0.1.md` | ON-REQUEST | SESSION-ONLY | Writing workbook template review/use; verify proposed status before treating as governing | — |
| `CoSyn-18-core-trinity/tier 3/attas/cgs-v18.0.1-wbg-project-attas-drill-review-profile-v1.2.2-092526-ratified.md` | CONDITIONAL | PROJECT-CACHE | Explicit ATTAS Drill; Bookfox overlay only if explicitly requested | — |
| `CoSyn-18-core-trinity/Tier 2 Personal/TVA-gmail-retrieval-prompt-v1.0.0.md` | ON-REQUEST | SESSION-ONLY | User requests this TVA email consolidation workflow | — |

## 3. Available but not automatically authoritative

- **ATTAS story canon:** Repository has `CoSyn-18-core-trinity/tier 3/attas/attas-canon-v1.1.2.md`. The previously locally ratified v1.1.3 was **not found** in the observed GitHub tree. For ATTAS canon work, resolve the appropriate controlling source using explicit user/project authority; do not silently treat v1.1.2 as the ratified v1.1.3 successor or fail an unrelated bind.
- **New/changed and unindexed files:** Discover candidate names from the smallest relevant folder; read only candidate source headers/content required to determine authority and task applicability. A new file is not automatically current governance and does not invalidate unrelated routes.
- **Other WBG General, WBG Personal, Tier 2, and Tier 3 sources:** Many are present, including legacy/current-looking version pairs with unresolved authority. Do not promote by filename alone. For a task requiring one, perform narrow source-level resolution; unresolved candidates do not block unrelated work.
- **Knowledge base:** `CoSyn-18-core-trinity/knowledge-base/` contains `Guppi-CoSyn-Intro-v1.1.0.md`, `LLM-manual-v2.2.4.docx`, and `place-holder`. These are reference materials, **not baseline governance**. Retrieve on explicit reference/research need; no routine preload. The `.docx` was identified by the repository tree, not semantically inspected.
- **Writing reference corpus:** `CoSyn-18-core-trinity/WBG General/Writing-Team-Professional-Reference-Corpus-Index-v1.1.0.md` and several large transcript/corpus files exist. Retrieve selectively only for applicable professional-reference tasks; no routine preload and no source-status inference from mere presence.
- **Historical, packages, duplicate files, and 0-byte placeholder:** `NEVER-NORMAL`. Source existence alone does not establish operating authority. The empty `Tier 2 General/suspect-output-prompt v1.0.0.md` has no readable instructions.

## 4. Minimal exception and maintenance policy

- If a required current route fails, correct its path/identity through focused discovery; continue unaffected routing. Full binding fails only when a genuinely required source cannot be established or a required authority conflict remains unresolved.
- If a relevant file is missing from this directory, inspect the pertinent directory listing and at most the source candidates needed to resolve that task. Do not conduct routine repository-wide semantic scans.
- On an authorized future index update, adjust only affected entries and any directly affected dependency/authority decisions; verify affected paths and stop. Retain history, cleanup, provenance, and revision evidence in their existing sources, not in the routine routing directory.
- This revision makes **no** repository file changes, cleanup actions, or independent ratifications of underlying source artifacts. Only this successor Index is ratified by the user's instruction. The current Index is installed in the canonical GitHub repository.
