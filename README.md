# Fate Weaver Narrative Engine

## An Emotion-Environment Driven Multi-Agent Narrative Simulation Architecture

Fate Weaver Narrative Engine is a conceptual architecture for building long-running AI narrative worlds where stories emerge from simulated lives rather than being directly generated as plots.

It is not intended to be a conventional AI novel generator, chatbot, or role-playing prompt system. The core idea is to explore whether believable long-form narrative can arise from agents with persistent emotional states, environmental pressures, evolving memories, social relationships, and high-level causal compression.

The project is currently a research-oriented architecture proposal, not a complete implementation.

---

## 中文简介

Fate Weaver Narrative Engine（命运编织者叙事引擎）是一套面向长期 AI 叙事世界的概念架构。

它并不是普通的 AI 写小说工具、多角色聊天系统或角色扮演 Prompt 模板，而是试图探索一种新的叙事模拟范式：故事不是被模型直接“写出来”的，而是由具备情绪、记忆、环境压力、关系网络和人格变化的智能体在世界中“生活出来”的。

本架构的核心观点是：

```text
真正驱动角色行为的，不是单纯的记忆检索，
而是环境刺激与情绪压力先激活记忆，
再推动人格偏移、行为选择和世界变化。
```

因此，Fate Weaver 关注的不是如何一次性生成精彩剧情，而是如何让角色在时间中持续存在，如何让平凡事件在特定情绪场中变得有意义，如何通过 Observer 对长期因果进行压缩，并在角色已经发生主动变化之后，由 Fate 系统轻微放大既有趋势，最终实现自然涌现与宿命收束之间的平衡。

当前仓库是一份研究型架构提案，适合与多智能体系统、AI NPC、计算叙事、人工生命、长期记忆与涌现式故事生成方向的研究者和开发者交流。

---

## 日本語紹介

Fate Weaver Narrative Engine は、長期的に持続する AI ナラティブ世界を構築するための概念的アーキテクチャです。

これは通常の AI 小説生成ツール、複数キャラクターのチャットシステム、あるいはロールプレイ用プロンプトではありません。目的は、物語を直接生成するのではなく、感情、記憶、環境からの圧力、人間関係、人格変化を持つエージェントが世界の中で「生きる」ことによって、物語が自然に立ち上がる可能性を探ることです。

中心となる仮説は次の通りです。

```text
キャラクターの行動を本当に駆動するのは、
単なる記憶検索ではない。
環境刺激と感情の変化が記憶を呼び起こし、
そこから人格の揺らぎ、行動選択、世界の変化が生まれる。
```

Fate Weaver が重視するのは、優れたシーンを一度だけ生成することではなく、キャラクターが時間の中でどのように連続して存在し、平凡な出来事が特定の感情状態の中でどのように意味を持ち、Observer が長期的な因果関係をどのように圧縮し、Fate システムが既に始まった内面的変化をどのように増幅できるかという点です。

このリポジトリは現時点では実装済みのシステムではなく、研究および議論のためのアーキテクチャ提案です。マルチエージェントシステム、AI NPC、計算物語論、人工生命、長期記憶、創発的ストーリーテリングに関心を持つ研究者や開発者との対話を目的としています。

---

## Core Question

Most current AI character systems are driven by a simple loop:

```text
retrieve memory -> generate response -> save new memory
```

Fate Weaver proposes a different model:

```text
environmental stimulus
-> emotional shift
-> memory emergence
-> personality drift
-> action
-> world change
-> new environmental stimulus
```

In this model, memory is not the primary driver of behavior. Memory is activated by emotion and environment.

This distinction is central. A person does not usually act because they searched a database of past events. They act because the present situation creates emotional pressure, and that pressure awakens certain memories, fears, desires, or unresolved conflicts.

---

## Design Philosophy

The system is built around four narrative assumptions:

1. Stories should emerge from life, not from forced plot generation.
2. No character is meaningless. Even a minor person can become causally important.
3. Fate should not create change by force. It should amplify changes that have already begun inside characters.
4. Long-form narrative requires causal compression, not just longer context windows.

The intended result is a world where characters appear to live before they are written about.

---

## What This Is Not

Fate Weaver is not:

- a prompt template for writing novels
- a multi-character chatroom
- a simple LangGraph workflow
- a Dify chatbot application
- a fully autonomous story generator
- a claim that current consumer hardware can simulate a complete living world

It is closer to a research proposal for an AI narrative simulation engine, influenced by multi-agent systems, artificial life, computational narrative, game AI, social simulation, and cognitive architecture.

---

## High-Level Architecture

The proposed system has four major layers.

### 1. Character Simulation Layer

Each important character is treated as an autonomous agent with persistent internal state.

Core components:

- Personality Core
- Emotional State
- Long-Term Memory
- Short-Term Context
- Relationship Model
- Goal and Desire Model
- Trauma and Contradiction Model
- Behavior Decision Module

The key design principle is that the character should not be defined only by traits, but by lived experience.

Instead of:

```text
This character is cold, proud, and loyal.
```

The system should model:

```text
This character was abandoned early, learned to distrust kindness,
protects others indirectly, and rationalizes emotional distance as strength.
```

Personality is treated as sedimented experience.

---

### 2. World Simulation Layer

The world is not only background information. It is the soil in which characters live.

This layer manages:

- locations
- time progression
- local culture
- economic pressure
- social rules
- events
- resources
- environmental triggers
- social proximity

The world should be capable of creating pressure on characters without requiring a writer to explicitly command every dramatic moment.

---

