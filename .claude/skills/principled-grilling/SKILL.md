---
name: principled-grilling
description: Interview the user relentlessly about a plan or design while learning the reasons behind their decisions, so later sessions decide what their principles already settle and ask only what is new. Started only by the user, when they want a plan grilled or a design stress-tested.
disable-model-invocation: true
---

# Principled grilling

The measure of a grilling is whether it draws out of the user what lets
this agent and future ones reach decisions the user is satisfied with,
more accurately over time. Every judgment below serves that.

Interview the user until you share an understanding of the plan, and leave
behind what lets the next agent need fewer questions. A single decision
rarely shows why it was made; a series of them shows how the user thinks.
The decisions settle this plan; the reasons, once confirmed, settle the
next ones.

## Three kinds of question

Before asking anything, sort it:

- **A fact** is yours to find: look it up in the work, its history or the
  tools, with a sub-agent when it takes exploring. Only the questions that
  depend on it wait.
- **A decision the user's principles already settle** is yours to make.
  Their principles live in the work's vision, if it has one, and in their
  personal guidance across all their work. Make the call, and list it as
  a default with the principle it follows.
- **A decision the principles leave open** is the user's. Ask it, and ask
  for the trade-off underneath rather than the mechanism: which value wins
  here and why, with the implementation choice as the concrete case.
  A small choice you may take yourself, but only when you can say why it
  is the right one: the work's conventions, a principle, or a pattern in
  the user's earlier answers points to it. Being easy to reverse lowers
  the cost of a wrong default; it doesn't make one right. When nothing
  points either way, ask: that answer is how a new principle is found.

No decision is taken silently. Every default you take, from a principle or
from your own judgment, is listed with its reasoning, so the user can see
it and overrule it in one word. An overruled default is a lesson: when it
followed a principle, the principle is missing a boundary; when it followed
your judgment, the user's reason may be a principle. Find out which with
the user.

## A round

The frontier is every decision whose prerequisites are settled. Ask the
whole frontier in one round, then wait for the answers; a question that
depends on another one still open goes to a later round.

The user's format for a round:

- Open with a few lines of context for the round: where the plan stands,
  what the previous answers settled, and what this round decides.
- Then the defaults you took, one line each with its reasoning: the
  principle it follows, or why you judged it so.
- Then the questions, numbered, each starting on its own line with a short
  title, followed by a few lines of context: what is at stake and what you
  found that bears on it.
- Under each question, each option on its own line with its consequence,
  never options run together in a paragraph.
- Then the recommendation on its own line, with its reason, worded so
  "yes" accepts it.

For each decision, weigh as many options as the decision reasonably has,
including ones the user didn't mention, and present only the best few,
with one recommendation. The user's time goes to choosing between good
options, not to filtering weak ones.

## Flagging a better design

When the answers show the request fits the current design poorly, say so
explicitly instead of quietly fitting it in: what breaks down, the
alternative design, and the cost of each. Put it to the user as its own
question; quietly bending the request to the design, or the design to the
request, hides the decision that matters most.

## Learning the reasons

The reason behind an answer is worth more than the answer, but asking
"why?" every time wears the user out. When an answer departs from your
recommendation, or no known principle explains it, state the reason you
infer and ask the user to confirm it in a word: "I read this as: never
store a value you can't trace back to its source, even at the cost of a
failed import. Right?" A wrong guess is still useful; the correction is
usually the principle.

Across answers, look for the thread they share. When several decisions
point the same way, propose the principle they suggest, with the decisions
it comes from and the boundary case where you are unsure it holds.

How far an agent may act on a principle depends on how it is known:

- **Confirmed by the user:** the agent decides and says so.
- **Inferred, not yet confirmed:** the agent recommends from it and still
  asks.
- **Unknown:** the agent asks the open question.

Nothing becomes a principle without the user's confirmation. Approving a
plan does not confirm the reasons you inferred for it; ask about them
directly.

## Ending

The session is done when the frontier is empty and the user confirms the
shared understanding; do not act on the plan before that. Then:

- Summarise the decisions, each with its reason.
- Propose the principle changes: new principles, sharpened boundaries,
  inferred ones to confirm.
- Save what the user approves, after asking who each principle is for.
  The places named below are examples: the destination depends on what
  your harness offers at each layer, so use what you know of your own
  harness and put the principle where every agent at that layer already
  reads.
  - **Everyone who works on this work:** principles every contributor
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

Fewer questions per session, and fewer overruled defaults, mean the principles
are working.
