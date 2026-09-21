---
artifact_id: urn:cosyn:wbg:anti-ai-prose-signature-gate:1.1.0
artifact_title: WBG Anti-AI Prose Signature Gate
artifact_version: 1.1.0
package_id: urn:cosyn:wbg:package:1.0.0
package_version: 1.0.0
artifact_type: Generic
status: RATIFIED / ACTIVE / CURRENT
supersedes: cgs-v18.0.1-wbg-general-writing-voice-style-and-naturalness-v1.0.1.md
source_basis: User-provided Wikipedia AI Writing Reference captured 2026-09-21, selectively adapted for general prose use
---

# WBG Anti-AI Prose Signature Gate — v1.1.0

## 1. Purpose

Detect and correct recognizably synthetic prose patterns without replacing authorial voice.

This artifact answers one question:

`Does this prose contain patterns that make it read as generic, over-smoothed, templated, or recognizably model-generated?`

It does not define how the User should sound. User voice and style are governed separately by the applicable VS artifact and project-specific voice controls.

## 2. Authority and Boundary

AA is a diagnostic and corrective gate, not an authorial style authority.

- VS defines intended voice.
- AA identifies synthetic-pattern risk.
- AA may recommend or make a correction only when the authorized editing scope permits it.
- AA may not compress prose merely because shorter prose appears less synthetic.
- AA may not ban a legitimate word, punctuation mark, sentence length, rhetorical device, or stylistic habit solely because an LLM may also use it.
- AA may not smooth away deliberate roughness, asymmetry, dialect, humor, repetition, unusual punctuation, or idiosyncratic diction.
- When an AA indicator conflicts with established VS or approved project style, the established voice/style choice controls unless the User directs otherwise.

AA is complementary to VS, not a second style guide.

## 3. Source Basis and Use Limits

This revision incorporates selected observations from the User-provided `Wikipedia AI Writing Reference`, generated from Wikipedia's `Signs of AI writing` material and directly linked AI-writing pages.

The source itself states that its indicators are descriptive rather than prescriptive, that many signs also occur in human writing, and that signs should not be mistaken for the underlying problem. This artifact therefore adopts patterns as diagnostic signals, not proof of AI authorship and not automatic rewrite triggers.

Wikipedia-specific markup, citation, template, category, heading, and workflow artifacts are excluded from this general prose gate unless the task itself concerns Wikipedia or equivalent markup residue.

## 4. Core Diagnostic Principle — Regression Toward Generic Prose

The central AA failure is not the presence of a particular word or punctuation mark. It is loss of specificity through statistical smoothing.

Flag prose when it replaces the specific, unusual, physical, character-bound, situational, or causally meaningful detail with language that could apply to many unrelated subjects or stories.

Common manifestations include:

- generic importance replacing concrete consequence;
- generalized atmosphere replacing physical experience;
- polished interpretation replacing observable behavior;
- generic emotional language replacing character-specific response;
- literary-sounding abstraction replacing the actual mechanism, object, place, or action;
- prose that becomes more universally applicable as it becomes more polished.

Correction should restore specificity, not merely change vocabulary.

## 5. High-Value Prose Markers

### 5.1 Explanatory restatement after the scene already showed the point

Flag sentences that interpret, summarize, or explain the meaning of an action, expression, exchange, image, or fact after the reader can already infer it.

Examples of the pattern include narration that explicitly states that a look means attraction, that an action symbolizes a relationship state, or that an already-visible event demonstrates a theme.

Correction preference: trust the concrete action or replace the explanation with a missing specific fact only when one is genuinely needed.

### 5.2 Superficial significance language

Flag unnecessary language that tells the reader that something highlights, underscores, reflects, symbolizes, showcases, demonstrates, contributes to, resonates with, or represents a broader significance when the claim adds no concrete information.

Trailing present-participle constructions deserve extra scrutiny when they merely append significance to an otherwise complete sentence.

This is a pattern check, not a word ban.

### 5.3 AI-vocabulary clustering

Individual words are not prohibited. Flag density or repeated clustering of stock LLM vocabulary, especially when several appear close together without concrete need.

Examples observed in the source include words and constructions such as:

- `highlighting` / `highlight`;
- `showcasing`;
- `emphasizing`;
- `underscores`;
- `pivotal`;
- `intricate`;
- `enduring`;
- `fostering`;
- `enhance`;
- `robust`;
- `tapestry`;
- `testament`;
- `vibrant`;
- `valuable insights`;
- abstract `landscape`.

A single natural occurrence is not a defect. Repetition, density, or use as generic filler is the signal.

### 5.4 Inflated substitutes for simple language

Flag unnecessary replacement of ordinary constructions such as `is`, `are`, `has`, `was`, `said`, or another direct verb with inflated forms such as `serves as`, `stands as`, `marks`, `functions as`, `represents`, `features`, or `offers` when the replacement adds no real meaning.

Correction preference: use the simplest accurate construction unless voice or context supports the more elaborate form.

### 5.5 Negative parallelism reflex

Flag repeated rhetorical constructions such as:

- `not just X, but Y`;
- `not X, but Y`;
- `no X, no Y, just Z`;
- `Y rather than X` used as a recurring stylistic device.

One natural occurrence is not a failure. Habitual use, especially for manufactured emphasis, is.

### 5.6 Rule-of-three reflex

Flag repeated use of three adjectives, three clauses, three examples, three conceptual buckets, or three parallel beats where the grouping appears generated for rhetorical completeness rather than demanded by the content.

Do not disturb a natural or intentional three-part construction merely to avoid the marker.

### 5.7 Over-balanced or symmetrical prose

Flag repeated sentence or paragraph architecture that is conspicuously balanced, mirrored, uniformly polished, or consistently resolved into neat contrasts.

