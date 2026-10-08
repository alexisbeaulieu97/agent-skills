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
- **Guardrails, where they earn their place:** for a principle worth a
  check, what the check is and what it protects.

## Where it lives

Before choosing where a principle goes, ask who it is for. Each layer
below is read by different people and agents, and a principle stored at
the wrong one either binds people it shouldn't or misses agents that need
it. The places named are examples: the destination depends on what your
harness offers at each layer, so use what you know of your own harness,
put the principle where every agent at that layer already reads, and add
a line where agents start reading saying to decide from it before asking.

- **Everyone who works on this work:** principles every contributor should
  follow, such as the product's vision and its conventions. These go in
  the work's shared place, such as a document in its repository pointed to
  from the agent instructions file.
- **The owner, for this work:** how they personally work on it and
  preferences that aren't contributor rules. These go in the owner's own
  context for the work, such as a project's instructions or memory, never
  in what is shared with every contributor.
- **The owner, across all their work:** in their personal guidance, the
  skills every harness they use loads, worded for any work. It is loaded
  everywhere, so it holds only confirmed principles, and changes to it are
  shown to the owner as a diff before saving.

When the right place doesn't exist yet, propose one and confirm it with
the owner once. When this session can't write to it, give the owner the
text and where it goes.

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

Whether a principle deserves a check is a question for each one, and
"nothing worth a check" is a normal answer. When everything becomes a rule,
the rules start limiting improvement; an agent that notices something could
be better and flags it is worth more than one held in place. Where a check
is worth it, propose it so it protects a decision without freezing it:
its message says what it protects and why, so an agent that runs into it
can tell whether to comply or to propose changing the decision, and a
deliberate change updates the check along with the decision.

## Proving it

Before calling the vision done, take a handful of real decisions the work
still faces or recently faced, including ones the interview never touched,
and say how the vision decides each one, citing the principle. Where the
owner would decide differently, the vision is missing something: find
what, fix it, and try again. Show the vision and save what the owner
approves.

## Keeping it true

A principle enters the vision only with the owner's confirmation. One
inferred from their decisions but not yet confirmed may be kept in the
owner's own context for the work, marked as inferred, so agents recommend from it but
still ask; it moves to personal guidance only once confirmed and seen to
hold across different work. When an agent asked something the vision
should have answered, or decided against the owner's wish, find the
missing or unclear principle, propose its wording, and update the vision
once the owner confirms. Fewer questions and fewer overrides over time
mean the vision is working.
