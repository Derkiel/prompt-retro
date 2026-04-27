# prompt-retro

A Claude Code skill that mirrors your own prompts back to you — so you notice what you left vague, undefined, or assumed.

It does not rewrite your prompt for you. It shows you the gap and lets you close it. The point is to train your own thinking and expression, not to make the model work harder around you.

## The 3D lens

Every prompt is mirrored against three questions:

- **Define** — Which words are compressed or unmeasurable?
- **Done** — What would "successful" look like?
- **Disclose** — What context or assumption is hiding?

That's it. No taxonomy of mistakes, no scoring, no fixing.

## When it activates

The skill is **always on** but **mostly silent**. Most prompts pass through untouched — short follow-ups, already-precise asks, social messages. It only mirrors when it sees compressed labels, vague qualifiers, immeasurable adjectives, or a missing goal.

When in doubt, it skips. (False negatives are cheap; false positives are friction.)

You can also call it manually with `/retro` to mirror your previous prompt regardless.

## Install

This repo is a Claude Code marketplace containing a single plugin (also called `prompt-retro`).

**Add the marketplace, then install:**

```bash
claude plugin marketplace add Derkiel/prompt-retro
claude plugin install prompt-retro@prompt-retro
```

Or in a Claude Code session:

```
/plugin marketplace add Derkiel/prompt-retro
/plugin install prompt-retro@prompt-retro
```

Restart your Claude Code session after install so the new skill is registered.

**Verify:**

```bash
claude plugin list
# should show: prompt-retro@prompt-retro  enabled
```

## Why it exists

Most "prompt improver" tools polish your prompt for you. That makes the model's life easier and yours harder over time — you don't grow.

`prompt-retro` does the opposite: it shows the seam and asks you to close it. Over many sessions, you start writing tighter prompts before you hit "send."

See [EXAMPLES.md](EXAMPLES.md) for what the mirror looks like in practice.

## License

MIT — see [LICENSE](LICENSE).
