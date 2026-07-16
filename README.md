# The Garage - C4 Architecture Model

Professional software architecture repository for **The Garage**, a digital platform where users can collect, manage, and trade virtual vehicle cards through pack openings, a marketplace, personal collections, and subscription plans.

This repository contains the architectural artifacts developed using the **C4 Model** and **Structurizr DSL**. Its purpose is to document the system architecture from a high-level business perspective down to its internal software components.

---

## Project Overview

The Garage is a web platform that enables users to:

- Collect vehicle cards by opening free packs.
- Manage a personal card collection.
- Buy and sell cards through a marketplace.
- Expand collection capacity through subscription plans.
- Manage card catalogs and user permissions through administrative features.

The platform follows a modular architecture that separates business capabilities into well-defined domains to facilitate maintainability and future scalability.

---

## Repository Purpose

This repository centralizes all architecture-related artifacts for **The Garage**.

Its objectives are to:

- Document the software architecture using the C4 Model.
- Maintain architecture diagrams as code using Structurizr DSL.
- Support academic documentation.
- Provide a technical reference for implementation.
- Keep architectural decisions versioned alongside the project.

---

## Architecture Vision

The architecture is designed following the following principles:

- Domain-Driven Design (DDD)
- C4 Model
- Separation of Concerns
- Layered Architecture
- RESTful API Design
- High Cohesion and Low Coupling
- Maintainability and Scalability

---

## Technology Stack

| Layer | Technology |
|--------|------------|
| Frontend | React |
| Backend | Java Spring Boot |
| Database | MySQL |
| Authentication | JWT |
| Architecture Modeling | Structurizr DSL |
| Version Control | Git & GitHub |

---

## Planned C4 Diagrams

This repository will include the following architectural views:

- Level 1 — System Context Diagram
- Level 2 — Container Diagram
- Level 3 — Component Diagrams

---

## Repository Structure

```
the-garage-diagrams/
│
├── diagrams/
├── exports/
├── .github/
│   └── workflows/
├── .gitignore
├── .gitattributes
├── LICENSE
└── README.md
```

---

## Git Workflow

### Branching Strategy

```
main
develop
feature/*
```

### Conventional Commits

Examples:

```
feat: initialize Structurizr workspace
feat: add system context diagram
docs: update repository documentation
refactor: reorganize diagram structure
chore: configure GitHub Actions
```

---

## Roadmap

- [ ] Configure Structurizr DSL workspace
- [ ] Create System Context Diagram
- [ ] Create Container Diagram
- [ ] Create Component Diagrams
- [ ] Automate diagram exports using GitHub Actions

---

## Contributors

Developed by the **The Garage Studio** project team.

---

## License

This project is licensed under the MIT License.