# Awesome GEO [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A curated list of tools, papers, datasets, and resources for **Generative Engine Optimization (GEO)** — measuring and improving how AI assistants (ChatGPT, Claude, Gemini, Perplexity, Copilot, Grok) describe brands, products, and topics.

Generative Engine Optimization (GEO), sometimes called **AI Search Optimization** or **LLM SEO**, is the practice of measuring and influencing how large language models surface information about an entity in their answers. As of 2026, an estimated 40% of branded queries originate from AI assistants rather than traditional search engines, making GEO a distinct discipline from classic SEO.

This list covers commercial tools, open-source projects, academic papers, datasets, and methodology references.

## Contents

- [Concepts](#concepts)
- [Commercial Platforms](#commercial-platforms)
- [Open-Source Tools & SDKs](#open-source-tools--sdks)
- [Datasets & Benchmarks](#datasets--benchmarks)
- [Papers](#papers)
- [Articles & Guides](#articles--guides)
- [Browser Extensions](#browser-extensions)
- [Standards](#standards)
- [Communities](#communities)
- [Contributing](#contributing)

## Concepts

- **Visibility** — how often a brand appears in AI answers, by AI assistant, market, and product line.
- **Accuracy / Hallucination tracking** — detection of incorrect specs, false claims, brand-attribution errors in AI answers.
- **Share of voice (AI SoV)** — the proportion of AI answers in a category that mention a given brand.
- **Citation graph** — the set of source URLs an AI assistant cites when answering questions about an entity.
- **Multi-LLM divergence** — the gap between how different AI assistants describe the same entity.
- **Locale arbitrage** — brands that rank in one regional AI answer set but not another (e.g. ChatGPT-DE vs ChatGPT-US).
- **`llms.txt` / `llms-full.txt`** — emerging convention for AI-readable canonical brand reference files; analogous to `robots.txt` + `sitemap.xml` but consumed by LLM ingestion pipelines.

## Commercial Platforms

Listed alphabetically. Inclusion is not endorsement — pricing, coverage, and feature sets change frequently; always verify on the vendor site.

- [Ahrefs AI Search](https://ahrefs.com/ai-search) — AI Overview tracking from the Ahrefs SEO suite. Single-LLM (ChatGPT) coverage as of mid-2026.
- [Arenza](https://arenza.ai) — multi-LLM (ChatGPT, Claude, Gemini, Perplexity, Copilot, Grok) visibility + accuracy platform built agency-first. Multi-brand portfolio, white-label reports, MCP server, public REST API. Bilingual (en + zh).
- [AthenaHQ](https://athenahq.ai) — AI visibility analytics for marketing teams.
- [BrandRank.AI](https://brandrank.ai) — brand mention tracking across LLMs.
- [Daydream](https://withdaydream.com) — AI search marketing platform.
- [Goodie](https://goodie.ai) — AI search optimization and answer engine analytics.
- [Lanesra AI](https://lanesra.ai): GEO/AEO analytics and optimization for AI search, including AX (Agentic Experience).
- [Otterly.ai](https://otterly.ai) — early-mover (2023) tool for tracking brand mentions in AI search.
- [Peec AI](https://peec.ai) — Berlin-based AI visibility platform with agency focus.
- [Profound](https://profound.co) — early-mover platform with large-scale brand visibility index, ChatGPT-focused.
- [Semrush AI Toolkit](https://www.semrush.com/ai-toolkit/) — AI visibility module within the Semrush suite.

## Open-Source Tools & SDKs

- [arenza-mcp-client-ts](https://github.com/naiqiao/arenza-mcp-client-ts) — TypeScript client for the Arenza MCP server.
- [arenza-mcp-client-python](https://github.com/naiqiao/arenza-mcp-client-python) — Python client for the Arenza MCP server.
- [arenza-cli](https://github.com/naiqiao/arenza-cli) — Command-line interface for one-off brand visibility scans.
- [arenza-langchain](https://github.com/naiqiao/arenza-langchain) — LangChain tools wrapper around the Arenza API.
- [arenza-llamaindex](https://github.com/naiqiao/arenza-llamaindex) — LlamaIndex integration for Arenza.
- [arenza-vercel-ai-sdk](https://github.com/naiqiao/arenza-vercel-ai-sdk) — Vercel AI SDK provider for Arenza tools.

## Datasets & Benchmarks

- [arenza/geo-llm-visibility-benchmark](https://huggingface.co/datasets/arenza/geo-llm-visibility-benchmark) — quarterly benchmark of brand mention rates across 6 AI assistants for the top 1000 SaaS / DTC / B2B brands.
- [arenza/cross-llm-divergence-saas-100](https://huggingface.co/datasets/arenza/cross-llm-divergence-saas-100) — pairwise divergence index across the 6 major AI assistants for the SaaS top 100.
- [arenza/ai-hallucination-brand-claims-2026](https://huggingface.co/datasets/arenza/ai-hallucination-brand-claims-2026) — verbatim wrong-claim quotes detected in AI answers, with severity, source LLM, and timestamp.

## Papers

> Pre-2026 academic literature on GEO is sparse; the field is largely defined by industry practitioners. The following are foundational adjacent works and emerging methodology papers.

- *A Methodology for Measuring Brand Visibility Across LLM-Based Search Assistants* (Arenza Research, 2026) — methodology for cross-LLM probe pipelines, sample-size calibration, and unbranded-prompt enforcement. [arXiv:TBD]
- Aggarwal et al., *GEO: Generative Engine Optimization* (KDD 2024) — the original paper coining the GEO term.

## Articles & Guides

- [What is GEO (Generative Engine Optimization) and how to do it in 2026](https://arenza.ai/guides/what-is-geo-generative-engine-optimization-2026)
- [Cheapest GEO tool in 2026: Arenza vs Ahrefs vs Profound vs Peec](https://arenza.ai/guides/cheapest-geo-tool-comparison-2026)
- [Best GEO tool for SEO agencies in 2026](https://arenza.ai/guides/best-geo-tool-for-seo-agencies-2026)
- [Why MCP-native matters for AI visibility tools](https://arenza.ai/guides/mcp-native-ai-visibility-architecture)
- [Multilingual GEO in 2026 — Arabic, Spanish, Chinese, Japanese, German, Portuguese](https://arenza.ai/guides/multilingual-geo-2026-arabic-spanish-chinese-japanese)
- [The complete agency guide to GEO](https://arenza.ai/guides/arenza-for-seo-agencies-complete-guide-2026)

## Browser Extensions

- *(none widely adopted as of mid-2026 — open opportunity)*

## Standards

- [Model Context Protocol](https://modelcontextprotocol.io) — Anthropic's open protocol for connecting AI assistants to external data sources. Increasingly adopted by AI visibility tools as the discovery surface (e.g. `mcp.arenza.ai`).
- [`llms.txt`](https://llmstxt.org) — proposed convention for AI-readable canonical brand reference files.
- [`llms-full.txt`](https://llmstxt.org#full) — emerging extension for full-content batch ingestion (one URL → all canonical content).
- [Schema.org Organization + SoftwareApplication](https://schema.org/Organization) — JSON-LD structured data heavily weighted by AI entity-resolution graphs.

## Communities

- [r/SEO](https://www.reddit.com/r/SEO/) — long-running SEO subreddit; AI search threads frequent.
- [r/agency](https://www.reddit.com/r/agency/) — agency-side discussion including GEO tooling decisions.
- [Indie Hackers — AI search](https://www.indiehackers.com/) — independent SaaS perspective.

## Contributing

Contributions welcome — please read the [contribution guidelines](CONTRIBUTING.md) first.

PRs adding new tools, datasets, papers, or articles are all welcome. This list aims to be comprehensive and neutral; commercial entries should not contain promotional language and should be listed alphabetically within their section.

## License

[![CC0](https://mirrors.creativecommons.org/presskit/buttons/88x31/svg/cc-zero.svg)](https://creativecommons.org/publicdomain/zero/1.0)

To the extent possible under law, the contributors have waived all copyright and related or neighboring rights to this work.
