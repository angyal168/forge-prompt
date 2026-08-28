# /forge-prompt -- Prompt Coaching for Claude Code

> Turn vague requests into action-first prompts that get results.

Paste a draft prompt. Get it rated 1-5 flames, sharpened with targeted questions, and rewritten into action-first form. Teaches better prompting by doing.

## Install

```bash
mkdir -p ~/.claude/commands
cp forge-prompt.md ~/.claude/commands/
```

Then type `/forge-prompt` in any Claude Code session and paste your draft.

## How It Works

1. **Rate** your prompt (1-5 flames)
2. **Sharpen** with 1-3 targeted questions if under 4 flames
3. **Rewrite** into action-first form (before/after comparison)
4. **Fire** the rewritten prompt immediately if you approve

## Good Prompt DNA

- Action-first (starts with the verb)
- Dense context (file paths, project names, current state)
- One task per prompt
- No fluff ("please", "could you maybe", "I was thinking perhaps")
- States energy/intent ("tired tonight", "quick win", "sharp and ready")


<!-- forge-usage:v1 -->

## What it actually does

`/forge-prompt` is a coach, not a rewriter. You hand it a rough prompt; it rates the prompt
1–5 flames, asks 1–3 sharpening questions if it scored under 4, rewrites it in action-first
form so you can see the before and after, then asks whether to fire it. If you say fire, it
runs the rewritten prompt immediately.

The rating scale is blunt on purpose:

| Flames | Meaning |
|---|---|
| 1 | Vague. No action, no context. |
| 2 | An idea buried in fluff. Needs excavation. |
| 3 | Decent direction, missing specifics — file paths, current state, desired outcome. |
| 4 | Strong. Action-first with context. Minor tightening. |
| 5 | Ship it. |

## The prompt DNA it coaches toward

Seven traits, from the command file itself: **action-first** (start with the verb),
**dense context** (real file paths and project names), **one task per prompt**, **no fluff**
(no "could you maybe"), **stream-of-consciousness is fine** (raw voice-to-text is welcome —
the thread matters, not the grammar), **trusts the system** (do not re-explain what your
assistant already knows), and **states energy** ("tired tonight", "quick win") because that
legitimately changes what should be suggested.

Strong, in its own examples: *"Fix the video template — source content needs to be 60-70% of
frame. It's too small right now."*
Weak: *"Can you help me with the video project?"* and *"Please review the codebase and let me
know what you think"* — no verb, no target, no outcome.

## The point is that it stops

The command tells the coach to be *encouraging but honest* — "that's a 2, let's sharpen it,"
not "great start!" — and states the actual goal plainly: after 5–10 rounds you should have
internalised the pattern and stopped needing it. A coaching tool that is designed to become
unnecessary is being honest about what it is.

## Usage

```bash
mkdir -p ~/.claude/commands
cp forge-prompt.md ~/.claude/commands/
```

```
/forge-prompt
i want to do something about the newsletter thing maybe clean it up
```

Expect to be asked what outcome you want, which file or project this is, and what you
already tried — then to get that back as one prompt worth firing.

## When not to use it

- When your prompt is already specific. A 5-flame prompt does not need a round trip.
- In the middle of a long working session where the extra turn costs more than the sharper
  prompt saves.
- For conversation rather than tasks — this coaches instructions, not discussion.

## Requirements

Claude Code with a `~/.claude/commands/` directory. No dependencies, no configuration.

<!-- /forge-usage:v1 -->


<!-- forge-siblings:v1 -->

## More from the same author

Other free, open-source Claude Code tools in this family. Each one stands
alone -- none of them depend on this repo, or on each other.

- [smelt](https://github.com/angyal168/smelt) -- Extract actionable insights from any resource -- burn off the slag, keep the pure metal
- [dar](https://github.com/angyal168/dar) -- Lightweight audit trail for Claude Code -- Discovery, Artifact, Receipt
- [ralph](https://github.com/angyal168/ralph) -- Autonomous iteration loop for Claude Code -- define task, set condition, let it run
- [serious](https://github.com/angyal168/serious) -- Precision mode for Claude Code -- no hype, no ambiguity, only what's true
- [council](https://github.com/angyal168/council) -- AI advisory board for Claude Code -- 6 executive perspectives debate any decision
- [rally](https://github.com/angyal168/rally) -- Multi-agent coordination for Claude Code -- keep parallel agents in sync through a shared bus file
- [ouroboros](https://github.com/angyal168/ouroboros) -- Stop prompting. Start specifying
- [logos-protocol](https://github.com/angyal168/logos-protocol) -- Forge an AI that knows you, remembers, and ascends. Open source, free, yours to imprint

<!-- /forge-siblings:v1 -->

## Part Of

This command is part of the [Logos Protocol](https://github.com/angyal168/logos-protocol) -- an open protocol for building an AI assistant that actually knows you.

## License

MIT

<!-- forge-related:v1 -->

## Related

This repo is one module. It handles sharpening the prompt before you send it; it does not compose itself into a working system -- that wiring is a separate job.

- **[The Creator Studio Skill Stack for Claude Code](https://notes.aingyal.com/go/gh-forge-prompt/mcgdqpi/)** -- a paid pack of Claude Code commands from the same author ($9+).
- [All tools, free and paid](https://tools.aingyal.com/?utm_source=github&utm_medium=readme&utm_campaign=forge-prompt) -- the full index.

Listed so you can find them if they are useful to you. Nothing here is required to use this repo, which stays free.

<!-- /forge-related:v1 -->
