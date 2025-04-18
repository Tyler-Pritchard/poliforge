# PoliForge Development Roadmap

This document outlines the current and planned development milestones for the PoliForge platform. It is meant to provide transparency to contributors and the community about where the project is headed and how to get involved.

---

## ✅ Phase 0: Foundation Planning (Complete)

- ✅ Define vision and scope (`vision.md`)
- ✅ Identify campaign functions that can be digitized
- ✅ Map campaign roles to software responsibilities (`roles.md`)
- ✅ Architect core services and boundaries (`architecture.md`)
- ✅ Draft project-level documentation (`README.md`, `CONTRIBUTING.md`, etc.)

---

## 🚧 Phase 1: MVP Prototypes (In Progress)

### Candidate-Facing Services
- [ ] Build `candidate-service` (profile, voice, speech drafts)
- [ ] Build `campaign-service` (calendar, messaging, fundraising coordination)
- [ ] Build `constituency-intel` service (demographics, issue analysis)

### Infra / DevOps
- [ ] Setup API Gateway or reverse proxy (NGINX, Fastify, etc.)
- [ ] Create full Docker environment with `docker-compose`
- [ ] Standardize environment variable & secrets strategy

### Documentation
- ✅ Central `README.md`
- ✅ `CONTRIBUTING.md`, `architecture.md`, `vision.md`, `roles.md`, `faq.md`
- [ ] Add service-specific READMEs

---

## 🧠 Phase 2: AI Integration + RAG Pipelines

- [ ] Implement LLM generation templates per service
- [ ] Build RAG pipeline for `constituency-intel` (news, census, legislation)
- [ ] Create prompt libraries tuned for tone, position alignment
- [ ] Develop AI drafting engine (emails, speeches, posts)
- [ ] Build receipts engine for opposition content (screenshots, citations, logs)

---

## 🧩 Phase 3: Feature Expansion

- [ ] `counter-campaign`: analyze opponents, generate contrast material
- [ ] `media-manager`: automate flyer, graphic, and deck creation
- [ ] `volunteer-mobilizer`: manage events, SMS/email outreach
- [ ] `voterbot`: conversational Q&A and voter-facing messaging

---

## 📦 Phase 4: Deployment Readiness

- [ ] Create Helm charts & k8s manifests
- [ ] Add Prometheus/Grafana monitoring & logging stack
- [ ] Finalize CI/CD with GitHub Actions + tests
- [ ] Build SaaS-friendly deployment script & self-hosting CLI
- [ ] Draft usage/ethics guidelines & production deployment checklist

---

## 🌍 Phase 5: Pilots + Launch

- [ ] Run demo campaign simulation for testing & feedback
- [ ] Pilot with small local or grassroots campaign team
- [ ] Publish findings from pilots
- [ ] Promote usage for 2026 campaign season (midterms, city council, etc.)
- [ ] Formalize contributor community and open governance model

---

This roadmap will evolve. Feedback and proposals welcome via GitHub Issues or Discussions.

