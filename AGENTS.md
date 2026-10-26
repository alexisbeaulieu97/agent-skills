# Maintaining this repository

The user's personal agent skills, read by several harnesses. Read [README.md](README.md)
first for what each skill is for and where the skills load. How to write or revise a skill
is in [maintaining-skills](.claude/skills/maintaining-skills/SKILL.md): read it before
changing one. The user owns every skill here, so where maintaining-skills speaks of the owner,
it means the user.

## Writing skills here

- The user uses these skills in all their work, not only software. So the contexts a
  skill's job covers are every kind of work where that job comes up.
- What these skills say is the user's judgment. Change what a skill means only from the
  user's own words, what they showed, or wording they confirmed; an answer another agent
  gave on their behalf is not their judgment.
- Skills are harness-neutral: no instruction that only one harness can follow, unless the
  skill says which harness it is for.
- A skill the user starts themselves, such as a session they lead, sets
  `disable-model-invocation: true`.
- A skill calls the person it works for "the user".

## Layout

Besides the files that describe and install it, the repository holds only skills: each is
a folder under `.claude/skills` with a `SKILL.md` and the files it points to. That folder
holds the only copy; every other location is a link to it. When a skill is renamed or
removed, or what it is used for changes, update its row in README's table.

## Changes

- The repository is public: no secrets, no personal data beyond the user's first name,
  nothing naming an employer or its systems. Work skills live in the work repository.
- Put your changes on a branch and open a pull request for the user to review; never push
  to `main`.
- One change per commit, its message saying why. A signal that maintaining-skills leaves
  with the owner goes in that commit's message.
