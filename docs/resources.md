# External Resources

A curated set of references across agents, skills, repositories, APIs, and finance-oriented data providers.

Use this page as a companion to the core guide when you want examples, implementation patterns, or market references beyond this repository.

## Agents

### AutoGPT
https://github.com/Significant-Gravitas/AutoGPT

One of the earlier agent frameworks to popularize the plan-act-review loop. Useful for understanding autonomous task execution patterns and how agent systems evolved.

## Skills and Workflow Patterns

### last30days (Claude Skill)
https://github.com/mvanhorn/last30days-skill

A research-oriented skill that analyzes recent discussions across sources such as Reddit and X. Useful for trend detection, theme extraction, and fast-moving topic monitoring.

### Claude Research Skill
https://github.com/altmbr/claude-research-skill/blob/main/SKILL.md

An example of a structured research workflow packaged as a reusable skill. Helpful when studying how prompt instructions, constraints, and output structure can be made repeatable.

### 500 AI Agents Projects
https://github.com/ashishpatel26/500-AI-Agents-Projects?tab=readme-ov-file#use-case-table

A broad collection of agent project ideas and implementations organized by use case. Good for inspiration, benchmarking, and scanning the range of current applications.

### Awesome Agent Skills
https://github.com/heilcheng/awesome-agent-skills

A curated list of reusable agent capabilities and skill patterns. Useful for discovering packaging conventions and practical workflow ideas.

## MCPs


## MCPs

### mail-mcp  
https://github.com/dastrobu/mail-mcp

mail-mcp is a local MCP server that connects AI assistants to macOS Mail.app, letting them read, search, and draft emails through a structured interface without needing external credentials.

It uses macOS automation (JXA/AppleScript) to safely bridge AI and Apple Mail, enabling powerful on-device email workflows while keeping data local and user-controlled.


## Core Repositories and Frameworks

### Anthropic on GitHub
https://github.com/anthropics

Useful for tracking official examples, tooling, and protocol-related work published by Anthropic.

### LangChain
https://github.com/langchain-ai/langchain

A widely used framework for building LLM-powered applications, including agent systems, retrieval pipelines, and tool integrations.

### LlamaIndex
https://github.com/run-llama/llama_index

A framework focused on connecting language models to external data sources. Particularly relevant for retrieval-augmented generation and structured data access patterns.

## Financial Data APIs

### Quartr API
https://www.quartr.com/api

Provides structured access to earnings calls, transcripts, and related financial data. Relevant for research workflows, transcript analysis, and market-intelligence use cases.

### EarningsCall API
https://earningscall.biz/api-pricing

Provides API access to earnings calendars, transcripts, audio files, and real-time notifications. Based on the vendor's pricing page, plans differ by rate limit and transcript/audio feature access.

## Earnings Call Transcript Providers

| Provider | API Access | Free Tier | Data Quality | Coverage | Key Features | Best For |
|----------|------------|-----------|--------------|----------|--------------|----------|
| **Quartr API** | ✅ Yes | ❌ No | ⭐⭐⭐⭐⭐ | ⭐⭐⭐⭐⭐ (13k+ companies) | Real-time transcripts, audio, speaker labels, summaries | Production apps, fintech |
| **FactSet** | ✅ Yes (enterprise APIs / feeds) | ❌ No | ⭐⭐⭐⭐⭐ | ⭐⭐⭐⭐⭐ | Near real-time transcripts, XML, audio, structured metadata | Institutional and quant systems |
| **Bloomberg** | ⚠️ Limited (enterprise only) | ❌ No | ⭐⭐⭐⭐⭐ | ⭐⭐⭐⭐⭐ | Terminal and enterprise feeds, transcripts in document ecosystem | Large firms already using Bloomberg |
| **Financial Modeling Prep (FMP)** | ✅ Yes | ✅ Limited free | ⭐⭐⭐ | ⭐⭐⭐ | Real-time transcripts API, bulk endpoints, affordable pricing | Startups and small production teams |
| **Alpha Vantage** | ✅ Yes | ✅ Free | ⭐⭐ | ⭐⭐ | Transcript endpoint plus sentiment signals | Lightweight apps and experimentation |
| **API Ninjas** | ✅ Yes | ⚠️ Limited free | ⭐⭐⭐ | ⭐⭐⭐ | Structured transcripts, participants, sentiment | Simple integrations |
| **EarningsCall.biz** | ✅ Yes | ❌ No public free tier listed | ⭐⭐⭐ | ⭐⭐⭐⭐ | Event calendar, basic and enhanced transcripts, audio files, real-time notifications | Cost-conscious transcript workflows and prototyping |
| **Yahoo Finance** | ❌ No official API | ✅ Free | ⭐⭐⭐ | ⭐⭐⭐ | Web transcripts for some companies, earnings calendar, news integration | Manual lookup and scraping |
| **Seeking Alpha (unofficial)** | ❌ No official API | ✅ Free (scraping) | ⭐⭐⭐⭐ | ⭐⭐⭐⭐ | High-quality transcripts with speaker attribution | DIY pipelines |
| **Company IR sites** | ❌ No | ✅ Free | ⭐⭐⭐⭐ | ⭐⭐⭐ | Official transcripts in PDF and HTML formats | Custom scraping |

Notes:

- Free-tier availability, pricing, and API terms may change over time.
- Data-quality and coverage ratings are directional comparisons, not formal benchmarks.
- Unofficial or scraping-based options may introduce reliability, legal, or maintenance tradeoffs.

## Articles and Learning

### State of AI Agents (a16z)
https://a16z.com/2024/01/19/ai-agents/

A clear overview of common agent architectures, constraints, and where the ecosystem is heading. Useful for establishing shared terminology.

## Experiment Backlog

Suggested additions for this section:

- Internal agent experiments
- Retrieval and indexing prototypes
- Prompt workflows that performed well in practice
- Evaluation setups and benchmark notes
- Lessons learned from production integrations


