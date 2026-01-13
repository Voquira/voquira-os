---
layout: docs
title: Landscaping
---

## Landscaping Operations in Voquira OS

Landscaping businesses operate on volume, consistency, and efficiency.  
Voquira OS is designed to support **route-based, recurring field work** while adapting to seasonal demand and property-level complexity.

This document outlines how Voquira OS models landscaping operations without forcing generic field-service assumptions.

---

## Core Characteristics of Landscaping Operations

Landscaping differs from many service industries in key ways:

- High job volume
- Strong reliance on recurring services
- Route density matters more than individual appointment times
- Crews operate as units, not individuals
- Seasonality impacts workload, staffing, and pricing

Voquira OS accounts for these realities at the system level.

---

## Jobs in Landscaping

In landscaping, Jobs typically represent **service agreements**, not single visits.

Examples:
- Weekly lawn maintenance
- Bi-weekly commercial grounds care
- Seasonal cleanup services
- One-time enhancement projects

A Job defines **what service is promised**.  
Each execution of that service is a **Visit** generated from the Job.

---

## Visits and Recurring Services

Recurring landscaping work is modeled as:

- One Job  
- Multiple Visits  

Each Visit:
- Can be scheduled independently
- May be skipped, rescheduled, or adjusted
- Retains history without altering the Job definition

This allows flexibility while preserving contract intent.

---

## Route-Based Scheduling

Efficiency in landscaping is geographic.

Voquira OS scheduling prioritizes:
- Property proximity
- Route continuity
- Crew start/end locations
- Travel time minimization

Schedules are evaluated as **routes**, not isolated appointments.

This improves:
- Fuel efficiency
- Crew productivity
- Completion reliability

---

## Crews as First-Class Resources

Landscaping work is executed by **crews**, not individuals.

Crew definitions include:
- Crew size
- Assigned equipment
- Capability profile (maintenance vs enhancements)
- Typical route assignments

Scheduling assigns Jobs to crews as units, respecting capacity and equipment constraints.

---

## Property-Centric Customers

Landscaping customers are often **properties**, not people.

Examples:
- HOAs
- Commercial properties
- Multi-site clients

Voquira OS supports:
- One customer → many properties
- Property-level service history
- Property-specific instructions and constraints

This is critical for commercial and HOA operations.

---

## Seasonal Workflows

Seasonality is not an edge case—it is a core operating condition.

Voquira OS supports:
- Seasonal activation/deactivation of Jobs
- Temporary service frequency changes
- Staffing and capacity adjustments
- Weather-based scheduling rules

Seasonal logic lives in workflows and agents, not hardcoded assumptions.

---

## Job Prioritization

Not all landscaping Jobs are equal.

Common prioritization rules:
- Commercial before residential
- HOA routes before one-off work
- Weather-sensitive services first

Voquira OS allows prioritization rules without breaking scheduling logic.

---

## Invoicing and Billing

Landscaping billing models vary:

- Per-visit billing
- Monthly flat-rate contracts
- Seasonal packages
- Project-based invoicing

Voquira OS decouples **Job execution** from **billing logic**, allowing flexible invoicing without compromising operations.

---

## Automation Opportunities

Landscaping operations benefit heavily from automation.

Common automations include:
- Auto-generating Visits from recurring Jobs
- Route optimization
- Invoice generation on Visit completion
- Missed Visit alerts
- Weather-based schedule adjustments

These automations operate on Jobs and Visits—not spreadsheets.

---

## AI Agents in Landscaping

AI agents enhance execution rather than replace crews.

Examples:
- Route Optimization Agent improves daily efficiency
- Scheduling Agent balances workload across crews
- AR Agent tracks completed Visits awaiting billing
- Customer Comms Agent sends service notifications

Agents operate continuously, responding to operational events.

---

## Design Principle

Voquira OS does not attempt to micromanage landscaping businesses.

Instead:
- Jobs define intent
- Visits define execution
- Crews define capacity
- Routes define efficiency

The system adapts to how landscaping businesses actually work.

---

## Summary

- Landscaping is volume-driven and route-sensitive
- Jobs represent service agreements
- Visits represent execution
- Crews and routes are first-class concepts
- Seasonality is built into workflows, not bolted on

Voquira OS treats landscaping as a system—not a scheduling problem.
