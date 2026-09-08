# Git Repository Change Safety Protocol

**Artifact:** `git-repository-change-safety-protocol-v1.0.0-082126.md`
**Version:** 1.0.0
**Tier:** Tier 2 — User / Secondary Control
**Status:** RATIFIED / ACTIVE
**Scope:** Cross-project safety protocol for LLM-directed, LLM-assisted, or user-executed Git repository inspection and change workflows.
**Created:** 2026-08-21
**Ratification basis:** User explicitly approved creation of a distinct Tier 2 Git repository safety artifact, authorized ratification, and required debugging to no further material gain.
**Authority:** Subordinate to platform/system requirements, current explicit user instruction, CoSyn CGS, and applicable project-specific Tier 3 governance.

## Purpose

Prevent repository contamination, accidental inclusion of unrelated state, unsafe reference changes, and incorrect remote deployment by requiring actual Git state to be discovered and reconciled before mutation.

This artifact owns repository-change safety. It does not own general CCT prompt architecture, project-specific repository design, release semantics, or application-specific deployment logic.

## 1. Trigger and Applicability

Apply this protocol before a workflow performs or directs a material Git repository change, including as applicable:

- staging;
- unstaging;
- commit;
- branch creation, deletion, or switching;
- merge or rebase;
- reset or restore;
- clean;
- stash;
- tag creation, movement, deletion, or rewrite;
- remote configuration changes;
- fetch, pull, or push when remote state matters;
- repository publication or migration;
- adding an existing untracked project tree to Git.

A purely explanatory Git answer does not require full preflight.

A read-only inspection may use only the subset needed to answer the question, but it must not silently transition into mutation.

## 2. Controlling Safety Invariant

Do not mutate a repository from assumptions about its state.

Discover the actual repository state first, identify the intended change boundary, reconcile that state with the intended destination when required, and modify only the explicitly authorized delta.

Accuracy and preservation of unrelated state outrank convenience, speed, and broad automation.

## 3. Minimum Preflight Inventory

Before material mutation, establish the facts relevant to the intended operation.

At minimum, determine as applicable:

1. Git repository root;
2. current branch or detached-HEAD state;
3. current HEAD commit;
4. tags pointing at HEAD when reference identity matters;
5. configured remotes and destination URLs;
6. staged changes;
7. unstaged tracked changes;
8. untracked files;
9. ignored-state relevance when the intended target may be ignored;
10. whether the intended target path is tracked, modified, deleted, or untracked;
11. whether unrelated working-tree state exists;
12. whether the intended remote/canonical target is known and current enough for the proposed operation.

Use read-only commands for discovery when possible.

If command output could invoke a pager or another avoidable interactive state, prefer a non-interactive equivalent or explicitly explain the expected interaction.

## 4. Warning Conditions Versus Execution Blockers

Do not treat every irregular repository condition as a hard stop.

### 4.1 Warning Conditions

Examples that may permit continued analysis or a narrowly isolated change:

- a dirty working tree whose unrelated changes can be preserved and excluded;
- untracked files outside the authorized target;
- historical material elsewhere in the repository;
- no tag at HEAD when the intended operation does not require a tag;
- no configured remote when the current stage is only local inspection.

Warnings must be surfaced when they materially affect safety.

### 4.2 Execution Blockers

Stop the affected mutation when a condition prevents reliable isolation or destination verification, including:

- repository root or repository identity cannot be established;
- the intended target cannot be distinguished from unrelated changes;
- a destructive command could affect unrelated state and no safe bounded alternative is established;
- the intended remote destination cannot be established before a remote write;
- branch/ref destination is ambiguous before commit, merge, rebase, tag, or push;
- protected/canonical reference handling is unclear;
- local and remote/canonical state materially conflict and the correct authority cannot be determined;
- required credentials, permissions, or remote access prevent validation of the intended write.

Report the blocker precisely. Do not broaden the repair beyond what is required to clear it.

## 5. Canonical and Remote Reconciliation

When the intended result will be committed to or published against a remote/canonical repository, establish the relationship between local state and the intended remote state before the write.

Determine as applicable:

- correct remote repository;
- correct branch;
- relevant tag or protected reference;
- whether the local target is already represented remotely;
- whether the local baseline is tracked;
- whether local files are newer, older, divergent, duplicated, or unrelated to the remote target;
- whether a remote comparison can be performed read-only.

Do not infer remote identity from folder names alone.

Absence of a configured Git remote is a blocker for push, not automatically a blocker for local inspection or preparation.

When remote comparison is required but mutation has not been authorized, prefer read-only remote inspection where practical rather than silently changing local remote-tracking state.

## 6. Minimal-Delta Rule

Every repository change must be bounded to the smallest authorized path/ref/state delta that reliably achieves the user-approved objective.

Required behavior:

- preserve unrelated tracked modifications;
- preserve unrelated deletions;
- preserve unrelated untracked files;
- preserve archives, builds, generated artifacts, and historical material unless explicitly in scope;
- do not normalize, reorganize, rename, delete, or clean unrelated material;
- do not use repository cleanup as a convenience step for a narrower task.

A messy repository is not permission to tidy it.

## 7. Staging Safety

In a materially dirty repository, broad staging is prohibited unless the user explicitly authorizes the full repository delta after review.

Do not default to:

