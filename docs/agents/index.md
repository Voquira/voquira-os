---
layout: docs
title: AI Agents
---

## AI Agents in Voquira OS

In Voquira OS, AI agents are **operators**, not assistants.

They do not chat.  
They do not brainstorm.  
They do not replace human judgment.

They **execute operational responsibilities** continuously based on system events, rules, and real-time data.

---

## What an AI Agent Is

An AI agent in Voquira OS is a long-running operational role with:

- A defined responsibility
- Clear inputs and outputs
- Authority to act within constraints
- Continuous execution (not on demand)

Agents observe Jobs, Schedules, Visits, and Financial states and act when conditions are met.

---

## What AI Agents Are Not

To be explicit, AI agents are **not**:

- Chatbots
- Virtual employees
- Decision makers without guardrails
- Free-form LLM prompts

They are **controlled execution layers** embedded into operations.

---

## Core Design Principles

All Voquira OS agents follow these principles:

1. **Event-Driven** – Agents react to system events
2. **Constraint-Aware** – Agents respect rules and limits
3. **Auditable** – Every action is logged
4. **Reversible** – Humans can override outcomes
5. **Scoped** – Each agent has a single responsibility

This keeps the system safe, predictable, and scalable.

---

## Core AI Agents

Voquira OS defines a standard set of agents that can be enabled or extended per industry.

---

## Dispatcher Agent

### Responsibility
Assign Jobs to the appropriate crew or technician.

### Inputs
- Job priority
- Job type
- Location
- Technician / crew availability
- Skill and certification data

### Actions
- Assign Jobs automatically
- Reassign Jobs when schedules change
- Escalate conflicts to humans

### Example
> A high-priority plumbing Job is created after hours.  
> The Dispatcher Agent assigns it to the on-call technician and updates the schedule immediately.

---

## Scheduling Optimizer Agent

### Responsibility
Optimize schedules for efficiency and reliability.

### Inputs
- Existing schedules
- Route density
- Time windows
- Capacity constraints
- Weather data (when applicable)

### Actions
- Reorder Jobs to improve routing
- Resolve schedule conflicts
- Suggest or execute rescheduling

### Example
> A landscaping route becomes inefficient due to a cancellation.  
> The Scheduling Agent reorders remaining Jobs to reduce travel time.

---

## Accounts Receivable (AR) Agent

### Responsibility
Ensure completed work gets billed and paid.

### Inputs
- Job completion events
- Invoice status
- Payment terms
- Aging data

### Actions
- Trigger invoice creation
- Flag overdue invoices
- Initiate follow-up workflows

### Example
> A Job is completed but not invoiced after 24 hours.  
> The AR Agent flags the issue and triggers invoicing automatically.

---

## Customer Communications Agent

### Responsibility
Handle operational customer notifications.

### Inputs
- Job status changes
- Schedule updates
- Arrival and completion events
- Exception events

### Actions
- Send arrival windows
- Notify of delays
- Confirm completion
- Route escalations to humans

### Example
> A technician is delayed due to an emergency Job.  
> The Comms Agent notifies affected customers automatically.

---

## Compliance Agent (Industry-Specific)

### Responsibility
Ensure regulatory and documentation requirements are met.

### Inputs
- Job and Visit data
- Treatment records
- Certification data
- Industry rules

### Actions
- Flag missing documentation
- Prevent Job closure when compliance is incomplete
- Generate audit-ready records

### Example
> A pest control Visit is missing treatment documentation.  
> The Compliance Agent blocks Job closure until resolved.

---

## How Agents Interact

Agents do not operate in isolation.

Example flow:
1. Job created
2. Dispatcher Agent assigns it
3. Scheduling Agent optimizes timing
4. Job completed
5. AR Agent invoices
6. Comms Agent updates customer

Each agent handles **its slice**, preventing complexity creep.

---

## Human Oversight

Humans remain in control.

- Agents can be paused
- Decisions can be overridden
- Rules can be tightened or loosened
- Execution can be limited by role or dollar value

Voquira OS treats AI as **infrastructure**, not autonomy.

---

## Why This Matters

Most “AI tools” assist with thinking.

Voquira OS agents:
- Reduce operational drag
- Eliminate manual follow-ups
- Enforce consistency
- Improve execution speed

They quietly run the business so humans can focus on judgment and growth.

---

## Summary

- AI agents are operational roles
- They act on Jobs, not conversations
- Each agent has a narrow responsibility
- Execution is auditable and reversible
- AI exists to run systems, not replace people

Voquira OS uses AI where it belongs: **inside operations**.
