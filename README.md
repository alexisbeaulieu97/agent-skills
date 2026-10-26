# agent-skills

My personal agent skills, one folder each under [.claude/skills](.claude/skills).

| Skill | Use |
| --- | --- |
| `apprentice` | A teaching session: I show how I do something, the agent records it in the skills |
| `checking-perspectives` | Tries a design others will use from each party's side, to find friction before it settles |
| `experimenting` | Decides a fork between approaches by trying it, with evidence instead of guesses |
| `maintaining-skills` | How to write and revise agent skills so they improve an agent's judgment |
| `personal-ui-preferences` | My UI and UX defaults, for designing, building or reviewing an interface |
| `shaping` | Shapes a plan: asks what I want, restates it, then shows me a reviewed design to react to |
| `writing-documentation` | Where each fact lives in a project's documents and how much detail it gets; glossaries as a reference |

## Where they load

- **On a machine**: `untaped dotfiles` links every skill into `~/.claude/skills` (Claude
  Code) and `~/.agents/skills` (Codex and other harnesses), from [dotfiles.yml](dotfiles.yml):

  ```sh
  untaped dotfiles subscribe git@github.com:alexisbeaulieu97/agent-skills.git
  untaped dotfiles enable skills
  untaped dotfiles apply
  ```

- **In a Claude Code Project** (cloud sessions): add this repository to the project; each
  thread loads the skills in `.claude/skills`.

## Add a skill

Create `.claude/skills/<name>/SKILL.md`, add it to the table above, commit. Machines get it
on their next `untaped dotfiles sync`; projects on their next thread.
