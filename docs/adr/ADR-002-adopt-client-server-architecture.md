# ADR-002: Adopt a Client–Server Architecture

## Status

Accepted

## Context

The Garage must support different user roles, including visitors, collectors, and administrators. The platform also integrates with external services such as Stripe and an Email Service while exposing its functionality through a web interface.

A distributed architecture is required to separate presentation, business logic, and data persistence.

## Decision

The system adopts a web-based client–server architecture.

Users interact through web clients that communicate with a REST API. The backend implements the business rules and manages persistence in a relational database while integrating with external providers.

## Consequences

### Positive

- Clear separation of concerns.
- Independent evolution of frontend and backend.
- Simplifies integrations with external services.
- Accessible from any modern browser.

### Negative

- Requires network communication.
- Depends on API availability.
- Authentication and API security become critical.

## Alternatives Considered

### Desktop application

Rejected because it requires installation and limits accessibility.

### Mobile-only application

Rejected because administrators require desktop-oriented management capabilities.

### Monolithic local application

Rejected because it does not support distributed access.

## Related Artifacts

- System Context Diagram
- Container Diagram