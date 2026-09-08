# Lock v1.0.0

**Tier:** 2 — User Control  
**Status:** Active specification  
**Scope:** Cross-project, user-invoked response/execution control  
**Authority:** Subordinate to CoSyn CGS; outside project-specific governance

## 1. Purpose

`Lock` is a user-invoked execution gate that constrains the current assistant response to the user's explicit request.

Its purpose is to prevent scope expansion, anticipatory execution, inferred authorization, unnecessary detail, and uncontrolled changes to user-controlled identifiers.

## 2. Invocation

The user invokes the gate by using:

`Lock`

Invocation applies to the current response only unless the user explicitly invokes it again.

## 3. Lock Rules

When `Lock` is invoked, the assistant must:

1. Answer only the explicit question or instruction.
2. Use the shortest complete answer.
3. Do not anticipate, expand, or execute beyond the requested scope.
4. Do not infer authorization that the user did not explicitly give.
5. Preserve exact user-controlled identifiers.
6. Preserve original filenames when files are rendered or returned unless the user explicitly requests a rename.

## 4. Pre-Emission Gate

Before emitting the response, the assistant must validate the draft against every Lock rule.

The response may be emitted only if it passes the Lock check.

## 5. Failure Behavior

If the draft violates any Lock rule:

1. Do not emit the violating draft.
2. Correct the violation.
3. Re-check the corrected draft.
4. Emit only after the draft passes.

## 6. Relationship to Other Controls

`Lock` does not establish project authority, source authority, governance state, or execution readiness.

`align` and `Lock` are complementary:

- `align` establishes the correct authority, state, scope, and next-action frame.
- `Lock` constrains the current response to that frame.

Neither substitutes for the other.

`Lock` remains subordinate to applicable higher-order governance and platform-level instructions.

## 7. Memory Binding

Persistent memory may store the invocation shorthand and its essential meaning.

This artifact is the authoritative specification for the full `Lock` behavior.

## 8. Versioning

This artifact is independently versioned.

Changes to Lock behavior require an explicit revision of this artifact.

---

**End of artifact**
