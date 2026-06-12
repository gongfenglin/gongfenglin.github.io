---
layout: blog_post
title: "Agent 评估笔记"
date: 2026-06-09
lang: zh
lang_switch_url: /blog/agent-evaluation-notes/
tags: [Agent 评估, promptfoo, Benchmark]
permalink: /zh/blog/agent-evaluation-notes/
excerpt: "我关注的 Agent 评估不是单一指标，而是失败语义、可复现 benchmark 和能解释通过/失败原因的工作流。"
---

### 评估本身也是系统设计

Agent Evaluation 不只是选一个 metric。它更像一个系统设计问题：如何让我们解释 Agent 的行为。

这包括任务切片、期望输出、评分规则、工具 trace、provider 差异和失败类别。一个好的 eval 不应该只告诉我们 Agent 失败了，还要告诉我们是哪一种失败，以及这种失败是不是已知且被跟踪的。

### 失败语义很重要

这也是我关注 xfail 和 XPASS 的原因。在真实评估里，有些失败是已知的、被记录的、暂时接受的。但如果一个已知失败突然通过了，这同样重要。它可能代表真实改进，也可能代表 flaky test 或断言本身出了问题。

目标是让这些状态可见，而不是全部压成一个通过率。

### 我正在围绕什么构建

我目前的评估方向连接了 promptfoo 的 assertion workflow、swarm-eval-lab 的 benchmark study，以及 Agent runtime 的 trace。更大的目标是支持真实 Agent 迭代：比较策略、定位失败、判断什么可以发布。
