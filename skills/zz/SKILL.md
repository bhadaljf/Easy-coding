---
name: zz
description: Force a gated alignment-only first response before action. Use when the user wants Codex to spend the current reply only on restating the user's goal, scope, assumptions, and uncertainties, then ask whether the understanding is correct before starting work in the next reply.
---

# ZZ

Before doing any substantive work, your response for this invocation must only contain:

1. your understanding summary of the user's latest message
2. any material uncertainties or clarifying questions
3. a final question asking whether the understanding matches the user's intent

Do not include analysis, planning, tool use, implementation, or execution in this response.

This alignment-only response is mandatory on every invocation of this skill.

Start with the exact heading:

```text
我的理解：
```

Then restate your understanding in a natural way.

Keep the restatement concrete and task-oriented:

- say what the user wants done
- say the relevant scope or target object
- say important constraints or preferences
- say any assumption you are making if something is still implicit

If something material is uncertain, ask the user before proceeding.

Even if the request looks clear, still ask whether the understanding matches before starting work.

Rules:

- Always output `我的理解：` before anything else.
- This response must only contain restatement, uncertainties, and the final confirmation question.
- If a key detail is missing, ambiguous, or could change the implementation direction, ask a direct clarifying question.
- Do not turn the restatement into filler, apology, or generic politeness.
- Do not repeat the entire user message; compress it into a practical execution summary.
- If the task has multiple stages, restate only the part you are acting on now.
- Do not skip the understanding summary even when the task looks obvious or trivial.
- Do not include `接下来我会…` or any equivalent implementation preview in this response.
- Do not use tools or start implementation until the user confirms that the understanding is correct.

Preferred pattern:

```text
我的理解：
…

我还不确定的地方：
…

如果以上理解符合你的意思，我再开始处理，可以吗？
```

or, if there are no material uncertainties:

```text
我的理解：
…

如果以上理解符合你的意思，我再开始处理，可以吗？
```
