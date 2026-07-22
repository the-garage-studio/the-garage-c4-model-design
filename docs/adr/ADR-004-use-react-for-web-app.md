# ADR-004: Use React for the Web Applications

## Status

Accepted

## Context

The Garage provides two web interfaces:

- A public Landing Page.
- An authenticated Web Application for collectors and administrators.

The frontend framework should support reusable components, efficient state management, and communication with REST APIs.

## Decision

React with TypeScript is selected as the frontend technology for both the Landing Page and the Web Application.

React components consume the backend REST API through HTTPS while maintaining the presentation layer independent from backend business logic.

## Consequences

### Positive

- Component-based architecture.
- Strong ecosystem.
- Easy integration with REST APIs.
- Type safety through TypeScript.
- Good maintainability.

### Negative

- Initial learning curve.
- Client-side rendering may require optimization.
- State management becomes more complex as the application grows.

## Alternatives Considered

### Angular

Rejected because it introduces a larger framework and additional complexity for the project scope.

### Vue.js

Rejected because React provides broader community support and ecosystem familiarity for the development team.

### Server-side rendered pages

Rejected because the application requires rich client-side interactions.

## Related Artifacts

- Container Diagram
- Web Application Container
- Landing Page Container