# Jump in Coding

[中文说明](README_CN.md)

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
