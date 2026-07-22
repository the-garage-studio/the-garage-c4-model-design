# ADR-007: Communicate Between Bounded Contexts Using Anti-Corruption Layers

## Status

Accepted

## Context

Several bounded contexts require functionality owned by other contexts.

For example:

- Marketplace requires Wallet.
- Marketplace requires Collection.
- Collection requires Catalog.
- Administration interacts with multiple contexts.

Direct dependencies would tightly couple the domains.

## Decision

Communication between bounded contexts will occur through Anti-Corruption Layers (ACLs).

Each ACL exposes only the operations required by the consuming bounded context while hiding the internal implementation of the provider.

## Consequences

### Positive

- Reduced coupling.
- Clear ownership of business rules.
- Independent evolution of bounded contexts.
- Easier replacement of implementations.

### Negative

- Additional interfaces must be maintained.
- Slight increase in implementation complexity.