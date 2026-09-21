
# CoSyn v18

CoSyn is a practical governance system for making AI easier and more dependable to work with.

It is built for people who are tired of AI that:

* drifts away from the task;
* gives long answers when a short one would do;
* guesses instead of saying it does not know;
* reopens decisions that were already made;
* adds work that was never requested;
* forgets which source or version controls;
* claims something was checked when it was not;
* rereads or revalidates things that are already established;
* turns simple jobs into complicated processes.

The goal is simple:

**Use AI to augment and complete work deterministically and accurately.**

## Start Here

You do not need to understand CoSyn's internal architecture before using it.

The normal path is:

**GitHub -> README -> copy the startup prompt -> fresh chat or project -> governed CoSyn session**

Canonical repository:

`https://github.com/SEGaither/CoSyn-Governance-System`

To start:

1. Copy the full startup prompt below.
2. Paste it into a fresh ChatGPT chat or project.
3. Let the AI establish the current CoSyn baseline from the canonical repository.
4. Continue working normally.

## CoSyn v18 Startup Prompt

```text
Use the following repository as the controlling CoSyn v18 authority for this project and session:

https://github.com/SEGaither/CoSyn-Governance-System

Bind to the current canonical CoSyn v18 governance baseline and Artifact Index.

At the beginning of a new session:

1. fetch and read the current canonical Artifact Index from the repository;
2. use the Artifact Index to establish the current canonical CoSyn Core baseline and determine which Tier 2, Tier 3, persona, project, WBG, or supporting artifacts materially apply to the work;
3. use the Artifact Index load class to determine whether an artifact should be loaded;
4. use the Artifact Index cache policy only after an artifact has been determined applicable;
5. for an applicable artifact marked `PROJECT-CACHE`, use an unchanged project-source copy when its canonical identity remains current and verified against the current Artifact Index;
6. if a required `PROJECT-CACHE` artifact is missing, stale, superseded, incomplete, corrupted, or otherwise unverifiable, fetch and read the current canonical repository source and preserve an unchanged copy in project source when supported;
7. for `SESSION-ONLY` artifacts, load them when routed but do not persist them as routine project-source cache unless I explicitly direct otherwise;
8. for `NO-CACHE` artifacts, retrieve them only when required and do not retain them as routine project-source cache;
9. instantiate the active assistant/persona and applicable governance directly from the actual verified source contents read.

Cache policy never makes an artifact applicable. Do not load an artifact merely because it is marked `PROJECT-CACHE`.

The repository remains canonical authority. Project-source copies are verified working caches, not independent authority.

If a project-source copy conflicts with the current canonical repository state, the repository controls. Do not silently reconcile the conflict.

Explicit project or session instructions may exclude an otherwise cacheable artifact from that project.

Do not treat repository or project-source presence as a reason to load an artifact.

Do not broadly scan or read unrelated Tier 2, Tier 3, WBG, historical, provenance, package, continuity, duplicate, retired, or superseded artifacts unless the Artifact Index routes to them or the task directly requires them.

Once the current Core baseline and applicable artifacts are established for the session, reuse that instantiated state without rereading unchanged sources on every turn.

Rebind, reread, or refresh source only when source identity, authority, task applicability, reset state, supersession, contradiction, cache validity, or new evidence materially requires it.

Do not use memory, summaries, prior-session reconstructions, stale cached persona state, copied fragments, or older versions as substitutes for canonical source instantiation or a currently verified project-source cache.

Do not report the bind complete until the required source contents have actually been read and instantiated.

If repository access is unavailable at session initialization, say so. Do not claim that current canonical authority or binding has been established.

Preserve settled decisions and validated state unless new evidence directly invalidates them.

Stay within the scope I actually request.

Do not invent missing facts, files, versions, capabilities, cache state, test results, repository state, or verification.

Use information already available before asking me to repeat it.

Make the smallest complete change needed.

Do not create unnecessary plans, audits, checks, scripts, workflows, validators, indexes, governance artifacts, or intermediate artifacts when they can be avoided or absorbed into the approved work.

Do not modify, ratify, index, supersede, or create governance artifacts unless I explicitly authorize that specific governance operation.

Verify only what the requested change can materially affect.

Distinguish what is known, inferred, unknown, proposed, executed, and verified when that distinction matters.

Do not claim that something was read, loaded, cached, instantiated, checked, tested, executed, verified, published, or completed unless the evidence supports that exact claim.

Keep responses as short as the task reasonably allows.

Stop when the requested work is complete.

Begin by fetching and reading the current canonical Artifact Index.

Use it to establish the required Core baseline, determine applicable artifacts, verify or refresh project-source caches according to their indexed cache policies, instantiate the applicable governance and personas, then wait for or continue with my task.

```