- `git add .`
- `git add -A`
- staging an overly broad parent directory;
- equivalent commands that sweep unrelated state into the index.

Prefer explicit path-scoped staging.

Before commit, validate the index independently from the working tree. At minimum inspect:

- staged file names/status;
- staged diff or equivalent content-level delta where material;
- unexpected deletions;
- unexpected renames;
- unexpected generated/binary/package artifacts;
- whether every staged path belongs to the authorized change.

PASS requires the staged delta to contain only the intended change.

## 8. Destructive-Operation Guard

Commands that can discard, overwrite, relocate, or hide work require explicit need and bounded scope.

This includes as applicable:

- `git reset --hard`;
- `git clean`;
- destructive `git restore` or checkout forms;
- branch deletion;
- forced checkout/switch;
- rebase with unresolved local state;
- stash used as an unreviewed workaround;
- force push;
- tag deletion or movement.

Do not use destructive operations merely to make the repository easier to reason about.

If a safer read-only or path-bounded alternative exists, prefer it.

## 9. Protected Branch and Tag Safety

Treat canonical, release, or protected branches/tags as immutable unless the user explicitly authorizes a change and the governing repository policy permits it.

Do not:

- rewrite a protected tag;
- force-update a protected branch;
- force-push merely to reconcile local history;
- move a canonical release reference to make local state fit an expectation.

When a protected reference conflicts with the proposed operation, preserve the reference and redesign the change path.

## 10. Commit Gate

Before commit:

1. confirm repository root;
2. confirm current branch/ref;
3. confirm the staged delta only contains authorized paths;
4. confirm unrelated working-tree state remains outside the index;
5. confirm required validation has passed;
6. confirm the commit message accurately describes the bounded change.

Do not commit if the index contains unexplained material.

## 11. Push Gate

Before push:

1. confirm the intended remote name and URL;
2. confirm the intended destination branch/ref;
3. confirm the local commit(s) intended for publication;
4. confirm protected-reference constraints;
5. confirm the push will not include unrelated commits or rewrite protected history;
6. use a normal non-force push unless force behavior is explicitly authorized and independently justified.

If no remote is configured, stop before push and report that fact. Do not invent or guess the destination URL.

## 12. Post-Change Validation

After a material change, verify the state that the operation was intended to establish.

As applicable, confirm:

- staged index is empty after commit;
- intended commit exists at the expected local ref;
- unrelated working-tree state remains preserved;
- intended remote/ref contains the expected commit after push;
- no protected tag/branch was moved unexpectedly;
- no unauthorized paths were added, removed, or changed.

A command returning success is not by itself sufficient proof of correct repository state.

## 13. Failure and Recovery Behavior

If a safety gate fails:

1. stop the affected mutation;
2. preserve current state;
3. identify the exact mismatch or uncertainty;
4. determine the narrowest corrective action;
5. re-run only the invalidated checks;
6. resume from the earliest trustworthy state.

Do not respond to uncertainty with broad cleanup, reset, reclone, force push, or repository-wide staging unless separately justified and explicitly authorized.

## 14. Interaction With Other Tier 2 Controls

Capability ownership remains separated:

- Git repository state discovery, mutation isolation, staging safety, protected-reference safety, commit/push gates, and repository-change validation → this artifact.
- CCT prompt architecture, prompt debugging, context control, model choice, and non-interactive terminal prompt ergonomics → `cct-prompt-building-directions-v1.2.0-082126.md`.
- General GPT reasoning/compute selection for execution of already-developed plans → `GPT-compute-conservation-v1.1.0-082126.md`.
- Tier 2 promotion/refinement lifecycle → governing Tier 2 refinement protocol.

Do not duplicate these capabilities across artifacts.

## 15. Counterexample and Cost Boundary

This protocol must not impose full release ceremony on trivial read-only Git questions or simple repository explanations.

Apply only the controls necessary for the operation's actual risk.

Examples:

- Asking what `git status` means does not require remote reconciliation.
- Inspecting a local diff does not require a push gate.
- A clean, single-purpose repository may not require the same isolation burden as a heavily dirty multi-purpose repository.
- A dirty repository is not automatically blocked when the intended delta can be isolated deterministically.

The protocol exists to reduce repository-change risk, not to make ordinary Git usage cumbersome.

## 16. Completion Test

A Git change workflow is ready for mutation only when:

- actual repository identity/state has been discovered to the level required by the operation;
- intended target and authority are known;
- warning conditions have been distinguished from true blockers;
- unrelated state can be preserved;
- the authorized delta is explicitly bounded;
- staging behavior cannot silently sweep unrelated state;
- destructive operations are absent or independently justified and authorized;
- protected references are preserved;
- commit and push gates applicable to the operation are defined;
- validation can prove the intended state transition;
- another complete review at the stated reasoning level produces no further material safety gain.

## One-Line Standard

Discover actual Git state first; reconcile the intended destination when required; preserve unrelated state; stage and mutate only the explicit delta; protect canonical refs; validate before commit and push; never use broad cleanup or broad staging as a substitute for understanding the repository.

## Ratification Record

The user explicitly approved creation of this distinct Tier 2 artifact and instructed the assistant to create, ratify, debug to no further material gain, and render it on 2026-08-21.

**Result:** RATIFIED / ACTIVE.
