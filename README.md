# Hi, I'm Rohan Anthony

**Backend & Distributed Systems Engineer (ex-IBM)**  
MSc Data Science — University of Bristol

I design and build distributed backend systems with a focus on reliability, delivery guarantees, and correctness.

At IBM, I worked on event-driven security infrastructure designed for operation across 10k+ endpoints, implementing versioned policy evaluation, content-addressable deduplication, and at-least-once delivery semantics.

My technical interests include:

- Agent architectures  
- Event-driven systems  
- Secure communication (TLS / mTLS)  
- Persistence and delivery guarantees  
- Applied ML where it strengthens system capability  

---

## 🚀 Featured Projects

### 🛡️ Sentinel — Windows Security Agent (C++)

A production-style Windows posture agent modeling real-world distributed endpoint architecture.

**Core capabilities**

- osquery-based posture checks  
- SQL + Lua rule evaluation engine  
- Policy evaluation with local persistence  
- SHA-256 content-addressable deduplication  
- Durable retry queue with exponential backoff and crash recovery  
- HTTP delivery with idempotent backend (hash verification, 409 on duplicates)  
- SQLite-backed offline-first storage  

**Design focus**

- Persist-before-send: delivery intent survives agent crashes  
- Exponential backoff with jitter (1s → 300s cap)  
- Interface-based delivery abstraction (HTTP shipped, MQTT planned)  
- Content-addressable deduplication across agent and backend  
- Clear separation between collection, evaluation, persistence, and delivery  

**Next:** Go aggregation service (Prometheus, Docker Compose) → MQTT delivery client → load simulation

Repo: https://github.com/rohan2107/Sentinel

---

### 🏋️ Gym-Bro — Offline-First Fitness Platform

A production-ready full-stack fitness tracking application built for daily use.

**Architecture**

- FastAPI backend (REST APIs, SQLModel, PostgreSQL)  
- React + TypeScript frontend (mobile-first PWA)  
- Google OAuth 2.0 authentication with JWT  
- Offline-first sync via service workers  
- CI pipeline with backend and frontend test coverage  

**Next:** AI meal photo logging (Google Vision + USDA nutrition API) — backend complete, frontend in progress

**Engineering emphasis**

- Multi-tenant data isolation  
- Rate limiting for external API usage  
- Database migrations with Alembic  
- Test-driven backend development  

Repo: https://github.com/rohan2107/gym-bro

---

### 🤖 Fraud Detection API — Anomaly Detection Service

A REST-exposed anomaly detection service focused on clean model serving.

- Isolation Forest–based fraud detection  
- Feature preprocessing and evaluation pipeline  
- FastAPI `/predict` endpoint  
- Dockerised deployment  

Repo: https://github.com/rohan2107/fraud-detection

---

## 🔧 Technical Stack

**Languages**  
C++, Java, Go, Python, SQL  

**Distributed Systems & Protocols**  
Kafka, MQTT, TLS / mTLS, REST APIs, event-driven architecture, at-least-once delivery semantics, exponential backoff

**Cloud & Infrastructure**  
AWS (EC2, ASG, S3, SQS), Docker, Kubernetes, CI/CD (GitHub Actions, Jenkins)  

**Data & Storage**  
PostgreSQL, SQLite, content-addressable hashing (SHA-256)  

**ML & Analytics**  
scikit-learn, Pandas, NumPy, Elastic Net, Random Forests, cross-validation  

**Other Tools**  
osquery, Lua, Git, R (tidyverse, caret)

---

## 💼 Experience

### Software Engineer — IBM Security (2023–2025)

- Architected event-driven posture system designed for 10k+ endpoints  
- Implemented SHA-256 deduplication to reduce network traffic  
- Built versioned SQL + Lua policy engine with idempotent updates  
- Implemented offline queueing with retry semantics  
- Developed Kafka-based ingestion pipelines  
- Built Kubernetes Operator for service lifecycle automation  

### Software Engineering Intern — IBM Cloud (2023)

- Developed Java and Node.js microservices for billing and orchestration  
- Authored OpenAPI documentation and implemented scheduled jobs  

---

## 🎓 Education

**MSc Data Science — University of Bristol (2025–2026)**  
Large Scale Data Engineering, Statistical Computing, AI and Text Analytics  

- Built ML pipelines in R (Elastic Net + tuned Random Forest, F1 = 0.787)  
- Deployed AWS micro-application with SQS-driven Auto Scaling  

**B.Tech, Electronics & Communication Engineering — MIT Manipal (2023)**

---

## 📫 Connect

LinkedIn: https://linkedin.com/in/rohan-anthony-9b03bb210  
GitHub: https://github.com/rohan2107  
Email: rohan.anthony2107@gmail.com
