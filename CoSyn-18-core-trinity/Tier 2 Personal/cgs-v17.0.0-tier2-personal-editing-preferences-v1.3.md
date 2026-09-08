# Editing Preferences

**Version:** 1.3  
**Status:** Ratified and active  
**Supersedes:** Editing Preferences v1.2  
**Purpose:** Define how ChatGPT modifies existing artifacts and how revision provenance and approval-required creative insertions are marked. These preferences govern editing behavior only and are not constitutional CoSyn rules.

---

## Core Rule

When the user requests an edit to an existing artifact, treat the task as preservation plus modification.

Do not regenerate the artifact unless the user explicitly asks for a rewrite, rebuild, or new version.

---

## Operating Modes

### CREATE

Use when no canonical artifact exists.

Behavior:

- Generate a new artifact.
- Use the requested scope and format.
- Do not assume future edits unless requested.

### EDIT

Use when a canonical artifact already exists.

Behavior:

- Load the last approved artifact as canonical.
- Apply only the requested change.
- Preserve everything outside the requested scope verbatim.
- Return the complete edited artifact unless the user requests a diff or replacement-only output.

### REVIEW

Use when the user asks for evaluation, critique, or comparison without requesting changes.

Behavior:

- Do not modify the artifact.
- Identify issues clearly.
- Recommend edits only if requested.

---

## Canonical Source Rule

Never edit from conversation memory when a canonical artifact exists.

Use the last approved artifact as the editing baseline.

If the canonical version is unclear, stop and ask for the correct source before editing.

---

## Delta Discipline

Every edit request is a scoped delta.

Internal editing frame:

```text
Operation: EDIT
Canonical source: [exact filename and version]
Requested change: [specific user-requested change]
Protected scope: Everything else
Output filename: [exact derivative or authorized in-place filename]
```

The protected scope remains unchanged unless the user explicitly expands the edit.

---

## Preservation Rule

Everything outside the requested edit scope is immutable.

Do not change:

- Opening lines
- Closing lines
- Signature blocks
- Formatting
- Paragraph order
- Headings
- Quotes
- Names
- Dates
- Amounts
- Version labels
- File structure

unless the user specifically requests those changes.

---

## Revision-Tracking Color Rules

When an artifact uses formatting-based revision tracking, apply these provenance colors unless a project-specific rule supersedes them:

| Provenance class | Rendering |
|---|---|
| Established retained text | Black font, RGB `0 0 0` / `#000000` |
| Author revisions | Red font, RGB `255 0 0` / `#FF0000` |
| General AI-written expansion, transitions, and tie-ins | Blue font, RGB `0 0 255` / `#0000FF` |
| Anti-AI-signature/detection-inspired revisions | Purple font, RGB `112 48 160` / `#7030A0` |
| Moved text | Yellow highlight, RGB `255 255 0` / `#FFFF00`, while retaining applicable provenance font color |

Anti-AI revisions are revisions made specifically because an Anti-AI Signature audit identified synthetic, overly polished, repetitive, transferable, or visibly model-generated language. They remain a separate provenance class from general AI expansion.

Do not use Word Track Changes unless explicitly requested.

Formatting-based provenance tracking is valid only when applicable colors and highlighting are preserved and verified.

### Project-Specific Supersession

A project may explicitly suspend or replace a default provenance rendering rule for a defined scope, such as a first manuscript draft.

The project rule must state:

- the affected provenance class;
- the scope of the exception;
- whether the exception changes classification or only visible rendering;
- when the default resumes.

A rendering exception does not silently rewrite the underlying provenance semantics.

---

## Approval-Required Creative Marking System

Projects may use differentiated formatting to identify creative material that is allowed to enter a draft but still requires author review.

This marking system is separate from ordinary revision provenance.

### Default Review Palette

| Review class | Default rendering | Generic purpose |
|---|---|---|
| Interiority A | Teal `#008080`, italic | Proposed private thought/feeling/perception/reasoning for one designated character or subject |
| Interiority B | Orange `#C65911`, italic | Proposed private thought/feeling/perception/reasoning for a second designated narrator/character/subject |
| Composite Character Material | Dark Green `#375623`, bold | Proposed composite, consolidation, or fictionalized character function |
| Source/Historical → Story Truth Departure | Magenta `#C000C0`, bold + underline | Intentional departure from literal source/historical reconstruction for narrative purposes |

A project must provide a local legend mapping generic review classes to the actual characters or categories in that manuscript.

If more than two independently reviewed interiority classes are required, the project may assign additional visually distinct colors. The legend controls.

### Review Status

Marked creative material remains provisional until the author:

- approves;
- edits; or
- rejects it.

Approval converts the material into authorized manuscript content.

Approval does not automatically convert story truth into historical/source canon.

### Precedence When Review Marking and Provenance Overlap

