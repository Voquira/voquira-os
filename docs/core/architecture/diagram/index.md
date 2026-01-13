---
layout: docs
title: Architecture Diagram
---

## Voquira OS Architecture Overview

Voquira OS is designed as an **operational intelligence layer** that sits above tools, databases, and integrations.

It does not replace every system.  
It **coordinates them**.

This page explains the high-level architecture and how the pieces work together.

---

## High-Level Architecture

At a system level, Voquira OS is composed of five layers:

1. **Inputs**
2. **Core Operational Model**
3. **Automation & AI Agents**
4. **Execution Systems**
5. **Outputs & Feedback**

Each layer has a clear responsibility and limited scope.

---

## Conceptual Architecture Diagram

┌──────────────────────────────┐
│ Inputs Layer │
│──────────────────────────────│
│ • Web forms │
│ • CRM events │
│ • Job creation │
│ • Schedule changes │
│ • Payments │
│ • External APIs │
└───────────────┬──────────────┘
│
▼
┌──────────────────────────────┐
│ Core Operational Model │
│──────────────────────────────│
│ • Jobs │
│ • Visits │
│ • Schedules │
│ • Crews / Technicians │
│ • Customers & Properties │
│ • Invoices │
└───────────────┬──────────────┘
│
▼
┌──────────────────────────────┐
│ Automation & AI Agents │
│──────────────────────────────│
│ • Dispatcher Agent │
│ • Scheduling Agent │
│ • AR Agent │
│ • Comms Agent │
│ • Compliance Agent │
└───────────────┬──────────────┘
│
▼
┌──────────────────────────────┐
│ Execution Systems │
│──────────────────────────────│
│ • Field crews │
│ • Technicians │
│ • Scheduling tools │
│ • Billing platforms │
│ • Communication channels │
└───────────────┬──────────────┘
│
▼
┌──────────────────────────────┐
│ Outputs & Feedback │
│──────────────────────────────│
│ • Job completion │
│ • Invoices sent │
│ • Payments received │
│ • Customer notifications │
│ • Operational metrics │
└──────────────────────────────┘


This flow is **continuous**, not linear.  
Feedback loops constantly update the system state.

---

## Inputs Layer

The Inputs layer captures **signals from the business**.

Examples:
- A new Job is created
- A customer reschedules
- A technician marks work complete
- A payment is received
- Weather data changes

Inputs do not perform logic.  
They simply emit events into the system.

---

## Core Operational Model

This is the **heart of Voquira OS**.

The model defines:
- What a Job is
- How Scheduling works
- Who can perform work
- How execution and billing relate

Everything is normalized into a small set of primitives:
- Jobs
- Visits
- Schedules
- Resources
- Financial records

This keeps the system coherent as complexity grows.

---

## Automation & AI Agents Layer

This layer **acts on the model**, not on raw inputs.

Agents:
- Observe state changes
- Apply rules and constraints
- Execute actions within authority limits

Key point:
> Agents never bypass the operational model.

This prevents fragile automation and unintended side effects.

---

## Execution Systems

Execution happens outside Voquira OS.

Examples:
- Field crews perform work
- Technicians complete Jobs
- Billing platforms process payments
- Messaging tools send notifications

Voquira OS coordinates execution but does not micromanage it.

---

## Outputs & Feedback

Every execution generates feedback:
- Status updates
- Completion events
- Payment confirmations
- Exceptions and failures

These outputs feed back into the Inputs layer, keeping the system **self-updating**.

---

## Why This Architecture Matters

This design provides:

- **Scalability** — complexity is absorbed by the model
- **Flexibility** — tools can change without rewriting logic
- **Reliability** — automation is event-driven and auditable
- **Composability** — agents can be added without breaking flows

Most field service software collapses logic and execution together.  
Voquira OS keeps them deliberately separate.

---

## Comparison to Traditional Platforms

Traditional platforms often look like this:
UI → Workflow → Action


Voquira OS looks like this:
Event → Model → Agent → Execution → Feedback


This difference is what allows Voquira OS to operate as **infrastructure**, not just software.

---

---

## System Architecture Diagram

<p align="center">
  <img
    src="/assets/images/voquira-architecture.svg"
    alt="Voquira OS Architecture Diagram"
    width="100%"
  />
</p>

_This diagram shows how Voquira OS coordinates inputs, operations, AI agents, execution systems, and feedback loops._

## Summary

- Voquira OS is layered, not monolithic
- The operational model is the source of truth
- AI agents execute within constraints
- Execution systems remain replaceable
- Feedback loops keep the system accurate

This architecture allows service businesses to scale operations **without scaling chaos**.


