---
name: principled-grilling
description: Shape a plan or design with the user, asking what they want to achieve, restating it, then presenting a reviewed design for their reaction, while learning the reasons behind their decisions so later sessions ask less. Started only by the user, when they want a plan grilled or a design stress-tested.
disable-model-invocation: true
---

# Principled grilling

A grilling works when it draws out of the user what only they know: what
they want and whether a design gives it to them. It should also teach this
agent and later ones to reach decisions the user is happy with, more often
over time. Every judgment below serves that.

The user's time goes where only they can help. Facts about the work, and
how to build it, are for agents to find and decide; the user may not know
the code, and asking them about it wears them out without improving the
design. A session that hands the user a long list of questions and
defaults to clear has failed, even if every answer is good.

## Understand the goal

Ask questions one at a time, each building on the last answer, about what
the user wants to achieve: the problem, who it serves, what better looks
like, and what must not happen. Stay off code and architecture unless the
goal itself turns on them. One question at a time keeps each one easy to
answer and lets the next one follow from what the user actually said.

Before each question, sort it:

- **A fact** is yours to find: look it up in the work, its history or the
  tools, with a sub-agent when it takes exploring.
- **How to build it** is yours to decide later, in the design.
- **What the user wants** is the user's. Ask it with a line of context, and
  when options help, give the best few with a recommendation worded so
  "yes" accepts it.

## Restate

When you can say what the user wants, restate it in your own words: their
goals, the problem they are solving and what success looks like. The user
corrects it. The restate ends the questions; ask more only where the
correction opened something new.

## Design without the user

Design the solution as if building it from scratch: the design you would
be proud of, not held to the work's current structure. When the current
structure is what's wrong, say so and rework it; landing close to what
exists is a fine outcome, as long as it was questioned. A design built
from scratch tends to make wrong claims about the existing work, so it
says how to get from today's work to the new design, checked against the
work itself.

Then have the design reviewed by someone other than its author, before the
user sees it: an agent reviewing its own design misses what it got wrong.
Fix what the review finds. What the author and reviewer still disagree on
becomes an open question for the user.

Every default you take is written in the design with its reason, so the
user can skim and overrule any of it. Defaults are not walked through in
the conversation.

## Present and react

Present the design in the form that shows what is at stake. Where people
will use it, show worked examples: what they type or do, what they see,
and what happens when it fails. Where other work will build on it, show
the interface itself and something using it. These are illustrations; the
point is that the user judges the design by seeing it, not by reading
about it.

The user reacts in their own words. Their reactions are worth more than
their picks between options: a condition they add, a part they reject, a
case they bring up. Open questions come last, each with its context, the
options and their consequences on their own lines, and a recommendation.
A change that alters the design goes back through review before the user
approves it.

## Learning the reasons

The reason behind a reaction is worth more than the reaction, but asking
"why?" every time wears the user out. When a reaction departs from the
design, or no known principle explains it, state the reason you infer and
ask the user to confirm it in a word: "I read this as: never store a value
you can't trace back to its source, even at the cost of a failed import.
Right?" A wrong guess is still useful; the correction is usually the
principle.

Across reactions, look for the thread they share. When several point the
same way, propose the principle they suggest, with the decisions it comes
from and the boundary case where you are unsure it holds.

How far an agent may act on a principle depends on how it is known:

- **Confirmed by the user, in their own words:** the agent decides and
  writes the default in the design.
- **Inferred, not yet confirmed:** the agent recommends from it and says
  so. An answer someone else gave on the user's behalf, such as another
  agent deciding for them, counts as inferred, not as their precedent.
- **Unknown:** the agent asks, or leaves it as an open question in the
  design.

Nothing becomes a principle without the user's confirmation. Approving a
design does not confirm the reasons you inferred for it; ask about them
directly.

## Ending

The session is done when the user approves the design. Then:

- Summarise what their reactions changed, each with its reason.
- Propose the principle changes (new principles, sharpened boundaries,
  inferred ones to confirm), each with who it is for and where it would
  go, so the user's approval covers the destination too.
- Save what the user approves where they approved it.

## Where a principle goes

To choose a principle's destination, work out who it is for. The places
named below are examples: the destination depends on what your harness
offers at each layer, so use what you know of your own harness and put the
principle where every agent at that layer already reads.

- **Everyone working on this work:** principles every contributor
  should follow, such as the product's vision and its conventions, go in
  the work's shared place, such as a document in its repository.
- **The user, for this work:** how they personally work on it and
  preferences that aren't contributor rules go in their own context for
  the work, such as a project's instructions or memory, never in what is
  shared with every contributor.
- **The user, across all their work:** in their personal guidance, the
  skills every harness they use loads, worded for any work. It is loaded
  everywhere, so it takes only confirmed principles.
- **Inferred, not yet confirmed:** in the user's own context for the
  work, marked as inferred with the decisions behind it, so later
  sessions recommend from it and confirm it when it recurs.

When the right place doesn't exist yet, propose one. When this session
can't write to it, give the user the text and where it goes.

Fewer questions, shorter sessions and fewer rejected designs mean the
principles are working.
