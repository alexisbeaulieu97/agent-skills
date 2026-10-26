---
name: maintaining-skills
description: How to write and revise agent skills so they improve an agent's judgment without replacing it. Use when creating or editing a skill, tuning a skill's description, deciding what belongs in a skill or where, or checking whether a skill change improved behaviour.
---

# Maintaining skills

A skill shapes an agent's judgment without replacing it. Each idea in it
should improve a decision the agent would otherwise get wrong, including in
cases the skill never names, without constraining decisions the agent could
make well on its own.

## How agents read a skill

- Only the description is always in context, and the agent loads a skill
  on it alone, among many others. So the description says what the skill
  covers and the requests it serves, in the language users are likely to
  use, and claims only its own ground; it grows more insistent only after
  the skill was seen not to load.
- An agent loads a skill for one need, by a description written for it.
  So each skill does one job: one kind of decision at one kind of moment.
  An idea that serves a different decision gets its own skill, even when it
  shares a method with an existing one; a shared method is not a shared job.
- Anything a skill copies from elsewhere goes stale when the source changes,
  and an agent cannot tell a stale copy from a current one. So a skill
  states only what it is the source of truth for, such as its owner's
  judgment and conventions, and for anything else says where to look and
  when.
- Text depends on the agent's cooperation; a check, a template field, a
  permission or a script does not. So what can be enforced is enforced, and
  recurring work fully determined by its input becomes a script the skill
  runs.
- An agent generalises from a principle and its reason, and matches a list.
  So an open set is given as the principle that produces it, with cases as
  illustrations; a list is kept for a set that is truly complete, such as
  the steps of a procedure.
- An agent copies an example's incidental details. So examples differ in
  everything but the point they share, and say they are illustrations.
- An agent acts on a statement at the strength its wording carries: "must",
  "never" and "rule" bind, "prefer" and "idea" leave room, and capitals or
  "CRITICAL" spread a statement past its intent. So each statement is worded
  at the strength it has: how far the agent may depart from it, and how
  sure it is.
- An agent follows a method or an order it is given, even where another
  would serve better. So method and order are given only where they matter;
  elsewhere the skill describes the result, in terms the agent can check.
- A prohibition tells the agent what to avoid but not what to do. So a
  skill says what to do, and adds a prohibition only where that leaves a
  costly wrong action open; an action that cannot be undone gets its
  safeguard from the start.
- An agent reads two names as two things and a past state as a current
  one. So each concept keeps one term, and the skill states current
  behaviour, not its history.
- An agent cannot count on another skill being loaded, but it sees every
  skill's description. So a skill works on its own and leaves routing to
  descriptions: it states the task plainly enough to match the skill that
  owns it, without naming or restating that skill. When that skill fails
  to load, the instruction or its description is unclear; a clearer
  description serves every route to it, a name only one.
- An agent opens a reference only when its pointer says when it is worth
  reading. So each pointer says when.
- An agent exists only in the session that reads the skill: it cannot
  count on remembering an earlier run and will see no later one. So a
  skill speaks of now, what to do in this session, checked by what this
  session can see. A signal that shows only across sessions, such as fewer
  questions over time, is for the skill's owner and stays with them, such
  as in the commit that made the change, not in the skill.
- An agent treats a choice the skill assigns to the user as a question to
  ask. So a skill names only the decisions the task cannot proceed
  without; what the user might do afterwards, on their own, it leaves
  unsaid.

## Questions to ask of a draft

- What decision does each idea improve, why does that matter where it is
  not obvious, and how would you know it worked? When you cannot tell, the
  idea is unclear or holds more than one; rewrite or split it.
- Where an idea comes from a result that worked, does it keep the criterion
  that produced the result, or only the result's shape?
- Does it constrain a decision the agent could make well on its own? An
  owner's conventions are not such decisions; they stay, at the strength
  the owner gave them.
- If this fact changed, whose change would it be? It belongs at the
  narrowest scope where it stays true; what varies by project belongs in
  the project, whose own conventions win.
- Before you finish, reread each list you wrote: if an agent following it
  would check its items and stop, put the principle first.
- When something new arrives mid-draft, such as a correction, a wider goal
  or a new case, would you still split, frame and name the skills this way
  if you started from it? The draft's shape was chosen with less; revise
  the shape, not only the text, rather than fitting the new idea into it.

## Learning from use

A skill improves through use: everyday work brings the cases it never
names. When an agent working with it does something its owner would not,
find out why before changing anything, change the one idea responsible,
and let the owner judge by the next uses whether it helped. Because each
idea is a unit, the effect of a change can be traced to it; a change
spread across several ideas cannot be. More text fixes only guidance that
was missing.
