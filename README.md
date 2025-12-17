# Hestia-system

**Hestia-system** is an architectural framework for building intention-ready systems,
designed from the ground up for constrained environments and distributed orchestration.

It is not a product, not a platform, and not a monolithic framework.
It is a **reference architecture** that defines how low-level systems can remain
deterministic, observable, and composable while staying compatible with higher-level
intentional reasoning.

---

## Core idea

Hestia-system starts from a simple premise:

> **Intention must not be embedded prematurely,  
> but systems must never prevent its emergence.**

For this reason, Hestia focuses first on:
- time,
- state,
- observation,
- and controlled execution,

before introducing intention as a higher-level concern.

---

## What Hestia-system is

Hestia-system defines:

- a **set of conceptual layers**
- a **separation of responsibilities**
- and **contracts** between subsystems

that allow:
- autonomous IoT subsystems to operate independently,
- while remaining compatible with supervision and intention engines.

It provides guidance for building:
- embedded SDKs,
- temporal primitives,
- state evaluation tools,
- supervision layers,
- and optional intention engines,

without forcing all components to exist or run at the same level.

---

## What Hestia-system is NOT

- Not a home-automation framework
- Not a rule engine
- Not a scheduler
- Not tied to Home Assistant
- Not dependent on cloud connectivity
- Not an AI system

Domotics, Home Assistant, and MQTT are **use cases**, not foundations.

---

## Architectural layers (conceptual)

### Intention & Arbitration 
- (optional, slow, contextual)
- e.g. Hestia-intent (HA addon or external)

### Supervision & Observation
- Aggregation, configuration, visualization
- e.g. HestiaSDK_HA (Home Assistant)

### Deterministic Embedded Subsystems
- Time, state evaluation, execution, resilience
- e.g. HestiaSDK, HestiaTempo, HestiaCheck


Each layer can exist **independently**.

---

## Embedded focus: deterministic first

At the embedded level (ESP32 and similar):

- systems must remain:
  - deterministic
  - debuggable
  - resource-aware
  - temporally explicit

Tools such as:
- `HestiaTempo` (temporal primitives)
- `HestiaCompare / HestiaCheck` (state evaluation)

are intentionally designed as **automation-grade building blocks**.

They may return:
- verdicts,
- thresholds,
- transitions,

but they must remain:
- observable,
- traceable,
- and compatible with future fact-based reasoning.

They do **not** embed intention.

---

## Intention is external by design

In Hestia-system:

- **intention is not required**
- **intention is not embedded**
- **intention is not time-critical**

An intention engine:
- operates at a higher level,
- consumes observations and temporal signals,
- produces goals or directives,
- and may run in Home Assistant or elsewhere.

This separation is deliberate.

---

## Compatibility principle

A subsystem compatible with Hestia-system should be able to state:

> *I expose qualified states and temporal behavior,  
> and I can execute directives,  
> without knowing who produced them or why.*

This principle is the cornerstone of the architecture.

---

## Current status

Hestia-system is currently in an **automation-enriched phase**.

This is intentional.

The focus is on:
- stabilizing primitives,
- validating APIs,
- and preserving architectural openness,

before introducing formal intention models.

---

## Scope of repositories

Typical repositories under the Hestia-system organization include:

- `hestia-sdk` — Embedded SDK for ESP32 systems
- `hestia-tempo` — Temporal primitives
- `hestia-check` — State evaluation tools
- `hestia-ha-sdk-addon` — Supervision and configuration
- `hestia-ha-intent` — Optional intention engine

Not all projects need all components.

---

## Philosophy

Hestia-system follows a simple rule:

> **Do not confuse what a system does  
> with what it is allowed to become.**

Automation is a starting point, not a failure.
Intention is a destination, not a shortcut.

---

## License and openness

Hestia-system is designed as an open, modular, and evolvable ecosystem.
Each repository defines its own license and scope.

The organization exists to preserve **architectural coherence** over time.


---



