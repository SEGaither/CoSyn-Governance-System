# Checkpoint — Project Session Continuity

**Artifact:** `Checkpoint v1.1.1.md`  
**Version:** 1.1.1  
**Tier:** 2 — Cross-project operational workflow instructions  
**Status:** RATIFIED / ACTIVE / CURRENT — user-authorized 2026-11-25; installed in canonical GitHub repository  
**Date:** 2026-11-25  
**Scope:** In-session provenance checkpoints, verbatim Markdown conversation records, and planned or forced session continuation  
**Consolidation sources:** `cosyn-tier2-provenance-and-verbatim-record-management-v1.0.1.md`; `cgs-v17.0.0-tier2-general-end-session-package-prompt-v1.2.1-110126.md`  
**Canonical routing authority:** CoSyn Artifact Index v1.1.30 (index routing update pending for ACTIVE status)  
**Repository:** https://github.com/SEGaither/CoSyn-Governance-System

## 1. Purpose and authority

Provide one entry point for three related but independently selectable continuity functions: (A) provenance checkpoint, (B) verbatim Markdown record, and (C) end-session continuation package. Preserve established output conventions, source fidelity, and the seven-member end-session ZIP contract. Do not make users perform unrelated record operations merely because one has been requested.

This artifact consolidates operating instructions, not the resulting records. It does not independently amend canonical CoSyn governance, ratify project sources, change artifact authority, or authorize installation in GitHub. Until this successor is ratified and indexed as appropriate, the two named canonical source instructions remain controlling.

Operate through CoSyn's behavioral constraints, not an expanding set of if/then rules. Preserve human authority, persona identity, project scope, authoritative source primacy, truthfulness about access and execution, and proportionate effort.

## 2. Invocation and selection

When the user invokes **`checkpoint`** as a command, do not generate a record immediately. On the next assistant turn, ask which of the three outputs the user wants:

- **Provenance checkpoint** — a versioned Markdown record of the current operating state.
- **Verbatim record** — a versioned Markdown record of actually accessible conversation dialogue.
- **End-session package** — the seven-file ZIP continuation package, including a snapshot of the living verbatim record.

Allow any one, any two, or all three selections in a single request. Accept the user's equivalent plain-language selection without requiring a precise label. If the user has already explicitly selected the desired output(s), execute the selection directly without an unnecessary extra question. Do not treat ordinary discussion mentioning “checkpoint” as an invocation.

Selection authorizes creation of only the selected standalone outputs and any internal members explicitly required by the selected operation. End-session packaging requires its project-provenance member and a snapshot of the session's living verbatim record; these are **internal package dependencies**, not authorization to render separate standalone outputs that the user did not select. A request for a checkpoint alone does **not** require a verbatim record. A verbatim request alone does **not** require a checkpoint. Selecting end-session packaging authorizes updating the existing living verbatim record as necessary to supply its mandatory package member; no parallel verbatim lineage is created. No operation automatically closes a conversation.

Before creating any selected provenance or verbatim record, use the **user-specified session name** in its output filename. Reuse the name already expressly established for that session; if none has been supplied, obtain that single missing input before generating the affected record. Do not infer a session name from project, chat title, persona, or topic. The end-session package retains its established project/session naming requirements; its required project provenance is not a substitute for a separately requested session checkpoint.

## 3. Shared evidence and continuity discipline

Identify the actual project and session, applicable CoSyn sources, user decisions, current authoritative artifacts, and relevant evidence. Reuse verified state when still valid; retrieve only what material source conflicts, missing evidence, or output requirements justify.

Preserve current objectives, established decisions, corrections, approvals, constraints, source linkage, completed work, and unresolved matters. Distinguish user-confirmed state, user reports, assistant interpretation, provisional records, superseded positions, verified observations, proposed actions, and unknowns when material. Neither compressed records nor historical dialogue outrank current user direction or applicable canonical and project authority.

Keep unrelated projects, sessions, and historical material contextually separate. Historical evidence is available for selective consultation but does not automatically govern current reasoning. Do not turn a continuity operation into a reconstruction from memory or a generalized history project. Do not claim that record creation clears host context, resets token capacity, prevents truncation, preserves every inaccessible message, or guarantees unlimited conversation length.

