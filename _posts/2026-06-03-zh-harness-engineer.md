---
layout: blog_post
title: "Harness Engineer：为可靠 Agent 搭工程外壳"
date: 2026-06-03
lang: zh
lang_switch_url: /blog/harness-engineer/
tags: [AI Agent, Harness, 评估]
permalink: /zh/blog/harness-engineer/
excerpt: "Harness Engineer 不是只写 prompt 或 demo，而是为 AI Agent 构建可评估、可控制、可复现的工程外壳。"
---

### 为什么需要 Harness Engineer

我用 **Harness Engineer** 描述一种 AI Agent 时代很重要的工程角色：不只是写 prompt，不只是做 demo，而是构建让 Agent 真的可用、可测、可控的外部系统。

Harness 是包在模型外面的那一层：数据集、任务定义、工具权限、trace、断言、预期失败、scorecard、发布门禁和失败恢复路径。没有这一层，Agent 很容易在演示里显得很强，但在真实项目中无法评估、无法调试，也无法持续改进。

### Harness 包含什么

一个有用的 harness 至少要做四件事。

第一，把任务定义成可以复现的形式。第二，记录 Agent 看到了什么、计划了什么、执行了什么、验证了什么。第三，把失败变成结构化信号，而不是主观感觉。第四，把这些信号接到决策上：通过、失败、预期失败、重试，或者阻止发布。

### 我的方向

我在 promptfoo、pydantic-ai、Haystack、swarm-eval-lab 和 omni-agent 上关注的东西，本质上都和 harness 有关。我更关心的不是 Agent 某一次能不能答对，而是能不能建立一个 loop，让可靠性变得可见。
