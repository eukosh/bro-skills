---
name: bro-shorter
description: Cut your AI bro's last message down to its core in a few sentences.
disable-model-invocation: true
---

# bro-shorter

The user looked at your last message, saw a wall of text, and wants the **gist**. Rewrite **your own last message** as one to three sentences that carry what actually matters.

## What survives

Rank everything in the original by one question: does it change what the user knows or does next? Keep from the top until three sentences are full; the rest goes.

Usually at the top:

- The outcome: what is now true, fixed, decided, found, or still broken.
- What the user must do or decide, if anything.
- A risk or caveat that would change their next move.
- The one or two specifics that make it concrete: the name, number, path, or command.

Usually cut: process narration, reasoning, rejected alternatives, background the user already has, minor caveats, recaps, and politeness.

## How it reads

- **Specific, never generic.** A sentence that only says what happened is a useless summary; name the actual result. "Fixed the login bug" says nothing. "Login broke on uppercase emails; `normalizeEmail` now lowercases them, tests pass" is the gist.
- **Sequences as arrows.** A chain of steps collapses to `fetch → dedupe → write to S3`, one arrow per step, no sentence per step.
- **Facts verbatim.** Paths, commands, flags, filenames, numbers, and URLs that make the cut carry over character for character.
- **Compress, do not re-answer.** Work only from what you already said: no new information, no tool calls.
- **Same language** as the original.

## Done when

The reply is at most three sentences, every sentence names something specific, and a user who reads only this knows the outcome and their next move.

## Edge case

When the conversation has no previous assistant message, say there is nothing to shorten yet.
