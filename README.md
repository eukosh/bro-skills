<div align="center">

# 🤙 bro-skills

**Your agent rambled. These make it say it again like your bro would, short and plain.**

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Format: Agent Skills](https://img.shields.io/badge/format-Agent%20Skills-blue)](https://agentskills.io)

</div>

---

## What is this?

Your agent just answered your question. Thoroughly. In eleven paragraphs of words nobody has ever said out loud. You read it several times and still can't grasp the point.

Time for a bro skill. Two of them so far:

| | |
|---|---|
| [**`bro-what`**](skills/bro-what/SKILL.md) | Too dense, too jargony. Say it again in plain words, and no longer than before. |
| [**`bro-shorter`**](skills/bro-shorter/SKILL.md) | I don't have the whole day to read this wall of text. Say it again, I have things to do today. |

`bro-what` re-explains it in plain words and never comes back longer than the original.
`bro-shorter` cuts it to the gist in one to three sentences and keeps the specifics that matter.

## The fine print

They only re-say. Nothing new gets answered, nothing gets looked up, no tool gets called, so a wrong answer comes back wrong in plainer language.

`bro-shorter` drops anything that wouldn't change your next move. If you need every detail, the original is still right above it.

## Install

Any agent that reads the [Agent Skills](https://agentskills.io) format:

```bash
npx skills add eukosh/bro-skills -g -y -a universal -a claude-code -s '*'
```

On Claude Code there's also a plugin. It installs as one read-only bundle you subscribe to, rather than files you own and edit:

```bash
claude plugin marketplace add eukosh/bro-skills
claude plugin install bro-skills@eukosh
```

Pick one route or the other.

Then restart your session and type `/bro-what` or `/bro-shorter` after any reply that made your eyes glaze over.

## The family

More `bro-` skills will follow. The word after it says what the skill does: `what` for clarity, `shorter` for length. Conventions live in [AGENTS.md](AGENTS.md).

## License

[MIT](LICENSE)
