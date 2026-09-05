# Rohan Anthony

Backend and distributed-systems engineer (ex-IBM Security). MSc Data Science, University of Bristol.

I build scalable backend and distributed systems with a focus on reliability, performance, and correctness, shaped by a security-engineering background at IBM. MSc Data Science thesis on Causal State Recovery in Reinforcement Learning.

**Interests:** distributed systems and delivery guarantees, event-driven architectures, security engineering (detection, TLS/mTLS), agentic AI and LLM-integrated systems, causal ML and reinforcement learning.

## Featured work

### Causal state recovery for reinforcement learning (MSc thesis)

"Recovering Causal State Variables for Reinforcement Learning via Probabilities of Necessity and Sufficiency." Solo research project across causal inference, reinforcement learning, and representation learning.

- **A benchmark where the correct answer is known.** A factored-MDP gridworld with four planted causal variables, an injected noise control, and an engineered spurious variable whose association with a genuine cause is tunable in both strength and sign, so any recovery method can be scored against ground truth.
- **An interventional oracle ("replay-PN") estimating Pearl's probability of necessity.** A state-overwrite do-operator edits the simulator mid-episode, then the recorded action sequence is replayed unchanged, isolating the world's causal response from a policy's reaction to a perturbed observation. Recovery is exact and stable across five policy seeds, two RL algorithms (PPO and TRPO), and five map layouts.
- **Located the boundary of observational recovery.** Correlation, mutual information, conditional independence, a sparse L1 gate, and an adapted CaSN objective all recover the planted set exactly through the intermediate regime, and all collapse at both deterministic endpoints, where the spurious variable becomes an exact copy or an exact inversion of the cause it shadows. At the copy endpoint the two are literally the same column of data, so no estimator restricted to that distribution can prefer one over the other. Direct intervention separates them throughout.
- **Success rate hides spurious reliance.** Under a matched evaluation differing in exactly one input channel, three of five full-observation policies depend on the spurious variable, including one that holds a 1.000 success rate while changing route on 6 of 100 episodes.
- **Reproducible by construction.** 22 experiment scripts and 14 test modules over a 14-module package, every run seeded end to end, with headline results regression-gated against recorded baselines.

Stack: Python, PyTorch, Stable-Baselines3, sb3-contrib, Gymnasium, MiniGrid, scikit-learn, pytest, ruff.

Repo: https://github.com/rohan2107/causal-state-recovery

### Sentinel (C++): endpoint security agent

A from-scratch endpoint security agent modelling production-grade distributed endpoint architecture and reliability patterns.

- osquery-based posture checks with a SQLite-backed, offline-first store.
- Sandboxed Lua rule-evaluation engine with local persistence.
- SHA-256 content-addressable deduplication across agent and backend.
- Durable retry queue with exponential backoff and jitter, and crash recovery.
- Persist-before-send delivery: delivery intent survives agent crashes.
- Interface-based delivery abstraction (HTTP shipped, MQTT planned), with an idempotent backend (hash verification, 409 on duplicates).

Next: Go aggregation service (Prometheus, Docker Compose), MQTT delivery client, load simulation.

Repo: https://github.com/rohan2107/Sentinel

### Gym-Bro: full-stack fitness platform

A full-stack fitness tracking application built end to end for daily use.

- FastAPI backend (REST APIs, SQLModel, PostgreSQL) with Alembic migrations.
- React and TypeScript mobile-first PWA with offline-first sync via service workers.
- Google OAuth 2.0 with JWT, per-user data isolation, and rate limiting on external APIs.
- AI meal logging (Google Vision plus USDA nutrition API).
- Test-driven backend, 160 automated tests, 84% backend coverage, CI with preview deploys.

Repo: https://github.com/rohan2107/gym-bro

### Fraud detection API

A REST-exposed anomaly-detection service focused on clean model serving.

- Isolation Forest fraud detection with a feature preprocessing and evaluation pipeline.
- FastAPI /predict endpoint, containerised with Docker.

Repo: https://github.com/rohan2107/fraud-detection

## Experience

### Software Engineer, IBM Security (2023 to 2025)

- Designed the data model and POC for an event-driven endpoint posture system targeting 10k+ endpoints.
- Redesigned reporting to be state-change-triggered with SHA-256 content-addressable deduplication and heartbeat liveness, cutting network traffic 95 to 98%.
- Implemented guaranteed at-least-once delivery in the C++ agent (ACK persistence, offline replay via thread-safe SQLite).
- Built a versioned Lua policy engine with idempotent updates and hot-reload.
- Contributed to Kafka Streams detection pipelines correlating high-volume event streams.
- Built a Kubernetes Operator in Go for service lifecycle automation, and owned CI/CD across two production services.

### Software Engineering Intern, IBM Cloud (2023)

- Built Java and Node.js microservices for billing and orchestration, with distributed deduplication (IBM Cloudant), OpenAPI documentation, and scheduled jobs.

## Technical stack

**Languages:** Go, Java, C++, Python, SQL, Bash

**Distributed systems and protocols:** event-driven architecture, Kafka, MQTT, REST APIs, at-least-once delivery, deduplication, retries and backoff, TLS/mTLS

**Cloud and infrastructure:** AWS (EC2, ASG, S3, SQS), Docker, Kubernetes (custom Operator in Go), CI/CD (GitHub Actions, GitLab CI, Jenkins)

**Data and storage:** PostgreSQL, SQLite, Redis, content-addressable hashing (SHA-256)

**Machine learning and research:** PyTorch, Stable-Baselines3, causal inference, reinforcement learning, scikit-learn, experimentation and evaluation

**AI-assisted engineering:** agentic coding harnesses (Claude Code), AI-assisted development workflows

## Education

**MSc Data Science, University of Bristol (2025 to 2026)**

Relevant coursework: Large Scale Data Engineering, Statistical Computing, Introduction to AI and Text Analytics, Data Science Methods and Practices. Built ML pipelines in R (Elastic Net and tuned Random Forest, F1 = 0.787) and deployed an AWS micro-application with SQS-driven Auto Scaling.

**B.Tech, Electronics and Communication Engineering, MIT Manipal (2023), 8.1/10**

Relevant coursework: Data Structures and Algorithms, Object-Oriented Programming (C++), Computer Organization and Architecture, Linux Programming.

## Contact

- LinkedIn: https://linkedin.com/in/rohan-anthony-9b03bb210
- GitHub: https://github.com/rohan2107
- Email: rohan.anthony2107@gmail.com
