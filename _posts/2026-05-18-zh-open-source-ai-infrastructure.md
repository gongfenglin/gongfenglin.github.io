---
layout: blog_post
title: "开源 AI 基础设施"
date: 2026-05-18
lang: zh
lang_switch_url: /blog/open-source-ai-infrastructure/
tags: [开源, pydantic-ai, Haystack]
permalink: /zh/blog/open-source-ai-infrastructure/
excerpt: "我关注的开源 AI 基础设施，主要靠近工具调用、provider 集成、文档转换和边界场景下的可靠性。"
---

### 基础设施决定可靠性

开源 AI 基础设施看起来没有模型 demo 那么耀眼，但真正的可靠性往往就体现在这里。

Provider 集成、工具调用序列化、文档转换、向量检索、异步管线和错误处理，看起来都是细节。但在实践里，这些细节决定一个 AI 系统能不能重复运行，能不能保留上下文，能不能避免静默退化。

### 小修复为什么重要

我合并进 pydantic-ai 的 PR 修复了 Anthropic code-execution 工具结果在续聊时可能丢失的问题。Haystack 相关贡献则包括 pgvector 检索排序修复，以及 Docling Serve converter 的异步 job mode。

这些不是孤立补丁，而是同一种工程直觉：保留证据、让执行过程可观察、把隐藏失败模式从 AI workflow 里移出去。

### 后续方向

我想继续在 Agent 框架、评估系统和文档/知识管线的交叉处做工作。这里是研究想法变成可用工程系统的地方。
