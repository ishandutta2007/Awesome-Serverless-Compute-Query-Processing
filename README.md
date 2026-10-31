# Awesome-Serverless-Compute-Query-Processing

# Top Serverless Compute & Query Processing Ecosystem

**Curated List of SaaS Products & Open-Source GitHub Projects**  
*Focused on Elastic Query Engines, Serverless Functions & Self-Hosted Compute Runtimes*  
**Last updated: October 2026**

This repository tracks notable **SaaS platforms** and **open-source projects** for **Serverless Compute & Query Processing**. These tools enable organizations to run code and queries without provisioning or managing servers—scaling automatically from zero to handle unpredictable workloads, from API endpoints and background jobs to interactive SQL analytics and GPU inference.

**Examples** include Snowflake Serverless Warehouses, AWS Lambda, Google Cloud Run, Azure Functions, Databricks Serverless, Neon Serverless Postgres, Modal, Momento, Cloudflare Workers, and Supabase Functions (the category leaders).

**Open-source emphasis**: Serverless Compute & Query Processing is a domain where open-source tooling is **mature at the function runtime and container platform layers, but fragmented across the full spectrum of serverless workloads**. **OpenFaaS** and **OpenWhisk** provide production-grade FaaS on Kubernetes . **Nuclio** excels at data-intensive and GPU workloads, processing hundreds of thousands of requests per second . **Beam** offers an open-source Modal alternative with GPU checkpoint/restore and long-running sandboxes . For serverless Postgres, **Neon's storage engine** is open-source, though the managed service includes proprietary components . The critical caveat: **no single open-source project replicates the turnkey managed experience** of AWS Lambda or Google Cloud Run—self-hosting means owning the orchestration, scaling, and operational infrastructure .

Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.

