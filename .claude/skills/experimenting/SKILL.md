---
name: experimenting
description: Settle a choice between approaches by trying them instead of guessing. Use when torn between ways to do something, unsure whether an approach will work or how it will perform, or when you and the user, a reviewer or another agent disagree on what something will do; also for "try both", "which is faster" or "verify instead of guessing". Settles it with a spike, prototype, test, benchmark or side-by-side samples.
---

# Experimenting

When a choice between options turns on what something will actually do, find
out instead of predicting. A prediction about code, a library, a system or how
a page reads feels like knowledge and is often wrong; a small experiment
replaces the argument with a result. The aim is the right decision at a cost
in proportion to what it decides, not certainty for its own sake.

## When an experiment is worth it

Run one to decide when all three hold:

- **The answer exists outside anyone's head.** Which option is faster, whether
  a library handles this input, whether a migration keeps every row, what an
  API returns, whether a command hangs without a terminal. Do not ask the user
  what an experiment can tell you. A question of taste is different; see the
  section on it below.
- **The result could change the choice.** If every plausible result leads to
  the same option, take it.
- **Being wrong costs more than finding out.** Weigh how hard the choice is to
  undo, and how much will be built on it, against the experiment's cost. A
  choice that is cheap to reverse can be made now and corrected later; one that
  sets a format, moves data or carries other work earns an experiment even when
  you are fairly sure.

When the other two hold, feeling sure is not a reason to skip one. The claims
most worth checking are the obvious-seeming ones about how something you did
not write behaves.

## Design it to decide

- **State, before running it, which result picks which option**, including
  which wins when no threshold is met. For example, "the separate table only
  if it is at least twice as fast at real size, otherwise the simpler JSON
  column", or "B is out if it loses a single row". A criterion fixed first
  cannot drift to fit the result.
- **Test where the options differ, and only that.** Build the smallest thing
  that exercises the point of difference: one tricky input through both
  libraries usually decides more than half-building both designs.
- **Match the conditions the answer depends on**, such as data shape and size,
  versions and environment. Where the experiment differs from the real
  conditions, say how and whether that could flip the result.
- **Give each option its best fair shot, then freeze it.** Same inputs, same
  conditions, each written the way someone who favoured it would write it, and
  settled before running. Afterwards, change an option only to fix a mistake,
  and say so. When measuring time or resources, warm up, repeat, and compare
  the difference with the spread between runs: a difference inside the noise
  is no difference.
- **Observe the thing itself where you can.** As illustrations, not a menu: a
  failing test pins a behaviour, a benchmark measures a cost, a call against
  the real service shows what it returns, a prototype shows whether parts fit,
  a rendered screen shows how it reads.

## Keep it safe and bounded

Run experiments where they cannot change anything that matters: a copy of the
data, a sandbox, read-only calls. An experiment that would write to a shared
system, spend money or reach people needs the user's go-ahead first, like the
real action would.

Keep experiments apart from the work, so nothing half-built ships by
accident. Bring over only what earned its place, on purpose: a check that
pinned a real behaviour can become a test, a benchmark worth rerunning can
join the project. When building an option for real is as cheap as testing it,
build it where it is easy to back out, and check it there.

Fix a budget before starting, in proportion to the choice. When the
experiment grows towards the cost of building the real thing, or the result
stays unclear, stop: an inconclusive result is a finding. Choose on other
grounds, such as the option that is simpler or easier to undo, and say that
is how you chose.

## When the result is awkward

- **Every option fails.** Report that rather than taking the least bad one;
  the choice itself may be the wrong question.
- **It goes against something the user decided.** Show them the result and
  let them decide; do not switch on your own.
- **It cannot run here**, for lack of access, data or an environment. Say what
  would settle it, choose provisionally the option that is easier to undo, and
  say the choice is unverified.

## When the choice is a matter of taste

Some choices turn on taste rather than fact. Follow the project's conventions
or the user's recorded preferences when they settle it. When neither does and
the choice would be costly to change later, build each option just far enough
to be seen, such as two screens, two sample outputs or two ways a command
reads, alike in everything but the point in question, and let the user react
to them instead of to a description. Meanwhile, carry on with the option that
is easier to undo.

## Report the evidence

Say what was compared, the criterion set beforehand, the conditions, what came
out, what the experiment does not show, and the choice it led to. Include what
it takes to rerun it, such as the command or script, so the result can be
checked rather than trusted. "B is faster" alone cannot be told apart from a
guess.
