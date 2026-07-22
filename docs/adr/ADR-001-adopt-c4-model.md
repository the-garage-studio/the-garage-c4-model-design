# ADR-001: Adopt the C4 Model for Architecture Documentation

## Status

Accepted

## Context

The Garage is composed of multiple architectural elements, including frontend applications, backend services, databases, external systems, and several bounded contexts. As the project evolves, the development team requires a documentation approach that clearly communicates the architecture to developers, reviewers, and stakeholders while remaining easy to maintain alongside the source code.

## Decision

The project adopts the C4 Model as the standard for documenting its software architecture.

The architecture will be represented using four hierarchical levels:

- System Context Diagram
- Container Diagram
- Component Diagrams
- Class Diagrams

All diagrams are maintained as PlantUML source files and automatically exported as PNG images through a GitHub Actions workflow.

## Consequences

### Positive

- Architecture documentation is easy to understand.
- Multiple abstraction levels are available for different audiences.
- Diagrams remain version-controlled together with the source code.
- Documentation can be automatically regenerated.

### Negative

- Additional effort is required to keep diagrams synchronized with implementation.
- Contributors must understand the C4 Model notation.

## Alternatives Considered

### UML-only documentation

Rejected because UML diagrams alone do not provide a progressive architectural view.

### Informal documentation

Rejected because it is difficult to maintain and quickly becomes outdated.

## Related Artifacts

- System Context Diagram
- Container Diagram
- Component Diagrams
- Class Diagrams