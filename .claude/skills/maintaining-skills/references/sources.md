# Sources

The guides the skill is distilled from, with the date each was last read and
what it contributed. A refresh reads each one again; a source that no longer
exists or has moved is replaced or dropped, and the date updated.

## Skill format and authoring

| Source | Last read | Contributed |
|---|---|---|
| [Agent Skills specification](https://agentskills.io/specification) | 2026-10-05 | Frontmatter fields and limits shared by the harnesses that load skills |
| Anthropic, [Skill authoring best practices](https://platform.claude.com/docs/en/agents-and-tools/agent-skills/best-practices) | 2026-10-05 | Third-person descriptions, progressive disclosure, references one level deep, contents list past 100 lines, freedom matched to fragility, testing with every model used |
| Anthropic, [Claude Code skills docs](https://code.claude.com/docs/en/skills) | 2026-10-05 | Descriptions in the user's words with the main use first, since the skill list is cut at 1,536 characters |
| Anthropic, [skill-creator](https://github.com/anthropics/skills/tree/main/skills/skill-creator) | 2026-10-05 | Reasons over MUSTs, tests with and without the skill, should-load and should-not-load queries for descriptions |
| Anthropic, [claude-api skill](https://github.com/anthropics/skills/tree/main/skills/claude-api), `shared/` docs | 2026-09 | Pointers that say when to read a reference, pitfalls sections, step structure |
| OpenAI, [skill-creator](https://github.com/openai/skills/blob/main/skills/.system/skill-creator/SKILL.md) | 2026-10-05 | "The context window is a public good"; scripts for fragile, deterministic steps |
| Matt Pocock, [writing-for-agents](https://github.com/mattpocock/skills/tree/main/skills/productivity/writing-for-agents) | 2026-10-05 | A skill that restates the environment is a cache; one trigger per meaning; the leading word first; positive targets; one term per concept |
| Cursor, [pstack](https://github.com/cursor/plugins/tree/main/pstack/skills) (blast-radius, architect, figure-it-out) | 2026-09 | Defined deliverables; "nothing to change" as a valid result |

## Prompting the models that read skills

| Source | Last read | Contributed |
|---|---|---|
| Anthropic, [Prompting best practices](https://platform.claude.com/docs/en/build-with-claude/prompt-engineering/claude-prompting-best-practices) | 2026-09-30 | Emphatic language makes recent Claude models over-apply rules; give the reason; say what to do rather than what not to do |
| OpenAI, [Prompt guidance for the current GPT model](https://developers.openai.com/api/docs/guides/prompt-guidance) | 2026-09-30 | Outcome-first, shorter instructions; absolute rules only for true invariants; explicit stopping conditions |

## Harness behaviour

| Source | Last read | Contributed |
|---|---|---|
| GitHub Copilot CLI issues [#4438](https://github.com/github/copilot-cli/issues/4438) and [#4637](https://github.com/github/copilot-cli/issues/4637) | 2026-09-30 | `disable-model-invocation: true` hides the skill from the model entirely; drop the note from the skill once both are fixed |
