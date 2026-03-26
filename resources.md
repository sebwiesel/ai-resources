# 🤖 AI Resources (Team Knowledge Base)

A curated list of high-signal AI resources across agents, skills, repositories, APIs, and articles.  
Focused on practical usage, fast learning, and staying current in a fast-moving ecosystem.

> Use this page as a starting point for exploring agent patterns, RAG workflows, research tooling, and financial AI use cases.

---

## 🤖 Agents

### AutoGPT
https://github.com/Significant-Gravitas/AutoGPT

One of the earliest widely adopted autonomous agent frameworks. It is useful for understanding core agent-loop patterns such as planning, tool use, task execution, and iterative refinement.

---

## 🧠 Skills / Workflows

### last30days (Claude Skill)
https://github.com/mvanhorn/last30days-skill

A research-oriented skill that analyzes discussions from the past 30 days across sources like Reddit and X. Useful for spotting trends, extracting themes, and generating prompts to stay current in rapidly changing AI domains.

### Claude Research Skill
https://github.com/altmbr/claude-research-skill/blob/main/SKILL.md

A structured research workflow for Claude-style skill systems. Helpful for studying how reusable prompt-and-tool workflows can be packaged for repeatable analysis tasks.

### 500 AI Agents Projects
https://github.com/ashishpatel26/500-AI-Agents-Projects?tab=readme-ov-file#use-case-table

A broad collection of AI agent project ideas and implementations organized by use case. Useful for inspiration, benchmarking patterns, and quickly scanning the current landscape of agent applications.

### Awesome Agent Skills
https://github.com/heilcheng/awesome-agent-skills?utm_source=chatgpt.com

A curated list of agent skills and reusable capabilities. Good for discovering practical building blocks, workflow ideas, and examples of how skills can be structured across agent systems.

---

## 🧰 GitHub Repositories

### Anthropic GitHub
https://github.com/anthropics

Useful for tracking official repositories, examples, and tooling published under Anthropic’s GitHub organization.

### LangChain
https://github.com/langchain-ai/langchain

A popular framework for building LLM-powered applications, including agents, RAG pipelines, and tool integrations. Widely used in production and a strong foundation for many AI-powered systems.

### LlamaIndex
https://github.com/run-llama/llama_index

A framework focused on connecting LLMs with external data sources. Particularly strong for retrieval-augmented generation (RAG), indexing pipelines, and structured data querying workflows.

---

## 🔌 APIs

### Quartr API
https://www.quartr.com/api

Provides structured access to earnings calls, transcripts, and financial data from public companies. Useful for finance-focused AI workflows, research agents, and market intelligence tools.

**Note:** No free tier — access requires a paid plan.

---

## 📚 Articles / Learning

### State of AI Agents (a16z)
https://a16z.com/2024/01/19/ai-agents/

A clear overview of how AI agents work, including common architecture patterns, limitations, and future directions. Good for aligning on terminology and understanding the broader agent ecosystem.

---

# 📊 Earnings Call Transcript API Providers

| Provider | API Access | Free Tier | Data Quality | Coverage | Key Features | Best For |
|----------|------------|-----------|--------------|----------|--------------|----------|
| **Quartr API** | ✅ Yes | ❌ No | ⭐⭐⭐⭐⭐ | ⭐⭐⭐⭐⭐ (13k+ companies) | Real-time transcripts, audio, speaker labels, summaries | Production apps, fintech |
| **FactSet** | ✅ Yes (enterprise APIs / feeds) | ❌ No | ⭐⭐⭐⭐⭐ | ⭐⭐⭐⭐⭐ | Near real-time transcripts, XML, audio, structured metadata | Institutional / quant systems |
| **Bloomberg** | ⚠️ Limited (enterprise only) | ❌ No | ⭐⭐⭐⭐⭐ | ⭐⭐⭐⭐⭐ | Terminal + enterprise feeds, transcripts in document ecosystem | Large firms already using Bloomberg |
| **Financial Modeling Prep (FMP)** | ✅ Yes | ✅ Limited free | ⭐⭐⭐ | ⭐⭐⭐ | Real-time transcripts API, bulk endpoints, affordable pricing | Startups / hobby to semi-production |
| **Alpha Vantage** | ✅ Yes | ✅ Free | ⭐⭐ | ⭐⭐ | Transcript endpoint + sentiment signals | Lightweight apps, experimentation |
| **API Ninjas** | ✅ Yes | ⚠️ Limited free | ⭐⭐⭐ | ⭐⭐⭐ | 8k+ companies, structured transcripts, sentiment, participants | Simple integrations |
| **Yahoo Finance** | ❌ No official API | ✅ Free | ⭐⭐⭐ | ⭐⭐⭐ | Web transcripts for some companies, earnings calendar, news integration | Manual lookup / scraping |
| **Seeking Alpha (unofficial)** | ❌ No official API | ✅ Free (scraping) | ⭐⭐⭐⭐ | ⭐⭐⭐⭐ | High-quality transcripts with speaker attribution | DIY pipelines |
| **Company IR sites** | ❌ No | ✅ Free | ⭐⭐⭐⭐ | ⭐⭐⭐ | Official transcripts in PDF/HTML formats | Custom scraping |

> **Notes**
> - “Free tier” availability and API terms may change over time.
> - “Data Quality” and “Coverage” are directional comparisons, not strict benchmarks.
> - Unofficial or scraping-based options may carry reliability, legal, or maintenance tradeoffs.

---

## 🧪 Experiments / Ideas

_To be expanded._

Suggested additions for this section:
- Internal agent experiments
- RAG prototypes and indexing patterns
- Prompt workflows that worked well
- Evaluation setups and benchmarks
- Lessons learned from production integrations
- https://www.youtube.com/watch?v=foMJtBLh2xM
