Here’s a cleaner, more structured version with improved hierarchy, tighter descriptions, and consistent formatting:

---

# External Resources

A curated collection of references spanning **agents, workflows, frameworks, APIs, and financial data providers**.

Use this page alongside the core guide when you need:

* Real-world implementations
* Reusable patterns
* Market data sources
* Ecosystem context

---

## Agents

### AutoGPT

[https://github.com/Significant-Gravitas/AutoGPT](https://github.com/Significant-Gravitas/AutoGPT)

One of the earliest agent frameworks to popularize the **plan → act → review loop**.
Useful for understanding how autonomous agent systems evolved and how iterative execution works in practice.

---

## Skills & Workflow Patterns

### last30days (Claude Skill)

[https://github.com/mvanhorn/last30days-skill](https://github.com/mvanhorn/last30days-skill)

A research-oriented skill that analyzes recent discussions across platforms like Reddit and X.
Best for:

* Trend detection
* Theme extraction
* Monitoring fast-moving topics

---

### Claude Research Skill

[https://github.com/altmbr/claude-research-skill/blob/main/SKILL.md](https://github.com/altmbr/claude-research-skill/blob/main/SKILL.md)

A structured research workflow packaged as a reusable skill.
Highlights how prompts, constraints, and outputs can be standardized and reused.

---

### 500 AI Agents Projects

[https://github.com/ashishpatel26/500-AI-Agents-Projects](https://github.com/ashishpatel26/500-AI-Agents-Projects)

A large collection of agent use cases and implementations.
Useful for:

* Inspiration
* Benchmarking ideas
* Exploring real-world applications

---

### Awesome Agent Skills

[https://github.com/heilcheng/awesome-agent-skills](https://github.com/heilcheng/awesome-agent-skills)

A curated list of reusable agent capabilities and patterns.
Helpful for discovering:

* Skill packaging conventions
* Practical workflow building blocks

---

## MCP (Model Context Protocol)

### mail-mcp

[https://github.com/dastrobu/mail-mcp](https://github.com/dastrobu/mail-mcp)

A local MCP server that connects AI assistants to **macOS Mail.app**, enabling:

* Reading and searching emails
* Drafting responses
* Fully local, privacy-preserving workflows

Uses macOS automation (JXA/AppleScript) to bridge AI and Mail safely.

---

### Quick Setup (Homebrew)

```bash
# Install
brew tap dastrobu/tap
brew install mail-mcp

# Start service (required)
brew services start mail-mcp
```

### Setup Steps

1. Open **Mail.app**
2. Connect your MCP client to:
   `http://localhost:8787`
3. Trigger any mail action → approve the Automation prompt

### Accessibility Permissions

* Go to: **System Settings → Privacy & Security → Accessibility**
* Add:

  * `/opt/homebrew/bin/mail-mcp` (Apple Silicon)
  * `/usr/local/bin/mail-mcp` (Intel)
* Enable access

---

## Core Frameworks & Repositories

### Anthropic (GitHub)

[https://github.com/anthropics](https://github.com/anthropics)

Official examples, tooling, and protocol-related work from Anthropic.

---

### LangChain

[https://github.com/langchain-ai/langchain](https://github.com/langchain-ai/langchain)

A widely used framework for building LLM-powered systems, including:

* Agents
* Retrieval pipelines
* Tool integrations

---

### LlamaIndex

[https://github.com/run-llama/llama_index](https://github.com/run-llama/llama_index)

Focused on connecting LLMs to external data sources.
Key use cases:

* Retrieval-augmented generation (RAG)
* Structured data access
* Indexing pipelines

---

## Financial Data APIs

### Quartr API

[https://www.quartr.com/api](https://www.quartr.com/api)

Provides structured access to:

* Earnings calls
* Transcripts
* Audio

Best suited for **production-grade financial research workflows**.

---

### EarningsCall API

[https://earningscall.biz/api-pricing](https://earningscall.biz/api-pricing)

Offers:

* Earnings calendars
* Transcripts
* Audio files
* Real-time notifications

Plans vary by rate limits and feature access.

---

## Earnings Call Transcript Providers

| Provider             | API            | Free Tier | Quality | Coverage | Key Strength                | Best For              |
| -------------------- | -------------- | --------- | ------- | -------- | --------------------------- | --------------------- |
| **Quartr API**       | ✅              | ❌         | ⭐⭐⭐⭐⭐   | ⭐⭐⭐⭐⭐    | Real-time + structured data | Production fintech    |
| **FactSet**          | ✅ (Enterprise) | ❌         | ⭐⭐⭐⭐⭐   | ⭐⭐⭐⭐⭐    | Institutional-grade data    | Quant systems         |
| **Bloomberg**        | ⚠️ Limited     | ❌         | ⭐⭐⭐⭐⭐   | ⭐⭐⭐⭐⭐    | Terminal ecosystem          | Large firms           |
| **FMP**              | ✅              | ✅         | ⭐⭐⭐     | ⭐⭐⭐      | Affordable + simple APIs    | Startups              |
| **Alpha Vantage**    | ✅              | ✅         | ⭐⭐      | ⭐⭐       | Sentiment + transcripts     | Lightweight apps      |
| **API Ninjas**       | ✅              | ⚠️        | ⭐⭐⭐     | ⭐⭐⭐      | Easy integration            | Prototypes            |
| **EarningsCall.biz** | ✅              | ❌         | ⭐⭐⭐     | ⭐⭐⭐⭐     | Notifications + audio       | Cost-conscious builds |
| **Yahoo Finance**    | ❌              | ✅         | ⭐⭐⭐     | ⭐⭐⭐      | Free + accessible           | Manual workflows      |
| **Seeking Alpha**    | ❌              | ✅         | ⭐⭐⭐⭐    | ⭐⭐⭐⭐     | High-quality transcripts    | DIY pipelines         |
| **Company IR Sites** | ❌              | ✅         | ⭐⭐⭐⭐    | ⭐⭐⭐      | Official filings            | Custom scraping       |

### Notes

* Pricing and availability may change
* Ratings are directional, not benchmarked
* Scraping-based solutions introduce:

  * Reliability risks
  * Legal considerations
  * Maintenance overhead

---

## Articles & Learning

### State of AI Agents (a16z)

[https://a16z.com/2024/01/19/ai-agents/](https://a16z.com/2024/01/19/ai-agents/)

A strong overview of:

* Agent architectures
* Design constraints
* Ecosystem trends

Useful for building shared mental models.

---

## Experiment Backlog

Suggested additions:

* Internal agent experiments
* Retrieval and indexing prototypes
* High-performing prompt workflows
* Evaluation setups and benchmarks
* Production lessons learned

---

https://github.com/NeuroDong/Ai-Review/blob/main/ai-review-skills/SKILL.md
https://github.com/BevalZ/awesome-prompt-for-academic?tab=readme-ov-file#-categories-overview


* Turn this into a **Notion-ready version**
* Add **“when to use what” decision guidance**
* Or convert it into a **visual architecture map**
