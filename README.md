# smooth-coding-skills

<a id="zh"></a>

[中文](#zh) | [English](#en)

smooth-coding-skills 是一个用于存放多个 Codex Skill 的仓库。

每个 Skill 都是独立目录，可以单独下载、单独安装、单独调用，不需要把整个仓库一起塞进本地技能目录。

## Skill 目录

- [ZZ](#skill-zz)

## 仓库结构

```text
skills/
  zz/
    SKILL.md
    agents/
      openai.yaml
```

## 如何使用这个仓库

你有两种常见方式：

1. 作为用户，手动下载某个 Skill，然后放到本地 Codex skills 目录。
2. 作为 AI 或 Agent 使用者，把本仓库里的某个 Skill 路径告诉 Agent，让 Agent 帮你安装。

同一个 README 里可以通过锚点上下跳转，所以点上面的 Skill 目录会直接滚动到对应介绍位置。

<a id="skill-zz"></a>

## Skill: ZZ

### 描述

`ZZ` 是一个非常轻量的对齐型 Skill。

它的作用是让 Agent 在开始实质工作前，先复述它对你输入内容的理解，并在关键点不确定时先向你提问，而不是直接猜。

适合场景：

- 你给的是比较抽象的要求，担心 Agent 理解偏了
- 你想让 Agent 先说清楚目标、范围、限制、假设
- 你希望 Agent 在不确定时先问，而不是直接开做

### Skill 标题

Skill 内部标题仍然是 `ZZ`。  
仓库名是 `smooth-coding-skills`，只是为了方便集中管理多个 Skill。

### 目录位置

仓库内路径：

```text
skills/zz
```

### 用户安装方式

适合不想折腾命令、想手动管理文件的人。

做法：

1. 打开本仓库页面。
2. 下载仓库压缩包，或者只取出 `skills/zz` 目录。
3. 把 `zz` 整个文件夹放到你的 Codex skills 目录里。

常见安装位置：

- Windows: `%USERPROFILE%\\.codex\\skills\\zz`
- macOS/Linux: `~/.codex/skills/zz`
- 项目内模式: `<你的项目>/.codex/skills/zz`

放进去以后，重启 Codex，让它重新发现新 Skill。

### AI / Agent 安装方式

适合你直接把仓库链接或 Skill 路径发给 Agent，让 Agent 帮你装。

你可以直接对 Agent 这样说：

```text
请从 GitHub 仓库 bhadaljf/smooth-coding-skills 安装 skills/zz 这个 Codex skill
```

或者这样说：

```text
用 $skill-installer 从 bhadaljf/smooth-coding-skills 安装 skills/zz
```

也可以直接发仓库网址并补一句：

```text
这是我的 skills 仓库：https://github.com/bhadaljf/smooth-coding-skills
请帮我安装其中的 skills/zz
```

如果 Agent 走的是 GitHub 路径安装逻辑，核心目标就是让它安装：

```text
repo: bhadaljf/smooth-coding-skills
path: skills/zz
```

### 调用方式

安装完成后，可以直接这样调用：

```text
$zz
```

### 行为说明

这个 Skill 会要求 Agent：

1. 先自然复述它对你需求的理解
2. 主动说出目标、范围、限制和假设
3. 遇到会影响实现方向的不确定点时，先提问
4. 在需求已经足够清楚时，直接继续执行

### 后续扩展建议

如果你以后继续往这个仓库里加 Skill，建议保持这个格式：

```text
skills/<skill-name>
```

然后在本 README 的“Skill 目录”里新增条目，并给每个 Skill 都补上：

- 描述
- 仓库内路径
- 用户安装方式
- AI / Agent 安装方式
- 调用方式

<details>
<summary>English</summary>

<a id="en"></a>

smooth-coding-skills is a multi-skill repository for Codex.

Each skill lives in its own folder and can be installed independently. Users do not need to copy the whole repository into their local skills directory.

## Skill Index

- [ZZ](#skill-zz-en)

## Repository Layout

```text
skills/
  zz/
    SKILL.md
    agents/
      openai.yaml
```

## How To Use This Repository

There are two common ways to use this repo:

1. As a user, manually download one skill and place it into your local Codex skills directory.
2. As an AI or Agent user, send the repository link and the skill path to the Agent and ask it to install that specific skill.

This README uses same-page anchor links, so clicking a skill name in the index will jump to that section in the same file.

<a id="skill-zz-en"></a>

## Skill: ZZ

### Description

`ZZ` is a minimal alignment-oriented skill.

It tells the Agent to restate its understanding before doing substantive work, and to ask clarifying questions when key details are still uncertain instead of guessing.

Good use cases:

- you want the Agent to restate intent before implementation
- you want scope, constraints, and assumptions surfaced early
- you want the Agent to ask before acting when something important is unclear

### Skill Title

The skill title remains `ZZ`.  
The repository name `smooth-coding-skills` is only for organizing multiple skills in one place.

### Path In This Repository

```text
skills/zz
```

### Install As A User

This is the manual path for users who prefer direct file management.

Steps:

1. Open this repository.
2. Download the repository archive, or extract only `skills/zz`.
3. Place the whole `zz` folder into your Codex skills directory.

Common install locations:

- Windows: `%USERPROFILE%\\.codex\\skills\\zz`
- macOS/Linux: `~/.codex/skills/zz`
- project-local mode: `<your-project>/.codex/skills/zz`

After copying the folder, restart Codex so it can discover the new skill.

### Install Through An AI / Agent

This is the best path when you want another Agent to install it for you.

You can tell the Agent:

```text
Please install the Codex skill at skills/zz from the GitHub repository bhadaljf/smooth-coding-skills
```

Or:

```text
Use $skill-installer to install skills/zz from bhadaljf/smooth-coding-skills
```

Or send the repository URL directly:

```text
This is my skills repository: https://github.com/bhadaljf/smooth-coding-skills
Please install skills/zz from it
```

The important install target is:

```text
repo: bhadaljf/smooth-coding-skills
path: skills/zz
```

### Invocation

After installation, invoke it with:

```text
$zz
```

### Behavior

This skill tells the Agent to:

1. restate its understanding naturally
2. surface goal, scope, constraints, and assumptions
3. ask direct questions when uncertainty could change the implementation path
4. continue immediately when the request is already clear enough

</details>
