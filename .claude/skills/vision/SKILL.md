---
name: vision
description: Interview the owner about what a piece of work should become, such as a codebase, product, body of writing or process, covering its purpose, priorities, trade-offs and refusals, and record it so agents make the owner's calls without asking. Started only by the user, to define a direction or to sharpen it after agents kept asking or deciding wrongly.
disable-model-invocation: true
---

# Vision

The measure of a vision is whether an agent reading only it makes the
owner's call on a choice the vision never mentions. Every judgment below
serves that.

An agent that lacks the owner's goal asks about mechanics: typed interface
or strings, one section or two, a table or a list. Each such answer settles
one case and teaches nothing about the next. A vision states what those
answers have in common: what the work is for, what it optimizes, which
value wins when two conflict and where that stops being true. With it, an
agent can decide the forks itself and spend the owner's time only where
the vision is silent.

## What a vision holds

The owner's intent, not the work's current state, and nothing an agent can
read from the work itself. Typically:

- **Purpose:** what the work is for, who it serves, and what better would
  look like a year from now.
- **Priorities in order:** what wins when they conflict, and where the
  ordering flips (correctness over delivery speed, except in a prototype).
- **Principles:** each with its reason and the boundary case that shows how
  far it reaches. A principle without a reason is applied literally; one
  without a boundary is applied everywhere.
- **Refusals:** what the work will not do or depend on, and why.
- **Intended shape:** the structure that should make good choices the easy
  ones, such as a codebase's abstractions or a document set's outline.
- **How each principle is held:** a check where something can enforce it
  (a lint rule, a test, a template field, a form), judgment where it can't.

## Where it lives

Each principle is stored at the scope where it holds, in a place every
agent working at that scope already reads, whichever harness it runs in:

- **One piece of work:** with the work. Use the place it already keeps
  durable context, such as a document in its repository pointed to from
  the agent instructions file, a project's instructions or memory, or a
  file in its folder. When it has none, propose one and confirm it with the
  owner once. Add a line where agents start reading, saying to decide from
  the vision before asking.
- **All the owner's work:** in their personal guidance, the skills that
  every harness they use loads, worded for any work. It is loaded
  everywhere, so it holds only confirmed principles, and changes to it are
  shown to the owner as a diff before saving.

When this session can't write to the right place, give the owner the text
and where it goes.

## Before asking

Gather the evidence yourself: the existing documents, the work's
conventions, its history, and corrections the owner made to agents. Most of
the owner's philosophy is already visible in what they accepted and
rejected. Turn it into proposed principles, so most questions become
confirmations; the owner's time is for what only they know.

## The interview

Ask about the goal first, then the priorities, then the principles; each
answer frames the next. Ask in numbered rounds, each question with a
recommended answer, worded so "yes" accepts it.

Ask at the level of the principle and use a concrete case as the probe,
preferably a real fork from this work. Two illustrations: "In the
importer, an agent could validate each row strictly or accept what parses.
Which matters more here, never storing a wrong value or never blocking an
import?" Or, for a guide: "This page could explain the concept first or
start with the steps. Is the reader here to understand, or to get it done?"
Then record the principle and its boundary, not the case. When an answer
contradicts an earlier one or the evidence, say so; the contradiction
usually hides a boundary worth writing down.

When the owner answers with a preference about mechanics, find the reason
behind it before recording anything; the preference is evidence, the
reason is the principle.

For each principle, ask whether something could check it and propose the
check. A rule an agent must remember is weaker than one a tool enforces,
and a structure that removes the bad option is stronger than a rule
against it.

## Proving it

Before calling the vision done, take a handful of real decisions the work
still faces or recently faced, including ones the interview never touched,
and say how the vision decides each one, citing the principle. Where the
owner would decide differently, the vision is missing something: find
what, fix it, and try again. Show the vision and save what the owner
approves.

## Keeping it true

A principle enters the vision only with the owner's confirmation. One
inferred from their decisions but not yet confirmed may be listed apart in
the work's vision, marked as inferred, so agents recommend from it but
still ask; it moves to personal guidance only once confirmed and seen to
hold across different work. When an agent asked something the vision
should have answered, or decided against the owner's wish, find the
missing or unclear principle, propose its wording, and update the vision
once the owner confirms. Fewer questions and fewer overrides over time
mean the vision is working.
