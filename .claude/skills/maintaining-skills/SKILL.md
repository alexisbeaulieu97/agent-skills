---
name: maintaining-skills
description: How to write, revise and test agent skills (SKILL.md files and their references) so agents use them well, and keep what they produced in line with them. Use when creating or editing a skill, tuning a skill's description, deciding what belongs in a skill or where, or checking whether a skill change improved behaviour.
---

# Maintaining skills

A skill earns its place by changing what an agent does, at the lowest cost
in context: its description is read in every session, its body in every
session that loads it. Write what the agent cannot know or find out, so that
it decides well in cases the skill never names.

## What goes in

Teach how to think rather than what to match. Open with the one principle
the skill's judgments serve; an agent that knows what is being optimized can
decide the cases the skill leaves out. Then give:

- what a good result looks like, stated so it can be checked;
- the constraints that protect shared systems and anything irreversible:
  preview first, say what selects the objects an action touches, how to
  recover, and wait for the user's approval;
- the reason behind an idea when it changes how the idea applies at the
  edges; an idea that is clear on its face needs none.

Each idea stands on its own, narrow enough that why it is there and how to
test it are plain from the text. When they are not, the idea is unclear or
holds more than one; rewrite or split it before changing what it says.

Leave out what the agent does well by default, and what it can find by
looking: a tool's `--help`, a config file, the live system. A skill that
restates them is a cache that goes stale; say where to look instead, and let
the live system win when the two disagree. Say nothing twice.

Before writing a rule, ask whether something could enforce it instead: a
check, a template field, a permission, a script. Work whose output is fully
determined by its input and recurs belongs in a script the skill runs.

Be exact only where deviation breaks something; elsewhere describe the
result and leave the method to the agent.

## How it reads

- Phrase instructions as what to do. Add a prohibition only after an agent
  actually did the wrong thing, and only if it would help most sessions;
  actions that cannot be undone get their safeguard from the start. The
  incident behind a rule goes in the commit message, not the skill.
- Write calmly. Capitals and "CRITICAL" make current models apply a rule
  too broadly; a reason works better than emphasis.
- A list of cases gets matched: an agent checks its items and stops. Lead
  with the principle that produces them and present the cases as
  illustrations; a complete list, such as the steps of a procedure, stays a
  list. When options must be listed, give each the situation it fits and
  the one where it does not. Before you finish, reread each list you wrote:
  if an agent following it would check its items and stop, put the
  principle first.
- Examples are several, varied in the ways that matter, and labelled as
  illustrations. Anything that may leave its owner's hands uses invented
  names.
- Choose each word for how an agent will act on it. A "rule" is obeyed
  and an "idea" weighed; "must" binds where "prefer" leaves room. Give
  each idea the strength it needs, no more.
- One term per concept, kept throughout. State current behaviour, not the
  history of how it came to be.
- Give order only where results depend on each other, and end each step on
  something checkable.

## Shape and routing

- **Description.** The only part always loaded, so it routes rather than
  instructs: third person, what the skill covers, then the intents that
  should load it, one per distinct meaning, in words a user would say, with
  the main use first. It shares the context with every other skill's
  description, so it claims only its own ground; make it more insistent
  only after the skill was seen not to load. Aim for under 60 words (hard
  limit 1024 characters).
- **Name.** Lowercase letters, digits and hyphens, at most 64 characters,
  matching the directory; "claude" and "anthropic" are reserved.
- **Body.** SKILL.md holds what every use needs. What only some uses reach
  goes in `references/`, one level deep, each pointer saying when to read
  it ("read references/x.md when ..."); a reference past about 100 lines
  opens with a list of its contents. Keep SKILL.md well under 500 lines.
- **Invocation.** Set `disable-model-invocation: true` only on a process
  the user starts. Some harnesses (Copilot CLI) then hide the skill from the
  model entirely, so a skill that other skills load stays model-invocable.
- **Placement.** Each fact lives in the skill of the system that defines it
  (if it changed, whose change would it be?). Write each skill as if no
  other existed: never restate or name another skill; say what to do
  ("update the relevant skills") and let the agent load what applies. A
  general skill holds no domain's specifics. What varies from one project
  to the next is best stated in the project itself (a template, a
  contributing guide, a check), with the skill saying the project's own
  rules win.

## Testing

Structure checks (frontmatter, size, links) say nothing about behaviour.
Behaviour is tested with cases, kept outside the skill so they never ship
with it:

1. Write the request as a user would phrase it, not in the skill's words:
   a request that echoes the skill measures reading, not understanding.
   Make it substantial enough that an agent would look for help; a simple
   one loads no skill whatever the description says. Name the skills that should and should not load, and write a few yes/no
   criteria before running anything.
2. Pair it with a near-miss: a request that sounds alike but where the
   skill should not apply, or should apply differently.
3. Run it in a fresh session, once with the previous version of the skills
   and once with the new one, and compare the two plans without knowing
   which is which, each judged on what it would actually do. A plan is
   usually enough to show the behaviour and costs far less than a full run.
   Keep the test hidden from the session under test: its folders, files
   and prompt look like ordinary work, with no word that suggests a test.
4. A case the previous version already passes does not test the change.
   Trust only differences that repeat.

When a skill changes, what it already produced may no longer match it:
skills written to the old rules, an interface built to an old preference.
Find what you can reach and offer to bring it in line.
