# PowerShell Script-Writing Instructions

**Version:** v1.1.1  
**Date:** 2026-08-26  
**Status:** RATIFIED / ACTIVE / TIER 2 OPERATIONAL CONTROL  
**Scope:** ChatGPT-generated PowerShell scripts for user execution  
**Supersedes:** `powershell-script-writing-instructions-v1.0.0-082126.md`

## 1. Purpose

Establish a compact Tier 2 operational standard for writing PowerShell scripts that are safe, paste-and-run usable, objective-focused, minimally complex, independently verified, and explicit about the difference between simulated validation and actual PowerShell runtime validation.

## 2. Authority

This artifact is subordinate to CoSyn CGS and current explicit user instruction.

It applies across projects whenever ChatGPT writes PowerShell for the user. Project-specific governance may add narrower controls but may not silently weaken higher-authority requirements.

## 3. Core Requirements

1. **Render executable PowerShell in a fenced code block.**
2. **Write for paste-and-run use.** Keep compound syntax such as `if/else`, `try/catch`, loops, and functions together so interactive execution does not separate dependent syntax.
3. **Validate only true blockers.** Do not invent prerequisites or require conditions that are not materially necessary to complete the objective.
4. **Distinguish real failures from harmless console artifacts.** Do not report non-material interactive-shell noise, such as a detached `else` caused by line-by-line execution, as a substantive script failure when the intended operation already succeeded.
5. **Protect unrelated files and state.** Scope all reads and mutations to the requested objective.
6. **Use exact paths for mutation.** Prefer explicit literal paths when changing, moving, replacing, or removing files.
7. **Fail closed on destructive uncertainty.** Do not perform a destructive action when identity, authority, target, or prerequisite evidence is materially uncertain.
8. **Verify the requested result after mutation.** A script is not complete merely because the command ran without error.
9. **Debug iteratively to no further material gain.** Continue bug-fix and validation passes only while they materially improve correctness, safety, or reliability.
10. **Challenge test assumptions before declaring no gain.** Repeating the same successful check is not sufficient if the check itself may be wrong or incomplete.
11. **Count and report debug/bug-fix passes.** When debugging or refinement occurs, report the number of passes performed.
12. **Stop when the objective is satisfied.** Do not expand the script beyond the requested task without material need.
13. **Separate logic simulation from runtime validation.** A virtual or simulated test may validate control flow, expected state transitions, selection logic, limits, and failure behavior, but it does not establish that PowerShell syntax, cmdlet parameter sets, provider behavior, or version-specific semantics will execute successfully.
14. **Validate PowerShell-specific semantics before claiming a script is debugged to no further material gain.** Where material to execution, check syntax, cmdlet parameter compatibility, parameter sets, quoting, path handling, and version-sensitive behavior against the intended PowerShell environment or authoritative PowerShell semantics.
15. **Disclose runtime-validation limits.** If the target PowerShell environment is unavailable and the script has not actually been executed there, state that plainly. Do not describe static review or virtual testing as actual PowerShell execution testing.
16. **Protect whole-script fail-stop behavior for paste-and-run use.** When a script is intended to be pasted interactively, design the delivered block so a terminating failure prevents later success-reporting or dependent operations from running as though the script completed.
17. **Gate success reporting on verified completion.** A success message such as `COMPLETE`, `PASS`, or equivalent may be emitted only after all required operations and postconditions have completed successfully.

## 4. Anti-Verbosity

Use the shortest script and output that reliably completes and verifies the requested objective.

Do not add explanatory comments, diagnostics, abstractions, defensive scaffolding, alternate paths, or reporting unless they materially improve safety, correctness, or execution reliability.

Runtime-semantic validation should be proportional to the script. Do not turn a simple script into a broad compatibility audit when only a small number of execution-sensitive commands require verification.

## 5. Failure-Learning Rules

The following recurring failure patterns are specifically prohibited:

- false prerequisite failures;
- validation that is internally consistent but does not test the actual objective;
- treating harmless interactive PowerShell syntax noise as substantive failure;
- overbuilt scripts whose complexity adds no material gain;
- premature declaration of no further gain without challenging test assumptions;
- mutation without sufficient precondition or postcondition verification;
- representing logic simulation or virtual testing as actual PowerShell runtime validation;
- declaring a script fully debugged when material PowerShell syntax or parameter-set semantics have not been checked;
- allowing interactive paste execution to continue into a false success report after an earlier terminating failure;
- reporting successful completion without verified execution-state evidence.

## 6. Validation Classes

When validation is material, distinguish the following classes:

### 6.1 Static / Logic Review

Checks:

- objective alignment;
- control flow;
- scope;
- safety;
- state handling;
- algorithmic correctness;
- obvious syntax or construction defects.

### 6.2 Virtual Behavioral Test

Simulates representative inputs and expected outcomes without claiming that the target PowerShell engine executed the script.

Useful for:

- filtering;
- ordering;
- cumulative limits;
- branch behavior;
- mutation planning;
- expected fail-stop conditions.

### 6.3 PowerShell Semantic Validation

Checks execution-sensitive PowerShell behavior such as:

- command syntax;
- parameter-set compatibility;
- quoting;
- provider/path semantics;
- version-sensitive cmdlet behavior.

This may be performed through actual target-shell execution or authoritative PowerShell documentation/metadata when actual execution is unavailable.

### 6.4 Runtime Execution Test

Actual execution in the intended or materially equivalent PowerShell environment.

Only this class establishes that the tested code path executed successfully in that runtime.

Do not collapse these classes into a single generic statement such as `tested` when the distinction matters.

## 7. Paste-and-Run Failure Boundary

For scripts intended to be pasted directly into an interactive PowerShell console:

- deliver the operational script as a coherent block;
- ensure terminating failures prevent later operational and success-reporting sections from executing;
- do not rely on the user's console paste behavior to create script-level fail-stop semantics;
- prefer an explicit outer failure boundary when needed to guarantee that a failed operation cannot be followed by a misleading completion report.

A script that fails and then prints a success message is a material correctness failure even if no destructive mutation occurred.

## 8. Output Discipline

For a normal PowerShell request, return only what is materially needed:

- the executable PowerShell code;
- a debug/bug-fix pass count when debugging or refinement occurred;
- the validation classes actually performed when testing is requested or materially relevant;
- no-further-material-gain status when that threshold was actually reached;
- any material limitation that affects safe or correct execution.

Do not add tutorial explanation, redundant commentary, or speculative edge cases unless requested or materially necessary.

## 9. Completion Standard

A PowerShell script is complete when it:

- directly addresses the requested objective;
- avoids the known recurring failure patterns above;
- preserves unrelated state;
- verifies the intended result where mutation occurs;
- has PowerShell-specific execution semantics checked to the level materially required by the task;
- does not misrepresent virtual or static validation as actual runtime execution;
- cannot report success after a prior material failure in the delivered execution path; and
- has reached no further material gain without unnecessary complexity.

## 10. Revision Basis

v1.1.1 incorporates a failure observed on 2026-08-26 during a non-destructive archive-copy task.

The script's high-level logic and virtual behavior had been reviewed, but the delivered code contained a PowerShell parameter-set incompatibility in a `Split-Path` invocation. The defect was not detected because simulated testing was treated too broadly as if it covered target-shell semantics.

When the user executed the code interactively:

- source enumeration succeeded;
- the copy plan was built;
- execution failed before the first file copy;
- no source file was deleted or modified;
- later pasted reporting commands still ran and incorrectly printed a completion message.

The retained general lesson is:

> **Logic validation, PowerShell semantic validation, and runtime execution are different evidence classes. Debug-to-no-gain must not claim evidence from a class that was not actually performed, and success reporting must be gated on verified completion.**

This refinement does not require maximal testing. It requires the minimum execution-sensitive validation necessary to support the claims made about the script.

---

**Ratification:** RATIFIED / ACTIVE by explicit user instruction on 2026-08-26.  
**Advancement:** v1.1.1 supersedes `powershell-script-writing-instructions-v1.0.0-082126.md` as the active Tier 2 PowerShell script-writing artifact.
