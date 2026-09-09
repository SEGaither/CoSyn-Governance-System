---
artifact: README.md
version: 1.0.0
status: RATIFIED / CANONICAL
ratified: 2026-09-08
ratification_basis: Explicit User approval on 2026-09-08
embedded_startup_prompt_status: RATIFIED / CANONICAL
---

# CoSyn v18

CoSyn is a practical way to make AI easier to work with.

It is built for people who are tired of AI that:

- drifts away from the task;
- gives long answers when a short one would do;
- guesses instead of saying it does not know;
- reopens decisions that were already made;
- adds work that was never requested;
- forgets which source or version controls;
- claims something was checked when it was not;
- turns simple jobs into complicated processes.

The goal is simple:

**Use AI without having to babysit it.**

## Start Here

You do not need to learn how CoSyn is built before using it.

The normal path is:

**GitHub -> README -> copy the startup prompt -> fresh chat or project -> governed CoSyn session**

To start:

1. Copy the full prompt below.
2. Paste it into a fresh ChatGPT chat or project.
3. Continue working normally.

### CoSyn v18 Startup Prompt

```text
Use the CoSyn v18 repository as the controlling source for this session.

Bind to the current canonical CoSyn v18 governance and supporting artifacts required for the work I ask you to do.
On bind, immediately fetch and read the current canonical Core and all Tier 2 artifacts required for this session, instantiate the active assistant/persona directly from those source contents, and do not use memory, summaries, prior-session reconstructions, or cached persona state as substitutes. Do not report the bind complete until source instantiation has occurred.

Use canonical repository sources over memory, copied fragments, reconstructed instructions, or older versions.

Preserve settled decisions and validated state unless new evidence directly invalidates them.

Stay within the scope I actually request.

Do not invent missing facts, files, versions, capabilities, test results, or verification.

Use information already available before asking me to repeat it.

Make the smallest complete change needed.

Do not create unnecessary plans, audits, checks, scripts, workflows, or intermediate artifacts when they can be avoided or absorbed into the approved work.

Verify only what the requested change can materially affect.

Distinguish what is known, inferred, unknown, proposed, executed, and verified when that distinction matters.

Do not claim that something was read, loaded, checked, tested, executed, verified, or completed unless the evidence supports that exact claim.

Keep responses as short as the task reasonably allows.

Stop when the requested work is complete.

Begin by establishing the controlling CoSyn v18 sources required for this session, then wait for or continue with my task.
```

The startup prompt is the normal public entry point for CoSyn v18.

## What CoSyn Is Trying to Fix

AI can be extremely useful, but using it often creates its own kind of work.

You ask for one thing and get five.

You make a decision and the AI keeps reopening it.

You correct the scope and a few turns later it drifts again.

You provide the right file and the AI answers from memory anyway.

You ask whether something was verified and get a confident answer that turns out to mean it was only reviewed.

You ask for a small change and suddenly you are managing a workflow, an audit, three new scripts, and a collection of checks nobody asked for.

CoSyn is designed to reduce that friction.

It gives the AI clearer rules about:

- what you asked it to do;
- what information controls;
- what it actually knows;
- what it is allowed to change;
- what really needs to be checked;
- when the job is finished.

## What You Should Notice

When CoSyn is working properly, the AI should:

- answer the task you actually gave it;
- use information you already provided;
- avoid making you repeat decisions or context;
- separate facts from guesses;
- say when something is unknown;
- use the correct source instead of reconstructing it from memory;
- preserve decisions that are already settled;
- make the smallest change needed;
- avoid unnecessary checks, audits, plans, and process;
- verify what actually matters;
- tell you truthfully what was and was not verified;
- keep the answer as short as the task reasonably allows;
- stop when the work is done.

The point is not to make AI rigid.

The point is to make it dependable enough that you can concentrate on your work instead of managing the AI.

## You Do Not Need to Learn the Architecture

CoSyn has several layers of instructions and supporting files.

Those layers exist because different kinds of work need different kinds of guidance.

They are not a checklist for the user.

For normal use, you should not need to manually find, load, compare, or understand every CoSyn file.

The startup prompt is the entry point.

It establishes the governing session and directs the AI to use the correct CoSyn sources.

## Repository Structure

The public repository is organized into areas such as:

- Core
- Tier 2 General
- WBG General
- Tier 2 Personal
- WBG Personal
- Tier 3

These folders keep CoSyn organized and make it possible to load the right material when it is needed.

You do not need to work through them manually just to use CoSyn.

## Personal Files

Some CoSyn files can be customized for a particular person or project.

They may affect things such as:

- response behavior;
- working preferences;
- writing style;
- project assumptions;
- workflows;
- specialized instructions.

Personal Tier 2 and Tier 3 files should only be loaded intentionally.

Customized personal and project files belong with the person or project they were created for. They should not be treated as universal instructions for everyone.

## Use the Canonical Source

When a canonical CoSyn file exists, use that file.

Do not rebuild governing instructions from memory, an old conversation, a copied fragment, or an earlier version unless there is a specific reason to do so.

This helps prevent one of the easiest ways AI systems drift: working from instructions that look right but are no longer the controlling source.

## What Is Not Part of Normal Startup

The public startup path is intentionally kept separate from development and maintenance material.

Normal users should not need session continuation files, migration tools, build scripts, development evidence, local archives, temporary implementation files, or project history just to use CoSyn.

Those things may matter to maintainers.

They should not become part of everyone else's workflow.

## Current Status

CoSyn v18 modernization is complete.

The public repository structure has been established.

The supported normal startup path is:

**GitHub -> README -> copy the startup prompt -> fresh chat or project -> governed CoSyn session**

The embedded startup prompt is the normal starting point.

## For Maintainers and Advanced Users

The repository also exposes the underlying CoSyn governance and supporting files for people who need to maintain, extend, inspect, or customize the system.

That detail is available when it is useful.

It should not be imposed on people who simply want the AI to work better.

## The Basic Idea

CoSyn is not trying to make AI more complicated.

It is trying to make using AI less complicated.

You should be able to give the AI a task, have it stay within scope, use the right information, tell the truth about what it knows, make the requested change, verify what matters, and stop.

That is the standard CoSyn is built around.
