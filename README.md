# smooth-coding-skills

[English](README.en.md)

偷懒skill大合集不定时更新中！喜欢的话可以给个⭐持续追踪哦~

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

两种常见方式：

1. 用户：手动下载某个 Skill，然后放到本地 Codex skills 目录。
2. AI 或 Agent 使用者：把本仓库里的某个 Skill 路径告诉 Agent，让 Agent 帮你安装。

## Skill: ZZ

### 描述

`ZZ` 是一个非常轻量的对齐型 Skill，它的作用是让 Agent 在开始实质工作前，**强制**让Agent先复述它对你输入内容的理解，并向你提问不确定的地方，对齐用户与Agent的认识，若对齐则正式开工。

其实主要是每次都打一遍“请重复对我内容的理解……”太累了，不如直接调用 `/ZZ` 吧！精心挑选26个字母最后一个字符 `Z` 保证这个skill一定排在所有skill的最后，做到从**想起到调用完成只需要三步：**

1. 输入“/”打开调用界面
2. 键盘方向键选择向上“↑”点击一次
3. 回车！

### 目录位置

仓库内路径：

```text
skills/zz
```

### 用户安装方式

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

放进去以后，重启 Codex，让它重新发现新 Skill。

项目内模式把目标路径改成 `<你的项目>/.codex/skills/zz` 即可。

### AI / Agent 安装方式

```text
请从 GitHub 仓库 bhadaljf/smooth-coding-skills 安装 skills/zz 这个 Codex skill
```

### 调用方式

```text
$zz
```

## 后续扩展

如果你想以后继续往这个仓库里加 Skill，建议保持这个格式：

```text
skills/<skill-name>
```
