# create-pr-with-evidence

A reusable agent skill that prepares and creates a pull request with evidence that reviewers can verify.

## What it does

- Records the exact `base...head` range and separates stacked changes from the PR's own changes.
- Writes a PR body that matches the scope: summary, change map, diagrams, risks, and verification.
- Adds `Before` and `After` diagrams for a fix that changes a flow or a state model.
- Maps each high-risk invariant to a test, a check, or a named gap.
- Captures before/after screenshots for UI changes and uploads them as GitHub user assets.
- Follows up on review threads and check status after the PR is open.

Repository instructions and PR templates take priority over the skill.

## When to use it

Use it when you ask an agent to open, create, publish, or prepare a PR from the current branch.

Do not use it to review another person's PR.

## Requirements

- `git` and the `gh` CLI, or another GitHub workflow that the agent can use.
- For UI changes: a screenshot tool, and a way to upload GitHub user assets, for example an `upload-github-attachment` skill.

## Installation

```bash
npx skills add luoling8192/create-pr-with-evidence-skill
```

Or copy this directory to `~/.claude/skills/create-pr-with-evidence` or `~/.agents/skills/create-pr-with-evidence`.

## Credits

This skill comes from the [`create-pr` skill](https://github.com/moeru-ai/airi/tree/main/.agents/skills/create-pr) of [Project AIRI](https://github.com/moeru-ai/airi). [@nekomeowww](https://github.com/nekomeowww) wrote the original version, and [@luoling8192](https://github.com/luoling8192) extended it.

This repository removes the AIRI-specific parts, such as the Vishot screenshot workflow, so that the skill works in any repository.

## License

MIT