## Table of Contents
- [SaaS/Hosted Platforms](#saas-products)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## SaaS/Hosted Platforms

- **[Snowflake Serverless Warehouses](https://www.snowflake.com/)**  
  Serverless compute for SQL queries and Snowpark workloads; automatically scales compute up and down based on demand, with per-second billing and no infrastructure management.

- **[AWS Lambda](https://aws.amazon.com/lambda/)**  
  The pioneering FaaS platform; runs code in response to events with automatic scaling and pay-per-invocation pricing. The benchmark for serverless functions.

- **[Google Cloud Run](https://cloud.google.com/run)**  
  Fully managed container platform that scales to zero and handles HTTP requests; runs any containerized application without Kubernetes management.

- **[Azure Functions](https://azure.microsoft.com/en-us/products/functions)**  
  Microsoft's serverless compute with triggers and bindings across Azure services; supports C#, JavaScript, Python, Java, and PowerShell.

- **[Databricks Serverless](https://www.databricks.com/)**  
  Fully managed serverless compute for notebooks, workflows, and SQL; eliminates cluster provisioning with per-second billing and automatic scaling.

- **[Neon Serverless Postgres](https://neon.tech/)**  
  Serverless Postgres with **autoscaling, scale-to-zero, and database branching**; separates storage and compute, with a serverless driver for JavaScript/TypeScript that uses HTTP instead of TCP for edge compatibility .

- **[Modal](https://modal.com/)**  
  Serverless compute for Python functions and containers on GPUs, billed per second with scale-to-zero and fast cold starts; Python-native developer experience with environment defined in code.

- **[Momento](https://www.gomomento.com/)**  
  Serverless cache and pub/sub platform with per-request pricing and global distribution; designed for low-latency data access from serverless and edge functions.

- **[Cloudflare Workers](https://workers.cloudflare.com/)**  
  Edge serverless platform running JavaScript/TypeScript (and WASM) on V8 isolates across Cloudflare's global network; sub-millisecond cold starts and integration with KV, R2, D1, Durable Objects, and Queues.

- **[Supabase Functions](https://supabase.com/docs/guides/functions)**  
  Edge Functions within the Supabase platform; runs Deno-based TypeScript functions close to users with integration to Supabase Auth, Database, and Storage.

## Open-Source GitHub Projects

### Serverless Functions Platforms (FaaS)

- **[OpenFaaS](https://github.com/openfaas/faas)**  
  Kubernetes-native **serverless functions platform** (Apache-2.0 for Community Edition) . Deploy event-driven functions and microservices as OCI-compatible images with auto-scaling (including to zero), UI portal, CLI, and templates for any language . **Critical licensing caveat**: the Community Edition is licensed for **individual exploration and hobbyist use only**—commercial and production workloads require OpenFaaS Standard or Enterprise . **Best for learning and non-commercial deployments**; production use requires a commercial license.

- **[Apache OpenWhisk](https://github.com/apache/openwhisk)**  
  Apache-licensed serverless functions platform for building cloud applications; rich programming model with functions, triggers, rules, and packages . **Breaking change**: migrated to Apache Pekko framework in October 2025—existing clusters must be re-deployed . Supports Kubernetes deployment and a standalone mode for local development . **Best for organizations wanting an Apache-governed FaaS** with a mature ecosystem.

- **[Nuclio](https://github.com/nuclio/nuclio)**  
  High-performance **serverless framework for data, I/O, and compute-intensive workloads** (Apache-2.0) . Features: **GPU support**, integration with Jupyter and Kubeflow, support for variety of data and streaming sources, and processing **hundreds of thousands of HTTP requests or data records per second**—10-100x faster than some other frameworks . Deployable as standalone Docker container or on Kubernetes; can be used through the Iguazio Data Science Platform . **Best for data science, ML, and real-time event processing**—not a general-purpose web FaaS.

- **[fn0](https://github.com/namseent/fn0)**  
  Fully open-source **V8 and Wasmtime-based FaaS** positioned as a Cloudflare Workers alternative for on-premise and cloud . Features: WebAssembly components (WASI 0.3, Component Model), JavaScript/TypeScript via V8-based runtime, built-in transactional document storage, S3-compatible object storage, HTTP/WebSocket, and **OpenTelemetry** observability . Self-hostable with configurable infrastructure; fn0 Cloud managed option available . **Best for teams wanting a Workers-like runtime with full source access**—but it is newer and less proven than OpenFaaS or OpenWhisk.

- **[OpenLambda](https://github.com/open-lambda/open-lambda)**  
  Apache-licensed serverless computing platform written in Go, based on Linux containers . Primary goal is **enabling exploration of new approaches to serverless computing**—a single-node worker that takes HTTP requests and invokes lambdas locally . Cluster mode (OpenLambda boss) is in development . **Best for research and experimentation** with serverless architectures—not production-ready.

- **[Self-Hosted Serverless](https://github.com/mstgnz/self-hosted-serverless)**  
  Production-ready, self-hostable **FaaS alternative to AWS Lambda and Google Cloud Functions** (Go, v1.1.0) . Functions run as Go plugins or WASM modules (WASI-compatible via wazero) with compiled module caching; dual HTTP and gRPC support; PostgreSQL/SQLite/Redis integration; API key auth, rate limiting, function timeout, panic recovery, and built-in metrics . Docker deployment. **Best for teams wanting Lambda-like execution on their own infrastructure** with minimal dependencies .

### Container & Application Platforms (Cloud Run Alternatives)

- **[OpenRun](https://github.com/openrundev/openrun)**  
  Open-source alternative to **Google Cloud Run and AWS App Runner** (Apache-2.0) . Features: declarative GitOps-based app deployment (config in Git, not CLI/UI operations), **scale-to-zero** for app containers, OAuth/OIDC/SAML with RBAC, TLS certs and secrets management, staging mode for app updates, and atomic updates across multiple apps . Deploys any containerized web app; AppSpecs for Streamlit/Gradio/FastHTML/NiceGUI/Shiny/Reflex enable zero-config deployment . **Best for teams wanting declarative, Git-driven container deployment** with built-in auth and scaling .

### Serverless Postgres & Data

- **[Neon (Storage Engine)](https://github.com/neondatabase/neon)**  
  The **open-source storage engine** underlying Neon Serverless Postgres (Apache-2.0) . Separates storage and compute to offer **autoscaling, database branching (copy-on-write), and scale-to-zero** . The storage engine is open-source; the managed Neon service includes proprietary components . **Best for teams wanting to understand or build on serverless Postgres architecture**—but running the full stack requires significant operational expertise .

### GPU & AI Compute (Modal Alternatives)

- **[Beam](https://github.com/beam-cloud/beta9)**  
  Open-source **Modal alternative** for running GPU inference, background jobs, and sandboxes (100% open source and self-hostable) . Features: **fast image builds, GPU support, memory/file system snapshotting, GPU checkpoint restore** (stop and resume sandboxes preserving running processes), long-running sessions (24h+), and gVisor isolation . Used by Coca-Cola, Magellan AI, and Shippabo for serverless inference and sandboxes . **Best for AI teams wanting Modal-like serverless GPU compute** without vendor lock-in—but requires self-hosting infrastructure.

### Edge & Runtime Infrastructure

- **[workerd](https://github.com/cloudflare/workerd)**  
  The **JavaScript/Wasm runtime that powers Cloudflare Workers** (open-source, but **not a hardened sandbox**) . Can be used as an application server to self-host Workers-compatible code, as a development tool, or as a programmable HTTP proxy. **Critical warning**: "workerd on its own does not contain suitable defense-in-depth"—when running untrusted code, you must run it inside a secure sandbox like a VM . **Best for teams wanting the Workers runtime** with full awareness that Cloudflare's hosting adds many additional security layers not present in the open-source binary.

- **[ramune](https://github.com/i2y/ramune)**  
  Self-host **Cloudflare Workers handlers** in Go (npm package, v0.x) . Features: run/test/type-check/format/lint/REPL TypeScript/JS; compile to a **single binary**; tri-backend (JavaScriptCore, qjswasm/QuickJS-WASM, goja) with no Cgo required; pluggable `env.KV` and `env.DB` backends (Redis, Postgres, DynamoDB, in-memory); and custom bindings via Go callbacks . **Best for Go developers** wanting to self-host Workers-compatible code without Cloudflare—but it is newer and less proven than workerd itself.

### Additional Strong Open-Source Options

- **Knative** — Kubernetes-based platform for deploying and managing serverless workloads with request-driven autoscaling (including scale-to-zero) and traffic splitting . **Infrastructure layer**—used as the foundation for many managed serverless offerings.
- **Kubeless** — Kubernetes-native serverless framework using Custom Resource Definitions; simple architecture, but **no scale-to-zero** functionality at the time of writing . **Best for simple K8s-native functions** without scale-to-zero requirements.
- **Fission** — Kubernetes-native serverless framework with ~100ms cold starts via warm container pools; supports NodeJS, Python, Ruby, Go, PHP, Bash, and any Linux executable; HTTP, message queue, and schedule triggers.

**Frameworks for building custom systems**: For **general-purpose FaaS on Kubernetes**, OpenFaaS (accepting the commercial license for production) or OpenWhisk . For **data/ML-intensive serverless**, Nuclio . For **Cloud Run-like container deployment**, OpenRun . For **serverless GPU compute**, Beam . For **Workers-compatible edge runtime**, workerd (with sandboxing) or ramune (Go self-hosting) . For **Lambda-like execution on your own infrastructure**, Self-Hosted Serverless . No open-source project replicates the **turnkey managed experience** of AWS Lambda or Google Cloud Run—self-hosting means owning orchestration, scaling, and operational responsibility.

## How to Contribute

1. Fork the repo.
2. Add/edit entries in `README.md` (follow existing format).
3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.
4. Submit PR with a short explanation.

Star the repo if you find it useful!

## Disclaimer

- This is a **community-curated** list — not exhaustive and not an endorsement.
- Serverless platforms handling application code and data must comply with applicable security policies; **running untrusted code requires proper sandboxing**—workerd explicitly warns it is not a hardened sandbox, and OpenFaaS Community Edition is restricted to non-commercial use .
- **Open-source serverless is mature at the function runtime and container layers**—OpenFaaS, OpenWhisk, Nuclio, and OpenRun provide production-grade platforms . However, **no single open-source project replicates the managed turnkey experience** of AWS Lambda or Google Cloud Run—self-hosting requires operational investment in scaling, monitoring, and infrastructure. Choose based on workload type (general FaaS vs. data/GPU vs. container deployment) and tolerance for operational responsibility.
- Verify license terms for commercial use; OpenFaaS Community Edition is **non-commercial** , OpenWhisk uses Apache-2.0, Nuclio uses Apache-2.0, and Beam is open-source (check repository) .

---

**Made for platform engineers, AI infrastructure teams, and developers choosing their serverless compute stack.**  
Let's make serverless compute more open, but with clear eyes about the licensing restrictions and operational responsibility that self-hosting introduces.
