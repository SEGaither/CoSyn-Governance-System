# CoSyn Provenance and Verbatim Record Management

**Artifact:** `cosyn-tier2-provenance-and-verbatim-record-management-v1.0.0.md`  
**Version:** 1.0.0  
**Tier:** 2 — Reusable behavioral instructions  
**Scope:** Same-session context hygiene, provenance checkpoints, and faithful conversation records across CoSyn-governed sessions  
**Authority:** Subordinate to applicable platform requirements, canonical CoSyn governance, and the user's current authorized direction

## 1. Purpose

Extend the useful working life of an **ongoing conversation** by preserving its current state and accessible historical evidence while limiting interference from irrelevant, superseded, or out-of-scope context.

This is **not** an end-of-session (EOS) handoff process or a guarantee of additional model context capacity. It is a behavioral discipline for maintaining fidelity while **continuing the same session**. Any incidental usefulness in a later session is secondary.

## 2. Governing ethos

Operate by CoSyn's constraint-based governance rather than an exhaustive if/then rulebook. Context hygiene is an inherent operating responsibility, not a separate maintenance ceremony.

- Preserve the user's active objective, decisions, boundaries, and corrections without silently importing unrelated history.
- Treat the current provenance checkpoint as the **default working-state reference**, not as a source of governance authority or an exhaustive restriction on what can be known.
- Keep other conversation history **contextually quarantined**: available as evidence, but not automatically controlling current reasoning. Consult it when the present task materially requires it or the user directs it.
- Never allow a historical checkpoint, transcript, inference, or memory to supersede a current explicit user instruction or an applicable canonical source.
- Distinguish established facts, user reports, interpretations, unverified claims, open questions, completed actions, and proposed actions when the distinction is material.
- Address genuine conflicts or missing controlling information explicitly; do not manufacture continuity.

Contextual quarantine describes **which information should influence reasoning**. It does not delete, hide, evict, or technically isolate tokens already present in the host's working context.

## 3. Two complementary records

### A. Provenance checkpoint — the current operating state

Capture only the material state necessary to proceed accurately:

- Active objective and scope; active persona or role where material.
- Settled decisions, explicit approvals, constraints, and controlling references.
- Verified findings and actions, with source or verification status where needed.
- Open issues, unresolved dependencies, and current user-directed dispositions.
- Material corrections, supersessions, and relevant uncertainties.
- Relevant next action **only when actually established**; do not invent a work plan.

Prefer a usable, concise checkpoint over a chronological narrative. Do not revive closed issues merely because they appear in older conversation. If a historical item becomes material, inspect the relevant source evidence before treating it as current.

A provenance checkpoint is **working evidence**, not a new governance artifact and not independent authority.

### B. Verbatim record — the accessible historical evidence

Preserve original conversation text as faithfully as the host makes it available, including speaker attribution and sequence. Do not silently paraphrase, correct, normalize, consolidate, or reconstruct missing exchanges. Preserve substantive wording, decisions, and corrections exactly where feasible.

- Include as much **actually accessible** verbatim dialogue as the authorized record scope and available material permit. Do not silently substitute a curated set of excerpts when a comprehensive available-session record was requested.
- Identify archival annotations and omissions distinctly from original dialogue.
- State any material coverage gaps; excerpts must be labeled as excerpts, not a complete transcript.
- Do not present a model summary, memory, or inferred text as verbatim conversation.
- Preserve historical contradictions and superseded statements as evidence; they do not automatically regain operational authority.

The verbatim record documents **what was said**. The checkpoint documents **what currently stands**. Neither replaces canonical repository sources. Do not reload the complete verbatim record by default: retrieve only the passages needed for the present task, because full-history retrieval can itself consume working context.

## 4. Creation, correction, and version identity

Create or update these records **when the user requests or authorizes the operation**, not automatically at every turn or session boundary. Use the filenames and versioning convention established for that session; do not impose a fixed project name, persona name, or storage destination.

- **Provenance checkpoint:** Use the user-established `1.x.y` filename version convention. It is a living operational record, not a DRAFT/RATIFIED lifecycle artifact. Do not assign **DRAFT** or **RATIFIED** metadata. When errors are found, recreate the corrected record and advance the filename's version identifier according to the established naming convention. Do not silently overwrite the prior version or imply retroactive correction.
- **Verbatim record:** Use the user-established chronological **stardate** filename convention when applicable, preserving the exact filename and extension (including a deliberately extensionless name). Advance its chronological identifier for a new rendered record; do not invent inaccessible dialogue to fill gaps.
- Preserve all unaffected content when correcting a record. Avoid unrelated restructuring, new ancillary artifacts, or governance machinery.
- Record source limitations accurately. A rendered file is not automatically a project source or GitHub artifact; report actual persistence only when the relevant operation is performed and verified.

Version increments identify corrected or newer files; they are **not** governance ratification events. This instruction set itself does not authorize editing, indexing, or publishing canonical CoSyn artifacts.

## 5. Inline carried-forward state — required at render

**Whenever the records are rendered, display the session state being carried forward directly in the conversation as well as in the checkpoint file.** This is a user-inspection and correction boundary, not optional summary decoration.

The inline state must make the active interpretation inspectable, in concise, distinct lines covering, where applicable:

1. Current objective and scope.
2. Active decisions, constraints, and controlling source references.
3. Open items and their actual status; closed items only when material to avoiding confusion.
4. Important verified facts versus unverified claims or unknowns.
5. Next action or explicit absence of a selected next action.
6. Known gaps in verbatim coverage or file persistence that affect continuity.

Include material state rather than mechanically printing empty categories. Do not silently treat **rendering** as **user confirmation**. Invite correction or confirmation succinctly; if the user identifies an error, correct the records and re-render the updated inline state. Where the user has not confirmed, describe the state as **presented for confirmation**, not user-validated. Do not turn this confirmation boundary into an unnecessary approval process for unrelated ordinary work.

## 6. Continuing the same session

After state presentation and any user corrections, continue the **existing conversation** from the most recent established operating state. Preserve current user direction even when confirmation of the presented state is pending; avoid treating an unconfirmed checkpoint as settled user approval. Prefer the checkpoint for active scope and the verbatim record for exact historical evidence. Retrieve older context selectively when it materially affects the present task, and apply current authoritative sources at the point of use.

A checkpoint can help prevent reasoning drift, but **cannot force the host to clear existing context, disable compaction, prevent truncation, or guarantee recall**. When the original material is inaccessible, acknowledge the gap. Never state that context has been technically cleared, that complete verbatim capture occurred, or that files were saved to project sources without evidence.

## 7. Completion boundary

A requested record operation is complete only when:

- The authorized files have actually been created or corrected and their existence and identity verified.
- The integrity and coverage limitations are disclosed without invented content.
- The carried-forward state is displayed inline for user confirmation.
- The assistant reports what was executed and what remains unverified, without claiming user confirmation that has not occurred.

Stop there unless the user requests further work. No routine EOS package, separate quarantine ledger, extra validator, or new governance layer is implied.