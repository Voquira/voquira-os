---
layout: docs
title: Pest Control
---

## Pest Control Operations in Voquira OS

Pest control operations balance compliance, repeatability, and responsiveness.  
Voquira OS models pest control as a **treatment-centric, history-aware service system** designed to handle recurring treatments, inspections, and reactive calls without operational drift.

This document describes how Voquira OS supports pest control businesses at scale.

---

## Core Characteristics of Pest Control Operations

Pest control differs from other service industries in several ways:

- Regulatory and compliance requirements
- Treatment history matters
- Follow-up visits are common
- Mix of recurring contracts and reactive calls
- Technician skill and certification constraints

Voquira OS treats these as **core system concerns**, not edge cases.

---

## Jobs in Pest Control

In pest control, Jobs typically represent a **treatment agreement or service intent**.

Examples:
- Monthly residential pest service
- Quarterly commercial inspections
- One-time infestation treatment
- Emergency response calls

A Job defines the **scope of pest management**, not just a single visit.

---

## Visits and Treatment History

Each Job generates **Visits** that represent individual treatments or inspections.

Each Visit records:
- Treatment type
- Chemicals or methods used
- Technician notes
- Compliance artifacts (when required)

Visit history is preserved and referenced for future scheduling and compliance checks.

---

## Recurring Services and Follow-Ups

Recurring pest control Jobs are common and expected.

Voquira OS supports:
- Fixed schedules (monthly, quarterly)
- Conditional follow-ups
- Escalation logic for unresolved issues

A follow-up Visit can be automatically generated based on inspection results or customer reports.

---

## Compliance and Documentation

Many pest control operations require:
- Treatment logs
- Technician certifications
- Inspection records
- Audit-ready history

Voquira OS stores compliance data **alongside the Job and Visit**, ensuring traceability without duplicating systems.

---

## Technician-Centric Scheduling

Pest control is typically technician-based, not crew-based.

Scheduling accounts for:
- Certifications and licensing
- Treatment type authorization
- Geographic coverage
- Availability windows

Jobs are assigned only to qualified technicians by design.

---

## Priority and Risk Handling

Certain pest issues require faster response:
- Health-related infestations
- Commercial compliance risks
- Repeat unresolved treatments

Voquira OS allows priority escalation without breaking scheduling integrity.

---

## Invoicing and Billing

Common pest control billing models:
- Monthly service plans
- Per-visit billing
- Commercial contracts
- One-time treatments

Billing is triggered by Visit completion, inspection outcomes, or contractual rules.

---

## Automation Opportunities

High-impact pest control automations include:
- Automatic Visit generation
- Follow-up scheduling after inspections
- Compliance reminders
- Treatment history validation
- Invoice generation on completion

Automation reduces administrative overhead while preserving accuracy.

---

## AI Agents in Pest Control

AI agents operate on Jobs and Visits.

Examples:
- Scheduling Agent balances technician workload
- Compliance Agent monitors documentation gaps
- AR Agent tracks completed treatments awaiting billing
- Customer Comms Agent handles service notifications

Agents act continuously and proactively.

---

## Design Principle

Voquira OS does not attempt to replace technician expertise.

Instead:
- Jobs define intent
- Visits define treatment
- History defines intelligence
- Automation ensures consistency

---

## Summary

- Pest control is treatment-centric and history-aware
- Jobs represent service agreements
- Visits capture execution and compliance
- Technicians are primary scheduling resources
- Automation ensures repeatability and accuracy

Voquira OS treats pest control as a regulated operational system—not just appointments.
