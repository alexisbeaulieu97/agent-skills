---
name: principled-grilling
description: Shape a plan or design with the user, from their goal or from a plan they bring, asking what they want to achieve, restating it, then presenting a reviewed design piece by piece for their reaction, while learning the reasons behind their decisions so later sessions ask less. Started only by the user, when they want a plan grilled or a design stress-tested.
disable-model-invocation: true
---

# Principled grilling

A grilling works when it draws out of the user what only they know: what
they want and whether a design gives it to them. Every judgment below
serves that.

The user's time goes where only they can help. Facts about the work, and
how to build it, are for agents to find and decide; the user may not know
the code, and asking them about it wears them out without improving the
design. A session that hands the user a long list of questions and
defaults to clear has failed, even if every answer is good.

Before designing, read what the work already settles: its direction, if it
has one written down, and its rules and conventions, so that where the
design departs from them, it does so knowingly and says why.

## Understand the goal

Ask questions one at a time, each building on the last answer, about what
this change should achieve: the problem it solves, what done looks like,
and what must not break. Stay off code and architecture unless the goal
itself turns on them. When the user brings a plan or a few ideas, those
are the starting draft: ask about the goal behind them, not about their
details. One question at a time keeps each one easy to answer and lets the
next one follow from what the user actually said.

Before each question, sort it:

- **A fact** is yours to find: look it up in the work, its history or the
  tools, with a sub-agent when it takes exploring.
- **How to build it** is yours to decide later, in the design.
- **What the user wants** is the user's. Ask it with a line of context, and
  when options help, give the best few with a recommendation worded so
  "yes" accepts it.

## Restate

When you can say what the user wants, restate it in your own words: their
goals, the problem they are solving and what done looks like. The user
corrects it. The restate ends the questions; ask more only where the
correction opened something new.

## Design without the user

Design as if building from scratch: the design you would be proud of with
nothing already built, not held to the work's current structure. Ask this
every time, whatever the size of the change; it is how a wrong design gets
found. When the answer lands roughly where the work already is, say so in
a line and design within it. When it departs, say what is wrong with the
current structure, and show how to get from today's work to the new
design, checked against the work itself: a design made from scratch tends
to make wrong claims about what exists.

Then have the design reviewed by someone other than its author, before the
user sees it: an agent reviewing its own design misses what it got wrong.
The reviewer checks:

- every claim the design makes about the existing work, against the work
  itself, and the path from today's work to the new design;
- whether the request was forced into the current structure when a
  reworked one would serve it better;
- for a design that adds or changes something others build on or use,
  such as an interface, a command or a format, how it holds up from each
  seat: someone building on it, someone using it, an agent driving it,
  whoever maintains it. Separate reviewers each arguing one seat find what
  a single reader misses.

The author fixes what the review finds, and the reviewer checks the fixes.
Stop after two rounds: what the author and reviewer still disagree on
becomes an open question for the user, with both positions.

Every decision you make that the user did not is written in the design
with its reason, so the user can skim and overrule any of it. These are
not walked through in the conversation. What the author and the reviewer
settled between them is one of these decisions, not the user's.

## Present and react

Present the design piece by piece: one part at a time, and the user
reacts before the next part comes. The full design stays available for
the user who wants it. Present each part in the form that shows what is
at stake. Where people will use it, show worked examples: what they type
or do, what they see, and what happens when it fails. Where other work
will build on it, show the interface itself and something using it. These
are illustrations; the point is that the user judges the design by seeing
it, not by reading about it.

The user reacts in their own words. Their reactions are worth more than
their picks between options: a condition they add, a part they reject, a
case they bring up. Each open question comes with the part it belongs to,
after the user has seen that part: its context, the options and their
consequences on their own lines, and a recommendation. A reaction that
changes the design's approach goes back through one round of review
before the user approves; smaller changes the author folds in directly.

The reason behind a reaction settles the parts still to come, so it is
worth more than the reaction; but asking "why?" every time wears the user
out. When a reaction departs from the design and nothing you know explains
it, state the reason you infer and ask the user to confirm it in a word,
for illustration: "I read this as: never store a value you can't trace
back to its source, even at the cost of a failed import. Right?" A wrong
guess is still useful; the correction is usually the reason. Across
reactions, look for the thread they share; it settles parts the user has
not seen yet.

## Ending

The session is done when the user approves the design; do not act on it
before that. Then summarise the decisions, each with its reason.
