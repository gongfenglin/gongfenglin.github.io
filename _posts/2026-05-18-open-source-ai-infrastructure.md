---
layout: blog_post
title: "Open-Source AI Infrastructure"
date: 2026-05-18
lang: en
lang_switch_url: /zh/blog/open-source-ai-infrastructure/
tags: [Open Source, pydantic-ai, Haystack]
permalink: /blog/open-source-ai-infrastructure/
excerpt: "The AI infrastructure work I care about sits close to tool use, provider integrations, document conversion, and reliability under edge cases."
---

### Infrastructure is where reliability shows up

Open-source AI infrastructure is often less flashy than model demos, but it is where practical reliability becomes visible.

Provider integrations, tool-call serialization, document conversion, vector retrieval, async pipelines, and error handling all look like details. In practice, these details decide whether an AI system can run repeatedly without losing context or silently degrading.

### Why small fixes matter

My merged pydantic-ai PR fixed a continuation bug where Anthropic code-execution tool results could be dropped from conversation history. My Haystack contributions focused on pgvector retrieval ordering and async job mode support for Docling Serve conversion.

These are not isolated patches. They are examples of the same infrastructure instinct: preserve evidence, make execution observable, and remove hidden failure modes from AI workflows.

### The direction

I want to keep working at the intersection of agent frameworks, eval systems, and document/knowledge pipelines. This is where research ideas become usable engineering systems.
