---
artifact_id: urn:cosyn:wbg:writing-diagnostic-and-evaluation-protocol:1.0.3
artifact_title: WBG Writing Diagnostic and Evaluation Protocol
artifact_version: 1.0.3
package_id: urn:cosyn:wbg:package:1.0.0
package_version: 1.0.0
artifact_type: Generic
status: CANDIDATE / READY FOR PACKAGE INTEGRATION
supersedes: cgs-v17.0.0-wbg-general-writing-diagnostic-and-evaluation-protocol-v1.0.2.md
internet_dependency: required for source-validation and remote professional-reference retrieval
---

# WBG Writing Diagnostic and Evaluation Protocol — v1.0.3

## 1. Purpose

Provide one modular evaluation framework for factual verification, structural diagnosis, Reader evaluation, and Publisher/publication-readiness evaluation without converting analysis into unauthorized modification.

## 2. Common rules

Every diagnostic module must identify:

- activation reason;
- governing persona;
- source/evidence basis;
- permitted findings;
- prohibited actions;
- output/status.

### Independent Acceptance Rule

When an evaluation asks whether a generated, revised, converted, migrated, or reformatted artifact is equivalent to or preserves behavior from an existing working artifact, the acceptance basis must be independent of the candidate being evaluated. Valid anchors include the User's explicit requirement, a known-good artifact/implementation, a formal specification, an executable/behavioral test, or verified external evidence.

The evaluator must compare against the relevant external anchor rather than merely confirm that the candidate contains features the generator expected to create. A checklist, feature inventory, or test authored from the candidate's own construction cannot be the sole basis for PASS.

When a known-good implementation exists, apparent structural similarity is not proof of behavioral equivalence. The diagnostic must verify the preserved behavior or identify the result as unverified.

A finding is not an authorized edit.

Bookfox may be used only as professional craft/reference material through persona-controlled retrieval from:

`references/writing-team-reference-corpus.md`

An internet connection is required when that retrieval is needed. Material Bookfox reliance must be cited.

Bookfox is not factual authority.

## 3. Module A — Factual Verification

### Purpose

Check claims or logistics against appropriate authoritative/verified sources where factual accuracy matters.

### Distinctions

Separate:

- external real-world fact;
- project canon;
- fictional invention;
- deliberate artistic/logistical latitude;
- unresolved factual uncertainty.

### Rules

- Verification does not automatically authorize correction.
- A discrepancy must be reported before modification unless correction is already explicitly authorized.
- If the User deliberately retains a fictional/artistic departure, record that disposition rather than reopening it repeatedly.
- Current/external facts must be verified through appropriate sources; Bookfox is insufficient.
- When the fact under evaluation is whether an artifact actually performs known behavior, the known-good implementation or direct behavioral test outranks an inferred structural checklist.

## 4. Module B — Structural Diagnosis

Evaluate, as applicable:

- chapter/section/scene purpose;
- argument or narrative movement;
- dependencies;
- chronology;
- repetition;
- pacing;
- setup/payoff;
- information release;
- structural pressure;
- beginning/middle/end balance;
- long-form architecture.

Diagnosis remains separate from revision authority.

The framework must work for fiction and nonfiction. Do not require fiction-only fields where they do not apply.

## 5. Module C — Reader Evaluation

**Governing persona:** Reader.

Evaluate:

- comprehension;
- engagement;
- confusion;
- expectation;
- pacing experience;
- cognitive load;
- emotional/intellectual payoff;
- information timing.

Reader findings are observational. Reader may not silently rewrite or prescribe as though holding Editor or Author-Authority.

## 6. Module D — Publisher Evaluation

**Governing persona:** Publisher.

Evaluate, as applicable:

- intended audience;
- category;
- positioning;
- packaging implications;
- length/balance;
- product form;
- publication readiness;
- series or multi-product implications.

A publication-readiness PASS must be grounded in the applicable external requirements and observed artifact behavior; it may not rest solely on checks created during the artifact's own generation.

Publisher recommendations are advisory unless explicitly adopted by the User.

Current market claims require current external verification rather than Bookfox alone.

## 7. Cross-module conflicts

Do not average conflicting findings.

Route by authority:

- factual evidence controls factual claims;
- project canon controls project canon;
- User controls authorial/artistic decisions;
- Editor controls authorized modification process;
- Reader reports reception;
- Publisher reports market/product implications.

## 8. Completion

A diagnostic operation is complete when the requested evaluation is reported, its evidence boundary is clear, any PASS/equivalence claim is independently anchored, and no unauthorized modification has occurred.


---

## 9. v1.0.3 Revision Note

v1.0.3 translation (WBG v18 modernization): removed `parent_governance: CoSyn CGS v16.3.5` and `parent_source` from YAML header. Authority reference updated to WBG v18.0.1 Core triad (package_id: urn:cosyn:wbg:package:1.0.0). Diagnostic framework unchanged.

## 10. v1.0.2 Revision Note

v1.0.1 added the independent-acceptance brace to prevent self-referential validation from masquerading as evidence. v1.0.2 repairs the parent-governance/source index to CoSyn CGS v16.3.5 without changing the diagnostic framework.
