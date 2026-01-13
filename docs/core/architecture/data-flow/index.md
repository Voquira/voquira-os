---
layout: docs
title: Data Flow
hero:
  title: End-to-End Data Flow
  subtitle: How a job moves through Voquira OS from creation to payment.
---

## Overview

This document walks through a **real operational data flow** inside Voquira OS.

Rather than describing components in isolation, it shows how **events, state, agents, and execution** interact during normal business operations.

The example below represents a common scenario across landscaping, pest control, and plumbing businesses.

---

## Scenario Overview

A customer requests service.  
The job is scheduled, executed, invoiced, and paid.

Throughout this process:
- Humans perform the work
- AI agents coordinate execution
- The system maintains operational truth

No step relies on manual follow-ups or fragile workflows.

---

## Step 1 — Job Creation (Input Event)

A job enters the system through an input source:

Examples:
- Website form submission
- Office staff creating a job
- CRM integration
- Emergency call intake

### Event Emitted
JobCreated

### What Happens
- No automation runs yet
- No assumptions are made
- The event is recorded and passed to the model

Inputs describe **what happened**, not **what to do next**.

---

## Step 2 — State Normalization (Core Model)

The Job is written into the **Core Operational Model**.

Key attributes recorded:
- Job type
- Service category
- Location
- Priority
- Customer / property
- Constraints (time windows, skills, SLAs)

At this point:
- The job exists
- Nothing is scheduled
- No execution has started

This separation prevents premature automation.

---

## Step 3 — Dispatcher Agent Activation

The creation of a job triggers the **Dispatcher Agent**.

### Agent Responsibilities
- Evaluate job priority
- Identify eligible crews or technicians
- Respect skill, certification, and availability constraints

### Agent Action
AssignJob

If no valid assignment exists, the agent escalates to a human instead of guessing.

---

## Step 4 — Scheduling Optimization

Once assigned, the **Scheduling Agent** activates.

### Inputs Considered
- Existing schedules
- Route density
- Travel time
- Job duration estimates
- Time windows

### Agent Action
ScheduleVisit

The result is a scheduled Visit tied to the Job.

Scheduling remains **adjustable**, not locked.

---

## Step 5 — Execution Begins (External Systems)

Execution happens outside Voquira OS.

Examples:
- Crew performs landscaping service
- Technician completes pest treatment
- Plumber resolves an emergency

Voquira OS does not micromanage execution.  
It **observes it**.

---

## Step 6 — Job Completion Event

When work is completed, an external signal enters the system.

### Event Emitted
VisitCompleted

The system updates:
- Job status
- Visit history
- Timestamps
- Notes or compliance artifacts

Completion is now an explicit state change.

---

## Step 7 — Accounts Receivable Agent

The completion event triggers the **AR Agent**.

### Agent Responsibilities
- Validate billing readiness
- Apply pricing rules
- Trigger invoice creation

### Agent Action
CreateInvoice

If information is missing, the agent blocks invoicing instead of guessing.

---

## Step 8 — Customer Communications Agent

In parallel, the **Customer Comms Agent** may activate.

Examples:
- Completion confirmation
- Invoice notification
- Follow-up instructions

This communication is:
- Timely
- Context-aware
- Fully automated

---

## Step 9 — Payment Received (Feedback Event)

When payment is received:

### Event Emitted
PaymentReceived

The system updates:
- Invoice status
- Job financial state
- Customer account history

This event feeds back into the model.

---

## Step 10 — Feedback Loop Closes

All outcomes:
- Completion
- Billing
- Payment
- Exceptions

Feed back into the Inputs layer.

This allows:
- Metrics to update
- Agents to adapt
- Future decisions to improve

The loop never stops.

---

## Visual Flow Summary

JobCreated
↓
Core Model Updated
↓
Dispatcher Agent
↓
Scheduling Agent
↓
Execution (External)
↓
VisitCompleted
↓
AR + Comms Agents
↓
Invoice → Payment
↓
Feedback → Model


---

## Why This Matters

This flow demonstrates that:

- No step depends on manual follow-ups
- Automation is event-driven, not brittle
- AI agents execute responsibilities, not advice
- Humans stay focused on judgment and work
- The system improves with every cycle

This is what allows Voquira OS to scale **without chaos**.

---

## Key Design Takeaways

- Events drive everything
- State is always explicit
- Agents never bypass the model
- Execution remains replaceable
- Feedback is mandatory

Most platforms stop at “job completed.”  
Voquira OS continues until the business outcome is resolved.

---

## Summary

This data flow represents the **default operational loop** inside Voquira OS.

Every industry variation builds on this same foundation.

Once you understand this flow, you understand how Voquira OS works.