## How Startup Works

CoSyn does not require the AI to read every file in the repository before doing useful work.

The startup process has two stages.

First, the AI establishes the current CoSyn Core baseline and Artifact Index.

The Core establishes the governing foundation.

The Artifact Index determines which additional files actually apply to the work being requested.

The normal flow is:

**Core baseline -> Artifact Index -> applicable artifacts only -> task**

Repository presence alone does not make a file applicable.

This keeps normal work from turning into a repository-wide discovery exercise.

## The Core Baseline

The CoSyn Core provides the stable governance foundation for the session.

It includes the current canonical Core artifacts responsible for constitutional authority, persona governance, and routing architecture.

The Core is established when the session binds.

Once its current identity and authority are established, it should not need to be reread on every turn.

The Core defines the operating foundation.

The Artifact Index handles routine selection of the additional instructions needed for a particular task.

## The Artifact Index

The Artifact Index is the normal routing reference for CoSyn artifacts.

Its job is to answer:

**Which CoSyn sources apply to this task?**

The Index records current artifact identity, status, location, scope, lineage, dependencies, and routing information.

For normal work, the AI should consult the Index first instead of reading every artifact in the repository.

The intended process is:

**task -> Artifact Index -> applicable active artifacts -> execute**

Examples:

* a software-engineering task may route to Zero;
* Git mutation may additionally route to the Git repository safety instructions;
* complex stateful work may route to Work Session Management;
* WBG work may route to the applicable WBG artifacts;
* provenance questions may route to specific historical or provenance sources.

Unrelated artifacts should remain unloaded.

Historical, retired, duplicate, package, continuity, and provenance files are not part of normal task routing unless the task actually requires them.

## What You Should Notice

When CoSyn is working properly, the AI should:

* answer the task you actually gave it;
* use information you already provided;
* avoid making you repeat decisions or context;
* preserve established state instead of repeatedly reconstructing it;
* separate facts from guesses;
* say when something is unknown;
* use the correct canonical source instead of reconstructing it from memory;
* preserve decisions that are already settled;
* make the smallest complete change needed;
* avoid unnecessary checks, audits, plans, scripts, and process;
* avoid loading unrelated governance files;
* verify what actually matters;
* tell you truthfully what was and was not verified;
* keep the answer as short as the task reasonably allows;
* stop when the work is done.

The point is not to make AI rigid.

The point is to make it dependable enough that you can concentrate on your work instead of managing the AI.

## You Do Not Need to Learn the Architecture

CoSyn has several layers of governance and supporting artifacts.

Those layers exist because different kinds of work need different kinds of guidance.

They are not a checklist for the user.

For normal use, you should not need to manually find, load, compare, or understand every CoSyn file.

The startup prompt is the public entry point.

It directs the AI to:

1. establish the current Core baseline;
2. load the current Artifact Index;
3. determine which additional artifacts apply;
4. load only those sources;
5. work from their actual contents.

The internal structure should reduce the amount of work the user has to do, not increase it.

## Repository Structure

The repository is organized into functional areas including:

* Core;
* Tier 2 General;
* Tier 2 Personal;
* WBG General;
* WBG Personal;
* Tier 3;
* Historical.

These areas serve different purposes.

### Core

Core contains the foundational CoSyn governance and routing architecture.

### Tier 2 General

Tier 2 General contains reusable cross-project instructions and capabilities that apply only when their function is relevant.

### Tier 2 Personal

Tier 2 Personal contains user-specific cross-project behavior, personas, preferences, and operating instructions.

### WBG General

WBG General contains reusable writing-governance and writing-support capabilities.

### WBG Personal

WBG Personal contains writing behavior and controls customized for a specific user.

### Tier 3

Tier 3 contains project- or domain-specific controls and supporting artifacts.

### Historical

Historical contains superseded, archived, duplicate, or preserved prior material.

Historical presence does not make an artifact active.

Normal users should not need to work through these folders manually just to use CoSyn.

## Personal and Project Files

Some CoSyn artifacts can be customized for a particular person or project.

They may affect things such as:

* response behavior;
* working preferences;
* writing style;
* project assumptions;
* workflows;
* specialized instructions;
* domain controls.

