---
name: codebase-vision
description: Interview the owner about what a codebase should become, its purpose, priorities, trade-offs and refusals, and record it as the project's vision so agents make the owner's calls without asking. Started only by the user, to define a project's direction or to sharpen it after agents kept asking or deciding wrongly.
disable-model-invocation: true
---

# Codebase vision

The measure of a vision is whether an agent reading only it makes the
owner's call on a choice the vision never mentions. Every judgment below
serves that.

An agent that lacks the owner's goal asks about implementation: typed
interface or strings, one module or two. Each such answer settles one case
and teaches nothing about the next. A vision states what those answers have
in common: what the code is for, what it optimizes, which value wins when
two conflict and where that stops being true. With it, an agent can decide
the forks itself and spend the owner's time only where the vision is silent.

## What a vision holds

The owner's intent, not the code's current state, and nothing an agent can
read from the code. Typically:

- **Purpose:** what the codebase is for, who it serves, and what better
  would look like a year from now.
- **Priorities in order:** what wins when they conflict, and where the
  ordering flips (correctness over delivery speed, except in a prototype).
- **Principles:** each with its reason and the boundary case that shows how
  far it reaches. A principle without a reason is applied literally; one
  without a boundary is applied everywhere.
- **Refusals:** what the codebase will not do or depend on, and why.
- **Intended shape:** the abstractions and seams that should make good
  choices the easy ones, and which parts are meant to stay narrow.
- **How each principle is held:** a check (lint rule, type, test, boundary
  rule) where the principle is mechanical, review where it takes judgment.

Follow the project's own documents for where it lives; without one, use
`docs/vision.md` and a one-line pointer from the file every agent in the
repository reads, saying to decide from the vision before asking. A
principle that would hold in every project of the owner's belongs in their
personal guidance instead, worded for any project and confirmed on its own.

## Before asking

Gather the evidence yourself: the existing documents, the code's
conventions, commit history, review comments and corrections the owner made
to agents. Most of the owner's philosophy is already visible in what they
accepted and rejected. Turn it into proposed principles, so most questions
become confirmations; the owner's time is for what only they know.

## The interview

Ask about the goal first, then the priorities, then the principles; each
answer frames the next. Ask in numbered rounds, each question with a
recommended answer, worded so "yes" accepts it.

Ask at the level of the principle and use a concrete case as the probe,
preferably a real fork from this codebase: "In the importer, an agent
could validate each row strictly or accept what parses. Which matters more
here, never storing a wrong value or never blocking an import? I'd say the
first, because a wrong balance costs more than a retry." Then record the
principle and its boundary, not the case. When an answer contradicts an
earlier one or the evidence, say so; the contradiction usually hides a
boundary worth writing down.

When the owner answers with an implementation preference, find the reason
behind it before recording anything; the preference is evidence, the reason
is the principle.

For each principle, ask whether a check could hold it and propose the
check. A rule an agent must remember is weaker than one a tool enforces,
and an abstraction that removes the bad option is stronger than a rule
against it.

## Proving it

Before calling the vision done, take a handful of real decisions the
codebase still faces or recently faced, including ones the interview never
touched, and say how the vision decides each one, citing the principle.
Where the owner would decide differently, the vision is missing something:
find what, fix it, and try again. Show the document and save what the
owner approves.

## Keeping it true

The vision changes only with the owner's confirmation. When an agent asked
something the vision should have answered, or decided against the owner's
wish, find the missing or unclear principle, propose its wording, and
update the vision once the owner confirms. Fewer questions and fewer
overrides over time mean the vision is working.
