---
layout: blog_post
title: "Agent Evaluation Notes"
date: 2026-06-09
lang: en
lang_switch_url: /zh/blog/agent-evaluation-notes/
tags: [LLM Evaluation, promptfoo, Benchmark]
permalink: /blog/agent-evaluation-notes/
excerpt: "My evaluation work focuses on failure semantics, reproducible benchmarks, and workflows that can explain why an agent passed or failed."
---

### Evaluation is a design problem

Agent evaluation is not only about choosing a metric. It is about designing a system that can explain behavior.

That includes task slices, expected outputs, scoring rules, tool traces, provider differences, and failure categories. A useful eval should tell us not only that an agent failed, but what kind of failure happened and whether that failure was expected.

### Failure semantics matter

This is why I am interested in concepts such as xfail and XPASS. In real evaluation work, some failures are known, tracked, and temporarily tolerated. But if a known failure unexpectedly passes, that also matters. It may reveal a real improvement, a flaky test, or a broken assertion.

The goal is to make these states visible instead of hiding them inside pass/fail totals.

### What I am building around

My current evaluation direction connects promptfoo-style assertion workflows, swarm-eval-lab benchmark studies, and agent runtime traces. The larger goal is to build eval systems that can support real agent iteration: compare strategies, inspect failures, and decide what is ready to ship.
