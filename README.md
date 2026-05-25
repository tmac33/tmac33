### Hi, I'm Cosmo 👋

**Senior Backend Engineer · Go · Distributed Systems · LLM Applications**
📍 Auckland, New Zealand · 🌐 [tmac33.top](https://www.tmac33.top) · ✉️ therealtmac33@gmail.com

---

I build backend platforms that orchestrate complex, multi-party systems — telecom provisioning, number portability, wholesale APIs. 10+ years of experience, currently focused on Go, gRPC, and GCP-native architectures, with a parallel track in LLM-powered tooling and agent orchestration.

#### 🛠️ What I work with daily

- **Languages:** Go, Python, TypeScript, Rust *(learning)*, C#
- **APIs & RPC:** gRPC, Protocol Buffers, grpc-gateway, REST, SOAP/WSDL, TMF Open APIs
- **Cloud:** GCP (Cloud Run, BigTable, Pub/Sub, Firestore, BigQuery), Docker, Terraform
- **Databases:** PostgreSQL, MySQL, BigTable, Firestore — and **pgvector / LanceDB** for embeddings
- **Observability:** Datadog, Jaeger, OpenTelemetry, Prometheus, Sentry, OpenCensus
- **Patterns:** Microservices, event-driven, saga / compensating transactions, state machines, multi-tenancy

#### 🤖 LLM & agent work

I treat LLM systems with the same rigour as any other production backend — typed contracts, graceful degradation, observability, cost control. Things I've built or shipped:

- **Agent skill systems** — maintain 90+ reusable skills across two frameworks (Hermes, OpenClaw); designed the on-disk skill layout and Git-sync workflow so agents and humans share the same source of truth.
- **Multi-agent orchestration** — LangGraph / CrewAI workflows for content pipelines (research → draft → review → publish) with deterministic step boundaries instead of free-form planning loops.
- **MCP servers & Claude Skills SDK** — built tools that agents call directly; clean tool schemas, idempotent side effects, structured errors.
- **Retrieval** — pgvector for transactional metadata-adjacent search; LanceDB for local, file-backed embedding stores; hybrid retrieval (BM25 + vector) where pure semantic search underperforms.
- **Production LLM hygiene** — prompt caching / system-instruction reuse, 429-rate-limit fallbacks to local templates (real users never see a 500), function calling with strict JSON schemas, streaming responses with per-call token accounting for cost monitoring.

#### 📦 Open source

- **[go-saga](https://github.com/tmac33/go-saga)** — Tiny generic synchronous saga library for Go. Deterministic rollback, survives client disconnect via `context.WithoutCancel`, ~150 LOC, zero deps, 97% test coverage. Abstracts the pattern I've shipped to production several times for telecom provisioning.
- **[goauth-demo](https://github.com/tmac33/goauth-demo)** — Production-shaped JWT auth service. Single-use refresh-token rotation via atomic `UPDATE ... RETURNING`, bcrypt, Postgres, Prometheus + OpenTelemetry, k6 load tests with p95/p99 thresholds.

#### 🚀 Backend systems I've shipped

Most of my production work lives in private repos, so here are the systems I've designed and led:

- **UFB Product Service** *(One New Zealand, 2024–present)* — Tech lead for the central orchestration layer for Ultra-Fast Broadband provisioning on One NZ's wholesale NaaS platform. End-to-end provisioning across 7 microservices and 4 LFC operators (Chorus, Enable, Northpower, UFF), serving ~40 RSPs nationally. Synchronous saga with `defer`-based deterministic rollback across 5+ downstream gRPC services.

- **NZ Mobile Number Portability** *(IQ Hive / Vodafone NZ, 2022–2024)* — Implemented the full NZ TCF LMNP protocol as a dual-interface gRPC server. 13 port scenarios, characteristic-based state machine, two-phase inter-carrier activation with atomic MSISDN cutover at RFS. Replaced two legacy porting platforms.

- **Mobile Postpay & FWA Product Services** — Distributed saga provisioning for multi-resource allocation (MSISDN, OCS, Cellular, IPv4, SIM) with cascaded compensating transactions across 17 downstream gRPC integrations. `context.WithoutCancel` rollback ensures cleanup after client disconnect.

#### 🔭 Currently exploring

- Authentication protocols (OAuth, OIDC, SAML) and identity at scale
- Postgres operational concerns — schema migrations, multi-tenant patterns, pgvector tuning
- Rust for systems-level work
- Where the line should sit between deterministic workflows and agent autonomy

#### 📫 Get in touch

Open to senior backend / staff engineer roles, especially fully-remote teams working on developer infrastructure, identity, distributed systems, or AI-product platforms.

→ [LinkedIn](https://www.linkedin.com/in/cosmo-wu) · [Blog](https://www.tmac33.top) · therealtmac33@gmail.com
