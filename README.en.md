# smooth-coding-skills

[中文](README.md)

A small lazy-skill collection, updated from time to time. If you like it, feel free to star the repository.

smooth-coding-skills is a repository for multiple Codex skills.

Each skill lives in its own folder and can be downloaded, installed, and invoked independently. You do not need to copy the entire repository into your local skills directory.

## Skill Index

- [ZZ](#skill-zz)

## Repository Layout

```text
skills/
  zz/
    SKILL.md
    agents/
      openai.yaml
```

## How To Use This Repository

Two common paths:

1. User: install a specific skill locally.
2. AI or Agent user: send the skill path to an Agent and let it install the target skill for you.

## Skill: ZZ

### Description

`ZZ` is a very lightweight alignment skill. Its job is to **force** the Agent to restate its understanding of your input before doing substantive work, and ask about uncertain parts so the user and the Agent stay aligned.

In practice, typing “please repeat your understanding of my request first...” every time gets tiring, so it is easier to just call `/ZZ`. The name intentionally uses the last letter of the alphabet so it stays at the end of the skill list, making it easy to invoke in **three steps**:

1. Type `/` to open the skill picker
2. Press the Up arrow twice
3. Hit Enter

### Path

Repository path:

```text
skills/zz
```

### User Install

Windows PowerShell:

```powershell
git clone --depth 1 --filter=blob:none --sparse https://github.com/bhadaljf/smooth-coding-skills.git
cd smooth-coding-skills
git sparse-checkout set skills/zz
New-Item -ItemType Directory -Force "$env:USERPROFILE\.codex\skills" | Out-Null
Copy-Item -Recurse -Force ".\skills\zz" "$env:USERPROFILE\.codex\skills\zz"
```

macOS/Linux:

```bash
git clone --depth 1 --filter=blob:none --sparse https://github.com/bhadaljf/smooth-coding-skills.git
cd smooth-coding-skills
git sparse-checkout set skills/zz
mkdir -p ~/.codex/skills
cp -R skills/zz ~/.codex/skills/zz
```

Restart Codex after installation.

For project-local mode, change the destination path to `<your-project>/.codex/skills/zz`.

### AI / Agent Install

```text
Please install the Codex skill at skills/zz from the GitHub repository bhadaljf/smooth-coding-skills
```

### Invocation

```text
$zz
```

## Future Expansion

If you keep adding skills to this repository, use:

```text
skills/<skill-name>
```