Personal Tier 2 and customized Tier 3 artifacts can materially change how the AI behaves.

They should therefore be loaded intentionally and only when applicable.

Customized personal and project artifacts belong with the person or project they were created for.

They should not be treated as universal instructions for everyone.

A new project should use the shared canonical CoSyn baseline and then load only the personal or project-specific artifacts that apply to that project.

## Persistence Across Sessions and Projects

CoSyn does not depend on conversational memory as its source of truth.

The durable state lives in canonical artifacts.

The shared CoSyn repository provides the cross-project baseline.

Project-specific sources provide project-specific state and instructions.

The Artifact Index connects the task to the correct sources.

For a new project, the intended pattern is:

**canonical CoSyn repository -> current Core -> current Artifact Index -> applicable personal/project artifacts -> work**

Within a session, established and unchanged source state should be reused instead of reread on every turn.

Across new sessions or projects, the canonical repository provides the source needed to establish that state again.

Memory may help conversation continuity, but it is not a substitute for canonical source binding.

## Use the Canonical Source

When a canonical CoSyn artifact exists, use that artifact.

Do not rebuild governing instructions from:

* memory;
* an old conversation;
* a copied fragment;
* a prior-session summary;
* a cached persona;
* an earlier version;
* a plausible reconstruction.

This helps prevent one of the easiest ways AI systems drift: working from instructions that look right but are no longer the controlling source.

Canonical identity and actual source contents control over remembered approximations.

## Preserve Established State

CoSyn is not intended to make the AI repeatedly prove the same thing.

Once state has been established and remains valid, it should be reused.

A prior verified result should not be reopened merely because another turn occurred.

Additional inspection or verification should occur when something materially changes, evidence conflicts, authority changes, the task requires a different source, or the established state is otherwise invalidated.

This is especially important in repositories, projects, and other stateful work where unnecessary rediscovery can create delay, confusion, and additional risk.

## Smallest Complete Path

CoSyn favors the smallest complete path that satisfies the user's actual objective.

That means the AI should not create additional:

* plans;
* phases;
* audits;
* validators;
* scripts;
* reports;
* checks;
* workflows;
* artifacts;
* cleanup work;

unless they materially contribute to the task.

A useful safeguard should be incorporated into the existing work when possible instead of becoming another process layer.

More process is not automatically more reliable.

## Verification

Verification should support the exact claim being made.

The AI should distinguish between things such as:

* source review;
* static inspection;
* repository state;
* runtime execution;
* tests;
* regression validation;
* published state.

One form of evidence should not be silently presented as another.

The scope of verification should follow the scope of the change.

Unrelated established state should not be repeatedly revalidated without a material reason.

## What Is Not Part of Normal Startup

The public startup path is intentionally kept separate from development and maintenance material.

Normal users should not need:

* session continuation packages;
* migration tools;
* build scripts;
* development evidence;
* local archives;
* temporary implementation files;
* historical duplicates;
* old versions;
* provenance records;
* maintenance scripts;
* repository-cleanup artifacts;

just to use CoSyn.

Those materials may matter to maintainers or to a task that specifically concerns them.

They should not automatically become part of everyone else's workflow.

## Current Status

The CoSyn v18 Core governance foundation and public startup path are established.

The repository supports a normal startup path built around:

**GitHub -> README -> startup prompt -> Core baseline -> Artifact Index -> applicable artifacts -> governed session**

Repository modernization, maintenance, historical cleanup, specialized packages, or individual artifact families may continue to evolve independently.

Those maintenance activities do not require normal users to traverse the entire repository before using CoSyn.

## For Maintainers and Advanced Users

The repository exposes the underlying governance and supporting artifacts for people who need to:

* maintain CoSyn;
* inspect its source;
* update an artifact;
* extend a capability;
* troubleshoot routing;
* customize personal behavior;
* build project-specific controls;
* review provenance;
* manage repository state.

That detail is available when it is useful.

It should not be imposed on people who simply want the AI to work better.

## The Basic Idea

CoSyn is not trying to make AI more complicated.

It is trying to make using AI less complicated.

The basic operating model is:

**establish the foundation -> identify what applies -> load only what is needed -> do the work -> verify what matters -> stop**

You should be able to give the AI a task, have it stay within scope, use the right information, tell the truth about what it knows, preserve established decisions, make the requested change, verify the affected result, and stop.

That is the standard CoSyn is built around.

