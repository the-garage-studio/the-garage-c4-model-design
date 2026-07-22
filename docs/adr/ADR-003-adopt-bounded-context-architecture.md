# ADR-003: Adopt Domain-Driven Design with Bounded Contexts

## Status

Accepted

## Context

The Garage includes several business domains such as authentication, catalog management, collections, subscriptions, marketplace, wallet, notifications, and administration.

Implementing all business logic inside a single module would increase coupling and make maintenance more difficult.

## Decision

The backend is organized into independent bounded contexts following Domain-Driven Design principles.

Each bounded context owns its domain model, business rules, repositories, and services. Communication between bounded contexts is performed through well-defined interfaces and Anti-Corruption Layers (ACLs) when required.

## Consequences

### Positive

- High cohesion.
- Low coupling.
- Easier maintenance.
- Independent evolution of business domains.
- Improved scalability.

### Negative

- More architectural complexity.
- Additional interfaces between contexts.
- Increased number of classes.

## Alternatives Considered

### Layered architecture without bounded contexts

Rejected because business responsibilities become mixed as the system grows.

### Single domain model

Rejected because it creates excessive coupling between unrelated modules.

## Related Artifacts

- Container Diagram
- Component Diagrams
- Class Diagrams