# bro-skills

Each agent skill lives in `skills/<name>/SKILL.md`.

## Conventions

- Names start with `bro-`. The word after the prefix names what the skill does: e.g. `what` for clarity, `shorter` for length.
- `bro-what` and `bro-shorter` are user-invoked: `disable-model-invocation: true` in the `SKILL.md` frontmatter and `policy.allow_implicit_invocation: false` in `agents/openai.yaml`. Whenever a skill is user-invoked, the two flags stay in sync. A model-invoked skill carries neither, and its `description` is written for the model, with the trigger phrasing that fires it.
- A user-invoked `description` is written for a human scanning a slash-command list. One plain line, no "use when the user mentions..." trigger phrasing.
- Every skill carries `agents/openai.yaml` beside its `SKILL.md`, with `interface.display_name` and `interface.short_description` for the Codex picker.
- Every skill needs an entry in the `skills` array of `.claude-plugin/plugin.json`. Bump `version` there on release.
- List every new skill in the `README.md` table with a one-line "use it when".
