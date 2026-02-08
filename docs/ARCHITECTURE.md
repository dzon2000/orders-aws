# Architecture Design Document

## Problem statement

Designe a serverless, event-driven system responsible for accepting customer orders via HTTP API. Backend will process the requests asynchronusly 

1. What the system does
2. What it explicitly does not do
3. Constraints (latency, cost, scale, team size)

> Design a serverless system responsible for accepting customer orders via HTTP API and making them available for downstream processing in a reliable, scalable, and cost-efficient way.

**In Scope**
- Order intake via synchronous API
- Basic validation and acceptance
- Reliable handoff to downstream systems
- Event-driven integration

**Out of scope (explicit)**
- Payment processing
- Order fulfillment
- Complex workflows
- Cross-region replication

**Success criteria**
- API responds within ≤300 ms (p95)
- No order is silently lost
- System scales without pre-provisioning
- Operational overhead remains minimal

## Constraints & Assumptions