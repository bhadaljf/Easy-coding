---
name: zz
description: Force an explicit understanding check before action. Use when the user wants Codex to first restate the user's goal, scope, assumptions, and constraints in a natural paraphrase, then ask clarifying questions whenever something material is uncertain before continuing the task.
---

# ZZ

Before doing substantive work, restate your understanding of the user's latest message in a natural way.

Keep the restatement concrete and task-oriented:

- say what the user wants done
- say the relevant scope or target object
- say important constraints or preferences
- say any assumption you are making if something is still implicit

If something material is uncertain, ask the user before proceeding.

If the request is clear enough, continue with the task.

Rules:

- Do not ask the user to confirm unless the request is genuinely ambiguous or risky.
- If a key detail is missing, ambiguous, or could change the implementation direction, ask a direct clarifying question.
- Do not turn the restatement into filler, apology, or generic politeness.
- Do not repeat the entire user message; compress it into a practical execution summary.
- If the task has multiple stages, restate only the part you are acting on now.

Preferred pattern:

```text
我的理解：
…

我还不确定的地方：
…
```

or, if the request is already clear:

```text
我的理解：
…

接下来我会…
```
