# Awesome-Serverless-Compute-Query-Processing

## Top Serverless Compute & Query Processing Ecosystem

**Curated List of SaaS Products & Open-Source GitHub Projects**  
*Focused on Elastic Query Engines, Serverless Functions & Self-Hosted Compute Runtimes*  
**Last updated: October 2026**

This repository tracks notable **SaaS platforms** and **open-source projects** for **Serverless Compute & Query Processing**. These tools enable organizations to run code and queries without provisioning or managing servers—scaling automatically from zero to handle unpredictable workloads, from API endpoints and background jobs to interactive SQL analytics and GPU inference.

---

## Sector Overview & Market Dynamics

- **Market Size**: The global serverless architecture and compute market is valued at approximately **$20.8 billion in 2024–2025** and is projected to exceed **$65 billion to $90+ billion by 2030–2032**, expanding at a robust CAGR of ~22–25%. The query processing and cloud data warehouse segment alone represents an additional **$10+ billion** market driven by rapid cloud migration and modern real-time AI analytics.
- **Market Dynamics**: The market exhibits a **moderately concentrated, bifurcated structure** dominated by hyperscalers (AWS Lambda, Google Cloud Run, Azure Functions) and major data cloud incumbents (Snowflake, Databricks) holding the largest share of enterprise spend. Concurrently, high degrees of specialized innovation flourish among agile challengers leading niche segments such as edge execution (Cloudflare Workers), developer databases (Neon, Supabase), and serverless GPU/AI compute (Modal).

---

## Table of Contents

