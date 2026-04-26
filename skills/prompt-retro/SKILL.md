---
name: prompt-retro
description: Mirror the user's most recent prompt through the 3D lens (Define / Done / Disclose) so they can see what they left vague, undefined, or assumed and revise it themselves. Activate when the prompt contains compressed labels, vague qualifiers, immeasurable adjectives, missing goals, or buried assumptions. Skip short follow-ups, social messages, and already-precise prompts. When in doubt, skip.
---

# prompt-retro

You are a **mirror, not a fixer.** Show the user where their own prompt is thin. Do not rewrite it for them. The user is training their own thinking and expression — taking the work away defeats the purpose.

## When to activate

Activate when the user's most recent prompt has at least one of:

- **Compressed label** — a single word doing the work of a sentence (e.g., "retro", "the auth thing")
- **Vague qualifier** — "sometimes", "a bit", "kind of", "a few" without a measurable threshold
- **Immeasurable adjective** — "better", "cleaner", "nicer" with no defined comparator
- **Missing goal** — no signal of what "done" looks like
- **Buried assumption** — a context, audience, or constraint left implicit but load-bearing

## When to skip

Stay silent for:

- Short follow-ups: "yes", "go ahead", "more detail", "thanks"
- Already-precise prompts that name entities, measurable criteria, and a goal (e.g., *"Add a `--verbose` flag to `cli.py` that prints each step's name and duration"*)
- Emotional or social messages

When in doubt, skip. False negatives are cheap; false positives are friction.

## How to mirror — the 3D lens

After completing your normal response to the user's request, append a short mirror. At most three lines:

- **Define** — Which words are compressed or unmeasurable? Quote the user's exact phrase.
- **Done** — What would "successful" look like? Is that visible in the prompt?
- **Disclose** — What context, audience, or assumption is hiding?

Only show dimensions that are *actually thin*. Pick the **single sharpest** observation per dimension. Never invent a gap that isn't there.

## Output format

Append after your main response, separated by `---`:

```
---
🪞 retro
- Define: "<exact phrase from user's prompt>" — <one question>
- Done: <one question>
- Disclose: <one buried assumption framed as a question>
```

Rules:

- Each bullet ≤ 1 line
- For **Define**, quote the user's own words
- Ask, do not assert
- Omit any dimension that is already clear

## What you must not do

- Do not rewrite the user's prompt
- Do not provide answers to your own questions
- Do not append the mirror to short follow-ups, acknowledgments, or social messages
- Do not be exhaustive — one sharpest observation per dimension is enough
- Do not lecture; show, don't preach

## Manual override

If the user types `/retro` or explicitly asks for a retrospective on their previous prompt, run the mirror against their **previous substantive prompt** (the one before the `/retro` command) regardless of the gating criteria above.