Use the least work needed to maintain faithful continuity. Where materially necessary to understand a current decision or state, preserve a compact supported relationship such as **prior state → evidence or user decision → current state**. Do not invent causal links. Preserve original files outside authorized changes.

## 4. Output A — In-session provenance checkpoint

**Purpose:** Capture concise, current working state for accurate continuation of the *same* conversation. A checkpoint may also aid a subsequent conversation, but is not itself a formal end-session package.

Include only the material operating state:

- Active objective, scope, and lead persona where relevant.
- Settled decisions, approvals, constraints, controlling sources, and current artifact identities.
- Verified findings and executed actions, with material sources or verification status.
- Open issues, unresolved dependencies, actual status, and user-selected next actions when established.
- Material corrections, supersessions, uncertainty, and significant state transitions.

Prefer a compact usable checkpoint to a chronological narrative. Treat the most recent applicable checkpoint as the default state reference, subject to current evidence and authority. Distinguish a user-confirmed checkpoint from provisional state; rendering alone does not establish user acceptance.

**Naming/versioning:** Use the session-name-safe identifier and established `1.x.y` filename convention (for example, `zero-for-tva-provenance-v1.0.0.md`). Preserve the same session identifier through revisions unless the user changes it. Do not mark working checkpoints DRAFT or RATIFIED. Correct a record by producing a new version, preserving unaffected content, not silently overwriting an earlier version.

**At render:** Display the carried-forward state *inline in the conversation* as well as in the Markdown file. Concisely show material objective/scope, decisions/authority, open and closed statuses needed for clarity, verified facts versus uncertainties, established next action or absence of one, and coverage or persistence limitations. Present it for user confirmation or correction; do not demand confirmation before unrelated ordinary work. Correct and rerender if the user identifies a substantive error.

Do not automatically generate a verbatim record or end-session ZIP.

## 5. Output B — Verbatim Markdown record

**Purpose:** Maintain one living, cumulative record of accessible session dialogue as historical evidence, distinct from a checkpoint's current-state interpretation.

Preserve as much actually accessible conversation dialogue as the authorized record scope and available material permit, faithfully and in speaker order with attribution, without silently paraphrasing, rewriting, correcting, normalizing, consolidating, or inventing missing exchanges. Do not silently substitute selected or curated excerpts when the user requests a comprehensive available-session record. Preserve meaningful decisions, corrections, and historical contradictions. Separate archival annotations or omissions from original text. If only excerpts or partial history can be captured, label the record as excerpts or partial coverage, identify material omissions or access gaps, and do not call it a complete transcript. Do not substitute a summary, memory, or inferred text for verbatim dialogue.

**Living-record continuity:** Maintain one logical verbatim lineage per named session. Each authorized update begins with the latest available verified record and **appends only newly accessible dialogue** in chronological order. Never recreate the entire record from a summary or substitute a fresh truncated transcript, silently overwrite preserved content, duplicate already recorded exchanges, or repair historical dialogue through invented text. Preserve unchanged existing content byte-for-byte where feasible. Mark any gaps, duplicate-boundary uncertainty, or inaccessible intervening messages explicitly as archival annotations distinct from dialogue. If the previous record is unavailable or cannot be verified, do not claim a complete cumulative record: preserve what is accessible as a clearly qualified partial record and identify the missing predecessor.

**Naming/versioning:** Use the expressly user-specified session name and the session's established chronological **stardate** convention where applicable (for example, `zero-for-tva-verbatim-v1125.6.md`). Retain the session identifier and a single cumulative lineage across successive rendered versions, advancing the chronological identifier for each newly rendered snapshot as applicable. Preserve previous versions rather than silently overwriting them, while treating the latest verified version as the living record's current snapshot. Preserve any explicitly requested extension or lack of extension. Do not create fabricated bridging dialogue.

At render, identify material source-coverage gaps and persistence limitations, and show the relevant carried-forward state inline as required by the provenance/verbatim management workflow, without misrepresenting the transcript as an approved checkpoint. Do not reread the full verbatim record by default in subsequent turns; consult relevant passages only when needed.

