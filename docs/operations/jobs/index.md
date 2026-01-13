---
layout: docs
title: Jobs
---

## Jobs in Voquira OS

In Voquira OS, a **Job** is the atomic unit of work.

Everything the system does—scheduling, dispatching, invoicing, automation, reporting—centers around Jobs. If you understand Jobs, you understand Voquira OS.

A Job represents **real-world service work** that must be planned, executed, and accounted for.

---

## What a Job Represents

A Job is a commitment to perform a service at a specific place, for a specific customer, under defined conditions.

Examples:
- Mowing a residential lawn
- Treating a property for pests
- Repairing a plumbing issue
- Performing a recurring commercial service
- Completing a one-time emergency call

Jobs are **not tasks** and **not calendar events**.  
They are operational records with state, ownership, and downstream impact.

---

## Job Lifecycle

Every Job in Voquira OS moves through a predictable lifecycle:

1. **Created**
   - Generated manually, via automation, or from a contract
   - Contains service intent but may not yet be scheduled

2. **Scheduled**
   - Assigned a date, time window, and crew or technician
   - May be optimized for routing or capacity

3. **In Progress**
   - Actively being executed in the field
   - Status reflects real-world work, not assumptions

4. **Completed**
   - Service work finished
   - Triggers downstream actions

5. **Invoiced**
   - Financial record generated
   - May be immediate or deferred based on rules

6. **Closed**
   - Job fully resolved
   - Retained for history, reporting, and analytics

This lifecycle is event-driven. Each state change can trigger automation or AI agents.

---

## Job vs Task vs Visit

Understanding these distinctions prevents system bloat.

### Job
- The **business unit of work**
- What customers are billed for
- What crews are accountable to complete

### Task
- Internal checklist items
- Sub-steps within a Job
- Not billable and not independently scheduled

### Visit
- A single occurrence of a Job
- Used for recurring services
- One Job can generate many Visits

Example:
- Weekly lawn service = one Job
- Each weekly appointment = a Visit
- Mow, edge, blow = Tasks

Voquira OS treats **Jobs as primary**, everything else as supporting structure.

---

## Required Job Fields

Every Job must contain the following core fields:

- **Customer**
- **Service Type**
- **Location**
- **Status**
- **Priority**
- **Assigned Crew or Technician**
- **Scheduled Window (optional at creation)**

Optional but common fields:
- Notes
- Service instructions
- Estimated duration
- Required equipment
- SLA or deadline

The system remains flexible, but Jobs must always be **operationally complete**.

---

## Industry-Specific Interpretation of Jobs

Voquira OS uses a consistent Job model, but interpretation varies by industry.

### Landscaping
- Jobs are often recurring
- Emphasis on route density and crew efficiency
- Seasonal modifiers affect frequency and scope

### Pest Control
- Jobs may include compliance requirements
- Treatment history matters
- Follow-up visits are common

### Plumbing
- Jobs are often one-time or emergency-based
- Priority and response time are critical
- Technician skill matching is essential

The same Job structure adapts without fragmentation.

---

## Jobs as Automation Triggers

Jobs are **event emitters**.

Examples:
- Job created → auto-schedule
- Job completed → generate invoice
- Job overdue → notify dispatcher
- Job reassigned → update customer

This allows Voquira OS to automate operations without hardcoding logic into the Job itself.

---

## Jobs and AI Agents

AI agents in Voquira OS operate **on Jobs**, not conversations.

Examples:
- Dispatcher Agent assigns Jobs to crews
- Scheduling Agent optimizes Job timing
- AR Agent monitors Jobs awaiting invoicing
- Comms Agent updates customers about Job status

Jobs are the shared language between humans and agents.

---

## Design Principle

Voquira OS does not attempt to model every possible edge case.

Instead:
- Jobs remain simple
- State changes are explicit
- Intelligence lives in workflows and agents

This keeps the system scalable, auditable, and adaptable.

---

## Summary

- Jobs are the core abstraction in Voquira OS
- They represent real work, not software artifacts
- Every operational system builds on them
- Automation and AI exist to serve Jobs—not replace them

If Jobs are modeled correctly, everything else becomes easier.
