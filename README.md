# 👋 Hi — I'm Dinesh Suthar

**Java & Blockchain Systems Engineer** · Building high-throughput Spring Boot microservices & production EVM solutions · Open Source Contributor

I design and ship backend systems that scale: ultra-low-latency trading engines, resilient microservices, and gas-optimized smart contracts. I focus on real-world constraints — throughput, latency, security, and cost — and deliver engineering that survives production.

---

[![GitHub followers](https://img.shields.io/github/followers/dineshsuthar123?label=Follow&style=social)](https://github.com/dineshsuthar123)  
![Location](https://img.shields.io/badge/📍-India-blue) ![Open to Work](https://img.shields.io/badge/📂-Open%20to%20Internships--success)

---

## Table of contents
- [Quick snapshot](#quick-snapshot)
- [Core strengths](#core-strengths)
- [Technical stack](#technical-stack)
- [Selected projects](#selected-projects)
- [Performance & reliability goals](#performance--reliability-goals)
- [How I build things (workflow)](#how-i-build-things-workflow)
- [Open source & community](#open-source--community)
- [How to collaborate / contact](#how-to-collaborate--contact)
- [Resume / Socials](#resume--socials)

---

## Quick snapshot

- Backend & distributed systems engineer specializing in **Java**, **Spring Boot**, and **performance engineering**.  
- Production blockchain developer focused on **gas-optimized Solidity** and EVM tooling.  
- Practical engineering: I ship features that meet SLAs and cost targets — not just prototypes.

**One-line mission:** Build production systems that handle massive scale with clean code, predictable performance, and auditable behavior.

---

## Core strengths

- **High-volume systems** — design & implement APIs that sustain 10k+ RPS with predictable p99 latencies.  
- **Event-driven architectures** — Kafka-based pipelines, idempotency, backpressure, and observability.  
- **Low-latency systems** — microsecond-aware Java services, careful GC/heap tuning, LMAX-style patterns.  
- **Blockchain production** — gas-optimized smart contracts, testing, and deployment pipelines (Hardhat/Foundry).  
- **Cloud-native operations** — Kubernetes, Terraform, CI/CD, monitoring (Prometheus + Grafana).  
- **Performance tooling** — profiling (async-profiler, JFR), replayable benchmarks, eBPF as needed.

---

## Technical stack

### Languages
`Java` · `Kotlin` · `Python` · `Solidity` · `TypeScript`

### Backend & Frameworks
`Spring Boot` · `Spring Cloud` · `Hibernate` · `Netty` · `gRPC`

### Data & Messaging
`PostgreSQL` · `Redis` · `MongoDB` · `Kafka` · `ClickHouse`

### Blockchain & Crypto
`Solidity` · `Hardhat` · `Foundry` · `EVM` · `ZK` (Circom)

### Infra & Observability
`Docker` · `Kubernetes (EKS/GKE)` · `AWS` · `Terraform` · `Prometheus` · `Grafana`

---

## Selected projects — deep, production-ready work

### 1) Supply Ledger — Supply Chain Authentication System
**Stack:** Spring Cloud · Ethereum · Kafka · AWS EKS  
**What:** Distributed anti-counterfeiting platform for medical & luxury goods.  
**Highlights:**  
- Production throughput: **5k+ verifications/min**  
- Smart contracts: **~40% gas reduction** via packed storage and optimized calldata  
- Architecture: event-driven verification pipeline with tamper-proof proofs and audit trails  
**Link:** `https://supplyledger.vercel.app/` (demo)

**Architecture (high level):**
```mermaid
flowchart LR
    A["IoT Scanner"]
    B["Ingest API"]
    C["Kafka"]
    D["Processing Service"]
    E["Smart Contract"]
    F["Audit Database"]
    G["Monitoring / Dashboard"]

    A -->|signed event| B
    B --> C
    C --> D
    D -->|tx| E
    D --> F
    F --> G