Do not automatically generate a standalone provenance checkpoint or end-session ZIP.

## 6. Output C — End-session continuation package

**Purpose:** Produce a compact, transferable handoff so a new conversation can resume without reconstructing project state from memory or depending on the original conversation remaining usable.

**Timing:** Prefer a planned transition while the original conversation still accepts requests. Provenance checkpointing and verbatim capture do not expand conversation capacity. No dependable advance capacity indicator has been established; do not claim one or use arbitrary token, message, or age thresholds as verified limits. If continued use creates a material risk to continuity, recommend an orderly handoff without repeatedly interrupting normal work. The user chooses whether and when to transition.

### 6.1 Evidence consolidation

Use the latest applicable checkpoint as the primary working-state reference. Examine **earlier accessible checkpoints within the relevant session and project lineage** for material nonredundant decisions, findings, corrections, state changes, historical evidence, or open matters not retained in the latest checkpoint. Reconcile material gaps against accessible conversation evidence and authoritative project artifacts. Checkpoint version recency alone does not confer authority; resolve current state using source authority and user decisions.

Consolidate repeated unchanged facts. Retain material historical evidence only where it explains current state, establishes provenance, prevents repeating completed work, or is necessary to continue reliably. Preserve significant superseded states with their supported transition when necessary; do not re-promote them as current. Preserve unresolved contradictions explicitly, rather than silently choosing an unsupported version.

A review can only cover accessible records. Identify unavailable checkpoints, sources, and reconciliation gaps where they materially affect fidelity. The end-session ZIP contains a snapshot of the latest verified living verbatim record. A separate standalone verbatim deliverable is not required unless selected; the mandatory ZIP member remains subject to actual accessibility and honest coverage reporting. The continuation state should not routinely load the full transcript.

### 6.2 Mandatory package structure

Create a **flat ZIP containing exactly seven standalone files**:

1. **Continuation State** — current project objective/scope (primary), session objective/scope (secondary), state, governance bindings, controlling decisions and constraints, authoritative artifacts/versions, and open matters. For material open items, include actual status, known owner, next action, deadline, and source reference where available. Distinguish located-but-unread, reviewed-but-not-fully-evaluated, established, and reconciliation-pending evidence. Preserve a supported state-transition chain only when needed.
2. **New-Session Resume Prompt** — a standalone physical ZIP member directing the receiving session to bind current applicable authority, read the continuation state, preserve settled decisions and open matters, resolve missing essential sources or authority conflicts before claiming readiness, and stand by for instruction. Rendering this prompt only in chat is insufficient.
3. **Updated / Indexed Project Provenance** — the current project provenance lineage, preserved and advanced under its established convention. If no project provenance exists, initialize `<project>-provenance-v1.0.0.md`. Where a lineage exists, preserve its prior content and append material new provenance rather than creating a parallel session-provenance file. Capture decisions, approvals, corrections, significant changes, failures/recoveries, artifact dispositions, source-linked conclusions, and necessary supported transitions. This is a separate package member, even if an in-session provenance checkpoint was also selected.
4. **Artifact Reference Ledger** — controlling/relevant artifacts, exact filenames, versions, statuses, tier/layer where relevant, role, and whether included or merely referenced. The ledger records whether an artifact is one of the seven included package members or is only referenced. Do not add external source artifacts as extra ZIP members; identify any essential external artifact that must be available separately for safe resumption and disclose a material access gap when its availability cannot be established.
5. **Package Manifest** — package identity/version, project, closing session, date, purpose, exact seven-member inventory, and statement that the handoff is not ratification or promotion of authority.
6. **Verbatim Session Record** — the latest verified cumulative Markdown record for the closing session, updated by appending accessible dialogue not yet preserved before packaging. Preserve the original chronology, speaker attribution, historical contradictions, annotations, and actual coverage limitations. Include this as a packaged **snapshot of the existing living record**, not as a newly reconstructed or independent verbatim lineage. Where completeness cannot be established, disclose the precise known or material coverage gap; do not misrepresent a partial record as comprehensive. Do not automatically load this full record into the receiving session's working context; retrieve relevant passages selectively when needed.
7. **SHA256SUMS** — SHA-256 digest of each of the other six members, including the packaged verbatim record.

