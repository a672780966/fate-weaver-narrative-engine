# Architecture Notes

## Core Separation

Fate Weaver separates three concerns that are often merged in AI storytelling systems:

```text
Simulation: what happens.
Cognition: how agents interpret what happens.
Narrative: what is selected and told to readers.
```

This separation is essential because a language model should not be treated as the entire world. The world should maintain state independently from the prose used to describe it.

## System Layers

### Character Simulation Layer

Purpose: maintain persistent internal lives.

State examples:

- emotional valence
- stress level
- trust toward other agents
- unresolved conflict
- active desire
- dormant trauma
- self-image
- relationship dependency

### World Simulation Layer

Purpose: generate environmental pressure.

State examples:

- location
- time
- weather
- social density
- cultural expectations
- economic scarcity
- rumors
- recurring places

### Fate Weaver Layer

Purpose: compress causality and guide convergence.

Components:

- Observer
- Executor
- Converger

### Narrative Lens Layer

Purpose: turn selected events into prose.

Components:

- Chronicler
- point-of-view selector
- scene salience scorer
- motif tracker
- omission controller

## Data Flow

```text
World Event
-> Character Emotional Response
-> Memory Activation
-> Internal State Update
-> Behavior Selection
-> World State Update
-> Observer Compression
-> Optional Fate Intervention
-> Chronicler Scene Selection
```

## Design Constraint

Fate intervention must occur after internal change has begun.

The system should avoid:

```text
author goal -> forced character action
```

It should prefer:

```text
latent character tendency -> environmental pressure -> plausible action
```
