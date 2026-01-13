---
layout: docs
title: Scheduling
---

## Scheduling in Voquira OS

Scheduling is where Jobs become executable.

In Voquira OS, scheduling is not a calendar feature. It is an **operational system** that balances capacity, constraints, and real-world conditions to ensure Jobs are completed efficiently and reliably.

The goal of scheduling is simple:
> Put the right work, with the right people, at the right time.

---

## What Scheduling Represents

Scheduling answers four operational questions:

1. **When** should this Job be done?
2. **Who** should do it?
3. **In what order** should Jobs be executed?
4. **Under what constraints** must it operate?

Scheduling exists to support execution—not to create administrative overhead.

---

## Scheduling vs Calendar Events

Voquira OS deliberately separates scheduling from generic calendar concepts.

- Calendar events are static
- Schedules are **dynamic and constraint-aware**
- A schedule may change based on new information

A scheduled Job remains a Job.  
The schedule is an execution plan layered on top.

---

## Crews and Technicians

Scheduling operates against **resources**.

### Crews
- Groups of workers executing Jobs together
- Common in landscaping and commercial services
- Capacity-based (crew size, equipment, route)

### Technicians
- Individual operators with specific skills
- Common in plumbing, HVAC, pest control
- Skill- and certification-aware

Voquira OS supports both models without fragmentation.

---

## Time Windows and SLAs

Jobs may include time constraints such as:

- Customer availability windows
- Service-level agreements (SLAs)
- Regulatory or compliance deadlines

Scheduling respects these constraints first, then optimizes within them.

A Job that violates its SLA is considered operationally critical.

---

## Recurring Scheduling

Many service businesses rely on recurring work.

Examples:
- Weekly lawn maintenance
- Monthly pest treatments
- Quarterly inspections

In Voquira OS:
- Recurrence defines **intent**
- Each occurrence generates a **Visit**
- Visits are scheduled independently when necessary

This allows flexibility without breaking the Job model.

---

## Route-Aware Scheduling

For route-based businesses, efficiency is geographic.

Scheduling may account for:
- Job proximity
- Travel time
- Route density
- Start and end locations

This is especially critical for:
- Landscaping
- Pest control
- Commercial service routes

Voquira OS treats routing as a first-class scheduling concern.

---

## Scheduling Constraints

Scheduling must respect real-world limits.

Common constraints include:
- Crew availability
- Technician skills
- Equipment requirements
- Weather conditions
- Business hours
- Regulatory rules

Constraints are **inputs**, not exceptions.

The system assumes they exist and schedules accordingly.

---

## Scheduling States

A scheduled Job may move through scheduling-specific states:

- **Unscheduled**
- **Scheduled**
- **Rescheduled**
- **Blocked**
- **Released**

These states are distinct from Job lifecycle states and allow operational visibility without altering Job intent.

---

## Manual vs Automated Scheduling

Voquira OS supports both approaches.

### Manual Scheduling
- Dispatcher assigns Jobs directly
- Useful for edge cases and emergencies

### Automated Scheduling
- Rules and AI agents assign Jobs
- Optimizes for capacity, routes, and SLAs

Automation handles the majority of work. Humans intervene when judgment is required.

---

## Scheduling and AI Agents

AI agents operate on scheduling data, not calendars.

Examples:
- Scheduling Agent resolves conflicts
- Optimization Agent improves route density
- Dispatcher Agent reallocates Jobs based on delays
- Weather Agent adjusts schedules proactively

Agents act continuously, not on demand.

---

## Failure Handling

Schedules change. Systems must adapt.

When a schedule fails:
- Job is not lost
- Status reflects reality
- Agents and workflows respond
- Customers and crews are notified

Voquira OS prioritizes recovery over perfection.

---

## Design Principle

Scheduling is not about filling time slots.

It is about:
- Respecting constraints
- Preserving flexibility
- Maximizing execution reliability

Voquira OS treats scheduling as a living system, not a static plan.

---

## Summary

- Scheduling turns Jobs into executable work
- It balances time, people, and constraints
- Routing and recurrence are native concepts
- Automation handles scale; humans handle exceptions

Without scheduling, Jobs are intent.  
With scheduling, Jobs become operations.
