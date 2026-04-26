# Examples

Each example shows an original prompt, the mirror's response, and one possible revision. The mirror only fires on prompts where it has something useful to say — most prompts pass through silently.

---

## Example 1 — compressed label

**Original prompt**:

> My idea is `retro`. Search GitHub for similar topics.

**Mirror**:

```
---
🪞 retro
- Define: "retro" — retrospective, retro-style/throwback, or both?
- Disclose: which "similar"? same topic, same form, or same audience?
```

**Possible revision**:

> My idea is a *prompt retrospective* skill — let users review their own prompts. Search GitHub for skills with this exact theme.

---

## Example 2 — vague qualifier + immeasurable adjective

**Original prompt**:

> Make this code a bit cleaner sometimes when you see issues.

**Mirror**:

```
---
🪞 retro
- Define: "a bit cleaner" — by what measure? readability, fewer lines, fewer branches?
- Define: "sometimes when you see issues" — every PR, on demand, or only flagged ones?
- Done: what would I notice as different in the diff?
```

**Possible revision**:

> When I open a PR, run a readability pass: flag functions over 30 lines or with cyclomatic complexity above 8. Suggest renames and splits.

---

## Example 3 — no stated goal

**Original prompt**:

> Look at this file and tell me what you think.

**Mirror**:

```
---
🪞 retro
- Done: what should I be checking — bugs, design, naming, performance?
- Disclose: who's the audience for the answer — me reviewing, you learning, or a teammate getting handed this?
```

**Possible revision**:

> Review this file for naming and structure issues. I'm teaching it to a junior next week and want to flag confusing parts ahead of time.

---

## When the mirror stays silent

Prompts that already carry their goal, audience, and measure pass through untouched:

- *"Add a `--verbose` flag to `cli.py` that prints each step's name and duration."* → silent
- *"Write a one-paragraph release note covering the three commits since v0.4."* → silent
- *"Yes, go ahead."* → silent (follow-up)
- *"Thanks!"* → silent (social)

The skill is designed to be quiet most of the time. If it never fires on you, that's fine — your prompts are already doing the work.

## On reading the mirror

The mirror is a question, not a verdict. You decide whether the question is worth answering. Sometimes the right answer is *"that's intentionally loose, move on"* — and that's a valid thing to learn about your own prompts too.