Preserve project/session lineage and original artifact names; do not rewrite or rename unrelated source artifacts. Do not add baselines, manuscripts, Tier 1/Core sources, or supporting files as extra ZIP members. If an essential external artifact must travel with the handoff, preserve it through a separately authorized and verified transfer without modifying the seven-member ZIP contract. The seven-member contract replaces the previously required six-member contract for this proposed successor only.

### 6.3 Package integrity

Verify before delivery that:

- Exactly seven readable members exist in a flat ZIP; the resume prompt, project provenance, and cumulative verbatim snapshot are physical members.
- The project-provenance lineage is preserved and correctly advanced; if absent, its required initial file exists.
- Manifest names match all seven ZIP members and SHA-256 digests match the final bytes of the other six members, including the verbatim snapshot.
- Continuation state matches the best established current evidence, without superseded material presented as current.
- Material outstanding items retain known status, ownership, action, timing, and source references, while unknowns remain explicit.
- Significant state transitions retain necessary, evidence-supported context; summaries do not silently replace authoritative source evidence.
- Source-reading and reconciliation statuses are accurately distinguished; unfinished reconciliation is not claimed complete.
- The receiving-session instructions identify material evidence gaps and source conflicts before claiming readiness, without automatically reopening settled work.
- The packaged verbatim record is based on the latest verified living lineage, new accessible dialogue is appended once, prior content is retained, and any historical coverage gaps are stated honestly. The receiving session is not directed to preload the complete transcript.

Return the ZIP link, ZIP SHA-256, exact seven-file inventory, validation outcome, and material unresolved continuity defects only. A revised governing workflow artifact is separately supplied only when such a revision was explicitly authorized and actually made.

## 7. Forced conversation boundary

If the original conversation reaches its platform limit before an end-session ZIP can be made, a replacement session may proceed from **accessible authoritative project artifacts, available checkpoints, and other retrievable evidence**, reconciling material gaps before claiming readiness. Do not represent this recovery as an already-generated compliant seven-file package. Do not imply missing material was recovered or invent inaccessible history. Preserve source authority, artifact versions, and unverified gaps. This is a recovery path, not a substitute for planned transitions.

## 8. Authorization, completion, and scope

Create or correct only records requested or authorized by the user, plus the internal mandatory members of any selected end-session package. The `checkpoint` selection does not authorize publishing, committing, deploying, or changing the canonical repository, Index, or unrelated project artifacts. An authorized artifact operation is complete only after the final files exist and their exact identities and affected contents have been checked to the extent materially required. Report what was actually created, verified, and persisted; a local download is not proof of project-source or GitHub persistence.

When a checkpoint or verbatim record is rendered, also display the material carried-forward state inline for user inspection, distinguishing provisional from confirmed information. Invite correction succinctly. Do not convert this boundary into an unrelated approval process. After creating the selected outputs, return to the user's established session state and stop; no new governance mechanism or routine maintenance step is implied.

## 9. Amendment and transition to canonical status

This is a proposed consolidated successor. Adoption requires explicit user authorization and appropriate canonical repository and Artifact Index updates. The existing provenance/verbatim v1.0.1 and end-session package v1.2.1 source artifacts remain the governing references until that transition is verified. Material successor changes require user authorization and a new indexed version. Do not silently delete, supersede, or rewrite existing canonical sources.

**Revision identity:** Version `1.1.1` follows the user's independent `vZ.x.y` convention: `x` tracks AI-recommended changes and `y` tracks user-recommended changes, without counter resets. This revision adds the user-directed seven-member package and cumulative living verbatim lineage while retaining previously corrected source-fidelity requirements. Versioning does not establish canonical ratification.

**Operating principle:** One command; user-selected standalone outputs; mandatory internal package members; one cumulative verbatim lineage per session; faithful evidence consolidation; reliable planned continuation; minimal work beyond the authorized objective.