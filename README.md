# ZZ

`ZZ` is a minimal Codex skill that forces an explicit understanding check before action.

When the skill is invoked, the agent should:

- restate its understanding of the user's request in a natural way
- surface scope, constraints, and assumptions
- ask clarifying questions before proceeding if any material detail is uncertain
- continue immediately when the request is clear enough

The goal is simple: reduce drift before the agent starts doing work.

## Repository Layout

```text
zz/
  SKILL.md
  agents/
    openai.yaml
```

## Install

Copy the `zz` folder into your Codex skills directory:

- Windows: `%USERPROFILE%\\.codex\\skills\\zz`
- macOS/Linux: `~/.codex/skills/zz`

Or, if you already manage skills inside a project, place the folder under that project's `.codex/skills/`.

## Use

Invoke the skill with:

```text
$zz
```

Typical use cases:

- you want the agent to restate your intent before implementation
- you want assumptions and constraints surfaced early
- you want the agent to ask when something important is unclear instead of guessing

## Behavior

The skill keeps the instruction surface intentionally small.

It tells the agent to:

1. restate the user's goal, scope, constraints, and assumptions
2. ask direct clarifying questions when missing details could change the approach
3. avoid filler, generic politeness, and copying the user verbatim
4. proceed when the request is clear enough

## Skill Title vs Repository Name

The repository uses a descriptive name for discoverability, while the skill display title remains `ZZ`.
