---
layout: docs
title: Architecture
hero:
  title: The Voquira OS Architecture
  subtitle: How operational state, automation, and execution are coordinated as a single system.
---

## Overview

**This document defines the core architectural model of Voquira OS—how operational state, automation, and execution are coordinated as a single system.**

Voquira OS is not a traditional field-service platform.  
It is an **operational intelligence layer** designed to sit above tools, databases, and integrations and coordinate them reliably.

This architecture exists to solve one problem:  
**operational complexity that breaks down at scale.**

---

## Architectural Philosophy

Most service software is built around **screens and workflows**.  
Voquira OS is built around **state and execution**.

The system assumes:
- Jobs change
- Schedules break
- Humans make exceptions
- Automation must adapt without collapsing

As a result, the architecture prioritizes:
- Explicit state
- Event-driven execution
- Clear separation of responsibility
- Continuous feedback loops

---

## Core Architectural Layers

Voquira OS is composed of five primary layers:

1. Inputs  
2. Core Operational Model  
3. Automation & AI Agents  
4. Execution Systems  
5. Outputs & Feedback  

Each layer has a **single responsibility** and communicates through events rather than direct coupling.

---

## 1. Inputs Layer

The Inputs layer captures **signals from the real world**.

Examples include:
- Job creation
- Customer requests
- Schedule changes
- Technician updates
- Payment events
- External system events
- Weather or environmental data

Inputs **do not perform logic**.  
They emit events that describe *what happened*, not *what should happen next*.

This prevents fragile, UI-driven automation.

---

## 2. Core Operational Model (Source of Truth)

The Core Operational Model is the **heart of Voquira OS**.

All operational state is normalized into a small, consistent set of primitives:

- Jobs  
- Visits  
- Schedules  
- Crews / Technicians  
- Customers / Properties  
- Invoices  
- Status and Events  

Every automation, decision, and agent action operates **through this model**.

> If something cannot be represented in the model, it cannot be automated.

This guarantees consistency, auditability, and recoverability.

---

## 3. Automation & AI Agents

Automation in Voquira OS is **agent-based**, not rule-spaghetti.

Agents:
- Observe changes in the operational model
- Apply rules and constraints
- Execute scoped actions
- Log every decision

Examples:
- Dispatcher Agent assigns jobs
- Scheduling Agent optimizes routes
- AR Agent tracks invoicing gaps
- Customer Comms Agent handles notifications
- Compliance Agent enforces industry rules

Agents **never bypass the model** and **never operate without constraints**.

Humans can pause, override, or limit any agent at any time.

---

## 4. Execution Systems

Execution happens **outside** Voquira OS.

Examples:
- Field crews performing work
- Technicians completing jobs
- Billing platforms processing payments
- Messaging tools sending notifications

Voquira OS coordinates execution — it does not micromanage it.

This allows businesses to:
- Swap tools without breaking logic
- Scale execution independently
- Avoid vendor lock-in

---

## 5. Outputs & Feedback

Every execution generates feedback:

- Job completion events
- Status updates
- Invoices sent
- Payments received
- Exceptions and failures

These outputs feed back into the Inputs layer, closing the loop.

This creates a **continuously self-correcting system**.

---

## Architectural Flow (Conceptual)

Event → Model → Agent → Execution → Feedback → Event


This loop runs continuously.

There is no “final state.”  
The system is always adapting to reality.

---

## Why This Architecture Matters

This architecture enables:

- **Scalability** — complexity is absorbed by the model
- **Flexibility** — tools can change without rewrites
- **Reliability** — automation is predictable and auditable
- **Composability** — new agents can be added safely
- **Resilience** — failures do not cascade

Most field-service platforms collapse logic, UI, and execution into one layer.  
Voquira OS deliberately separates them.

---

## Comparison to Traditional Platforms

Traditional platforms typically follow this pattern:

UI → Workflow → Action

Voquira OS follows:

Event → Model → Agent → Execution → Feedback


This difference is what allows Voquira OS to function as **infrastructure**, not just software.

---

## Design Guarantees

Voquira OS guarantees that:

- All state changes are explicit
- All automation is auditable
- All agents operate within constraints
- All execution produces feedback
- Humans retain control

These guarantees are architectural, not optional features.

---

## Summary

- Voquira OS is event-driven, not UI-driven
- The operational model is the source of truth
- AI agents execute responsibilities, not suggestions
- Execution systems remain replaceable
- Feedback loops keep the system accurate

This architecture is what allows Voquira OS to run service businesses as systems — not struggle through them.




