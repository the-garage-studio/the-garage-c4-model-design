# ADR-006: Use Bounded Contexts Following Domain-Driven Design

## Status

Accepted

## Context

The Garage includes several business capabilities such as authentication, catalog management, trading, subscriptions, wallet operations, notifications, and administration.

Implementing all business logic inside a single module would increase coupling and reduce maintainability.

## Decision

The backend will be organized into the following bounded contexts:

- Identity & Access
- Catalog
- Collection
- Marketplace
- Subscription
- Wallet
- Notifications
- Administration

Each bounded context owns its domain model and business rules.

## Consequences

### Positive

- High cohesion.
- Better scalability.
- Easier maintenance.
- Independent evolution of business domains.

### Negative

- Requires defining clear boundaries.
- Communication between contexts becomes more complex.