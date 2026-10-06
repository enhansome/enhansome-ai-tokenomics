# Awesome AI Tokenomics with stars

[<img src=".github/logo.svg" align="right" width="110" alt="">](https://github.com/QuesmaOrg/awesome-ai-tokenomics)

> Pricing, measurement, optimization, and governance of tokens used by AI models.

Tools, papers, benchmarks, and vendor pages on what AI tokens cost and where they go.

## Contents

* [Monitor](#monitor)
  * [Dashboards](#dashboards)
  * [eBPF Kernel Capture](#ebpf-kernel-capture)
  * [Observability](#observability)
  * [Observability Platforms](#observability-platforms)
  * [OTel for LLMs](#otel-for-llms)
  * [Tracing](#tracing)
* [Optimize](#optimize)
  * [Caching](#caching)
  * [Cheap Local Models](#cheap-local-models)
  * [Compression](#compression)
  * [Context Engineering](#context-engineering)
  * [Cost Controls](#cost-controls)
  * [Gateways and Proxies](#gateways-and-proxies)
  * [Harness Efficiency](#harness-efficiency)
  * [Memory](#memory)
  * [Multi-Agent Systems](#multi-agent-systems)
  * [Prompt Agent Loop](#prompt-agent-loop)
  * [Retrieval Memory](#retrieval-memory)
  * [Retry and Reliability](#retry-and-reliability)
  * [Routing Model Selection](#routing-model-selection)
  * [Search and Retrieval Boundary](#search-and-retrieval-boundary)
  * [Serving Inference](#serving-inference)
  * [Test-Time Compute](#test-time-compute)
  * [Tool Protocol Overhead](#tool-protocol-overhead)
* [Govern](#govern)
  * [Allocation Chargeback](#allocation-chargeback)
  * [Anomaly Detection](#anomaly-detection)
  * [Billing Audit FinOps](#billing-audit-finops)
  * [Budgets Caps](#budgets-caps)
  * [Policy Enforcement](#policy-enforcement)
  * [Spend Management](#spend-management)
  * [Unit Economics](#unit-economics)
* [Understand](#understand)
  * [Buyer Incentives](#buyer-incentives)
  * [Compression Efficacy](#compression-efficacy)
  * [Consolidation](#consolidation)
  * [Market Competitors](#market-competitors)
  * [Market Sizing](#market-sizing)
  * [Model Economics](#model-economics)
  * [Pricing Models](#pricing-models)
  * [Reliability SLAs](#reliability-slas)
  * [Unit Economics](#unit-economics-1)
* [Measure](#measure)
  * [Benchmarks Evals](#benchmarks-evals)
  * [Cache Accounting](#cache-accounting)
  * [Cost Anatomy](#cost-anatomy)
  * [Energy Carbon](#energy-carbon)
  * [Harness Overhead](#harness-overhead)
  * [Metering](#metering)
  * [Transcript Analysis](#transcript-analysis)
  * [Whole Bill Accounting](#whole-bill-accounting)
* [Related lists](#related-lists)

### Legend

Each entry ends with a kind badge: ![tool: MIT](https://img.shields.io/badge/tool-MIT-blue?style=flat-square) (blue, with the license when known), or a gray badge for ![paper](https://img.shields.io/badge/paper-555?style=flat-square), ![bench](https://img.shields.io/badge/bench-555?style=flat-square), ![data](https://img.shields.io/badge/data-555?style=flat-square), ![co](https://img.shields.io/badge/co-555?style=flat-square) for companies, and ![report](https://img.shields.io/badge/report-555?style=flat-square). Plain entries are articles. GitHub-hosted tools also carry a live last-commit badge.

## Monitor

### Dashboards

* [CodexBar](https://github.com/steipete/CodexBar) ⭐ 22,216 | 🐛 176 | 🌐 Swift | 📅 2026-10-06 - Menu-bar app for macOS that shows limits, reset timers, credit balances, and spending across AI providers. ![tool: MIT](https://img.shields.io/badge/tool-MIT-blue?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/steipete/CodexBar?style=flat-square\&label=)
* [ccusage](https://github.com/ccusage/ccusage) ⭐ 18,893 | 🐛 14 | 🌐 Rust | 📅 2026-10-06 - CLI that reads local agent logs to report token usage and cost across coding-agent sources, with caching-aware pricing. ![tool: MIT](https://img.shields.io/badge/tool-MIT-blue?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/ccusage/ccusage?style=flat-square\&label=)
* [CodeBurn](https://github.com/getagentseal/codeburn#find-and-fix-waste) ⭐ 11,345 | 🐛 37 | 🌐 TypeScript | 📅 2026-10-06 - Usage tracker for coding tools whose optimize command flags harness-waste patterns with dollar estimates. ![tool: MIT](https://img.shields.io/badge/tool-MIT-blue?style=flat-square)
* [Claude Code Usage Monitor](https://github.com/Maciek-roboblog/Claude-Code-Usage-Monitor) ⭐ 8,731 | 🐛 38 | 🌐 Python | 📅 2026-07-05 - Live terminal dashboard for Claude Code usage with burn-rate analytics, limit detection, and session-expiry forecasts. ![tool: MIT](https://img.shields.io/badge/tool-MIT-blue?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/Maciek-roboblog/Claude-Code-Usage-Monitor?style=flat-square\&label=)
* [gh-aw](https://github.com/github/gh-aw) ⭐ 5,344 | 🐛 342 | 🌐 Go | 📅 2026-10-06 - GitHub Agentic Workflows runtime with per-run token and cost metering and budget caps that stop a workflow mid-run. ![tool: MIT](https://img.shields.io/badge/tool-MIT-blue?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/github/gh-aw?style=flat-square\&label=)
* [OpenUsage](https://github.com/robinebers/openusage) ⭐ 4,322 | 🐛 52 | 🌐 Swift | 📅 2026-10-06 - Native Swift macOS menu-bar meter for AI coding subscriptions, showing session and weekly limits, credits, and estimated spend. ![tool: MIT](https://img.shields.io/badge/tool-MIT-blue?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/robinebers/openusage?style=flat-square\&label=)
* [OpenLIT](https://github.com/openlit/openlit) ⭐ 2,818 | 🐛 144 | 🌐 TypeScript | 📅 2026-10-05 - OpenTelemetry-native platform with a self-hosted dashboard for LLM cost, token, and latency observability. ![tool: Apache-2.0](https://img.shields.io/badge/tool-Apache--2.0-blue?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/openlit/openlit?style=flat-square\&label=)
* [claude-usage](https://github.com/phuryn/claude-usage) ⭐ 2,251 | 🐛 32 | 🌐 Python | 📅 2026-07-10 - Local dashboard for Claude Code token usage, costs, and session history. ![tool: MIT](https://img.shields.io/badge/tool-MIT-blue?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/phuryn/claude-usage?style=flat-square\&label=)
* [TokenTracker](https://github.com/mm7894215/TokenTracker) ⭐ 1,975 | 🐛 50 | 🌐 JavaScript | 📅 2026-10-04 - Local-first token and cost dashboard for coding tools, with a desktop pet, native widgets, and achievements. ![tool: MIT](https://img.shields.io/badge/tool-MIT-blue?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/mm7894215/TokenTracker?style=flat-square\&label=)
* [ClaudeBar](https://github.com/tddworks/ClaudeBar) ⭐ 1,524 | 🐛 17 | 🌐 Swift | 📅 2026-10-06 - Menu-bar app for macOS that monitors AI coding quotas across multiple providers. ![tool: MIT declared in README](https://img.shields.io/badge/tool-MIT_declared_in_README-blue?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/tddworks/ClaudeBar?style=flat-square\&label=)
* [CodeZeno Usage Monitor](https://github.com/CodeZeno/Claude-Code-Usage-Monitor) ⭐ 572 | 🐛 7 | 🌐 Rust | 📅 2026-10-05 - Windows taskbar widget that shows Claude Code quota and usage without opening a terminal. ![tool: MIT](https://img.shields.io/badge/tool-MIT-blue?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/CodeZeno/Claude-Code-Usage-Monitor?style=flat-square\&label=)
* [antiburn](https://github.com/antiburn/antiburn) ⭐ 203 | 🐛 50 | 🌐 Rust | 📅 2026-10-06 - Desktop app for macOS, Windows and Linux that reads local session logs from coding agents, flags token-burn causes, and applies and verifies supported configuration fixes. ![tool: MIT](https://img.shields.io/badge/tool-MIT-blue?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/antiburn/antiburn?style=flat-square\&label=)
* [Codex Usage Tracker](https://github.com/douglasmonsky/codex-usage-tracker) ⭐ 196 | 🐛 13 | 🌐 Python | 📅 2026-08-20 - Local-first dashboard, CLI, and MCP tools that index Codex CLI logs into SQLite to show where tokens, credits, and cost go, including cache ratios. ![tool: MIT](https://img.shields.io/badge/tool-MIT-blue?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/douglasmonsky/codex-usage-tracker?style=flat-square\&label=)
* [Datadog LLM Observability Cost](https://docs.datadoghq.com/llm_observability/monitoring/cost/) - Datadog documentation on per-request LLM cost estimates computed from token counts and public pricing. ![co](https://img.shields.io/badge/co-555?style=flat-square)
* [Grafana Cloud GenAI Observability](https://grafana.com/docs/grafana-cloud/monitor-applications/ai-observability/genai/observability/) - Prebuilt Grafana Cloud dashboard for LLM cost, token usage, and latency, built on the OpenLIT SDK. ![co](https://img.shields.io/badge/co-555?style=flat-square)

### eBPF Kernel Capture

* [AgentSight](https://github.com/eunomia-bpf/agentsight) ⭐ 725 | 🐛 35 | 🌐 C | 📅 2026-10-05 - Uses eBPF to watch an AI agent from the kernel boundary and correlate what it said it would do with what it did. ![tool: MIT](https://img.shields.io/badge/tool-MIT-blue?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/eunomia-bpf/agentsight?style=flat-square\&label=)
* [OpenTelemetry eBPF Instrumentation](https://opentelemetry.io/docs/zero-code/obi/) - Zero-code eBPF instrumentation from OpenTelemetry that captures GenAI and MCP traces at the kernel layer without an SDK. ![tool: Apache-2.0](https://img.shields.io/badge/tool-Apache--2.0-blue?style=flat-square)

### Observability

* [Braintrust](https://www.braintrust.dev) - Closed-source eval and observability SaaS whose span metrics normalize cached prompt tokens across providers and expose per-user and per-model spend. ![co](https://img.shields.io/badge/co-555?style=flat-square)
* [Langfuse](https://langfuse.com) - Open-source platform for tracing, evaluating, and analyzing LLM and agent transcripts, with a prompt-management layer. ![tool: MIT](https://img.shields.io/badge/tool-MIT-blue?style=flat-square)

### Observability Platforms

* [OpenAI Prompt Cache Diagnostics](https://developers.openai.com/api/docs/guides/prompt-caching/diagnostics) - OpenAI guide to a Responses API feature that returns a machine-readable reason why a prompt prefix was not reused from the cache. ![tool: proprietary](https://img.shields.io/badge/tool-proprietary-blue?style=flat-square)

### OTel for LLMs

* [OpenLLMetry](https://github.com/traceloop/openllmetry) ⭐ 7,469 | 🐛 747 | 🌐 Python | 📅 2026-10-05 - Open-source set of OpenTelemetry-based SDKs and instrumentations for LLM apps, built by Traceloop. ![tool: Apache-2.0](https://img.shields.io/badge/tool-Apache--2.0-blue?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/traceloop/openllmetry?style=flat-square\&label=)
* [OpenTelemetry GenAI Semantic Conventions](https://github.com/open-telemetry/semantic-conventions-genai) ⭐ 408 | 🐛 208 | 🌐 Python | 📅 2026-10-06 - OpenTelemetry conventions that define vendor-neutral token, cost, and cache attribute names for GenAI telemetry.

### Tracing

* [Opik](https://github.com/comet-ml/opik) ⭐ 22,401 | 🐛 181 | 🌐 Python | 📅 2026-10-06 - Open-source (Apache-2.0) LLM observability platform from Comet, with per-span USD cost estimated from token usage. ![tool: Apache-2.0](https://img.shields.io/badge/tool-Apache--2.0-blue?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/comet-ml/opik?style=flat-square\&label=)
* [Arize Phoenix](https://github.com/Arize-ai/phoenix) ⭐ 11,720 | 🐛 1,099 | 🌐 Python | 📅 2026-10-06 - Source-available (Elastic License 2.0) LLM tracing platform that records per-span token counts and USD cost via OpenTelemetry. ![tool: Elastic-2.0](https://img.shields.io/badge/tool-Elastic--2.0-blue?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/Arize-ai/phoenix?style=flat-square\&label=)
* [claude-tap](https://github.com/liaohch3/claude-tap) ⭐ 3,263 | 🐛 40 | 🌐 Python | 📅 2026-09-22 - Local trace viewer that intercepts API traffic from coding agents and shows per-request token breakdowns: input, output, cache read, cache creation. ![tool: MIT](https://img.shields.io/badge/tool-MIT-blue?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/liaohch3/claude-tap?style=flat-square\&label=)
* [LangSmith Cost Tracking](https://docs.langchain.com/langsmith/cost-tracking) - LangChain documentation on cost tracking in LangSmith, its commercial LLM and agent observability service. ![co](https://img.shields.io/badge/co-555?style=flat-square)

## Optimize

### Caching

* [LMCache](https://github.com/LMCache/LMCache) ⭐ 11,961 | 🐛 753 | 🌐 Python | 📅 2026-10-06 - Self-hosted KV-cache layer beneath vLLM that gives token-level cache-hit observability for teams that own their GPUs. ![tool: Apache-2.0](https://img.shields.io/badge/tool-Apache--2.0-blue?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/LMCache/LMCache?style=flat-square\&label=)
* [prompt-cache](https://github.com/messkan/prompt-cache) ⭐ 428 | 🐛 6 | 🌐 Go | 📅 2026-08-18 - Go LLM proxy with a three-tier semantic cache that uses a cheap verification model for borderline similarity matches. ![tool: MIT](https://img.shields.io/badge/tool-MIT-blue?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/messkan/prompt-cache?style=flat-square\&label=)
* [khazad](https://github.com/GuglielmoCerri/khazad) ⭐ 33 | 🐛 0 | 🌐 Python | 📅 2026-07-10 - Transport-layer semantic cache for LLM APIs on Redis 8 Vector Sets that intercepts HTTP traffic without application code changes. ![tool: MIT](https://img.shields.io/badge/tool-MIT-blue?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/GuglielmoCerri/khazad?style=flat-square\&label=)
* [Redis LangCache](https://redis.io/langcache/) - Managed semantic cache with a REST API that returns a stored response when a new query is similar to a past one. ![tool: proprietary](https://img.shields.io/badge/tool-proprietary-blue?style=flat-square)

### Cheap Local Models

* [Ollama](https://github.com/ollama/ollama) ⭐ 182,313 | 🐛 4,179 | 🌐 Go | 📅 2026-10-06 - Runtime for running open-weight models locally on hardware you already own. ![tool: MIT](https://img.shields.io/badge/tool-MIT-blue?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/ollama/ollama?style=flat-square\&label=)
* [llama.cpp](https://github.com/ggml-org/llama.cpp) ⭐ 130,440 | 🐛 2,524 | 🌐 C++ | 📅 2026-10-06 - Open-source (MIT) local LLM inference engine with a built-in OpenAI-compatible server. ![tool: MIT](https://img.shields.io/badge/tool-MIT-blue?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/ggml-org/llama.cpp?style=flat-square\&label=)

### Compression

* [rtk](https://github.com/rtk-ai/rtk) ⭐ 82,490 | 🐛 1,505 | 🌐 Rust | 📅 2026-10-06 - Single-binary Rust CLI proxy that compresses the output of common dev commands before it reaches a coding agent's context window. ![tool: Apache-2.0](https://img.shields.io/badge/tool-Apache--2.0-blue?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/rtk-ai/rtk?style=flat-square\&label=)
* [headroom](https://github.com/headroomlabs-ai/headroom) ⭐ 74,473 | 🐛 416 | 🌐 Python | 📅 2026-10-06 - Apache-2.0 context-compression tool for LLM and agent pipelines. ![tool: Apache-2.0](https://img.shields.io/badge/tool-Apache--2.0-blue?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/headroomlabs-ai/headroom?style=flat-square\&label=)
* [Context Mode](https://github.com/mksglu/context-mode) ⭐ 25,509 | 🐛 332 | 🌐 TypeScript | 📅 2026-10-05 - MCP server that sandboxes tool calls and returns only the distilled result to the model. ![tool: Elastic-2.0](https://img.shields.io/badge/tool-Elastic--2.0-blue?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/mksglu/context-mode?style=flat-square\&label=)
* [TOON](https://github.com/toon-format/toon) ⭐ 25,454 | 🐛 1 | 🌐 TypeScript | 📅 2026-10-06 - Compact, human-readable, lossless serialization of the JSON data model, designed for LLM input. ![tool: MIT](https://img.shields.io/badge/tool-MIT-blue?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/toon-format/toon?style=flat-square\&label=)
* [LLMLingua](https://github.com/microsoft/LLMLingua) ⭐ 6,729 | 🐛 122 | 🌐 Python | 📅 2026-09-10 - Microsoft prompt-compression library that uses a small model to drop low-information tokens before a prompt reaches the target LLM. ![tool: MIT](https://img.shields.io/badge/tool-MIT-blue?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/microsoft/LLMLingua?style=flat-square\&label=)
* [lean-ctx](https://github.com/yvgude/lean-ctx) ⭐ 3,864 | 🐛 13 | 🌐 Rust | 📅 2026-10-06 - Rust MCP server that mediates what a coding agent reads, with a savings ledger and an accounting of its own context overhead. ![tool: Apache-2.0](https://img.shields.io/badge/tool-Apache--2.0-blue?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/yvgude/lean-ctx?style=flat-square\&label=)
* [snip](https://github.com/edouard-claude/snip) ⭐ 464 | 🐛 2 | 🌐 Go | 📅 2026-09-30 - Single-binary Go CLI proxy that filters dev-command output before it reaches a coding agent, using declarative YAML filter pipelines. ![tool: MIT](https://img.shields.io/badge/tool-MIT-blue?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/edouard-claude/snip?style=flat-square\&label=)
* [llmtrim](https://github.com/fkiene/llmtrim) ⭐ 244 | 🐛 12 | 🌐 Rust | 📅 2026-10-01 - Local proxy that compresses a coding agent's prompt, tool schemas, and history before forwarding, and can reroute Claude calls to Grok. ![tool: MPL-2.0](https://img.shields.io/badge/tool-MPL--2.0-blue?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/fkiene/llmtrim?style=flat-square\&label=)
* [Minification of State-in-Context Agents](https://arxiv.org/abs/2606.01326) - ICPC 2026 study of minifying code in a coding agent's context, measuring the input-token savings against the accuracy cost. ![paper](https://img.shields.io/badge/paper-555?style=flat-square)

### Context Engineering

* [Codex CLI Compaction Issue](https://github.com/openai/codex/issues/16812) ⭐ 127,996 | 🐛 20,861 | 🌐 Rust | 📅 2026-10-06 - GitHub issue reporting that a Codex CLI upgrade made context compaction fire more often and raised token consumption for identical tasks.
* [Serena](https://github.com/oraios/serena) ⭐ 30,042 | 🐛 162 | 🌐 Python | 📅 2026-10-06 - Open-source MCP toolkit that gives a coding agent IDE-grade semantic code retrieval and editing. ![tool: GPL-3.0-or-later](https://img.shields.io/badge/tool-GPL--3.0--or--later-blue?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/oraios/serena?style=flat-square\&label=)
* [Repomix](https://github.com/yamadashy/repomix) ⭐ 28,720 | 🐛 153 | 🌐 TypeScript | 📅 2026-10-03 - Packs an entire repository into a single AI-friendly file, reports token counts, and uses Tree-sitter to compress code to signatures. ![tool: MIT](https://img.shields.io/badge/tool-MIT-blue?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/yamadashy/repomix?style=flat-square\&label=)
* [RULER](https://github.com/NVIDIA/RULER) ⭐ 1,621 | 🐛 23 | 🌐 Python | 📅 2026-07-22 - NVIDIA long-context benchmark that measures how model quality holds up as the context window fills. ![bench](https://img.shields.io/badge/bench-555?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/NVIDIA/RULER?style=flat-square\&label=)
* [trace-mcp](https://github.com/nikolai-vysotskyi/trace-mcp) ⭐ 185 | 🐛 21 | 🌐 TypeScript | 📅 2026-10-06 - MCP server that pre-indexes a repository into a symbol and dependency graph so an agent can query call graphs, change impact, or file outlines instead of reading files. ![tool: MIT](https://img.shields.io/badge/tool-MIT-blue?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/nikolai-vysotskyi/trace-mcp?style=flat-square\&label=)
* [CliffCompaction](https://github.com/nguyenvuthientrang/cliffcompaction) ⭐ 52 | 🐛 0 | 🌐 Python | 📅 2026-09-23 - CMU autocompaction proxy that shrinks an agent's context only by truncating or dropping content, never by LLM rewriting, and works in front of Claude Code or Codex. ![tool: MIT](https://img.shields.io/badge/tool-MIT-blue?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/nguyenvuthientrang/cliffcompaction?style=flat-square\&label=)
* [AgentDiet](https://arxiv.org/abs/2509.23586) - Paper on an inference-time module that strips useless, redundant, and expired information from an agent's trajectory. ![paper](https://img.shields.io/badge/paper-555?style=flat-square)
* [Anthropic Context Management](https://platform.claude.com/docs/en/build-with-claude/context-editing) - Anthropic documentation for context editing, the memory tool, and server-side compaction in the Claude API.
* [Claude Code Compaction Engine](https://barazany.dev/blog/claude-codes-compaction-engine) - Blog post describing the three-tier compaction engine Claude Code uses to trim a filling context window, and its cache and correctness failure modes.
* [Context Rot](https://www.trychroma.com/research/context-rot) - Chroma study of how LLM output quality changes as input length grows, with task difficulty held fixed. ![report](https://img.shields.io/badge/report-555?style=flat-square)
* [ContextBudget](https://arxiv.org/abs/2604.01664) - Paper on BACM, a method where an agent decides when and how much to compress its history based on the remaining context budget. ![paper](https://img.shields.io/badge/paper-555?style=flat-square)
* [Cursor Dynamic Context Discovery](https://cursor.com/blog/dynamic-context-discovery) - Cursor blog post on loading tool schemas and large outputs on demand instead of eagerly, and on Composer self-summarization.
* [Self-Compacting Language Model Agents](https://arxiv.org/abs/2606.23525) - Paper introducing SELFCOMPACT, where the model itself decides when and how to compress a growing agent trace. ![paper](https://img.shields.io/badge/paper-555?style=flat-square)

### Cost Controls

* [Claude Code Runaway-Loop Guardrails](https://github.com/anthropics/claude-code/releases/tag/v2.1.212) ⭐ 149,562 | 🐛 14,284 | 🌐 TypeScript | 📅 2026-10-06 - Claude Code release notes for first-party guardrails against runaway agent loops.
* [Claude Code Changelog](https://code.claude.com/docs/en/changelog) - Official Claude Code changelog covering spend controls such as subagent caps, budget limits, and gateway spend limits.

### Gateways and Proxies

* [LiteLLM](https://github.com/BerriAI/litellm) ⭐ 60,211 | 🐛 5,206 | 🌐 Python | 📅 2026-10-06 - Open-source gateway fronting 100+ LLM APIs that computes per-request dollar cost from a pricing map, with spend limits. ![tool: MIT](https://img.shields.io/badge/tool-MIT-blue?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/BerriAI/litellm?style=flat-square\&label=)
* [Bifrost](https://github.com/maximhq/bifrost) ⭐ 8,576 | 🐛 1,191 | 🌐 Go | 📅 2026-10-06 - Go-based AI gateway from Maxim AI that fronts many models with low added latency. ![tool: Apache-2.0](https://img.shields.io/badge/tool-Apache--2.0-blue?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/maximhq/bifrost?style=flat-square\&label=)
* [Cloudflare AI Gateway Spend Limits](https://developers.cloudflare.com/ai-gateway/features/spend-limits/) - Cloudflare AI Gateway documentation on dollar-denominated spend limits that block or reroute requests once a budget is hit. ![co](https://img.shields.io/badge/co-555?style=flat-square)
* [Helicone](https://helicone.ai) - Open-source (Apache-2.0) LLM proxy that logs every request's cost, latency, and tokens. ![tool: Apache-2.0](https://img.shields.io/badge/tool-Apache--2.0-blue?style=flat-square)
* [Kong AI Gateway](https://developer.konghq.com/ai-gateway/) - AI layer of Kong's API-gateway platform that meters LLM, agent, and MCP traffic for billing, showback, and chargeback. ![co](https://img.shields.io/badge/co-555?style=flat-square)
* [OpenRouter Provider Selection](https://openrouter.ai/docs/guides/routing/provider-selection) - OpenRouter documentation on routing requests across models and providers by price, with fallback on outages. ![co](https://img.shields.io/badge/co-555?style=flat-square)
* [Portkey AI Gateway Budget Limits](https://portkey.ai/docs/product/ai-gateway/virtual-keys/budget-limits) - Portkey documentation on routing LLM traffic across providers and enforcing hard USD budget limits on virtual keys. ![co](https://img.shields.io/badge/co-555?style=flat-square)

### Harness Efficiency

* [SoL-Pi](https://nvlabs.github.io/SoL-Pi/) - NVIDIA Labs extension for the Pi coding harness that packages four token-efficiency mechanisms. ![tool: MIT](https://img.shields.io/badge/tool-MIT-blue?style=flat-square)
* [WOZCODE](https://wozcode.com) - Proprietary Claude Code plugin that publishes its own paired-task dataset comparing cost and tokens against stock Claude Code. ![tool: proprietary](https://img.shields.io/badge/tool-proprietary-blue?style=flat-square)

### Memory

* [claude-mem](https://github.com/thedotmack/claude-mem) ⭐ 96,830 | 🐛 88 | 🌐 TypeScript | 📅 2026-10-06 - Coding-agent memory layer that captures every session, compresses it with AI, and re-injects relevant context in later sessions. ![tool: Apache-2.0](https://img.shields.io/badge/tool-Apache--2.0-blue?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/thedotmack/claude-mem?style=flat-square\&label=)
* [Mem0](https://github.com/mem0ai/mem0) ⭐ 66,650 | 🐛 789 | 🌐 Python | 📅 2026-10-06 - Open-source memory layer that extracts salient facts from conversations and retrieves only the relevant ones per call. ![tool: Apache-2.0](https://img.shields.io/badge/tool-Apache--2.0-blue?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/mem0ai/mem0?style=flat-square\&label=)
* [Cognee](https://github.com/topoteretes/cognee) ⭐ 31,438 | 🐛 493 | 🌐 Python | 📅 2026-10-06 - Open-source (Apache-2.0) AI-memory platform that gives agents persistent memory through a self-hosted knowledge graph. ![tool: Apache-2.0](https://img.shields.io/badge/tool-Apache--2.0-blue?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/topoteretes/cognee?style=flat-square\&label=)
* [Supermemory](https://github.com/supermemoryai/supermemory) ⭐ 31,105 | 🐛 103 | 🌐 TypeScript | 📅 2026-10-06 - Memory and context engine for agents. ![tool: MIT](https://img.shields.io/badge/tool-MIT-blue?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/supermemoryai/supermemory?style=flat-square\&label=)
* [Letta](https://github.com/letta-ai/letta) ⭐ 25,043 | 🐛 0 | 📅 2026-09-10 - Platform for stateful agents, from the MemGPT project, that pages an LLM's context like an operating system. ![tool: Apache-2.0](https://img.shields.io/badge/tool-Apache--2.0-blue?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/letta-ai/letta?style=flat-square\&label=)
* [LangMem](https://github.com/langchain-ai/langmem) ⭐ 1,694 | 🐛 67 | 🌐 Python | 📅 2026-10-02 - LangChain long-term memory library that extracts and consolidates facts from conversations and integrates with LangGraph's memory store. ![tool: MIT](https://img.shields.io/badge/tool-MIT-blue?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/langchain-ai/langmem?style=flat-square\&label=)
* [claude-code-memory-setup](https://github.com/lucasrosati/claude-code-memory-setup) ⭐ 1,009 | 🐛 5 | 🌐 Python | 📅 2026-09-11 - Practitioner recipe that pairs an Obsidian memory vault with a local AST code-graph tool. ![tool: MIT](https://img.shields.io/badge/tool-MIT-blue?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/lucasrosati/claude-code-memory-setup?style=flat-square\&label=)
* [Karpathy's LLM Wiki](https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f) - Gist by Andrej Karpathy describing a pattern where an agent builds and maintains a persistent markdown wiki from your sources.
* [Zep / Graphiti](https://www.getzep.com/) - Memory platform for agents built on temporal knowledge graphs. ![tool: Apache-2.0](https://img.shields.io/badge/tool-Apache--2.0-blue?style=flat-square)

### Multi-Agent Systems

* [LangChain](https://github.com/langchain-ai/langchain) ⭐ 147,493 | 🐛 641 | 🌐 Python | 📅 2026-10-06 - MIT-licensed agent framework underneath LangGraph, LangMem, and LangSmith that defines cache-aware usage metadata and ships context-editing, summarization, and call-limit middleware. ![tool: MIT](https://img.shields.io/badge/tool-MIT-blue?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/langchain-ai/langchain?style=flat-square\&label=)
* [CrewAI](https://github.com/crewAIInc/crewAI) ⭐ 59,387 | 🐛 572 | 🌐 Python | 📅 2026-10-06 - MIT-licensed multi-agent orchestration framework whose crew object reports cache-aware token totals. ![tool: MIT](https://img.shields.io/badge/tool-MIT-blue?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/crewAIInc/crewAI?style=flat-square\&label=)
* [LangGraph](https://github.com/langchain-ai/langgraph) ⭐ 42,770 | 🐛 820 | 🌐 Python | 📅 2026-10-05 - LangChain graph orchestration library for stateful agents, with per-super-step checkpointing and an opt-in node result cache. ![tool: MIT](https://img.shields.io/badge/tool-MIT-blue?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/langchain-ai/langgraph?style=flat-square\&label=)
* [CrewAI Hierarchical Process](https://docs.crewai.com/en/learn/hierarchical-process) - CrewAI documentation on the hierarchical process, where a manager LLM plans and validates work delegated to other agents.
* [SupervisorAgent](https://arxiv.org/abs/2510.26585) - Paper on a lightweight, modular framework for runtime, adaptive supervision of multi-agent systems. ![paper](https://img.shields.io/badge/paper-555?style=flat-square)

### Prompt Agent Loop

* [benjamin-plus](https://github.com/JetBrains/benjamin-plus-skill) ⭐ 329 | 🐛 2 | 🌐 Shell | 📅 2026-08-27 - JetBrains skill, a small instruction payload that changes how a coding agent looks things up and waits, with a published A/B rig. ![tool: MIT](https://img.shields.io/badge/tool-MIT-blue?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/JetBrains/benjamin-plus-skill?style=flat-square\&label=)
* [token-ninja](https://github.com/oanhduong/token-ninja) ⭐ 38 | 🐛 0 | 🌐 TypeScript | 📅 2026-09-18 - Intercepts deterministic commands like `git status` or `npm test` before they reach the model and runs them locally. ![tool: MIT](https://img.shields.io/badge/tool-MIT-blue?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/oanhduong/token-ninja?style=flat-square\&label=)
* [LOOP Skill Engine](https://arxiv.org/abs/2605.14237) - Paper on recording an agent's first run of a repetitive task with full LLM reasoning, then replaying the extracted tool-call template without calling the LLM. ![paper](https://img.shields.io/badge/paper-555?style=flat-square)
* [Orchestrator-Worker Model Tiering](https://www.mindstudio.ai/blog/smart-orchestrator-cheaper-sub-agent-models-claude-code) - Blog post on the pattern where a capable model plans and cheaper agents execute, using Claude Code subagents.

### Retrieval Memory

* [LlamaIndex](https://github.com/run-llama/llama_index) ⭐ 52,418 | 🐛 897 | 🌐 Python | 📅 2026-10-05 - MIT-licensed data framework for LLM applications with a token-counting callback and an optional hard token budget. ![tool: MIT](https://img.shields.io/badge/tool-MIT-blue?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/run-llama/llama_index?style=flat-square\&label=)
* [PageIndex](https://github.com/VectifyAI/PageIndex) ⭐ 38,725 | 🐛 119 | 🌐 Python | 📅 2026-10-05 - Vectorless RAG engine that builds a hierarchical tree index over long documents and has an LLM reason over the index instead of embedding chunks. ![tool: MIT](https://img.shields.io/badge/tool-MIT-blue?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/VectifyAI/PageIndex?style=flat-square\&label=)
* [Signet AI](https://github.com/Signet-AI/signetai) ⭐ 303 | 🐛 84 | 🌐 TypeScript | 📅 2026-10-06 - Local-first memory and context layer that syncs memories, transcripts, and secrets across Claude Code, Codex, OpenCode, and other harnesses. ![tool: Apache-2.0](https://img.shields.io/badge/tool-Apache--2.0-blue?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/Signet-AI/signetai?style=flat-square\&label=)
* [xmemory](https://arxiv.org/abs/2604.27906) - Paper on schema-grounded agent memory that extracts structured facts instead of storing text. ![tool: proprietary](https://img.shields.io/badge/tool-proprietary-blue?style=flat-square)

### Retry and Reliability

* [Claude Code v2.1.199](https://github.com/anthropics/claude-code/releases/tag/v2.1.199) ⭐ 149,562 | 🐛 14,284 | 🌐 TypeScript | 📅 2026-10-06 - Claude Code release notes covering automatic retry of rate-limit errors with backoff and partial-output preservation.

### Routing Model Selection

* [ruflo](https://github.com/ruvnet/ruflo) ⭐ 73,964 | 🐛 1,116 | 🌐 TypeScript | 📅 2026-10-06 - Open-source agent meta-harness for Claude Code and Codex with swarm orchestration, persistent memory, and cost-adjusted model routing. ![tool: MIT](https://img.shields.io/badge/tool-MIT-blue?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/ruvnet/ruflo?style=flat-square\&label=)
* [Claude Code Router](https://github.com/musistudio/claude-code-router) ⭐ 37,568 | 🐛 1,171 | 🌐 TypeScript | 📅 2026-09-26 - Local gateway that puts Claude Code, Codex, and other coding CLIs behind one endpoint and routes each request by rules or a prompt tag. ![tool: MIT](https://img.shields.io/badge/tool-MIT-blue?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/musistudio/claude-code-router?style=flat-square\&label=)
* [Plano](https://github.com/katanemo/plano) ⭐ 7,078 | 🐛 144 | 🌐 Rust | 📅 2026-09-28 - Envoy-based proxy whose router matches queries to user-defined domains and actions using a small routing model. ![tool: Apache-2.0](https://img.shields.io/badge/tool-Apache--2.0-blue?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/katanemo/plano?style=flat-square\&label=)
* [vLLM Semantic Router](https://github.com/vllm-project/semantic-router) ⭐ 6,037 | 🐛 641 | 🌐 Go | 📅 2026-10-06 - Open-source, self-hostable router that sends routine queries to cheap or local models and hard ones to stronger backends. ![tool: Apache-2.0](https://img.shields.io/badge/tool-Apache--2.0-blue?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/vllm-project/semantic-router?style=flat-square\&label=)
* [Weave Router](https://github.com/workweave/router) ⭐ 5,574 | 🐛 157 | 🌐 Go | 📅 2026-10-06 - Drop-in proxy that picks a model for every request with an on-box embedding cluster scorer, under the Elastic License 2.0. ![tool: ELv2](https://img.shields.io/badge/tool-ELv2-blue?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/workweave/router?style=flat-square\&label=)
* [Antigravity CLI Changelog](https://github.com/google-antigravity/antigravity-cli/blob/main/CHANGELOG.md) ⭐ 2,487 | 🐛 658 | 📅 2026-10-06 - Release notes for Antigravity CLI covering per-subagent model-tier routing and an effort control. ![tool](https://img.shields.io/badge/tool-blue?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/google-antigravity/antigravity-cli?style=flat-square\&label=)
* [NadirClaw](https://github.com/NadirRouter/NadirClaw) ⭐ 656 | 🐛 2 | 🌐 Python | 📅 2026-10-06 - OpenAI-compatible pre-router proxy for coding harnesses that picks the cheapest model predicted to answer and escalates on failure. ![tool: PolyForm Noncommercial 1.0.0](https://img.shields.io/badge/tool-PolyForm_Noncommercial_1.0.0-blue?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/NadirRouter/NadirClaw?style=flat-square\&label=)
* [pi-model-router](https://github.com/yeliu84/pi-model-router) ⭐ 73 | 🐛 10 | 🌐 TypeScript | 📅 2026-07-20 - Heuristic per-turn model router for the pi coding agent, with an OpenCode counterpart that routes by keyword and word-count rules. ![tool: MIT](https://img.shields.io/badge/tool-MIT-blue?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/yeliu84/pi-model-router?style=flat-square\&label=)
* [Claude Code via LiteLLM](https://docs.litellm.ai/docs/tutorials/claude_non_anthropic_models) - LiteLLM tutorial for pointing Claude Code at a LiteLLM proxy so cheaper or non-Anthropic models can handle some work.
* [Cluster, Route, Escalate](https://arxiv.org/abs/2606.27457) - Paper proposing a two-stage cost-aware cascade for LLM serving that combines routing and escalation. ![paper](https://img.shields.io/badge/paper-555?style=flat-square)
* [Cursor Router](https://cursor.com/blog/router) - Cursor blog post on Auto mode, which classifies each request and routes it to a model under Intelligence, Balance, or Cost modes. ![co](https://img.shields.io/badge/co-555?style=flat-square)
* [Distilling Agent Behavior](https://arxiv.org/abs/2505.17612) - Paper on distilling a large agent's behavior into a small task-specific model to cut per-token cost.
* [GitHub Copilot Auto Model Selection](https://docs.github.com/en/copilot/concepts/models/auto-model-selection) - GitHub documentation on Copilot's Auto setting, which routes by model health and task complexity. ![co](https://img.shields.io/badge/co-555?style=flat-square)
* [MTRouter](https://arxiv.org/abs/2604.23530) - Paper on picking a different model for each turn of a multi-turn conversation to meet a cost budget. ![paper](https://img.shields.io/badge/paper-555?style=flat-square)
* [OpenCode](https://opencode.ai/docs/) - Open-source (MIT) coding-agent CLI with explicit cost and model routing configuration. ![tool: MIT](https://img.shields.io/badge/tool-MIT-blue?style=flat-square)
* [OrcaRouter](https://arxiv.org/abs/2605.30736) - Paper on a production LLM router built on a LinUCB bandit. ![paper](https://img.shields.io/badge/paper-555?style=flat-square)
* [TypeSafe Jev](https://typesafe.ai/blog/introducing-system-one-models-and-jev) - TypeSafe AI blog post on a hosted decision model that answers typed questions with a choice or score and a probability.

### Search and Retrieval Boundary

* [Firecrawl](https://github.com/firecrawl/firecrawl) ⭐ 189,033 | 🐛 530 | 🌐 TypeScript | 📅 2026-10-06 - Web scraping API that converts pages to markdown or structured JSON before they reach the model. ![tool: AGPL-3.0](https://img.shields.io/badge/tool-AGPL--3.0-blue?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/firecrawl/firecrawl?style=flat-square\&label=)
* [Valyu](https://github.com/valyuAI/valyu-benchmarks) ⭐ 14 | 🐛 0 | 🌐 Python | 📅 2026-05-04 - Search and deep-research API with an open benchmark harness for cost-versus-accuracy results on the DRACO benchmark. ![co](https://img.shields.io/badge/co-555?style=flat-square)
* [Exa](https://exa.ai/pricing) - Search API for agents that bills content retrieval separately per type, such as query-scoped highlights or summaries. ![co](https://img.shields.io/badge/co-555?style=flat-square)
* [Parallel Benchmarks](https://parallel.ai/benchmarks) - Parallel web search and extraction API benchmarks page with accuracy-versus-cost tables. ![co](https://img.shields.io/badge/co-555?style=flat-square)
* [Tavily](https://docs.tavily.com/documentation/api-credits) - Search API for agents that returns capped content snippets instead of full pages and prices by credit. ![co](https://img.shields.io/badge/co-555?style=flat-square)

### Serving Inference

* [vLLM](https://github.com/vllm-project/vllm) ⭐ 93,253 | 🐛 8,488 | 🌐 Python | 📅 2026-10-06 - Open-source LLM serving engine that uses PagedAttention to manage KV-cache memory in blocks. ![tool: Apache-2.0](https://img.shields.io/badge/tool-Apache--2.0-blue?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/vllm-project/vllm?style=flat-square\&label=)
* [SGLang](https://github.com/sgl-project/sglang) ⭐ 36,813 | 🐛 5,532 | 🌐 Python | 📅 2026-10-06 - Serving framework for large language and multimodal models. ![tool: Apache-2.0](https://img.shields.io/badge/tool-Apache--2.0-blue?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/sgl-project/sglang?style=flat-square\&label=)
* [TensorRT-LLM](https://github.com/NVIDIA/TensorRT-LLM) ⭐ 14,765 | 🐛 1,584 | 🌐 Python | 📅 2026-10-06 - NVIDIA open-source LLM inference engine with KV-cache reuse, in-flight batching, and prefill-decode disaggregation. ![tool: Apache-2.0](https://img.shields.io/badge/tool-Apache--2.0-blue?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/NVIDIA/TensorRT-LLM?style=flat-square\&label=)
* [RLM-Cascade](https://arxiv.org/abs/2606.22840) - Paper on response-level speculative decoding at the gateway, where a cheap draft model answers first and a stronger verifier accepts or rewrites it. ![paper](https://img.shields.io/badge/paper-555?style=flat-square)

### Test-Time Compute

* [Stop When Reasoning Converges](https://arxiv.org/abs/2605.17672) - Paper on stopping reasoning once a solution has stabilized, to avoid wasted tokens and latency from overthinking. ![paper](https://img.shields.io/badge/paper-555?style=flat-square)
* [When More Reasoning Hurts](https://arxiv.org/abs/2604.10739) - Paper on how giving a model more reasoning budget can lower performance and raise cost. ![paper](https://img.shields.io/badge/paper-555?style=flat-square)

### Tool Protocol Overhead

* [Coral](https://github.com/withcoral/coral) ⭐ 4,941 | 🐛 317 | 🌐 Rust | 📅 2026-10-02 - Gives agents one SQL interface over APIs and internal systems instead of many MCP servers, with its own task benchmark. ![tool: Apache-2.0](https://img.shields.io/badge/tool-Apache--2.0-blue?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/withcoral/coral?style=flat-square\&label=)
* [Code Execution with MCP](https://www.anthropic.com/engineering/code-execution-with-mcp) - Anthropic engineering post on agents calling MCP servers by writing and executing code so unused tool schemas stay out of the context window.
* [MCP Tool Descriptions Are Smelly!](https://arxiv.org/abs/2602.14878) - Study of how poorly written MCP tool descriptions affect agent efficiency, using an LLM-jury scanner on MCP-Universe. ![paper](https://img.shields.io/badge/paper-555?style=flat-square)
* [StackOne Falcon](https://www.stackone.com/blog/mcp-token-optimization/) - Execution engine that cuts tool-calling tokens by filtering tool definitions, shaping responses, and running code at the edge. ![co](https://img.shields.io/badge/co-555?style=flat-square)
* [Tool Attention Is All You Need](https://arxiv.org/abs/2604.21816) - Paper on the cost of MCP re-sending every tool's full schema on every turn, known as the MCP/Tools Tax. ![paper](https://img.shields.io/badge/paper-555?style=flat-square)

## Govern

### Allocation Chargeback

* [CloudZero](https://www.cloudzero.com/blog/ai-cost-optimization-at-scale/) - Commercial cloud and AI cost-intelligence and FinOps platform. ![co](https://img.shields.io/badge/co-555?style=flat-square)
* [JetBrains AI Credits for Business](https://blog.jetbrains.com/blog/2026/07/07/jetbrains-ai-for-teams-and-organizations-from-fragmented-ai-usage-to-coordinated-software-development/) - JetBrains blog post on moving business AI plans from monthly per-seat licenses to reallocatable credits with a governance dashboard.
* [Mavvrik](https://www.mavvrik.ai/press-releases/mavvrik-unveils-full-stack-ai-cost-governance/) - AI and hybrid-infrastructure cost governance and FinOps platform, formerly DigitalEx. ![co](https://img.shields.io/badge/co-555?style=flat-square)
* [Pay-i](https://docs.ascerta.com/) - SDK-based GenAI cost-observability platform, now Ascerta, that tracks token-level spend per call and rolls it up into cost-center allocation. ![co](https://img.shields.io/badge/co-555?style=flat-square)

### Anomaly Detection

* [Denial-of-Wallet Attacks](https://arxiv.org/abs/2601.10955) - Paper on attacks that exploit pay-per-token pricing to inflate a bill, through stolen credentials or agents steered into runaway token use. ![paper](https://img.shields.io/badge/paper-555?style=flat-square)
* [Governance Decay](https://arxiv.org/abs/2606.22528) - Paper showing that compacting an agent's context can silently erase governance and safety constraints. ![paper](https://img.shields.io/badge/paper-555?style=flat-square)

### Billing Audit FinOps

* [AgentMeasure](https://github.com/roy-tong/AgentMeasure) ⭐ 218 | 🐛 12 | 🌐 Python | 📅 2026-10-05 - Open-source (MIT) measurement standard and local checker that audits vendor billing claims against a named-rule settlement spec. ![tool: MIT](https://img.shields.io/badge/tool-MIT-blue?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/roy-tong/AgentMeasure?style=flat-square\&label=)
* [Cloud FinOps Skill](https://github.com/OptimNow/cloud-finops-skills) ⭐ 58 | 🐛 1 | 🌐 Python | 📅 2026-10-02 - Markdown reference library for agents, packaged as a Claude skill and an MCP server, covering billing mechanics for AI, cloud, and SaaS spend. ![tool: CC BY-SA 4.0](https://img.shields.io/badge/tool-CC_BY--SA_4.0-blue?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/OptimNow/cloud-finops-skills?style=flat-square\&label=)
* [FinOps for AI](https://www.finops.org/framework/scope/finops-for-ai/) - FinOps Foundation practitioner framework for governing AI, GPU, and token spend. ![tool](https://img.shields.io/badge/tool-blue?style=flat-square)
* [Vaudit TokenAudit](https://www.vaudit.com/token-audit) - Vaudit's LLM invoice-reconciliation product, from an independent spend-auditing and recovery platform. ![co](https://img.shields.io/badge/co-555?style=flat-square)

### Budgets Caps

* [Claude Max Plan Usage](https://support.claude.com/en/articles/11049741-what-is-the-max-plan) - Anthropic support article describing Max plan usage as multipliers of Pro, without absolute quota numbers.
* [TrueFoundry AI Gateway Budget Limiting](https://www.truefoundry.com/docs/ai-gateway/budgetlimiting) - TrueFoundry documentation on budget limits in its AI gateway for GenAI deployments. ![co](https://img.shields.io/badge/co-555?style=flat-square)

### Policy Enforcement

* [AEGIS](https://github.com/Justin0504/Aegis) ⭐ 493 | 🐛 4 | 🌐 TypeScript | 📅 2026-09-06 - Open-source (MIT) pre-execution firewall and cryptographic audit layer for AI agents. ![tool: MIT](https://img.shields.io/badge/tool-MIT-blue?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/Justin0504/Aegis?style=flat-square\&label=)
* [ActPlane](https://github.com/eunomia-bpf/ActPlane) ⭐ 104 | 🐛 15 | 🌐 C | 📅 2026-10-03 - Policy-enforcement engine, built on eBPF at the OS level, for AI-agent harnesses like Claude Code and Codex. ![tool: MIT](https://img.shields.io/badge/tool-MIT-blue?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/eunomia-bpf/ActPlane?style=flat-square\&label=)
* [MCPGuard-Dynamic](https://github.com/facebook/mcpguard-dynamic) ⭐ 74 | 🐛 1 | 🌐 C | 📅 2026-07-22 - Research-grade kernel-level eBPF sandbox for MCP, published under Meta's GitHub organization. ![tool: MIT](https://img.shields.io/badge/tool-MIT-blue?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/facebook/mcpguard-dynamic?style=flat-square\&label=)

### Spend Management

* [nable](https://github.com/getnable/finopsmcp) ⭐ 18 | 🐛 13 | 🌐 Python | 📅 2026-10-03 - MCP server that reports cloud and AI spend in one answer, running locally with a free local package and some paid features. ![tool: Apache-2.0](https://img.shields.io/badge/tool-Apache--2.0-blue?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/getnable/finopsmcp?style=flat-square\&label=)
* [ChatGPT Enterprise Spend Controls](https://openai.com/index/chatgpt-enterprise-spend-controls/) - OpenAI post on usage analytics and spend controls for ChatGPT Enterprise and Business: credit caps, request workflows, and a Cost API. ![tool: proprietary](https://img.shields.io/badge/tool-proprietary-blue?style=flat-square)
* [Claude Enterprise Admin Controls](https://www.claude.com/blog/giving-admins-more-visibility-and-control-over-claude-usage-and-spend) - Anthropic post on admin analytics and cost controls for Claude Enterprise and Team: spend caps, model defaults, and per-user cost analytics. ![tool: proprietary](https://img.shields.io/badge/tool-proprietary-blue?style=flat-square)
* [PointFive TokenShift](https://www.pointfive.co/press/pointfive-launches-ai-efficiency-os-tokenshift) - PointFive's AI Efficiency OS, which governs coding-agent token spend across Claude Code, Cursor, Codex, and other tools. ![co](https://img.shields.io/badge/co-555?style=flat-square)
* [Revenium](https://www.revenium.ai/) - Tracks AI agent spend at runtime, attributing every model call and tool cost to its workflow, with automatic shutoff on runaway budgets. ![co](https://img.shields.io/badge/co-555?style=flat-square)
* [Vantage](https://www.vantage.sh/blog/agentic-coding-costs) - FinOps platform that ingests token-level cost data from Anthropic and OpenAI usage APIs, plus Cursor and cloud spend. ![co](https://img.shields.io/badge/co-555?style=flat-square)
* [Vercel AI Gateway Budgets](https://vercel.com/changelog/budgets-for-api-keys-on-ai-gateway) - Vercel changelog on per-API-key dollar spend caps with daily, weekly, or monthly refresh. ![tool: proprietary](https://img.shields.io/badge/tool-proprietary-blue?style=flat-square)

### Unit Economics

* [Paid](https://paid.ai/) - Monetization platform for AI agents that sets pricing, tracks delivery cost per action, and reports margin per customer. ![co](https://img.shields.io/badge/co-555?style=flat-square)

## Understand

### Buyer Incentives

* [Claude Subscription Arbitrage](https://zed.dev/blog/anthropic-subscription-changes) - Zed blog post on routing agentic workloads through Pro and Max plans and Anthropic's changes to subscription terms.
* [Cursor Spend Controls Changelog](https://cursor.com/changelog/05-04-26) - Cursor changelog entry for admin spend controls: budget caps, credit metering, and usage dashboards.
* [GitHub Copilot Billing Backlash](https://news.ycombinator.com/item?id=47923357) - Discussion thread on reaction to GitHub's move from flat-rate Copilot plans to metered AI Credits.
* [Lanai](https://www.prnewswire.com/news-releases/lanai-launches-ai--work-operating-system-to-help-enterprises-close-the-ai-accountability-gap-302743892.html) - Lanai's AI @ Work platform, which discovers sanctioned and shadow AI workflows across an organization and maps token spend to the KPIs they drive. ![co](https://img.shields.io/badge/co-555?style=flat-square)
* [State of FinOps](https://data.finops.org/) - FinOps Foundation annual survey of how organizations manage cloud and AI spend. ![report](https://img.shields.io/badge/report-555?style=flat-square)
* [The $47k Claude Code Bill](https://yusufhansacak.medium.com/the-47-000-agent-bill-what-the-viral-token-stories-get-wrong-7ee1cdd81e65) - Teardown of a viral Claude Code bill story that traces the cost to quadratic context re-ingestion.
* [Uber AI Coding Spend Cap](https://techcrunch.com/2026/06/02/uber-caps-employee-ai-spending-after-blowing-through-budget-in-four-months/) - TechCrunch report on Uber capping per-employee AI-coding spend per tool.

### Compression Efficacy

* [JetBrains Token-Saving Skills Test](https://blog.jetbrains.com/ai/2026/07/rtk-claude-code-token-savings/) - JetBrains blog post that A/B-tests two token-saving skills against their own claims. ![bench](https://img.shields.io/badge/bench-555?style=flat-square)

### Consolidation

* [Cisco Acquires Galileo](https://blogs.cisco.com/news/cisco-announces-the-intent-to-acquire-galileo) - Cisco announcement of its intent to acquire Galileo, an LLM and agent evaluation and observability platform. ![co](https://img.shields.io/badge/co-555?style=flat-square)
* [Tokenomics Foundation](https://www.linuxfoundation.org/press/linux-foundation-launches-the-tokenomics-foundation-to-define-the-economics-and-roi-of-ai-value) - Linux Foundation project building open standards for AI token spend. ![co](https://img.shields.io/badge/co-555?style=flat-square)

### Market Competitors

* [OpenHands](https://github.com/OpenHands/OpenHands) ⭐ 90,086 | 🐛 911 | 🌐 TypeScript | 📅 2026-10-06 - MIT-licensed open-source coding-agent platform with a free local mode, a free cloud tier, and an at-cost LLM option. ![tool: MIT](https://img.shields.io/badge/tool-MIT-blue?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/OpenHands/OpenHands?style=flat-square\&label=)
* [Cline](https://github.com/cline/cline) ⭐ 69,924 | 🐛 1,601 | 🌐 TypeScript | 📅 2026-10-06 - Open-source (Apache-2.0) AI coding agent built on a bring-your-own-API-key cost model. ![tool: Apache-2.0](https://img.shields.io/badge/tool-Apache--2.0-blue?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/cline/cline?style=flat-square\&label=)
* [Aider](https://github.com/Aider-AI/aider) ⭐ 49,392 | 🐛 1,910 | 🌐 Python | 📅 2026-05-22 - Open-source (Apache-2.0) terminal coding agent with per-message dollar-cost tracking and a public polyglot leaderboard. ![tool: Apache-2.0](https://img.shields.io/badge/tool-Apache--2.0-blue?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/Aider-AI/aider?style=flat-square\&label=)
* [Amp](https://ampcode.com/) - Coding agent spun out of Sourcegraph, with monthly tiers and credits billed at provider API prices. ![tool](https://img.shields.io/badge/tool-blue?style=flat-square)
* [Factory](https://factory.com/pricing) - Pricing page for Factory's Droids coding agents, sold as subscription tiers with usage-based rate limits. ![co](https://img.shields.io/badge/co-555?style=flat-square)
* [Gemini CLI Retirement](https://developers.googleblog.com/an-important-update-transitioning-gemini-cli-to-antigravity-cli/) - Google Developers Blog post on transitioning from the open-source Gemini CLI to Antigravity CLI. ![tool](https://img.shields.io/badge/tool-blue?style=flat-square)

### Market Sizing

* [MMC Ventures AI Tokenomics](https://mmc.vc/research/ai-tokenomics-how-to-tokenmin-while-roimaxxing/) - MMC Ventures research mapping the token-efficiency vendor landscape across context and memory, multi-model systems, inference, routing, and output. ![report](https://img.shields.io/badge/report-555?style=flat-square)
* [Gartner AI Spending Forecast](https://www.gartner.com/en/newsroom/press-releases/2026-09-16-gartner-forecasts-worldwide-ai-spending-to-grow-49-point-5-percent-in-2026) - Gartner press release forecasting worldwide AI spending. ![report](https://img.shields.io/badge/report-555?style=flat-square)
* [Menlo Ventures State of Generative AI in the Enterprise](https://menlovc.com/perspective/2025-the-state-of-generative-ai-in-the-enterprise/) - Menlo Ventures report on enterprise generative-AI spend, including coding tools as an application category. ![report](https://img.shields.io/badge/report-555?style=flat-square)

### Model Economics

* [Artificial Analysis Coding Agent Index](https://artificialanalysis.ai/agents/coding-agents) - Benchmark that scores full model-plus-harness coding-agent stacks on quality and cost per task. ![bench](https://img.shields.io/badge/bench-555?style=flat-square)
* [Artificial Analysis Intelligence Index](https://artificialanalysis.ai/leaderboards/models) - Artificial Analysis leaderboard of base LLMs with a capability index, price, and cost-per-task. ![bench](https://img.shields.io/badge/bench-555?style=flat-square)
* [Claude API Release Notes](https://platform.claude.com/docs/en/release-notes/api) - Anthropic's Claude API release notes, listing model launches and API changes.
* [Gemini Flash Models](https://blog.google/innovation-and-ai/models-and-research/gemini-models/gemini-3-6-flash-3-5-flash-lite-3-5-flash-cyber/) - Google blog post introducing Gemini Flash models and their token-efficiency claims.
* [Kimi API Pricing](https://platform.kimi.ai/docs/pricing/chat-k27-code) - Moonshot's official API pricing page for Kimi models.
* [Qwen3.6-27B](https://huggingface.co/Qwen/Qwen3.6-27B) - Hugging Face model card for Qwen3.6-27B, an open-weight coding model.
* [OckBench](https://arxiv.org/abs/2511.05722) - Benchmark that measures token efficiency and verbosity of LLM reasoning for the same answer. ![paper](https://img.shields.io/badge/paper-555?style=flat-square)
* [OpenAI Reasoning Guide](https://developers.openai.com/api/docs/guides/reasoning) - OpenAI guide to reasoning models and how reasoning tokens are billed as output.
* [Reasoning-Token Consumption](https://arxiv.org/abs/2602.13517) - Paper on how chain-of-thought token use differs from effort, and why verbosity is a separate lever. ![paper](https://img.shields.io/badge/paper-555?style=flat-square)

### Pricing Models

* [AICostBudget AI API Pricing Dataset](https://aicostbudget.com/en/datasets/ai-api-pricing) - Source-linked AI API pricing records with normalized JSON and CSV exports. ![data](https://img.shields.io/badge/data-555?style=flat-square)
* [Anthropic Batch Processing](https://platform.claude.com/docs/en/docs/build-with-claude/batch-processing) - Anthropic documentation on asynchronous batch processing, which trades latency for a lower price.
* [Bessemer AI Pricing Playbook](https://www.bvp.com/atlas/the-ai-pricing-and-monetization-playbook) - Bessemer playbook on the shift in AI pricing from per-seat to usage and outcome-based models.
* [Anthropic Prompt Caching](https://platform.claude.com/docs/en/build-with-claude/prompt-caching) - Anthropic documentation on prompt caching, including cache-read and cache-write pricing.
* [ChatGPT Pricing](https://learn.chatgpt.com/docs/pricing) - OpenAI pricing page for ChatGPT subscription tiers and Codex bundling.
* [ChatGPT Credit Rate Card](https://help.openai.com/en/articles/11481834-chatgpt-rate-card-business-enterpriseedu-credit-based-pricing) - OpenAI help article with the credit-based rate card for ChatGPT Business, Enterprise, and Edu workspaces.
* [Claude Fable 5.1 and Mythos 5.1](https://www.anthropic.com/claude-fable-and-mythos-5-1) - Anthropic announcement with the rate card for Claude Fable 5.1 and Mythos 5.1.
* [Claude Opus 5.5 Overview](https://platform.claude.com/docs/en/models/opus-5-5/overview) - Anthropic documentation for Claude Opus 5.5, including pricing, cache rates, and default effort.
* [Claude Sonnet 5.5 Overview](https://platform.claude.com/docs/en/models/sonnet-5-5/overview) - Anthropic documentation for Claude Sonnet 5.5, including pricing and effort levels.
* [Claude Tokenizer Vocabulary](https://tokencontributions.substack.com/p/on-the-biology-of-claudes-tokenizer) - Substack analysis of how a smaller Claude tokenizer vocabulary changed token counts for plain English text.
* [Cursor Pricing](https://cursor.com/docs/account/pricing) - Cursor documentation on token-based metering, split into first-party and third-party pools.
* [DeepSeek API Pricing](https://api-docs.deepseek.com/quick_start/pricing) - DeepSeek's official pricing page listing per-token rates for its models, including cache hits and peak-window rates.
* [Devin Agent Compute Units](https://docs.devin.ai/admin/billing/enterprise) - Devin documentation on Enterprise billing in Agent Compute Units.
* [Doubleword](https://doubleword.ai) - Provider of asynchronous and batch inference on open models that publishes a cost-per-token table. ![co](https://img.shields.io/badge/co-555?style=flat-square)
* [Fable 5 Subscription Changes](https://www.anthropic.com/news/redeploying-fable-5) - Anthropic announcement on how Fable 5 is offered across subscription plans and usage credits.
* [Gemini API Pricing](https://ai.google.dev/gemini-api/docs/pricing#gemini-3.8-flash) - Google's Gemini API pricing page with per-token rates and dated rate changes for Flash models.
* [Google AI Subscriptions](https://gemini.google/us/subscriptions/) - Google page listing Google AI subscription tiers and their Gemini and Antigravity rate limits.
* [GPT-5.6 API Pricing](https://developers.openai.com/api/docs/pricing) - OpenAI API pricing page for the GPT-5.6 family.
* [GPT-6 Astra API Pricing](https://developers.openai.com/api/docs/models/gpt-6-astra) - OpenAI model page for GPT-6 Astra, with per-token rates and the long-context surcharge.
* [GPT-6 Sol and Luna API Pricing](https://developers.openai.com/api/docs/models/gpt-6-sol) - OpenAI model page for GPT-6 Sol and GPT-6 Luna, with per-token rates and the long-context surcharge.
* [LiteLLM Custom Pricing](https://docs.litellm.ai/docs/proxy/custom_pricing) - LiteLLM documentation on custom pricing, including flex and priority service-tier cost keys.
* [LLMflation](https://a16z.com/llmflation-llm-inference-cost/) - Andreessen Horowitz analysis of falling LLM inference prices alongside rising total AI spend.
* [Anthropic API Pricing](https://platform.claude.com/docs/en/about-claude/pricing) - Anthropic pricing documentation covering how tokens are metered and priced on the Claude API.
* [OpenAI Agents API Observability](https://developers.openai.com/api/docs/guides/agents-api/observability) - OpenAI documentation on usage and billing for hosted agent runs in the Agents API. ![tool: proprietary](https://img.shields.io/badge/tool-proprietary-blue?style=flat-square)
* [OpenAI Deprecations](https://developers.openai.com/api/docs/deprecations) - Page listing deprecated OpenAI APIs and models, including the wind-down of self-serve fine-tuning.
* [Tokenization Multiplicity and Overcharging](https://arxiv.org/abs/2506.06446) - Paper on how the same output can be billed a different token count depending on tokenization. ![paper](https://img.shields.io/badge/paper-555?style=flat-square)
* [Tokenomics Foundation Prompt Cache Explainer](https://www.tokeneconomics.com/cache-explainer/) - Explainer on prompt caching that defines Cache Hit Rate and Cache Cost Efficiency and maps cache economics across access modes. ![tool: CC BY 4.0](https://img.shields.io/badge/tool-CC_BY_4.0-blue?style=flat-square)
* [Devin Desktop Quota](https://docs.devin.ai/desktop/accounts/quota) - Devin documentation on token-based quota for Devin Desktop, formerly Windsurf.

### Reliability SLAs

* [Azure PTU and AWS Bedrock Reserved Capacity](https://learn.microsoft.com/en-us/azure/ai-foundry/openai/concepts/provisioned-throughput) - Microsoft documentation on Azure Provisioned Throughput Units, which reserve capacity billed hourly whether or not it is used.

### Unit Economics

* [Big-T Notation](https://www.tokeneconomics.com/projects/big-t-notation/) - Tokenomics Foundation vocabulary that classifies workloads by how token consumption grows with requests, calls per request, and agent depth. ![tool: CC BY 4.0](https://img.shields.io/badge/tool-CC_BY_4.0-blue?style=flat-square)
* [Cloud Capital Gross Margin in the Age of AI](https://www.cloudcapital.co/learn/gross-margin-in-the-age-of-ai) - Cloud Capital article on how inference and compute costs affect gross margin for AI-native software.
* [Cost-of-Pass](https://arxiv.org/abs/2504.13359) - Paper defining the expected dollar cost of one correct answer as inference cost divided by success rate. ![paper](https://img.shields.io/badge/paper-555?style=flat-square)
* [DORA AI Insights](https://dora.dev/insights/balancing-ai-tensions/) - DORA article on how AI adoption affects delivery throughput and stability. ![report](https://img.shields.io/badge/report-555?style=flat-square)
* [Faros AI Engineering Report](https://pages.faros.ai/hubfs/AI_Engineering_Report_2026_The_Acceleration_Whiplash_Faros.pdf) - Faros report on developer telemetry and the effect of AI on engineering velocity. ![report](https://img.shields.io/badge/report-555?style=flat-square)
* [getDX AI Coding Assistant Pricing](https://getdx.com/blog/ai-coding-assistant-pricing/) - Guide from getDX to AI coding assistant pricing and return on investment.
* [METR AI Productivity Study](https://metr.org/blog/2025-07-10-early-2025-ai-experienced-os-dev-study/) - METR randomized controlled trial of AI tool use by experienced open-source developers. ![paper](https://img.shields.io/badge/paper-555?style=flat-square)

## Measure

### Benchmarks Evals

* [promptfoo](https://github.com/promptfoo/promptfoo) ⭐ 25,739 | 🐛 712 | 🌐 TypeScript | 📅 2026-10-06 - Open-source CLI and CI harness for testing LLM prompts and agents that records per-eval token usage and cost. ![tool: MIT](https://img.shields.io/badge/tool-MIT-blue?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/promptfoo/promptfoo?style=flat-square\&label=)
* [SWE-bench](https://github.com/SWE-bench/SWE-bench) ⭐ 5,980 | 🐛 27 | 🌐 Python | 📅 2026-09-18 - Software-engineering benchmark of real GitHub issue tasks from Python repositories, published at ICLR 2024. ![bench](https://img.shields.io/badge/bench-555?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/SWE-bench/SWE-bench?style=flat-square\&label=)
* [LongMemEval](https://github.com/xiaowu0162/LongMemEval) ⭐ 1,131 | 🐛 46 | 🌐 Python | 📅 2026-05-11 - Benchmark for long-term memory in chat assistants, published at ICLR 2025. ![bench](https://img.shields.io/badge/bench-555?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/xiaowu0162/LongMemEval?style=flat-square\&label=)
* [MemoryBench](https://github.com/supermemoryai/memorybench) ⭐ 321 | 🐛 39 | 🌐 TypeScript | 📅 2026-10-02 - Pluggable harness that runs memory systems head-to-head across datasets like LoCoMo. ![bench](https://img.shields.io/badge/bench-555?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/supermemoryai/memorybench?style=flat-square\&label=)
* [RouterArena](https://github.com/RouteWorks/RouterArena) ⭐ 144 | 🐛 28 | 🌐 Python | 📅 2026-09-29 - Open evaluation platform and leaderboard for LLM routers that select a model per query. ![bench](https://img.shields.io/badge/bench-555?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/RouteWorks/RouterArena?style=flat-square\&label=)
* [Claw-SWE-Bench](https://github.com/TokenRhythm/claw-swe-bench) ⭐ 110 | 🐛 2 | 🌐 Python | 📅 2026-09-28 - Benchmark showing how adapter and harness design change an agent's score on the same model backbone. ![bench](https://img.shields.io/badge/bench-555?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/TokenRhythm/claw-swe-bench?style=flat-square\&label=)
* [Coding Benchmarks Are Misaligned with Agentic SE](https://arxiv.org/abs/2606.17799) - Position paper from Tessl arguing that current coding benchmarks do not measure what people assume. ![paper](https://img.shields.io/badge/paper-555?style=flat-square)
* [Deterministic Anchoring](https://arxiv.org/abs/2606.26979) - ISSTA 2026 paper on injecting static-analysis facts as plain-text comments for code agents. ![paper](https://img.shields.io/badge/paper-555?style=flat-square)
* [GitHub Copilot Agentic Harness Evaluation](https://github.blog/ai-and-ml/github-copilot/evaluating-performance-and-efficiency-of-the-github-copilot-agentic-harness-across-models-and-tasks/) - GitHub blog post comparing Copilot's agentic-harness resolution rate with cost per task across benchmarks and models. ![report](https://img.shields.io/badge/report-555?style=flat-square)
* [Harness-Bench](https://arxiv.org/abs/2605.27922) - Benchmark that holds task, model, and budget fixed while varying only the agent harness. ![paper](https://img.shields.io/badge/paper-555?style=flat-square)
* [Prompt Compression in the Wild](https://arxiv.org/abs/2604.02985) - ECIR 2026 study of end-to-end speed-ups from LLMLingua prompt compression. ![paper](https://img.shields.io/badge/paper-555?style=flat-square)
* [RedundancyBench](https://arxiv.org/abs/2605.29893) - Benchmark for step-level redundancy detection in agent trajectories. ![paper](https://img.shields.io/badge/paper-555?style=flat-square)
* [SWE-Effi](https://arxiv.org/abs/2509.09853) - Paper that re-ranks SWE-agents on a SWE-bench subset by cost under resource constraints. ![paper](https://img.shields.io/badge/paper-555?style=flat-square)
* [Terminal-Bench](https://www.tbench.ai/) - Benchmark for AI agents in real terminal and CLI environments, with a public leaderboard. ![bench](https://img.shields.io/badge/bench-555?style=flat-square)

### Cache Accounting

* [Gemini Context Caching Pricing](https://ai.google.dev/gemini-api/docs/pricing) - Google's Gemini API pricing page, including the per-hour storage charge for explicit context caching.
* [OpenAI Prompt Caching](https://platform.openai.com/docs/guides/prompt-caching) - OpenAI guide to prompt caching and the cached\_tokens usage field.
* [OpenAI Conversation State](https://developers.openai.com/api/docs/guides/conversation-state) - OpenAI guide to conversation state in the Responses API, including billing semantics and server-side compaction.
* [Open-SWE-Traces Cache Simulation](https://www.completeskeptic.com/p/kv-cache-rules-everything-around) - Replay simulation over NVIDIA's Open-SWE-Traces that splits an agentic bill into output tokens and cache traffic.

### Cost Anatomy

* [Anthropic Pricing Line Items](https://platform.claude.com/docs/en/about-claude/pricing#code-execution-tool) - Anthropic pricing documentation that enumerates the meters on a Claude API bill.
* [TensorZero Token-Count Divergence](https://www.tensorzero.com/blog/stop-comparing-price-per-million-tokens-the-hidden-llm-api-costs/) - TensorZero blog post on how the same input produces different token counts across vendor tokenizers.
* [Claude Vision Token Pricing](https://platform.claude.com/docs/en/build-with-claude/vision) - Anthropic vision documentation on how images convert to billed tokens, with OpenAI and Google equivalents.

### Energy Carbon

* [CodeCarbon](https://github.com/mlco2/codecarbon) ⭐ 1,926 | 🐛 194 | 🌐 Python | 📅 2026-10-05 - Open-source (MIT) library for estimating a workload's energy use and CO2e emissions. ![tool: MIT](https://img.shields.io/badge/tool-MIT-blue?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/mlco2/codecarbon?style=flat-square\&label=)
* [EcoLogits](https://github.com/mlco2/ecologits) ⭐ 344 | 🐛 16 | 🌐 Python | 📅 2026-09-29 - Library that estimates the energy and carbon footprint of calling generative-AI APIs, as a hosted counterpart to CodeCarbon. ![tool: MPL-2.0](https://img.shields.io/badge/tool-MPL--2.0-blue?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/mlco2/ecologits?style=flat-square\&label=)
* [claude-carbon](https://github.com/gwittebolle/claude-carbon) ⭐ 206 | 🐛 0 | 🌐 Shell | 📅 2026-10-05 - MIT-licensed Claude Code plugin that estimates each session's CO2 locally from token counts and shows it in the status line. ![tool: MIT](https://img.shields.io/badge/tool-MIT-blue?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/gwittebolle/claude-carbon?style=flat-square\&label=)
* [Alumet](https://github.com/alumet-dev/alumet) ⭐ 83 | 🐛 47 | 🌐 Rust | 📅 2026-10-05 - Rust measurement framework (EUPL-1.2 or later) that reads hardware energy counters and attributes energy to processes, cgroups, and Kubernetes pods. ![tool: EUPL-1.2-or-later](https://img.shields.io/badge/tool-EUPL--1.2--or--later-blue?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/alumet-dev/alumet?style=flat-square\&label=)
* [Epoch AI Energy per Query](https://epoch.ai/gradient-updates/how-much-energy-does-chatgpt-use) - Epoch AI analysis estimating from first principles how much energy one LLM query uses.
* [Google AI Inference Environmental Impact](https://cloud.google.com/blog/products/infrastructure/measuring-the-environmental-impact-of-ai-inference) - Google disclosure of the energy, carbon, and water footprint of a median Gemini Apps text prompt. ![report](https://img.shields.io/badge/report-555?style=flat-square)
* [ML.ENERGY Leaderboard](https://ml.energy/blog/measurement/energy/diagnosing-inference-energy-consumption-with-the-mlenergy-leaderboard-v30/) - Leaderboard that measures real GPU inference energy across models and tasks. ![bench](https://img.shields.io/badge/bench-555?style=flat-square)

### Harness Overhead

* [System Prompts and Models of AI Tools](https://github.com/x1xhlol/system-prompts-and-models-of-ai-tools) ⭐ 144,049 | 🐛 163 | 📅 2026-08-11 - Collection of extracted agent system prompts and tool-schema JSON files across many vendors, published as raw text. ![data](https://img.shields.io/badge/data-555?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/x1xhlol/system-prompts-and-models-of-ai-tools?style=flat-square\&label=)
* [System Prompts Leaks](https://github.com/asgeirtj/system_prompts_leaks) ⭐ 68,996 | 🐛 56 | 🌐 Python | 📅 2026-10-06 - CC0 corpus of extracted system prompts for AI harnesses and models, with dated Anthropic prompt series. ![data](https://img.shields.io/badge/data-555?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/asgeirtj/system_prompts_leaks?style=flat-square\&label=)
* [Claude Code System Prompts](https://github.com/Piebald-AI/claude-code-system-prompts) ⭐ 12,838 | 🐛 9 | 🌐 JavaScript | 📅 2026-10-05 - Piebald AI extraction of Claude Code's compiled prompt strings and tool descriptions for each release. ![data](https://img.shields.io/badge/data-555?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/Piebald-AI/claude-code-system-prompts?style=flat-square\&label=)
* [Claude Code vs OpenCode Token Overhead](https://systima.ai/blog/claude-code-vs-opencode-token-overhead) - Systima study of harness scaffolding token overhead in Claude Code and OpenCode. ![report](https://img.shields.io/badge/report-555?style=flat-square)
* [FrontierHarness Eval](https://runta.com/blog/introducing-frontierharness-eval/) - Runta benchmark of coding harnesses on one model through one gateway, comparing pass rates and cost per completed task. ![bench](https://img.shields.io/badge/bench-555?style=flat-square)
* [The Harness Tax](https://www.eishanlawrence.com/blog/harness-bench/harness-efficiency-paper.pdf) - Paper that holds model, tasks, and gateway fixed across coding-harness configurations and compares tokens per solved task. ![paper](https://img.shields.io/badge/paper-555?style=flat-square)

### Metering

* [OpenCost Inference Cost Tracking](https://github.com/opencost/opencost/blob/develop/docs/inference-cost-tracking.md) ⭐ 6,766 | 🐛 334 | 🌐 Go | 📅 2026-10-05 - OpenCost documentation on turning GPU and shared-infrastructure spend on vLLM and llm-d deployments into cost per million tokens. ![tool: Apache-2.0](https://img.shields.io/badge/tool-Apache--2.0-blue?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/opencost/opencost?style=flat-square\&label=)
* [AgentsView and caut](https://github.com/kenn-io/agentsview) ⭐ 6,058 | 🐛 137 | 🌐 Go | 📅 2026-10-06 - Open-source tools that read local session logs to aggregate token usage and cost across coding-agent vendors. ![tool: MIT](https://img.shields.io/badge/tool-MIT-blue?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/kenn-io/agentsview?style=flat-square\&label=)
* [tokview](https://github.com/headroomlabs-ai/tokview) ⭐ 78 | 🐛 2 | 🌐 Python | 📅 2026-09-30 - Local, zero-config proxy that shows a coding agent's token spend by session, model, and tool call. ![tool: MIT](https://img.shields.io/badge/tool-MIT-blue?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/headroomlabs-ai/tokview?style=flat-square\&label=)
* [How Do AI Agents Spend Your Money?](https://arxiv.org/abs/2604.22750) - Stanford study of token spend in agentic coding across frontier models on SWE-bench Verified tasks. ![paper](https://img.shields.io/badge/paper-555?style=flat-square)

### Transcript Analysis

* [token-optimizer (alexgreensh)](https://github.com/alexgreensh/token-optimizer) ⭐ 2,500 | 🐛 0 | 🌐 Python | 📅 2026-10-05 - Coding-agent plugin that runs heuristic waste detectors per session and prices the flagged tokens in dollars. ![tool: PolyForm-Noncommercial-1.0.0](https://img.shields.io/badge/tool-PolyForm--Noncommercial--1.0.0-blue?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/alexgreensh/token-optimizer?style=flat-square\&label=)
* [Failure-Aware Observability for Multi-Agent LLM Systems](https://arxiv.org/abs/2606.01365) - Paper on a live waste-detection framework for multi-agent systems that finds wasted computation early. ![paper](https://img.shields.io/badge/paper-555?style=flat-square)
* [Faros AI Token Intelligence](https://www.faros.ai/blog/token-intelligence-for-ai-engineering) - Faros AI blog post on token intelligence and its Token Attribution Ledger, from an engineering-intelligence SaaS. ![co](https://img.shields.io/badge/co-555?style=flat-square)

### Whole Bill Accounting

* [FOCUS Specification](https://focus.finops.org/focus-specification/) - Linux Foundation billing-data schema specification, with invoice detail and billing period datasets for reconciling spend against invoices. ![tool](https://img.shields.io/badge/tool-blue?style=flat-square)
* [FOCUS 1.5 and AI Cost](https://www.tokeneconomics.com/projects/what-1-5-does-for-ai-cost-and-what-it-does-not/) - Tokenomics Foundation post on the scope of FOCUS release 1.5 for AI cost, including what it leaves out.

## Related lists

* [awesome-mcp-servers](https://github.com/punkpeye/awesome-mcp-servers) ⭐ 95,864 | 🐛 3,012 | 📅 2026-09-27 - A collection of Model Context Protocol servers.
* [Awesome-LLM](https://github.com/Hannibal046/Awesome-LLM) ⭐ 27,440 | 🐛 472 | 📅 2025-07-31 - Curated papers, frameworks, and resources on large language models.
* [awesome-production-machine-learning](https://github.com/EthicalML/awesome-production-machine-learning) ⭐ 20,970 | 🐛 40 | 📅 2026-10-03 - Open-source libraries to deploy, monitor, version, and scale machine learning.
* [Awesome-LLMOps](https://github.com/tensorchord/Awesome-LLMOps) ⭐ 5,953 | 🐛 256 | 🌐 Shell | 📅 2026-10-05 - Tools and platforms for operating LLMs in production.
* [Green Software Landscape](https://landscape.bundesverband-green-software.de/) - Catalog of green-software tools maintained by Bundesverband Green Software e.V., with AI training and inference energy subcategories.

## Footnotes

Maintained by the team at [Quesma](https://quesma.com).

***

> _Enhansomed by [enhansome](https://github.com/enhansome) on 2026-10-06._
