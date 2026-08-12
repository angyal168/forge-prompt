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

## Part Of

This command is part of the [Logos Protocol](https://github.com/angyal168/logos-protocol) -- an open protocol for building an AI assistant that actually knows you.

## License

MIT

<!-- forge-related:v1 -->

## Related

This repo is one module. It handles sharpening the prompt before you send it; it does not compose itself into a working system -- that wiring is a separate job.

- **[The Creator Studio Skill Stack for Claude Code](https://andrewhangyal.gumroad.com/l/mcgdqpi?utm_source=github&utm_medium=readme&utm_campaign=forge-prompt)** -- a paid pack of Claude Code commands from the same author ($9+).
- [All tools, free and paid](https://tools.aingyal.com/?utm_source=github&utm_medium=readme&utm_campaign=forge-prompt) -- the full index.

Listed so you can find them if they are useful to you. Nothing here is required to use this repo, which stays free.

<!-- /forge-related:v1 -->
