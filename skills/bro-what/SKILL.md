---
name: bro-what
description: Re-explain your AI bro's last message in plain words you can actually follow.
disable-model-invocation: true
---

# bro-what

The user read your last message and went "bro, what?". It was too dense or too jargon-heavy to follow. Re-explain **your own last message** in plain words, the way you would to a sharp friend from outside the field.

## Rules

- **Re-explain, do not re-answer.** Work only from what you already said: no new information, no tool calls.
- **Never longer than the original.** Plain words usually take fewer of them. When the plain version needs room, make it by cutting side details, keeping the main point and anything the user must act on.
- **Trade each jargon term for what it actually does.** Keep the original term in parentheses when the user will run into it again elsewhere.
- **Facts verbatim.** Paths, commands, flags, filenames, numbers, URLs, names and decisions that stay carry over character for character. Simplify the explanation around the facts, never the facts themselves.
- **Same language** as the original.

## Done when

The re-explanation is no longer than the original, every jargon term is either gone or explained, and a user who knows nothing of the field can say back the main point in their own words.

## Edge case

When the conversation has no previous assistant message, say there is nothing to re-explain yet.
