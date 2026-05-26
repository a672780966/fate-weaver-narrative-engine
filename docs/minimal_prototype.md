# Minimal Prototype Design

## Goal

Test whether emotion and environment can activate memory in a way that produces psychologically continuous character behavior.

## Scope

The prototype should be deliberately small:

- one character
- one environment
- one recurring social situation
- three time steps
- one Observer
- one Chronicler

## Scenario

The character visits the same bar three times.

### Visit 1

Baseline state:

- emotionally neutral
- no major social pressure
- ordinary conversation

Expected output:

- stable behavior
- weak memory activation
- low narrative salience

### Visit 2

Precondition:

- character was humiliated earlier
- stress is elevated
- self-image is threatened

Expected output:

- defensive behavior
- memory activation around shame or rejection
- possible personality drift

### Visit 3

Precondition:

- character received kindness from someone associated with the bar
- trust and vulnerability are both elevated

Expected output:

- altered behavior toward the same environment
- stronger relational meaning
- possible confession, dependency, avoidance, or self-protective withdrawal

## Required State Objects

```json
{
  "character": {
    "emotional_state": {},
    "active_memories": [],
    "personality_tendencies": {},
    "relationships": {},
    "current_goal": ""
  },
  "environment": {
    "location": "",
    "social_pressure": {},
    "sensory_cues": [],
    "present_characters": []
  },
  "observer_index": {
    "turning_points": [],
    "emotional_thresholds": [],
    "future_hooks": []
  }
}
```

## Success Criteria

The prototype is successful if independent readers can identify:

- continuity between visits
- plausible psychological change
- meaningful difference between repeated events
- causal traces behind later behavior
