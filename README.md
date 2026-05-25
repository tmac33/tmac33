### Hi, I'm Cosmo 👋

**Senior Backend Engineer · Go · Distributed Systems**
📍 Auckland, New Zealand · 🌐 [tmac33.top](https://www.tmac33.top) · ✉️ therealtmac33@gmail.com

---

I build backend platforms that orchestrate complex, multi-party systems — telecom provisioning, number portability, wholesale APIs. 10+ years of experience, currently focused on Go, gRPC, and GCP-native architectures.

#### 🛠️ What I work with daily

- **Languages:** Go, Python, Rust (learning), C#
- **APIs:** gRPC, Protocol Buffers, grpc-gateway, REST, SOAP/WSDL, TMF Open APIs
- **Cloud:** GCP (Cloud Run, BigTable, Pub/Sub, Firestore, BigQuery), Docker, Terraform
- **Databases:** PostgreSQL, MySQL, BigTable, Firestore
- **Observability:** Datadog, Jaeger, OpenCensus, Prometheus, Sentry
- **Patterns:** Microservices, event-driven, saga / compensating transactions, state machines, multi-tenancy

#### 🚀 Recent work

Most of my production work lives behind enterprise repos, so here's a summary of the systems I've designed and shipped:

- **UFB Product Service** *(One New Zealand, 2024–present)* — Tech lead for the central orchestration layer for Ultra-Fast Broadband provisioning on One NZ's wholesale NaaS platform. Designed end-to-end provisioning architecture across 7 microservices and 4 LFC operators (Chorus, Enable, Northpower, UFF), serving ~40 RSPs nationally. Synchronous saga with `defer`-based deterministic rollback across 5+ downstream gRPC services.

- **NZ Mobile Number Portability** *(IQ Hive / Vodafone NZ, 2022–2024)* — Implemented the full NZ TCF LMNP protocol as a dual-interface gRPC server. 13 port scenarios, characteristic-based state machine, two-phase inter-carrier activation with atomic MSISDN cutover at RFS. Replaced two legacy porting platforms.

- **Mobile Postpay & FWA Product Services** — Distributed saga provisioning for multi-resource allocation (MSISDN, OCS, Cellular, IPv4, SIM) with cascaded compensating transactions across 17 downstream gRPC integrations. `context.WithoutCancel` rollback ensures cleanup after client disconnect.

#### 🔭 Currently exploring

- Authentication protocols (OAuth, OIDC, SAML) and identity systems
- Postgres at scale — schema migrations, multi-tenant patterns
- Rust for systems-level work

#### 📫 Get in touch

Open to senior backend / staff engineer roles, especially fully-remote teams working on developer infrastructure, identity, or distributed systems.

→ [LinkedIn](https://www.linkedin.com/in/cosmo-wu) · [Blog](https://www.tmac33.top) · therealtmac33@gmail.com