### 3. Fate Weaver Layer

The Fate Weaver layer is the high-level causal management system.

It does not directly write the plot. Instead, it observes emerging changes and lightly shapes future conditions so that independent worldlines may eventually converge.

This layer contains three conceptual roles.

### Observer

The Observer is not just a logger. It is a narrative compression engine.

It tracks:

- emotional thresholds
- personality drift
- relationship changes
- causal turning points
- repeated motifs
- unresolved tensions
- future hooks
- worldline divergence and convergence

Its purpose is to turn massive simulation history into usable causal indexes.

### Executor

The Executor introduces small environmental interventions after a character has already begun to change.

It should not force a character into an artificial arc. It should amplify existing internal tendencies.

Bad intervention:

```text
The plot needs this character to betray someone, so the system forces betrayal.
```

Better intervention:

```text
The character already has jealousy, insecurity, and fear of abandonment.
The system introduces a situation that makes betrayal psychologically plausible.
```

### Converger

The Converger is responsible for long-range worldline convergence.

Its job is to connect separate lives, towns, events, and emotional arcs into a larger destiny-like structure without making the story feel mechanically predetermined.

---

### 4. Narrative Lens Layer

The system must distinguish between:

```text
what happened in the world
```

and:

```text
what should be shown to the reader
```

This layer includes a Chronicler or Narrative Curator.

The Chronicler decides:

- which ordinary events matter
- which scenes should be skipped
- which small details should be emphasized
- whose point of view should frame a scene
- what should remain unsaid
- how daily life becomes literature

For example, a character walking past a flower shop may be meaningless on one day and emotionally decisive on another day. The event itself is ordinary. Its narrative value depends on emotional state, context, repetition, and future consequence.

---

## Key Concept: Emotion-Environment-Memory Triangle

The central cognitive model is:

```text
Environment
-> Emotion
-> Memory Emergence
-> Personality Drift
-> Behavior
-> Environment
```

This is different from RAG-style character design.

In a RAG-style system, memory is retrieved because it is semantically relevant.

In Fate Weaver, memory emerges because the current emotional and environmental state makes it psychologically active.

Two identical events may produce different outcomes:

```text
First drink:
stable mood + safe environment + ordinary relationship
-> no major change

Second drink:
recent failure + emotional vulnerability + trusted companion + late-night setting
-> confession, dependency, or personality shift
```

The meaning of an event is not in the event alone. It is in the state field around the event.

---

## Long-Term Narrative Problem

Long-form AI storytelling is not primarily limited by the ability to generate prose.

The harder problems are:

- causal continuity
- emotional inertia
- personality stability
- relationship evolution
- memory reinterpretation
- world state persistence
- narrative compression
- meaningful event selection

Long context windows alone do not solve these problems. A million-token context can still fail if the system does not know which events changed the future causal structure.

This is why the Observer is central. It converts raw history into causal structure.

---

## Relationship to Existing Work

The closest known research direction is Stanford's Generative Agents / Smallville, which showed that believable social behavior can emerge from agents with memory, reflection, and planning.

Fate Weaver differs in emphasis:

- stronger focus on emotional inertia
- stronger focus on personality drift
- stronger focus on environment-triggered memory emergence
- stronger focus on long-form narrative causality
- stronger focus on worldline convergence
- explicit separation between simulation and narration

It also relates to:

- AI Town
- artificial life systems
- autonomous NPC research
- GOAP-based game AI
- entity-component-system architectures
- social simulation
- computational narratology
- narrative planning
- long-term agent memory research

---

## Possible Technical Direction

A practical prototype would likely avoid using LLMs for every state update.

Possible stack:

- ECS for world and entity state
- graph database for relationships and causal memory
- event sourcing for world history
- vector search for semantic memory retrieval
- rule-based or lightweight model updates for low-level simulation
- LLMs only for high-level cognition, reflection, dialogue, and narration
- LangGraph or similar state-machine framework for agent orchestration

The system should separate:

```text
Simulation: what actually happens
Cognition: how agents understand what happens
Narrative: how selected events are told to humans
```

This separation is essential. If the LLM is treated as the whole world, the system will eventually collapse into prompt-driven improvisation.

---

## Minimal Research Prototype

A realistic first prototype should not attempt to build a full world.

A more feasible target:

- 1 character
- 1 small environment
- 3 recurring situations
- emotional state tracking
- environment-triggered memory activation
- personality drift over time
- Observer-generated causal summaries
- Chronicler-generated narrative scenes

The goal would be to test whether the same event can produce meaningfully different behavior depending on accumulated emotional state and environmental context.

Example experiment:

```text
The same person visits the same bar three times.

Visit 1: neutral state
Visit 2: after humiliation
Visit 3: after receiving kindness from someone connected to the bar
```

Research question:

Can the system produce behavior that feels like psychological continuity rather than random variation?

---

## Why This Matters

Current AI narrative systems can generate impressive scenes, but they often struggle to sustain life-like continuity.

Fate Weaver argues that the next step is not simply better prose generation. The next step is modeling the conditions under which characters change.

The ultimate research question is:

```text
Can narrative emerge from simulated emotional causality?
```

If so, AI storytelling may move from static generation toward persistent narrative life.

---

## Current Status

This repository is currently a conceptual architecture draft.

The goal is to share the idea with researchers, developers, writers, and designers working on:

- multi-agent systems
- AI NPCs
- computational narrative
- artificial life
- long-term memory
- agent simulation
- emergent storytelling

Feedback, critique, references, and collaboration discussions are welcome.
