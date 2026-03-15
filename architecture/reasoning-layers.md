# VERA Behavioral Reasoning Architecture — Reasoning Layers

> **Document:** `architecture/reasoning-layers.md`
> **Author:** Eva Leka · ORCID: [0009-0003-7239-706X](https://orcid.org/0009-0003-7239-706X)
> **Classification:** Research Documentation — Public
> **Version:** 1.0

---

## 1. Overview

The VERA Behavioral Reasoning Architecture processes human input through eight sequential reasoning layers before a response is generated. Each layer performs a specific conceptual operation — transforming raw conversational and behavioral signals into a contextualized, calibrated response that reflects the human's current psychological and cognitive state.

The layered structure ensures that no single signal drives response generation unilaterally. Instead, signal meaning is constructed progressively: each layer refines the interpretation passed to it, adds a layer of behavioral or contextual context, and forwards a richer understanding to the next stage. The result is a reasoning process grounded in the full human context rather than in the surface content of the input alone.

This document describes the conceptual role of each layer. It does not disclose implementation details, algorithmic logic, or proprietary system specifications.

---

## 2. Reasoning Layer Stack

```
┌──────────────────────────────────────────────────────────┐
│              VERA — REASONING LAYER STACK                │
│                                                          │
│  ┌────────────────────────────────────────────────────┐  │
│  │  Layer 1 — Conversation Entry Detection            │  │
│  └──────────────────────────┬─────────────────────────┘  │
│                             │                            │
│  ┌──────────────────────────▼─────────────────────────┐  │
│  │  Layer 2 — Micro-Signal Detection                  │  │
│  └──────────────────────────┬─────────────────────────┘  │
│                             │                            │
│  ┌──────────────────────────▼─────────────────────────┐  │
│  │  Layer 3 — Biological Driver Identification        │  │
│  └──────────────────────────┬─────────────────────────┘  │
│                             │                            │
│  ┌──────────────────────────▼─────────────────────────┐  │
│  │  Layer 4 — Adaptive Code Activation                │  │
│  └──────────────────────────┬─────────────────────────┘  │
│                             │                            │
│  ┌──────────────────────────▼─────────────────────────┐  │
│  │  Layer 5 — Latent Behavioral Map Placement         │  │
│  └──────────────────────────┬─────────────────────────┘  │
│                             │                            │
│  ┌──────────────────────────▼─────────────────────────┐  │
│  │  Layer 6 — Response Strategy Selection             │  │
│  └──────────────────────────┬─────────────────────────┘  │
│                             │                            │
│  ┌──────────────────────────▼─────────────────────────┐  │
│  │  Layer 7 — Response Generation                     │  │
│  └──────────────────────────┬─────────────────────────┘  │
│                             │                            │
│  ┌──────────────────────────▼─────────────────────────┐  │
│  │  Layer 8 — State Transition Tracking               │  │
│  └────────────────────────────────────────────────────┘  │
└──────────────────────────────────────────────────────────┘
```

---

## 3. Layer Descriptions

---

### Layer 1 — Conversation Entry Detection

**Conceptual role:** Establish the psychological and relational context in which the conversation begins.

Before interpreting the content of any message, VERA's architecture first characterizes the nature of the conversational entry itself. This layer examines how the interaction is initiated — the tone, pace, degree of specificity, and relational register of the opening signal — to establish a baseline understanding of the human's orientation at the moment they begin communicating.

Conversational entry patterns carry meaningful information independent of the message content. A person who initiates contact with high urgency and compressed expression is in a different psychological position than a person who engages reflectively and with deliberate structure. Layer 1 establishes the initial frame for all subsequent interpretation.

**Output to Layer 2:** Conversational context assessment — a characterization of the entry register, urgency indicators, and initial relational orientation.

---

### Layer 2 — Micro-Signal Detection

**Conceptual role:** Identify fine-grained behavioral signals embedded within the human's communication.

Micro-signals are subtle, often non-deliberate indicators of psychological state that appear within and alongside the primary content of a communication. They include patterns in linguistic pacing, word selection precision, the presence or absence of self-reference, hedging behaviors, tonal shifts, and structural anomalies in expression — signals that a person typically produces without awareness that they are producing them.

This layer is responsible for identifying these signals and characterizing their significance relative to the conversational baseline established in Layer 1. Micro-signals are meaningful precisely because they are difficult to manage consciously under normal conditions and become increasingly prominent as emotional intensity or cognitive load increases.

**Output to Layer 3:** Micro-signal inventory — a structured characterization of detected fine-grained behavioral indicators and their estimated significance.

---

### Layer 3 — Biological Driver Identification

**Conceptual role:** Identify the probable underlying biological or psychological driver motivating the human's communication.

Human behavior is driven by a combination of conscious intent and sub-conscious biological and psychological states. Under conditions of stress, emotional activation, or unmet need, biological drivers — such as threat response, attachment need, loss of safety, or autonomic dysregulation — often produce behavioral patterns that are inconsistent with, or only partially reflected in, the surface content of what a person communicates.

This layer draws on the behavioral signal inventory from Layer 2 and the conversational context from Layer 1 to identify the probable biological driver underlying the interaction. The distinction between what a person is asking and what biological state is producing the asking is the foundation of behaviorally informed response design.

Identification at this layer is probabilistic and uncertainty-weighted. Multiple candidate drivers may be held simultaneously when the signal pattern does not clearly disambiguate.

**Output to Layer 4:** Driver characterization — a ranked, uncertainty-weighted identification of probable biological and psychological drivers.

---

### Layer 4 — Adaptive Code Activation

**Conceptual role:** Recognize the learned behavioral pattern — the adaptive code — that the human is operating from.

Adaptive codes are the behavioral strategies that individuals develop — often during formative experiences, and often below the level of conscious awareness — to manage threat, maintain safety, and meet fundamental psychological needs. They are called adaptive because they were, in their original context, appropriate responses to real conditions. They are called codes because they operate as habitual programs: consistent, recognizable patterns of behavior activated in response to specific triggering conditions.

Common adaptive codes include hypervigilance in the face of perceived unpredictability, withdrawal under the threat of rejection, over-functioning as a response to early requirement for self-sufficiency, and people-pleasing as a strategy for maintaining connection in threatening relational environments. These patterns are neither pathological nor permanent — they are learned, and they can be recognized.

Layer 4 is responsible for identifying which adaptive code, or combination of codes, is active in the current interaction. This identification informs both the response strategy and the care with which certain topics or framings should be approached.

**Output to Layer 5:** Active code profile — the behavioral pattern currently governing the human's interaction approach.

---

### Layer 5 — Latent Behavioral Map Placement

**Conceptual role:** Locate the human's current position within the Latent Behavioral Map.

The Latent Behavioral Map is a conceptual topology of psychological states, organized as a set of zones that describe the dominant orientation of a person's cognitive and emotional functioning at a given moment. Based on the biological drivers identified in Layer 3 and the adaptive codes characterized in Layer 4, this layer determines which zone best describes the human's current condition.

Zone placement is not a fixed categorization — it is a dynamic positioning that changes as the interaction evolves and as state transition tracking (Layer 8) provides feedback. A person may occupy a primary zone with elements of adjacent zones; the placement represents the center of gravity of their current state rather than a rigid assignment.

The zones of the Latent Behavioral Map are described in detail in [`behavioral-map.md`](behavioral-map.md). In brief:

| Zone | Dominant Orientation |
|---|---|
| **Conflict** | The human is in active internal or relational tension, experiencing competing needs or values that feel irreconcilable |
| **Survival** | The human is in a threat-activated state, operating from self-protective biological programming with reduced access to deliberate reasoning |
| **Rumination** | The human is caught in a repetitive thought cycle, re-processing past events or anticipated future threats without resolution |
| **Clarity** | The human has sufficient cognitive and emotional resources to engage in deliberate, goal-directed reasoning |
| **Growth** | The human is in a state of active integration, capable of receiving new frameworks and incorporating change |

**Output to Layer 6:** Behavioral map position — the human's current zone placement and transition trajectory.

---

### Layer 6 — Response Strategy Selection

**Conceptual role:** Determine the response approach that best serves the human's current behavioral map position and underlying needs.

With the human's psychological state characterized across all preceding layers, Layer 6 selects the response strategy most likely to support movement toward regulatory capacity and constructive engagement. Response strategy is not equivalent to response content — it is the relational and structural approach that will govern how the response is framed, what it prioritizes, and what it deliberately avoids.

Different behavioral map zones require qualitatively different response strategies. A human in a survival-activated state requires responses that establish safety and reduce perceived threat before any informational content can be absorbed. A human in a rumination state requires responses that interrupt the cycle through grounding or gentle reframing before analytical support is useful. A human in a clarity state can receive and integrate more complex, structured information. A human in a growth state can benefit from expanded frameworks and reflective challenge.

Strategy selection also incorporates the identified adaptive code: certain communication approaches will engage adaptive codes in ways that protect rather than support the human, and the response strategy must account for this.

**Output to Layer 7:** Response strategy specification — the relational register, structural approach, and content priorities to be applied in response generation.

---

### Layer 7 — Response Generation

**Conceptual role:** Construct the response in accordance with the strategy specification and the full behavioral context established by preceding layers.

Layer 7 is where the response takes its final form. All preceding layers have contributed to a complete characterization of the human's current state, the biological and psychological drivers shaping their communication, their position in the behavioral map, and the strategy most appropriate to their condition. Response generation translates this characterization into actual output.

The response generated at this layer reflects not only what information is relevant but how that information should be expressed, in what order, at what level of complexity, with what relational tone, and with what explicit or implicit acknowledgment of the human's state. The goal is a response that the human can receive and use — not merely a response that is technically accurate.

Responses are not generated from content alone. The behavioral context established through Layers 1–6 acts as a persistent constraint on what is appropriate to say, how it should be said, and what should be withheld or deferred.

**Output to Layer 8:** Generated response — complete response content ready for delivery, accompanied by current state characterization for tracking purposes.

---

### Layer 8 — State Transition Tracking

**Conceptual role:** Monitor changes in the human's behavioral state across the interaction and feed updated state information back into the reasoning process.

A single exchange does not define an interaction. Layer 8 maintains a session-scoped record of the human's behavioral map positions, biological drivers, and adaptive code activations across all turns of the conversation. It tracks the direction and rate of state change — whether the human is moving toward greater regulatory capacity and clarity, remaining in a fixed state, or escalating in distress — and makes this trajectory information available to all upstream layers for subsequent turns.

State transition tracking serves two functions. First, it provides the feedback signal that allows the reasoning architecture to adapt dynamically as the interaction unfolds: what was appropriate in the early stages of a conversation may not be appropriate after several exchanges have shifted the human's state. Second, it creates a longitudinal behavioral picture of the interaction that can inform when to introduce more complex support, when to simplify, when to acknowledge progress, and when escalating distress requires a shift in response strategy.

**Output:** Updated state trajectory — fed back to Layers 1–6 as contextual prior for subsequent reasoning cycles.

---

## 4. Cross-Layer Principles

### Sequential Processing with Feedback
Layers are processed in sequence on each conversational turn. Layer 8's state trajectory output becomes available to all layers on the following turn, creating a feedback-informed reasoning cycle that becomes progressively more calibrated to the individual as the interaction continues.

### Uncertainty Preservation
No layer collapses uncertainty before passing its output forward. Each layer maintains and forwards confidence information alongside its primary output, allowing the full reasoning chain to reflect the actual quality of available evidence.

### Non-Reductive State Characterization
The architecture never reduces the human's state to a single label or score. Multiple layers contribute partial, overlapping characterizations that are held in composite, ensuring that nuance and complexity are preserved through the reasoning process.

### Behavioral Primacy
At every layer, the interpretation of what the human needs takes precedence over the interpretation of what the human literally expressed. This is the defining commitment of behavioral reasoning: the response is calibrated to the person, not only to the words.

---

## 5. Scope of This Document

This document describes the conceptual role of each reasoning layer. It does not disclose:

- Specific algorithmic or model-based implementations within any layer
- Feature sets, thresholds, or classification procedures
- Training data, datasets, or evaluation protocols
- Internal signal representations or data structures
- Proprietary system logic or configuration

For the Latent Behavioral Map zone descriptions, see [`behavioral-map.md`](behavioral-map.md).
For system-level architecture, see [`overview.md`](overview.md).

---

*VERA Behavioral Reasoning Architecture is proprietary intellectual property of VeraNeural.ai. This document is published for academic reference only. All rights reserved.*
