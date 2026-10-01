# Sylvan Chen

Toronto, ON | (226) 507-3888 | i4chen@uwaterloo.ca | [LinkedIn](https://www.linkedin.com/in/yixiangchen099)

## Education

**University of Waterloo** — Candidate for Honours Bachelor of Computer Science, December 2026

## Skills

- **Systems and backend:** Python, C/C++, TypeScript, FastAPI, PostgreSQL, Redis, Kafka, React/Next.js
- **Data and AI systems:** LLM agent orchestration, SQL/JSONB retrieval pipelines, evaluation and quality gating, streaming ingestion
- **Infrastructure:** Docker, AWS, Railway, GitHub Actions, Jenkins, Git, Linux, CI/CD

## Professional experience

### AMP Energy Intelligence — Backend Engineer (Co-op)

Toronto, ON | June 2026 – September 2026

- Sole backend engineer on the product: shipped a multi-tenant time-series analytics platform from zero to one, including its data model, APIs, background jobs, and AWS deployment using FastAPI and PostgreSQL.
- Designed a self-healing ingestion system for five-minute and hourly feeds. Idempotent writes, rolling backfills, bounded retries, and failure isolation recover delayed records without duplication.
- Rebuilt the aggregation and rollup architecture behind daily metrics and cost projections. Reduced p95 query latency from 9.3 seconds to under 300 milliseconds across more than 3.5 million records at 32-way concurrency, with more than 20 times the throughput.
- Enforced tenant isolation through role-based authorization, encrypted credentials, tenant-scoped queries, and cross-tenant security tests in CI.

### CNEM Corporation — Data and AI Engineering Intern

Mississauga, ON | January 2026 – April 2026

- Shipped a Claude-powered research agent with a two-pass quality gate for cross-entity retrieval, source verification, and evidence auditing, reaching approximately 80% Top-5 accuracy on a benchmark of more than 100 queries.
- Designed a PostgreSQL knowledge layer with more than 5,000 plant, compound, disease, mechanism, and PubChem entities in JSONB schemas for cross-entity SQL retrieval.

### Schneider Electric — Software Engineer Intern

Global R&D | June 2025 – September 2025

- Built an AI remediation pipeline for CI workflows that combined static-analysis signals, dynamically retrieved code context, and an issue knowledge base into targeted pull-request fixes.
- Parallelized analysis with asynchronous Python agents and surfaced fixes through a VS Code CodeLens extension, achieving a 76% resolution rate and reducing PR-to-merge time by 30%.

### Eth Tech — Software Engineer Intern

Newark, CA | December 2024 – April 2025

- Replaced batch ETL with Kafka streaming consumers for ML prediction services, sustaining more than 2,000 events per second and halving processing lag through batching and retry/backoff.
- Added a Redis cache-aside layer for preference lookups, reaching approximately 80% cache hit rate and reducing downstream load in a high-availability production path.

## Project

### WatDFS Distributed File System — C++, FUSE, RPC

January 2026 – April 2026

- Implemented a multi-client distributed file system with chunked RPC transfer, TTL/mtime cache validation, and write-back caching.
- Achieved 88.8 times faster warm-cache reads (110 versus 1.24 MB/s) and approximately 1.9 times scaling across two clients.

## Award

Production Impact Award, Schneider Electric RDCC AI Agent Competition
