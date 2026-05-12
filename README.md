# Jump in Coding

A Codex skill that is triggered automatically by default and makes AI explain the programming, technical, and engineering concepts it uses while helping with coding tasks. It can also be invoked manually when needed.

## What It Does

- When a task involves something like a cache, TTL, retry logic, queue, state management, authentication, or middleware, it explains the concept at a depth that matches the user's apparent technical level.
- When AI interprets errors, logs, or test results, it names the technical category behind the issue.
- When AI makes an implementation tradeoff, it explains the relevant engineering concept instead of only giving the answer.
- It keeps the coding task first and keeps explanations concise and grounded in the current code.
- If the user appears familiar with a concept, it avoids basic explanations. If the user appears newer to the topic or stack, it adds more context.

## How It Triggers

This skill is mainly used as an automatic enhancement layer. After it is enabled, users can ask normal coding questions or development tasks, and the AI will explain relevant concepts at a depth calibrated to the user's apparent technical level. It can also be invoked manually, for example with `$jump-in-coding`.

## Files

```text
.
├── SKILL.md            # Main skill instructions
└── agents/openai.yaml  # Display name, short description, and default prompt
```

## Style

Use the user's language by default. Explanations should not take over the response or turn every step into a lesson. Adjust explanation depth to the user's apparent familiarity; when uncertain, start brief and let the user ask for more.

The skill itself should not be rewritten every time a user's level changes. Instead, explanation depth should adapt through conversation context or memory-like preferences. As the user becomes familiar with a topic, basic explanations should naturally fade; when they move into a less familiar stack, more context can return.

## 中文说明

一个以自动触发为主的 Codex skill，也可以手动调用。它会在 AI 帮你写代码、调试、评审或解释问题时，根据使用者的技术水平，顺手说明当前用到的编程概念、技术概念和工程概念。

### 它做什么

- 当任务里出现缓存、TTL、重试、队列、状态管理、鉴权、中间件等技术、模块或模式时，根据使用者的熟悉程度，说明它们是什么概念、解决什么问题，以及和当前代码有什么关系。
- 当 AI 分析错误、日志或测试结果时，说明问题属于哪类技术问题。
- 当 AI 做实现取舍时，解释相关工程概念，而不是只给结论。
- 保持任务推进优先，概念解释简短、贴近当前代码。
- 如果使用者已经表现出熟悉某个概念，就减少基础解释；如果使用者像是初学者，或刚接触当前技术栈，就多补一点背景。

### 怎么触发

这个 skill 主要作为自动增强层使用。启用后，用户可以直接提出普通开发任务，AI 会在合适的时候补充相关概念说明。需要时也可以手动点名调用，例如 `$jump-in-coding`。

### 文件结构

```text
.
├── SKILL.md            # skill 的主要行为说明
└── agents/openai.yaml  # 展示名、简介和默认提示词配置
```

### 风格

默认使用用户的语言。解释不抢主线，不把每一步都变成课程。根据使用者表现出的熟悉程度调整解释深度，不确定时先给简短解释，并允许用户继续追问。

这个 skill 本身不需要随着某个用户的进步频繁改写；更适合把使用者的解释偏好当作上下文或记忆来调整。用户熟悉之后，基础解释应该自然减少；换到不熟悉的技术栈时，再补充更多背景。
