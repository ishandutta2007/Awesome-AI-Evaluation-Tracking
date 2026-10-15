# Awesome-AI-Evaluation-Tracking

## Top AI Evaluation & Tracking Ecosystem



**Curated List of SaaS Products & Open-Source GitHub Projects**  

*Focused on LLM Experiment Tracking, RAG Evaluation & Production Monitoring*  

**Last updated: October 2026**



This repository tracks notable **SaaS platforms** and **open-source projects** for **AI Evaluation & Tracking**. These tools enable teams to systematically measure LLM application quality—tracing every step, scoring outputs with LLM judges, comparing experiments, and catching regressions before they reach production.



**Examples** include Scale AI, Snorkel Flow, Braintrust, LangSmith, Arize Phoenix, Patronus AI, TruEra, Fiddler AI, Humanloop, and DeepEval (the category leaders).



**Open-source emphasis**: This section is heavily expanded with every major active project for self-hosting, OpenTelemetry-native tracing, and open evaluation frameworks—ideal for AI engineers, platform teams, and developers seeking transparent, vendor-independent evaluation infrastructure.



Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.



## Table of Contents

- [SaaS/Hosted Platforms](#saas-hosted-platforms)

- [Open-Source GitHub Projects](#open-source-github-projects)

- [How to Contribute](#how-to-contribute)

- [Disclaimer](#disclaimer)



## SaaS/Hosted Platforms



- **[Braintrust](https://www.braintrust.dev/)**  

  **Eval-first observability platform with CI/CD quality gates.** Trusted by Notion, Stripe, Vercel, Dropbox, and Coursera. **Freemium**: Starter free (1 GB logs/month, 14-day retention, 10k eval runs/month), Pro at $249/month (5 GB, 30-day retention, 50k evals), Enterprise with self-hosted/BYOC options . **AI-assisted Loop Agent** automates optimization of prompts and evaluations .



- **[LangSmith](https://smith.langchain.com/)**  

  LangChain's observability and evaluation platform with detailed tracing of every LLM call, chain execution, and agent step. **Free Developer plan** (1 seat, 5k base traces/month), **Plus at $39/seat/month** (10k base traces, 1 free serverless deployment), Enterprise with self-hosted/hybrid options . **Note**: LangSmith is **not fully open source**—it is a hosted, commercial product with a generous free tier .



- **[Scale AI](https://scale.com/)**  

  Data platform for AI with annotation, curation, and model evaluation services. Features **human evaluation** at scale, **RLHF preference data collection**, and **model benchmarking** against expert graders.



- **[Snorkel Flow](https://snorkel.ai/)**  

  Enterprise data development platform built on the open-source Snorkel library. Supports **programmatic labeling**, data curation, model training, and evaluation. **The most mature platform for weak supervision and programmatic data development.**



- **[Patronus AI](https://www.patronus.ai/)**  

  **Hosted evaluation API with configurable evaluators** for hallucination (Lynx), toxicity, PII, prompt injection, and custom judging. Single `/v1/evaluate` endpoint runs multiple evaluators per request with pass/fail verdicts and explanations. **Free Developer tier** .



- **[Fiddler AI](https://www.fiddler.ai/)**  

  Enterprise AI observability and model performance monitoring with explainability, bias detection, and LLM evaluation. **Experiments** feature supports A/B testing prompts, model version comparison, regression testing, safety validation, and RAG system evaluation using RAG Health Metrics (AnswerRelevance, ContextRelevance, RAGFaithfulness) .



- **[Humanloop](https://humanloop.com/)**  

  LLM Evals Platform for Enterprises with prompt engineering, evaluation, and observability. **Free tier**: 2 members, 50 eval runs, 10K logs/month. Enterprise adds SSO+SAML, RBAC, VPC deployment, and SLAs. Supports both UI-first and code-first workflows .



- **[TruEra](https://truera.com/)**  

  AI quality management platform with testing, monitoring, and explainability for ML and LLM applications. **Acquired by Snowflake (2024)** —platform evolving under new ownership.



## Open-Source GitHub Projects



- **[TruLens](https://github.com/truera/trulens)**  

  **The most comprehensive open-source evaluation and tracking framework for LLM experiments and RAG pipelines** (Apache-2.0). **3,000+ GitHub stars**. **OpenTelemetry-native**—instrument any app with a decorator, score every step with LLM judges that explain themselves, compare versions, and ship the one that earns it . **Trace every step** (latency, inputs, outputs, tokens, cost recorded per step), **compare versions** (scores, latency, cost per app version), **seven purpose-built evaluators for agentic systems** (LogicalConsistency, ExecutionEfficiency, PlanAdherence, PlanQuality, ToolSelection, etc.) . **Judges are graded against human annotations out of the box**: **95% agent errors caught with Agent GPA on TRAIL/GAIA** (vs 55% baseline), **0.81 Groundedness F1 on LLM-AggreFact**, **0.93 Context relevance NDCG@5** . Adopted by **Walmart Global Tech, Cisco, J.P. Morgan Chase, Equinix, VMware by Broadcom, Hitachi Digital Services, Thomson Reuters** . **Tracing is OpenTelemetry-native**—portable to any OTLP backend (Jaeger, Grafana Tempo, Datadog) .



- **[DeepEval](https://github.com/confident-ai/deepeval)**  

  **Simple-to-use open-source LLM evaluation framework** (Apache-2.0), similar to Pytest but specialized for unit testing LLM outputs. **The most practical open-source eval framework for CI/CD integration** . Features **large variety of ready-to-use metrics** powered by ANY LLM or local NLP models: G-Eval, Summarization, Answer Relevancy, Faithfulness, Contextual Recall, Contextual Precision, RAGAS, Hallucination, Toxicity, Bias. **Red teaming** for 40+ safety vulnerabilities with 10+ attack enhancement strategies. Evaluate entire datasets in bulk in under 20 lines of Python code in parallel. **Integrates seamlessly with ANY CI/CD environment**. Benchmarks any LLM on MMLU, HellaSwag, BIG-Bench Hard, TruthfulQA, HumanEval, GSM8K in under 10 lines of code .



- **[Arize Phoenix](https://github.com/Arize-ai/phoenix)**  

  **Open-source AI observability platform** (Elastic License 2.0) designed for experimentation, evaluation, and troubleshooting . Features **tracing** via OpenTelemetry-based instrumentation, **evaluation** using LLMs to benchmark performance, **datasets** for versioned examples, **experiments** for tracking prompt/model/retrieval changes, **playground** for prompt optimization and model comparison, and **prompt management** with version control . Vendor and language agnostic with out-of-the-box support for LlamaIndex, LangChain, Haystack, DSPy, smolagents, and LLM providers including OpenAI, Bedrock, MistralAI, VertexAI, LiteLLM, and Google GenAI . Runs practically anywhere: local machine, Jupyter notebook, containerized deployment, or cloud . **2.5M+ monthly downloads**, **10,800+ GitHub stars** .



- **[Ragas](https://github.com/vibrantlabsai/ragas)**  

  **The leading open-source RAG evaluation framework** (Apache-2.0) . Features **objective metrics** (LLM-based and traditional), **test data generation** (automatically create comprehensive test datasets covering wide range of scenarios), **seamless integrations** with LangChain and major observability tools, and **feedback loops** leveraging production data . Install via `pip install ragas`. CLI quickstart: `ragas quickstart rag_eval` creates complete RAG evaluation project .



- **[Promptfoo](https://github.com/promptfoo/promptfoo)**  

  **Open-source LLM testing and red-teaming framework** (MIT). **20,000+ GitHub stars**. Listed as one of five tools people actually use for LLM evaluation alongside Braintrust, LangSmith, Inspect, and Ragas . OpenAI announced acquisition in March 2026 with commitment to keep the open-source project going.



- **[Inspect](https://github.com/UKGovernmentBEIS/inspect_ai)**  

  **Open-source framework for large language model evaluations from UK AI Safety Institute**. Listed as one of five tools people actually use for LLM evaluation . **The most authoritative open-source evaluation framework from a government AI safety body.**



- **[Langfuse](https://github.com/langfuse/langfuse)**  

  **Open-source LLM engineering platform** (MIT core) with tracing, evaluations, prompt management, and datasets. **35,000+ GitHub stars**. Self-hostable. **Acquired by ClickHouse in January 2026 with commitment to keep it open source** .



- **[Comet Opik](https://github.com/comet-ml/opik)**  

  **Fully-permissive Apache-2.0 rival to Langfuse**. **22,000+ GitHub stars**. Full platform—backend included—free to self-host. Covers AI agent tracing, LLM evaluation, prompt optimization, production monitoring, and **Opik Guardrails** .



- **[OpenLLMetry (Traceloop)](https://github.com/traceloop/openllmetry)**  

  **Apache-2.0 OpenTelemetry instrumentation for LLM providers, vector DBs, and frameworks**. Emits standard `gen_ai` spans portable to any OTel backend . **The cleanest standards story: no lock-in, pure instrumentation.**



### Additional Strong Open-Source Options



- **[AgentCompass](https://github.com/open-compass/AgentCompass)** — Unified open-source evaluation infrastructure for agents (Apache-2.0, EMNLP 2026 Demo Track) . **30+ public benchmarks and 10+ agent harnesses** including Claude Code, Codex, OpenHands, and OpenClaw . **Composable architecture** decouples Model, Benchmark, Harness, and Environment . **Traceable and reproducible** with trajectory recording, tool calls, and failure analysis .

- **[ContextForge Eval](https://pypi.org/project/contextforge-eval/)** — **Open-source evaluation framework for agentic systems**. **Framework-agnostic** — adapters translate framework events into traces, graders operate only on traces . **Memory hygiene detection** catches stale context, missed facts, and contradictory fragments .

- **[clean-evals](https://pypi.org/project/clean-evals/)** — Open-source eval platform with blind review, golden answer locking, and LLM judge calibration .

- **[OpenAI Evals](https://github.com/openai/evals)** — Open-source framework for evaluating LLMs and LLM systems (MIT) .

- **[Anthropic Cookbook](https://github.com/anthropics/anthropic-cookbook)** — Includes evaluation recipes and patterns for Claude applications .

- Community **n8n** workflows for evaluation pipeline automation and regression alerting.



**Frameworks for building custom systems**: Combine **TruLens** for comprehensive experiment tracking and RAG evaluation with **DeepEval** for CI/CD-integrated testing, **Arize Phoenix** for OpenTelemetry-native tracing, **Ragas** for RAG-specific metrics, and **Promptfoo** for red-teaming—creating a fully self-hosted, enterprise-grade evaluation platform.



## How to Contribute



1. Fork the repo.

2. Add/edit entries in `README.md` (follow existing format).

3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.

4. Submit PR with a short explanation.



Star the repo if you find it useful!



## Disclaimer



- This is a **community-curated** list — not exhaustive and not an endorsement.

- AI evaluation platforms handling prompts and traces must comply with data protection regulations (GDPR, CCPA, etc.), especially when traces contain PII.

- **"Open source" means different things in this category.** TruLens, DeepEval, Ragas, Promptfoo, and Inspect are genuinely open source (Apache-2.0/MIT). Arize Phoenix uses Elastic License 2.0 (source-available, not OSI-approved). LangSmith is closed SaaS with open SDKs and Enterprise self-hosting. **Check the LICENSE file, not the marketing page** .

- **Self-hosting is a hard requirement when prompts or traces carry regulated data.** If they do, the field collapses to TruLens, DeepEval, Phoenix, Ragas, Langfuse, Opik, and OpenLLMetry. LangSmith and Braintrust cannot self-host on lower tiers .

- **Observability is not evaluation.** Tracing tells you what happened; evaluation tells you whether it was good. Most tools ship both—which makes it easy to buy one and never configure the other. **Tracing alone will not catch quality drift.**

- **Evaluation judges are themselves LLMs.** Their scores are probabilistic and should be validated against human annotations for high-stakes decisions. TruLens grades its judges against human annotations out of the box—a practice every evaluation deployment should follow .

- Self-hosted open-source solutions require proper security hardening, LLM infrastructure (or API keys), and ongoing maintenance. Evaluation is infrastructure—budget for it accordingly.



---



**Made for AI engineers, platform teams, and developers building transparent AI evaluation solutions.**  

Let's make AI Evaluation & Tracking more open, data-driven, and quality-obsessed.