Human prose may be orderly. The concern is repeated mechanical regularity that competes with the actual content.

### 5.8 Generic uplift, thematic closure, or significance

Flag conclusions that manufacture meaning, importance, resilience, legacy, transformation, connection, broader relevance, or emotional closure that the source or scene did not earn.

In fiction, do not append a thematic interpretation simply because a scene feels as though it should end on one.

### 5.9 Synthetic transitions and throat-clearing

Flag stock transitions, unnecessary setup, conversational scaffolding, or response residue that exists to organize the model rather than serve the prose.

Examples include repetitive `Additionally`, `Moreover`, `In conclusion`, `It is important to note`, or assistant-facing phrases such as `Certainly`, `I hope this helps`, `Would you like`, and similar chat residue when they leak into an artifact.

### 5.10 Generic emotional abstraction

Flag emotion described in broad, transferable terms when a character-specific action, perception, physical response, memory, or consequence should carry the moment.

AA does not authorize invention of interiority. If the source does not establish the feeling, preserve uncertainty.

### 5.11 Repetitive architecture

Flag repeated paragraph lengths, same-shape openings, same-shape endings, repeated cadence patterns, repeated rhetorical questions, or recurring construction templates that make the prose feel generated by a form rather than driven by content.

### 5.12 Punctuation as a supporting signal only

Em dashes, semicolons, colons, curly quotation marks, fragments, and other punctuation are not AA failures by themselves.

Flag punctuation only when it participates in a repeated synthetic construction or conflicts with established authorial/project style. Do not mechanically remove punctuation to evade detection.

## 6. Fiction-Specific AA Check

For narrative fiction, inspect especially for:

- cinematic staging that arranges characters for the reader instead of following the active viewpoint and action;
- stock romance, suspense, fantasy, or emotional language that could be transplanted into another novel;
- narration that explains attraction, fear, tension, trust, significance, or motive after behavior has already conveyed it;
- generic atmospheric filler disconnected from a physical source;
- character reactions that are interchangeable across the cast;
- dialogue polished into speeches or banter that exists primarily to signal chemistry, wit, competence, or theme;
- sensory inventories that read like a checklist rather than lived perception;
- excessive compression performed in the name of sounding natural.

The correction target is specific lived experience in the established voice, not minimal prose.

## 7. Severity and Correction Logic

Treat AA indicators cumulatively.

### Low concern

One isolated marker with clear contextual purpose. No change required.

### Moderate concern

Multiple related markers in a short span, especially where they create generic smoothing, explanatory restatement, rhetorical symmetry, or stock emotional language. Review the passage against source and VS.

### High concern

A cluster of markers that makes the passage transferable, generically polished, mechanically structured, or more literary/emotionally fluent than the source supports. Revise within authorized scope.

Correction order:

1. restore concrete subject-, scene-, or character-specific detail;
2. remove unnecessary interpretation or significance;
3. simplify inflated constructions where they add nothing;
4. break mechanical rhetorical patterns only where they are actually synthetic;
5. re-check against VS so the correction has not compressed or normalized the author's voice.

## 8. Anti-Evasion Rule

Do not optimize prose to fool AI detectors.

The objective is natural, specific, source-faithful writing, not detector manipulation. Automated detectors and human judgments both produce false positives. Do not rewrite good prose solely to reduce a detector score.

Do not perform superficial substitutions such as removing all em dashes, banning every flagged word, varying paragraph lengths randomly, or intentionally introducing errors. Such changes may make prose worse without addressing the underlying defect.

## 9. Output Rule

For an AA audit:

- identify only material synthetic-pattern defects;
- distinguish a marker from an actual prose problem;
- do not report ordinary mechanical errors when the editing team is authorized to fix them silently;
- do not overwhelm the User with a checklist when a smaller diagnosis will resolve the issue;
- when correction is authorized, preserve meaning, canon, agency, causality, and VS;
- when rendering revised prose, run VS fidelity after AA correction before delivery.

## 10. Completion Test

AA passes when:

1. important prose remains specific to its actual subject, scene, character, or mechanism;
2. no material explanatory restatement is doing work the scene already did;
3. no material cluster of stock LLM vocabulary or significance language dominates the prose;
4. rhetorical devices arise naturally rather than appearing as repeated templates;
5. simple language has not been inflated without purpose;
6. the prose has not been mechanically shortened, roughened, or randomized to appear human;
7. corrections preserve the applicable VS and project voice;
8. the result reads as authored prose rather than a model demonstrating polish.

## 11. v1.1.0 Revision and Ratification Note

v1.1.0 supersedes the prior combined `cgs-v18.0.1-wbg-general-writing-voice-style-and-naturalness-v1.0.1.md` capability for Anti-AI/naturalness diagnosis.

Changes:

- separates AA from personal Voice and Style authority;
- narrows this WBG artifact to synthetic-pattern diagnosis and correction;
- incorporates selected generalizable observations from the User-provided Wikipedia AI Writing Reference;
- adds regression-to-generic-prose as the core mechanism;
- adds superficial-analysis, vocabulary-clustering, inflated-copulative, negative-parallelism, rule-of-three, symmetry, generic-closure, assistant-residue, and punctuation-supporting-signal checks;
- excludes Wikipedia-specific markup/citation mechanics from ordinary prose auditing;
- establishes that indicators are diagnostic signals, not automatic failures or proof of AI authorship;
- prohibits detector gaming and mechanical humanization;
- makes VS fidelity a mandatory post-correction check.

Ratified by explicit User instruction on 2026-09-21.

---

*Document ID: WBG-Anti-AI-Prose-Signature-Gate-v1.1.0 — RATIFIED / ACTIVE / CURRENT.*
