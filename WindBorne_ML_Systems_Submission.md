# WindBorne Software Engineer Machine Learning Systems Application Challenge

## 1. Tell us about a problem you couldn't leave alone. What did you build to fix it?

At AMP Energy Intelligence, the part I kept coming back to was what happened when time-series data arrived late. A dashboard can look healthy while quietly missing five-minute or hourly readings; a naive retry can then create duplicates. As the sole backend engineer, I built the ingestion path around idempotent writes, rolling backfills, bounded retries, and failure isolation. Delayed records could be recovered without being counted twice. I also rebuilt the aggregation and rollup layer so the recovered data remained useful at query time. Across more than 3.5 million records at 32-way concurrency, p95 query latency fell from 9.3 seconds to under 300 milliseconds, with more than 20 times the throughput. I liked that the fix addressed both the visible slowness and the quieter question of whether the numbers could be trusted.

## 2. Tell us about a time you had to understand an unfamiliar system that wasn't behaving as expected. How did you get to the bottom of it?

While building AMP's time-series platform, I hit an aggregation path that took 9.3 seconds at p95. The symptom was a slow query, but I needed to understand how incoming observations became daily metrics and cost projections before changing it. I worked through that data flow and measured the query path under concurrency, rather than optimizing a single request in isolation. That pointed me toward a redesign of the aggregation and rollup architecture. I tested the new path against more than 3.5 million records at 32-way concurrency; p95 dropped below 300 milliseconds and throughput rose by more than 20 times. It reinforced a habit I now rely on when debugging: build a model of the whole path, establish a repeatable measurement, and only then change the part you think is responsible.

## 3. Describe a real coding task where AI tools helped you move faster. Where did you have to step in and think for yourself?

I use Codex and Claude Code to move faster on codebase exploration, first-pass implementations, and test ideas. One example was AMP's ingestion and backfill work. I used AI assistance to work through possible retry and duplicate-write cases, but I had to decide the actual correctness rules: writes needed to be idempotent, retries bounded, backfills able to recover late readings, and failures isolated so one feed would not hold up the others. I checked the resulting code against those cases instead of treating a generated implementation as finished. The tools were useful for getting to a candidate quickly; the harder part was defining what safe recovery meant for the data and verifying that the system behaved that way.

## 4. Describe the extent to which you have experience with production systems.

My production experience comes from four software engineering internships, mostly in backend, data, and AI systems. Most recently I was the sole backend engineer for AMP's multi-tenant analytics platform, responsible for its APIs, PostgreSQL data model, background jobs, AWS deployment, and recovery behavior when feeds were late or failed. I also added tenant-scoped queries, authorization, encrypted credentials, and cross-tenant tests in CI. At Eth Tech, I replaced batch ETL with Kafka consumers for an ML prediction service that sustained more than 2,000 events per second and cut processing lag in half. At Schneider Electric, I shipped an AI-assisted CI remediation workflow. My experience includes building a feature, measuring it under load, and staying accountable for how it behaves after launch; I have not yet operated a weather-model inference service.

## 5. How many years of relevant experience do you have?

About 1 year and 5 months of relevant software engineering internship experience across four roles, plus systems and distributed-computing projects at the University of Waterloo. I expect to complete my Honours Bachelor of Computer Science in December 2026.