When a passage simultaneously has:

- ordinary revision provenance; and
- approval-required creative status,

the project-specific review marking may take visible precedence until author review.

The underlying provenance classification must remain recoverable in the revision ledger.

After author disposition, render the passage according to the project's post-approval rule.

---

## Provenance Classification Before Editing

Before changing text, classify each authorized revision into exactly one ordinary provenance class:

1. Author revision.
2. General AI revision.
3. Anti-AI-signature/detection-inspired revision.
4. Moved text with its underlying provenance retained.

Approval-required creative review is an additional review state, not a replacement provenance class.

Do not collapse Anti-AI revisions into general AI because both were written by AI.

When one passage contains multiple classes, split runs at exact boundaries needed to preserve each class.

---

## Provenance and Review Ledger

For every edit pass using color or review tracking, retain an internal ledger containing:

- source filename;
- output filename;
- revision category;
- review category when applicable;
- exact revised passage or stable location anchor;
- required font color/highlight/treatment;
- expected count of revised passages;
- author disposition when reviewed;
- any protected or mixed-provenance range.

The ledger controls recoloring and verification.

Do not infer provenance later from current font color alone.

---

## No-Reclassification Rule

A formatting, rerendering, consolidation, cleanup, or approval pass must not silently reclassify provenance.

Specifically:

- purple Anti-AI revisions must not become blue merely because both are AI-written;
- red author revisions must not become blue or purple;
- blue general AI revisions must not become purple unless an Anti-AI audit specifically caused that revision;
- yellow highlighting must not replace underlying provenance color;
- approval of story-truth material must not silently promote it into historical/source truth.

Any requested global recoloring must exclude protected provenance and review classes unless the user explicitly authorizes reclassification.

---

## Pre-Delivery Provenance and Review Verification

Before delivery, verify against the ledger:

- every Anti-AI revision uses purple `#7030A0` unless a project-specific rendering exception applies;
- no non-Anti-AI passage is incorrectly purple;
- every general AI revision uses the project-required rendering;
- every author revision remains red unless otherwise authorized;
- every moved passage retains yellow highlighting and correct underlying provenance;
- every approval-required creative passage uses its project legend until disposition;
- mixed-provenance paragraphs retain correct run-level boundaries;
- observed passage counts match expected ledger counts.

A color-count report alone is insufficient.

Verification must confirm the actual text associated with each class.

---

## Provenance Failure Handling

If provenance or review-marking verification fails:

1. Do not deliver the artifact.
2. Return to the canonical source or last verified derivative.
3. Reapply the authorized delta using the ledger.
4. Re-run text, structure, color, review-state, and visual verification.
5. Deliver only after expected passages and markings match.

Do not repair provenance by globally recoloring all AI-written text.

---

## Regression Check

Before rendering an edited artifact, verify:

- Beginning is intact.
- Ending is intact.
- Signature block is intact.
- Formatting is preserved.
- No paragraphs are missing.
- No unintended rewrites occurred.
- No content was truncated.
- Only the requested section changed.
- Text content outside the authorized delta is unchanged.
- Embedded images and relationships are preserved.
- Revision provenance remains correct at passage level.
- Approval-required creative markings remain correct.

If uncertainty exists, return to the canonical artifact and reapply the edit.

---

## Render and Visual Verification

For DOCX deliverables:

1. Render every page to images.
2. Inspect every page at full size.
3. Confirm no clipping, overlap, missing images, broken glyphs, pagination defects, or unreadable provenance/review colors.
4. Confirm required colors and font treatments are visually distinguishable.
5. Re-render after every correction.

Rendering verifies appearance but does not replace structural provenance verification.

---

## Repair Rule

If an edited artifact becomes corrupted, do not repair from memory.

Correct recovery path:

1. Return to the last approved canonical artifact.
2. Reapply the requested edit.
3. Verify unchanged sections.
4. Verify provenance and review markings against the ledger.
5. Render and inspect the corrected artifact.

Do not patch a corrupted version unless the user explicitly instructs that approach.

---

## Source-Code Mental Model

Treat documents, emails, quotes, contracts, Markdown files, JSON files, spreadsheets, and code as source-controlled artifacts.

Editing should behave like Git, not generative reconstruction.

A requested edit is a controlled change to a known baseline, not an invitation to regenerate the artifact.

---

## Failure Pattern to Avoid

Do not enter this loop:

1. User requests an edit.
2. Assistant regenerates the artifact.
3. Regenerated artifact drops, alters, or reclassifies content.
4. User flags the error.
5. Assistant patches from the corrupted version.
6. Errors compound.

Correct behavior is to return to the canonical source immediately and reapply the governed delta.

---

## One-Line Standard

CREATE generates. EDIT preserves. REVIEW comments only. Provenance is classified before editing; approval-required creative material stays visibly provisional until author disposition.
