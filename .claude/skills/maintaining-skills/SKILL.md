---
name: maintaining-skills
description: How to write, revise and test agent skills (SKILL.md files and their references) so they improve an agent's judgment without replacing it. Use when creating or editing a skill, tuning a skill's description, deciding what belongs in a skill or where, or checking whether a skill change improved behaviour.
---

# Maintaining skills

A skill shapes an agent's judgment without replacing it. Each idea in it
should improve a decision the agent would otherwise get wrong, including in
cases the skill never names, without constraining decisions the agent could
make well on its own.

## How agents read a skill

What to write follows from how it is read. Each fact below comes with what
it means for the author.

- Only the description is always in context. The agent loads a skill on it
  alone, among many others, and handles a simple request without loading
  any. So the description says what the skill covers and the requests it
  serves, in the language users are likely to use, and claims only its own
  ground; it grows more insistent only after the skill was seen not to
  load.
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
  Anything that may leave its owner's hands uses invented names.
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

## Questions to ask of a draft

- What decision does each idea improve, why does that matter where it is
  not obvious, and how would you know it worked? When you cannot tell, the
  idea is unclear or holds more than one; rewrite or split it.
- How far may the agent depart from each statement, and does its wording
  say so?
- Where an idea comes from a result that worked, does it keep the criterion
  that produced the result, or only the result's shape?
- Does it constrain a decision the agent could make well on its own? An
  owner's conventions are not such decisions; they stay, at the strength
  the owner gave them.
- If this fact changed, whose change would it be? It belongs at the
  narrowest scope where it stays true: the skill of the system that defines
  it, and the project itself for what varies by project, whose own
  conventions win.
- Where a mistake would be costly or cannot be undone, is the safeguard
  stated as a constraint?
- Before you finish, reread each list you wrote: if an agent following it
  would check its items and stop, put the principle first.

Before setting frontmatter or splitting a skill into files, check the
skill format's specification and the documentation of each harness that
will load it.

## Finding out whether it works

A skill is measured by transfer: whether it improves decisions in cases it
never names. Improvement only on the cases it describes does not show
that. Structure checks say nothing about this; cases kept outside the skill
do:

1. Write the request as a user would phrase it, not in the skill's words,
   and substantial enough that an agent would look for help. Include
   requests the skill never mentions, and a near-miss: one that sounds
   alike but where the skill should not apply, or should apply differently.
2. Test the skill the way it is used. Where what it produces guides later
   work, give that to a fresh agent doing the work, and judge the work. Run
   it on each agent that will load the skill; they differ.
3. Run the previous version and the new one in fresh sessions whose
   folders, files and prompt look like ordinary work. Judge the results
   against the outcomes the skill is meant to produce, written down apart
   from its wording, using checks written before the run that the sessions
   under test never see, and without knowing which version produced which.
4. A case the previous version already passes does not test the change.
   Results vary from one batch of sessions to the next, so trust only a
   difference that repeats in a separate batch.

When an agent missed what a skill says, find out why before changing it,
and fix that cause. More text fixes only guidance that was missing.
