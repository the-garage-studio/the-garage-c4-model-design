# ADR-005: Adopt a Layered Architecture in the Backend

## Status

Accepted

## Context

The Garage is expected to support several business capabilities, including identity and access management, catalog management, card collections, marketplace trading, subscriptions, wallet management, notifications, and administration.

Although these capabilities represent different business domains, the expected project size, team size, and deployment requirements do not justify the operational complexity introduced by a microservices architecture.

The architecture should provide clear separation of responsibilities while maintaining a simple deployment model.

## Decision

The system will be implemented as a Modular Monolith following Domain-Driven Design (DDD) principles.

Each business capability will be implemented as an independent Bounded Context, encapsulating its own:

- Domain Model
- Application Services
- Repositories
- Domain Events
- Infrastructure components

Communication between bounded contexts will occur through well-defined interfaces and Anti-Corruption Layers (ACLs), avoiding direct access to another module's internal implementation.

All modules will be packaged and deployed as a single Spring Boot application.

## Consequences

### Positive

- Simple deployment and infrastructure.
- Lower operational cost.
- Clear separation of business domains.
- Easier maintenance and testing.
- Reduced coupling between modules.
- Future migration to microservices remains possible because module boundaries are explicitly defined.

### Negative

- All modules share the same deployment lifecycle.
- Poor discipline could lead to unwanted dependencies between modules.
- Runtime scalability is limited to scaling the entire application.