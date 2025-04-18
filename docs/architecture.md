# PoliForge Architecture Overview

This document outlines the high-level architecture of **PoliForge**, a modular, microservice-based platform designed to support political campaigns through AI-powered automation, strategic intelligence, and civic infrastructure tooling.

---

## 🧱 Architectural Philosophy

PoliForge follows key principles of modern systems architecture:

- **Microservice Boundaries**: Each campaign function is encapsulated in its own domain-driven service.
- **Loose Coupling, Strong Contracts**: Services communicate via well-defined APIs and message contracts.
- **Composability**: Users can deploy a single service, a subset, or the full stack.
- **Portability**: All services support Docker-based deployment, with Kubernetes orchestration.
- **Transparency**: All internal decisions, AI outputs, and workflows are inspectable.

---

## 🗺️ Core Services

| Service | Purpose |
|---------|---------|
| `candidate-service` | Manages candidate profile, preferences, calendar, tone, and speech reviews |
| `campaign-service` | Central orchestrator for strategy, messaging, fundraising, and coordination |
| `constituency-intel` | Collects and analyzes district data, demographics, legislation, and trends |
| `counter-campaign` | Flags opponent weaknesses, misalignments, and creates opposition content with receipts |
| `infrastructure` | Handles authentication, permissions, observability, secrets, and compliance tooling |
| `volunteer-mobilizer` | Organizes volunteer recruitment, field events, contact trees, and reminders |
| `media-manager` | Generates visuals, decks, flyers, and social assets from campaign themes |
| `voterbot` | Answers voter questions using campaign knowledge and public records (LLM-powered) |

---

## 🔄 Inter-Service Communication

- **API Gateway** (planned): Aggregates service endpoints for frontend clients
- **Internal gRPC / REST**: For service-to-service communication
- **Event Bus (optional)**: For pub-sub patterns (e.g., campaign launch triggers opposition analysis)

Each service exposes:
- REST/GraphQL endpoints (documented in OpenAPI specs)
- Healthcheck and readiness endpoints
- Auth middleware (JWT/OAuth2 compatible)

---

## 🐳 DevOps & Deployment

- **Containerization**: All services containerized with Docker
- **Orchestration**: Kubernetes manifests, Helm charts, and optional Compose setups
- **Secrets Management**: Integrates with Vault, Doppler, or SOPS (TBD)
- **Monitoring**: Prometheus/Grafana for metrics; Loki/Elastic for logs (planned)

---

## 📦 Example Stack per Service

**Language/Framework**:
- Candidate / Campaign / Infra: Node.js + TypeScript or C# + .NET Core
- Constituency & Counter: Python (scraping, ML/NLP)
- Media / VoterBot: Python or Go + LLM/FFMPEG integrations
- Gateway: Fastify or Apollo Gateway (TBD)

**Datastores**:
- PostgreSQL for relational data (e.g., events, donors)
- MongoDB for schema-flexible inputs (e.g., AI logs, text drafts)
- Redis for caching, job queues

---

## 📐 Future Architectural Features

- Role-based dashboards for Candidates, Staff, and Volunteers
- Plugin support for local legislation scrapers or alternate frontends
- Cloud deployment presets (Railway, GCP, AWS Fargate)
- CI/CD pipelines with GitHub Actions and service tests

---

## 🧭 Next Steps

- Define service-to-service API schemas and auth flows
- Create internal message schemas for AI pipelines and receipt generation
- Finalize tech stacks per service
- Implement shared code/linting guidelines

For more details on contributing, see `CONTRIBUTING.md`. To track this architecture's evolution, see `/docs/vision.md` and each service’s individual README.

---

_Last updated: April 2025_