- [Sector Overview & Market Dynamics](#sector-overview--market-dynamics)
- [SaaS/Hosted Platforms](#saashosted-platforms)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

---

## SaaS/Hosted Platforms

| Platform | Valuation / Revenue | Pricing (Starting Tier) | Free Tier Limit | Highlights / Description |
| :--- | :--- | :--- | :--- | :--- |
| **[Google Cloud Run](https://cloud.google.com/run)** | ~$3.05 Trillion MCap (Alphabet) / Google Cloud ~$43.7B Annual Revenue run-rate | Pay-as-you-go: CPU at $0.00002400/vCPU-sec, Memory at $0.00000250/GiB-sec, Requests at $0.40/million | **Free Forever**: 2 million requests/month, 360,000 vCPU-seconds, 180,000 GiB-seconds, plus 1 GiB outbound network egress/month (within Tier 1). $300 credits for 90-day trial for new accounts. | Fully managed container platform that scales automatically to zero; runs any containerized HTTP application without managing K8s clusters. |
| **[Azure Functions](https://azure.microsoft.com/en-us/products/functions)** | ~$3.02 Trillion MCap (Microsoft) / Microsoft Intelligent Cloud ~$105B+ Annual Revenue | Consumption plan: $0.20 per million executions + $0.000016/GB-sec execution time | **Free Forever**: 1,000,000 executions and 400,000 GB-seconds resource consumption per month. $200 credits for 30-day trial for new accounts. | Microsoft serverless compute platform with rich declarative bindings and triggers across Azure, supporting C#, Python, JS/TS, Java, and PowerShell. |
| **[AWS Lambda](https://aws.amazon.com/lambda/)** | ~$2.05 Trillion MCap (Amazon) / AWS ~$105B+ Annual Revenue | Pay-as-you-go: $0.20 per 1 million requests + $0.0000166667 per GB-second (x86) / $0.0000133334 per GB-second (Arm/Graviton2) | **Free Forever**: 1,000,000 free requests and 3,200,000 seconds of compute time (up to 400,000 GB-seconds) every month. | The benchmark FaaS platform running code in response to events with automated high-concurrency scaling and micro-billing. |
| **[Databricks Serverless](https://www.databricks.com/)** | $43 Billion Valuation (Private) / ~$2.6 Billion ARR | Serverless SQL compute billed per Databricks Unit (DBU): Serverless SQL starting at ~$0.07–$0.22/DBU-hour (e.g. ~$0.70/hour for Small Serverless SQL warehouse) | **Free Trial**: 14-day free trial with full platform access (usage credits included; underlying cloud provider compute/storage costs may apply). | Managed serverless compute for notebooks, workflows, and SQL; eliminates cluster provisioning with instant launch and auto-stopping. |
| **[Snowflake Serverless Warehouses](https://www.snowflake.com/)** | ~$48 Billion MCap (NYSE: SNOW) / ~$3.6 Billion ARR | Credit-based consumption: Standard Edition at ~$2.00 to ~$3.00 per Snowflake compute credit (1 credit/hour for X-Small serverless warehouse) | **Free Trial**: 30-day free trial with $400 worth of free usage credits (no credit card required upfront). | Elastic serverless compute for SQL analytics and Snowpark; scales instantly up and down per query workload with per-second billing. |
| **[Cloudflare Workers](https://workers.cloudflare.com/)** | ~$35 Billion MCap (NYSE: NET) / ~$1.7 Billion ARR | Paid Workers plan starts at $5/month (includes 10M requests/month + $0.30/million additional requests, CPU time at $0.02/million CPU-milliseconds) | **Free Forever**: 100,000 requests per day, up to 10ms CPU time per request, across 300+ global edge locations. | Ultra-low latency edge serverless platform executing JS/TS/WASM on V8 isolates with sub-millisecond cold starts and distributed key-value storage. |
| **[Supabase Functions](https://supabase.com/docs/guides/functions)** | ~$5 Billion Valuation (Private) / ~$40 Million ARR | Pro plan starts at $25/month (includes 2M invocations/month, additional invocations at $2 per 1M) | **Free Forever**: 500,000 function invocations per month, 100 concurrent executions, and 500MB database storage. | Edge Functions executing Deno/TypeScript tightly integrated with Supabase Auth, PostgreSQL Database, realtime subscriptions, and Storage. |
| **[Neon Serverless Postgres](https://neon.tech/)** | ~$1.0 Billion Valuation (Private) / ~$15 Million ARR | Launch plan starts at $19/month (includes autoscaling up to 4 CU, 10 GB storage; additional compute at $0.16/CU-hour, storage at $0.15/GB-month) | **Free Forever**: 0.5 Compute Units (CU) with scale-to-zero after 5 min of inactivity, 0.5 GB data storage, and 10 database branches. | Serverless Postgres separating storage from compute; features instant database branching, scale-to-zero, and an HTTP-based serverless connection driver. |
| **[Modal](https://modal.com/)** | ~$700 Million Valuation (Private) / ~$10 Million ARR | Pay-per-second usage: CPU starting at $0.000023/core-second (~$0.0828/core-hr), RAM at $0.0000023/GiB-sec; GPUs starting at ~$0.59/hr (T4) up to ~$4.50/hr (A100) | **Free Forever**: $30 of free compute credits renewed every month for all personal accounts (covers ~50 hours of CPU or ~35 hours of GPU compute). | Serverless cloud compute platform designed for Python and AI/ML workloads with fast cold starts, seamless GPU scaling, and code-defined environments. |
| **[Momento](https://www.gomomento.com/)** | ~$100 Million Valuation (Private) / Seed/Series A Funded (~$15M Raised) | Pay-as-you-go: $0.15 per GB of data transferred in/out for Momento Cache and Topics; no hourly instance or cluster fees | **Free Forever**: First 50 GB per month of data transfer completely free across Cache and Topics with no time expiration. | Serverless distributed cache and pub/sub messaging service built for sub-millisecond data access from serverless edge functions. |

---

## Open-Source GitHub Projects

All open-source tools below are equipped with live stargazers badges linking directly to their GitHub stargazers page, ordered by GitHub star count (descending).

| Project | Stars | Category / Description | License |
| :--- | :--- | :--- | :--- |
| **[vLLM](https://github.com/vllm-project/vllm)** [![vLLM Stars](https://img.shields.io/github/stars/vllm-project/vllm?style=social&color=white)](https://github.com/vllm-project/vllm/stargazers) | ~95.9k | High-throughput, memory-efficient LLM serving and serverless inference engine with PagedAttention and dynamic request batching. | Apache-2.0 |
| **[DuckDB](https://github.com/duckdb/duckdb)** [![DuckDB Stars](https://img.shields.io/github/stars/duckdb/duckdb?style=social&color=white)](https://github.com/duckdb/duckdb/stargazers) | ~42.7k | High-performance in-process vectorized analytical SQL query engine; ideal for serverless, local, and WebAssembly analytical processing. | MIT |
| **[OpenFaaS](https://github.com/openfaas/faas)** [![OpenFaaS Stars](https://img.shields.io/github/stars/openfaas/faas?style=social&color=white)](https://github.com/openfaas/faas/stargazers) | ~26.3k | Kubernetes-native serverless functions platform for event-driven microservices with auto-scaling (including scale-to-zero) and CLI. | Apache-2.0 (CE) |
| **[Neon](https://github.com/neondatabase/neon)** [![Neon Stars](https://img.shields.io/github/stars/neondatabase/neon?style=social&color=white)](https://github.com/neondatabase/neon/stargazers) | ~23.3k | Open-source serverless PostgreSQL storage engine separating compute and storage with copy-on-write branching and scale-to-zero. | Apache-2.0 |
| **[Trino](https://github.com/trinodb/trino)** [![Trino Stars](https://img.shields.io/github/stars/trinodb/trino?style=social&color=white)](https://github.com/trinodb/trino/stargazers) | ~13.4k | Fast distributed SQL query engine for big data analytics across object storage (S3, GCS), relational databases, and data lakes. | Apache-2.0 |
| **[KEDA](https://github.com/kedacore/keda)** [![KEDA Stars](https://img.shields.io/github/stars/kedacore/keda?style=social&color=white)](https://github.com/kedacore/keda/stargazers) | ~10.7k | Kubernetes-based Event Driven Autoscaling component providing event-driven scale (including scale-to-zero) for any container. | Apache-2.0 |
| **[Apache DataFusion](https://github.com/apache/datafusion)** [![DataFusion Stars](https://img.shields.io/github/stars/apache/datafusion?style=social&color=white)](https://github.com/apache/datafusion/stargazers) | ~9.6k | Extensible, embeddable, in-memory vectorized SQL query engine written in Rust, leveraging Apache Arrow for elastic query systems. | Apache-2.0 |
| **[workerd](https://github.com/cloudflare/workerd)** [![workerd Stars](https://img.shields.io/github/stars/cloudflare/workerd?style=social&color=white)](https://github.com/cloudflare/workerd/stargazers) | ~9.1k | The JavaScript / Wasm serverless runtime powered by Google V8 that drives Cloudflare Workers; programmable HTTP proxy and server. | Apache-2.0 |
| **[Fission](https://github.com/fission/fission)** [![Fission Stars](https://img.shields.io/github/stars/fission/fission?style=social&color=white)](https://github.com/fission/fission/stargazers) | ~8.9k | Fast, developer-friendly serverless functions framework for Kubernetes with ~100ms cold starts via warm container pools. | Apache-2.0 |
| **[Apache OpenWhisk](https://github.com/apache/openwhisk)** [![OpenWhisk Stars](https://img.shields.io/github/stars/apache/openwhisk?style=social&color=white)](https://github.com/apache/openwhisk/stargazers) | ~6.8k | Distributed, Apache-governed serverless cloud platform executing application logic in response to events at any scale. | Apache-2.0 |
| **[Knative Serving](https://github.com/knative/serving)** [![Knative Stars](https://img.shields.io/github/stars/knative/serving?style=social&color=white)](https://github.com/knative/serving/stargazers) | ~6.1k | Kubernetes-based platform for deploying and serving serverless applications with request-driven autoscaling down to zero. | Apache-2.0 |
| **[Nuclio](https://github.com/nuclio/nuclio)** [![Nuclio Stars](https://img.shields.io/github/stars/nuclio/nuclio?style=social&color=white)](https://github.com/nuclio/nuclio/stargazers) | ~5.8k | Ultra-high performance serverless platform tailored for real-time event processing, data science, I/O-intensive tasks, and GPU pipelines. | Apache-2.0 |
| **[Beam (beta9)](https://github.com/beam-cloud/beta9)** [![Beam Stars](https://img.shields.io/github/stars/beam-cloud/beta9?style=social&color=white)](https://github.com/beam-cloud/beta9/stargazers) | ~1.8k | Open-source serverless GPU inference engine and container sandbox platform with GPU checkpoint/restore and memory snapshotting. | Apache-2.0 |
| **[OpenLambda](https://github.com/open-lambda/open-lambda)** [![OpenLambda Stars](https://img.shields.io/github/stars/open-lambda/open-lambda?style=social&color=white)](https://github.com/open-lambda/open-lambda/stargazers) | ~1.0k | Research-driven Apache-licensed serverless computing platform exploring new system architectures and container virtualization techniques. | Apache-2.0 |
| **[OpenRun](https://github.com/openrundev/openrun)** [![OpenRun Stars](https://img.shields.io/github/stars/openrundev/openrun?style=social&color=white)](https://github.com/openrundev/openrun/stargazers) | ~992 | Declarative GitOps deployment platform and open-source Google Cloud Run alternative supporting scale-to-zero containerized apps. | Apache-2.0 |
| **[ramune](https://github.com/i2y/ramune)** [![ramune Stars](https://img.shields.io/github/stars/i2y/ramune?style=social&color=white)](https://github.com/i2y/ramune/stargazers) | ~8 | Go runtime with soundness-gated native compilation for self-hosting Cloudflare Workers handlers as single binaries. | MIT |
| **[fn0](https://github.com/namseent/fn0)** [![fn0 Stars](https://img.shields.io/github/stars/namseent/fn0?style=social&color=white)](https://github.com/namseent/fn0/stargazers) | ~6 | Lightweight V8 and Wasmtime-based serverless runtime with integrated document storage, WASI 0.3 support, and OpenTelemetry. | Apache-2.0 |
| **[Self-Hosted Serverless](https://github.com/mstgnz/self-hosted-serverless)** [![Self-Hosted Serverless Stars](https://img.shields.io/github/stars/mstgnz/self-hosted-serverless?style=social&color=white)](https://github.com/mstgnz/self-hosted-serverless/stargazers) | ~2 | Minimalist Go and WASI-compatible self-hostable FaaS alternative to AWS Lambda with gRPC, Redis, and Postgres integration. | MIT |

---

## Detailed Notes on Key Architectures

### Serverless Query Engines & Elastic Data
- **Vectorized In-Process Engines**: **DuckDB** and **Apache DataFusion** allow embedded analytical SQL execution inside edge functions, lambdas, and browser sandboxes without managing external database server clusters.
- **Distributed Query Federation**: **Trino** serves as the backbone for querying exabytes of data across heterogeneous data sources with high concurrency and decoupled storage/compute.
- **Decoupled Postgres Compute**: **Neon** implements a multi-tenant storage engine with copy-on-write branching, enabling serverless applications to spin up read/write isolated database instances in seconds.

### Serverless Functions & Autoscaling Runtimes
- **Kubernetes Autoscaling Foundation**: **Knative Serving** and **KEDA** supply the standardized primitives for scaling arbitrary containers from zero to tens of thousands of instances based on HTTP requests, event queues, and custom metrics.
- **Micro-VM & Edge Execution**: **workerd** provides the V8-isolate foundation for edge compute with sub-millisecond overhead, while **Beam** brings checkpoint-restore mechanisms to serverless GPU infrastructure.

---

## How to Contribute

1. Fork the repo.
2. Add/edit entries in `README.md` (follow the table formats and guidelines).
3. Include: name, links, accurate starting pricing / free tier limits, star badges, and factual descriptions.
4. Submit PR with a short explanation.

Star the repo if you find it useful!

---

## Disclaimer

- This is a **community-curated** list — not exhaustive and not an endorsement.
- Serverless platforms handling application code and data must comply with applicable security policies; running untrusted code requires proper sandboxing.
- Open-source serverless frameworks vary significantly in maintenance status, governance, and operational overhead; evaluate according to your deployment model and tolerance for infrastructure ownership.
- Verify license terms for production commercial use prior to deployment.

---

**Made for platform engineers, data engineers, and AI infrastructure teams choosing their serverless compute stack.**
