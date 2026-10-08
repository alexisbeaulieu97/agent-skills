---
name: principled-grilling
description: Interview the user relentlessly about a plan or design while learning the reasons behind their decisions, so later sessions decide what their principles already settle and ask only what is new. Started only by the user, when they want a plan grilled or a design stress-tested.
disable-model-invocation: true
---

# Principled grilling

Interview the user until you share an understanding of the plan, and leave
behind what lets the next agent need fewer questions. A single decision
rarely shows why it was made; a series of them shows how the user thinks.
The decisions settle this plan; the reasons, once confirmed, settle the
next ones.

## Three kinds of question

Before asking anything, sort it:

- **A fact** is yours to find: look it up in the code, the history or the
  tools, with a sub-agent when it takes exploring. Only the questions that
  depend on it wait.
- **A decision the user's principles already settle** is yours to make.
  Their principles live in the project's vision document if it has one and
  in their personal guidance across projects. Make the call, and list it in
  the round with the principle it follows, so the user can overrule it
  in one word. An overruled call means the principle is missing a boundary;
  find it with the user.
- **A decision the principles leave open** is the user's. Ask it, and ask
  for the trade-off underneath rather than the mechanism: which value wins
  here and why, with the implementation choice as the concrete case.

## A round

The frontier is every decision whose prerequisites are settled. Ask the
whole frontier in one round, then wait for the answers; a question that
depends on another one still open goes to a later round.

The user's format for a round:

- Open with a few lines of context for the round: where the plan stands,
  what the previous answers settled, and what this round decides.
- Then the calls you made from their principles, one line each with the
  principle.
- Then the questions, numbered, each starting on its own line with a short
  title, followed by its context: what is at stake, what you found that
  bears on it, and the options. End each with your recommended answer and
  the reason, worded so "yes" accepts it.

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
  inferred ones to confirm. Write each where it stays true: one that holds
  only for this project in its vision document, one that holds for all the
  user's work in their personal guidance, worded for any project.
  Inferred principles the user has not confirmed may be kept there marked
  as inferred, with the decisions behind them, so later sessions can
  recommend from them and confirm them when they recur.
- Save what the user approves.

Fewer questions per session, and fewer overruled calls, mean the principles
are working.
