# Maintaining this repository

Personal agent skills, read by several harnesses. Read [README.md](README.md) first.

- A skill is a folder under `.claude/skills` with a `SKILL.md`, and may hold a
  `principles.md`: the outcomes the owner intends it to produce. Nothing else belongs in
  this repository. `.claude/skills` holds the only copy: other locations are links.
- Skills are harness-neutral: no instruction that only one harness can follow, unless the
  skill says which harness it is for.
- Treat the repository as public: no secrets, no personal data beyond the owner's first
  name, nothing naming an employer or its systems. Work skills live in the work repository.
- One change per commit, with a message that says why.

## Testing a skill change

Judge a change against the skill's `principles.md`, with checks written for that test and
shown only to the judge, who is not told which version produced which result. Run the
sessions under test on a copy of the repository, where no other copy of these skills
loads (such as the links in `~/.claude/skills`).
