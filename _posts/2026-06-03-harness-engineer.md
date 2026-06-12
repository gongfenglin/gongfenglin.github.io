---
layout: blog_post
title: "Harness Engineer"
date: 2026-06-03
lang: en
lang_switch_url: /zh/blog/harness-engineer/
tags: [AI Agent, Harness, Evaluation]
permalink: /blog/harness-engineer/
excerpt: "Harness engineering is the discipline of making AI agents measurable, controllable, and useful under real work conditions."
---

### Why this role matters

I use **Harness Engineer** to describe a builder who does not only write prompts or demos, but builds the surrounding system that makes an AI agent trustworthy enough to use.

The harness is the layer around the model: datasets, task definitions, tool permissions, traces, assertions, expected failures, scorecards, release gates, and recovery paths. Without this layer, an agent can look impressive in a demo while still being impossible to evaluate, debug, or improve.

### What the harness contains

A useful harness normally includes four things.

First, it defines tasks in a way that can be replayed. Second, it records what the agent saw, planned, executed, and verified. Third, it turns failures into structured signals instead of vague impressions. Fourth, it connects those signals to decisions: pass, fail, expected fail, retry, or block release.

This is the common thread behind my work on promptfoo, pydantic-ai, Haystack, swarm-eval-lab, and omni-agent. The interesting part is not whether an agent can produce an answer once. The interesting part is whether we can build a loop that makes reliability visible.

### My current direction

My focus is to move coding agents and evaluation tools from "works in a lucky run" toward "works because the system can check itself." That means tighter eval workflows, better tool-result handling, clearer failure semantics, and practical infrastructure that can survive real repository work.
