# PoliForge FAQ

This FAQ addresses common questions from potential contributors, campaign staff, civic tech enthusiasts, and anyone interested in what PoliForge is, what it isn't, and how to get involved.

---

## ❓ What is PoliForge?

PoliForge is an open-source, modular, AI-powered platform for political campaigns. It automates research, messaging, outreach, and strategy, giving grassroots candidates access to the tools and infrastructure normally available only to major campaigns.

---

## ❓ Who is PoliForge for?

- Candidates running for local, state, or national office
- Campaign staff, strategists, and volunteers
- Engineers and designers interested in civic technology
- Researchers and activists seeking systemic political change

PoliForge is not for PACs, lobbyists, or profit-driven political consultants.

---

## ❓ Is this a partisan project?

No. PoliForge is politically neutral by design. The system has no ideological position, and its outputs are shaped by the data and campaign input it receives.

The mission is to lower the barrier to entry for everyone — regardless of party — and return the mechanics of political power to The People.

---

## ❓ What does PoliForge actually do?

- Scrapes and analyzes legislation, district data, and local news
- Suggests policy alignments based on constituent sentiment
- Drafts messaging: speeches, tweets, press releases, and more
- Generates outreach materials like flyers, volunteer emails, and Q&A scripts
- Identifies points of weakness in opponent campaigns using public data
- Helps with compliance, documentation, and campaign transparency

---

## ❓ What technologies does PoliForge use?

PoliForge uses:
- Docker and Kubernetes for orchestration
- A microservice architecture, with services in Node.js, Python, Go, and C#
- OpenAI-compatible LLM tooling (with optional self-hosted inference)
- RAG pipelines for news, legislation, and issue summarization
- PostgreSQL, MongoDB, and Redis for data storage

---

## ❓ Is this a chatbot?

No. PoliForge is a full-stack, multi-service system. It includes AI-generated outputs but also workflows, dashboards, analytics, and traditional software infrastructure. One component (`voterbot`) is conversational, but the overall system is far more comprehensive.

---

## ❓ Can this help me win an election?

PoliForge is a **force multiplier**, not a silver bullet. It helps you:
- Spend less time on logistics and more time connecting with voters
- Make data-informed decisions rather than guessing
- Compete with opponents who have large teams and budgets

You still need integrity, ideas, and community support.

---

## ❓ Can this be used for unethical campaigns?

It could — just like any tool. PoliForge encourages transparency and evidence-backed messaging, but cannot enforce ethics. However, its audit trails, receipts system, and modular design make it easier to **detect abuse** than traditional black-box campaigns.

We welcome feedback on ethical guardrails.

---

## ❓ How do I contribute?

- Start with the central `README.md` and `CONTRIBUTING.md`
- Choose a service repo to fork and explore
- Join an open issue or file one yourself
- Share ideas, research, or critiques in GitHub Discussions (TBD)

---

## ❓ Is there a live version?

Not yet. We are currently in the architecture and development phase. Deployment instructions and hosted demos will follow once the core services are stable.

---

## ❓ Can I use this in a real campaign?

Eventually, yes. As soon as services stabilize and pass basic security and compliance checks, PoliForge will be available for real-world use. You can help accelerate that by contributing to testing, documentation, and pilot feedback.

---

## ❓ What’s the long-term vision?

See `docs/vision.md` — but in short:
- Make running for office easier, cheaper, and more data-informed
- Rebuild trust through transparency
- Let communities build, run, and win their own campaigns

---

_For additional questions, feel free to open a GitHub Issue or contact the project maintainer._

