# AI Agents & Workflows: A Practical Guide for Portfolio Managers

**Version 1.0 — March 2026**

---

## How to Read This Document

This guide is structured as a progressive journey. Each section builds on the previous one. By the end, you will understand every layer — from what a simple text file is, to how multiple AI agents can orchestrate complex workflows together.

You do not need to be technical. You just need to be curious.

---

## Part 1: The Building Blocks

### 1.1 What Is a Markdown File?

A Markdown file (`.md`) is a plain text file with simple formatting rules. Think of it as writing a Word document, but instead of clicking buttons for bold or headings, you type small symbols.

**Why does it matter?**

Markdown is the universal language of technical documentation. GitHub, Notion, Confluence, and most AI tools use it. When you write a prompt, structure a document, or read a README on GitHub — you are reading Markdown.

**Quick reference:**

| What you type | What it looks like |
|---|---|
| `# Heading 1` | A large heading |
| `## Heading 2` | A smaller heading |
| `**bold text**` | **bold text** |
| `*italic text*` | *italic text* |
| `- item` | A bullet point |
| `1. item` | A numbered list |
| `[link text](url)` | A clickable link |

**When will you encounter Markdown?**

- Reading documentation on GitHub
- Writing structured prompts for AI tools
- Creating or editing content in tools like Notion, Confluence, or Obsidian
- Reviewing technical specs from engineering teams
- Reading and writing **skills** — reusable AI instruction files that are written in Markdown (more on this in Part 4)

---

### 1.2 What Is GitHub?

GitHub is a platform where code and documents live, are versioned, and are collaborated on. Think of it as a "Google Drive for code" — but with powerful version control.

**Key concepts:**

- **Repository (repo):** A project folder. It contains all files, history, and documentation for a project.
- **README:** The front page of a repo. Written in Markdown. It explains what the project is, how to use it, and how to contribute.
- **Commit:** A saved change. Every time someone modifies a file and saves it to GitHub, that is a commit. You can always go back to any previous commit.
- **Branch:** A parallel version of the project. Teams create branches to work on features without affecting the main version.
- **Pull Request (PR):** A proposal to merge changes from one branch into another. This is where code review happens.
- **Issues:** Task tickets. Used to track bugs, feature requests, or discussions.

**Why does it matter for Portfolio Managers?**

The shared GitHub repository will serve as a living knowledge base. You will find prompt templates, skill definitions, and documentation there. Understanding the basics of GitHub means you can browse, search, and even contribute to this resource without needing engineering support.

---

### 1.3 What Is an API?

An API (Application Programming Interface) is a way for two software systems to talk to each other. It is a structured contract: "Send me this information in this format, and I will send you back a response."

**Real-world analogy:**

Imagine a restaurant. You (the client) do not walk into the kitchen. Instead, you talk to the waiter (the API). You place your order in a specific format (from the menu), the waiter takes it to the kitchen (the server), and brings back your food (the response).

**Why does it matter?**

Every AI tool — ChatGPT, Claude, internal tools — operates through APIs. When we talk about "connecting an AI agent to data" or "integrating with a CRM," we are talking about APIs. Understanding this concept helps you evaluate feasibility and communicate with engineering teams.

---

### 1.4 What Is JSON?

JSON (JavaScript Object Notation) is the standard format for sending structured data between systems. It is how APIs communicate.

**Example — a client record:**

```json
{
  "client_name": "Sample Family Office",
  "portfolio_value": 12500000,
  "risk_profile": "moderate",
  "investment_focus": ["equities", "fixed income"],
  "last_review": "2026-01-15"
}
```

**Why does it matter?**

When AI agents interact with tools (retrieve client data, query a database, call an API), the data flows in JSON format. You do not need to write JSON, but recognizing it helps you understand what data an agent is working with and how it is structured.

---

## Part 2: AI Chat — The Foundation

### 2.1 What Are LLMs?

A Large Language Model (LLM) is the engine behind tools like ChatGPT and Claude. It is a neural network trained on massive amounts of text data that can understand and generate human language.

**Key characteristics:**

- **They predict the next word.** At a fundamental level, LLMs work by predicting what comes next in a sequence of text. This simple mechanism, scaled to billions of parameters, produces remarkably sophisticated behavior.
- **They do not "know" things like a database does.** An LLM does not store facts in neat rows. It has learned patterns from training data. This means it can be confidently wrong (called "hallucination").
- **They have a knowledge cutoff.** LLMs are trained up to a specific date. Without tools like web search, they do not know about events after that date.
- **They work with context windows.** Every conversation has a limited amount of text the model can "see" at once. This is called the context window — typically 100K to 200K tokens (roughly 75K to 150K words).

### 2.2 ChatGPT vs. Claude — What Is the Difference?

Both are LLM-powered assistants, but they have different strengths and philosophies.

| Aspect | ChatGPT (OpenAI) | Claude (Anthropic) |
|---|---|---|
| **Company** | OpenAI | Anthropic |
| **Strengths** | Broad ecosystem, plugins, GPTs, image generation (DALL·E) | Long-context reasoning, careful analysis, document processing, coding |
| **Context window** | Up to 128K tokens (GPT-4o) | Up to 200K tokens (Claude Opus) |
| **Tool use** | Custom GPTs, plugins, code interpreter | MCP protocol, tool use API, computer use, artifacts |
| **Skills / reusability** | Custom GPTs (preconfigured assistants shared via link) | Skills (Markdown-based instruction files that guide behavior for specific tasks) |
| **Safety approach** | RLHF, content policies | Constitutional AI, emphasis on harmlessness and helpfulness |
| **Best for** | General tasks, creative content, image work | Deep analysis, long documents, structured reasoning, coding |

**In practice:**

Both tools are useful. The choice depends on the task. For long document analysis, structured reasoning, and coding tasks, Claude tends to excel. For quick creative tasks or when image generation is needed, ChatGPT has strong offerings. Both platforms support the concept of reusable "skills" — packaged instructions that make the AI behave consistently for specific tasks — though they implement it differently (see Part 4). The important thing is knowing when to use which tool and how to leverage skills to avoid reinventing the wheel every time.

### 2.3 How to Use These Tools Effectively

Using an AI assistant is not like using a search engine. You do not type three keywords and hope for the best. You have a conversation. The quality of your input directly determines the quality of the output.

**The basics:**

- **Be specific.** Instead of "help me with a report," say "I need to write a 2-page executive summary of Q1 2026 portfolio performance for the board. Focus on asset allocation changes and risk-adjusted returns."
- **Provide context.** The model does not know your role, your audience, or your constraints unless you tell it.
- **Iterate.** The first response is rarely the final one. Ask the model to refine, restructure, or take a different angle.
- **Review critically.** AI outputs need human judgment. Verify facts, check reasoning, and ensure alignment with your goals.

---

## Part 3: Prompt Engineering

### 3.1 What Is a Prompt?

A prompt is the instruction you give to an AI model. Everything the model does starts with a prompt. The better the prompt, the better the result.

**A prompt is not just a question.** It can include:

- **Role definition:** "You are a senior investment analyst at a private bank."
- **Context:** "Here is the Q1 portfolio report [attached]. The clients are high-net-worth individuals with diversified portfolios."
- **Task:** "Analyze the performance trends and identify the three holdings with the highest risk-adjusted returns."
- **Format:** "Present your findings as a table with columns: Holding, Previous Score, Current Score, Change, Key Driver."
- **Constraints:** "Keep the analysis under 500 words. Use formal tone suitable for client-facing communication."

### 3.2 Prompting Techniques

Here are the techniques that make the biggest difference, ordered from simplest to most advanced.

**1. Zero-Shot Prompting**
Simply asking the model to do something with no examples.

> "Summarize this investment report in three bullet points."

Good for straightforward tasks. The model uses its general knowledge.

**2. Few-Shot Prompting**
Providing examples of what you want before asking for the actual task.

> "Here are examples of how we format client briefs:
>
> Example 1: [example]
> Example 2: [example]
>
> Now write a client brief for the following portfolio update: [data]"

Powerful when you need a specific style, format, or tone.

**3. Chain-of-Thought (CoT) Prompting**
Asking the model to reason step by step before giving an answer.

> "Analyze whether this company meets our investment inclusion criteria. Think step by step:
> 1. First, evaluate the financial fundamentals (revenue growth, margins, debt levels).
> 2. Then, check valuation metrics relative to peers.
> 3. Then, review recent news and market sentiment.
> 4. Finally, give your recommendation with reasoning."

Essential for complex analysis where you need transparent reasoning.

**4. System Prompts**
A special instruction that defines the model's behavior for an entire conversation. Set once, applies to every response.

> System: "You are an AI assistant for an investment management team. You always consider risk-adjusted returns in your analysis. You cite sources when possible. You flag uncertainties clearly. You use a professional, precise tone."

This is how internal AI tools are configured to behave consistently.

**5. Structured Output Prompting**
Asking the model to respond in a specific format (JSON, table, XML) so the output can be used programmatically.

> "Return the analysis as a JSON object with the following structure:
> ```json
> {
>   "company": "...",
>   "risk_score": ...,
>   "recommendation": "include | exclude | review",
>   "reasoning": "..."
> }
> ```"

Critical for building automated workflows where AI output feeds into other systems.

### 3.3 Common Prompting Mistakes

- **Being too vague:** "Make this better" — The model does not know what "better" means to you.
- **Not specifying the audience:** A report for the board is very different from one for the data team.
- **Ignoring format:** If you do not specify format, you get whatever the model defaults to (usually long paragraphs).
- **Single-turn thinking:** Do not try to get everything perfect in one prompt. Use follow-ups.
- **Not providing examples:** If you have a specific style in mind, show it. Do not describe it abstractly.

Once you find a prompt that works well for a recurring task, the natural next step is to save it as a **skill** — a reusable, shareable instruction set. That is what Part 4 covers.

---

## Part 4: Skills — Reusable AI Capabilities

### 4.1 What Is a Skill?

A skill is a packaged set of instructions that tells an AI model how to perform a specific task consistently and reliably. Think of it as a recipe: instead of explaining from scratch every time how to make a dish, you write the recipe once, and anyone can follow it to get the same result.

**At its simplest, a skill is a well-crafted prompt saved for reuse.** At its most advanced, a skill combines instructions, tool definitions, context, and output formatting into a single package that an AI can load and execute.

**The spectrum of skills:**

| Level | What it is | Example |
|---|---|---|
| **Saved prompt** | A reusable text instruction | "Summarize any investment report in 3 bullet points with this format..." |
| **Prompt template** | A prompt with variables that get filled in per use | "Analyze {company_name} against investment criteria {criteria_list} and output a score card" |
| **Skill file (SKILL.md)** | A structured Markdown document with instructions, best practices, and constraints | A file that tells the AI exactly how to create a professional PowerPoint, including layout rules, font choices, and slide structure |
| **Full skill package** | Instructions + tool definitions + context + validation rules | A complete capability: "Screen a list of companies for portfolio inclusion" that includes which APIs to call, how to interpret the data, what thresholds to apply, and how to format the output |

### 4.2 Why Do Skills Matter?

Without skills, every interaction with an AI starts from zero. You explain the context, the format, the constraints, the tone — every single time. This is inefficient and inconsistent.

Skills solve three problems:

- **Consistency:** The same skill produces the same quality of output regardless of who uses it. A junior analyst and a senior portfolio manager get the same level of analysis.
- **Efficiency:** Instead of writing a 200-word prompt every time, you load a skill and provide only the variable inputs (e.g., the company name or the dataset).
- **Knowledge capture:** When someone figures out the best way to prompt an AI for a specific task, that knowledge is saved and shared — not locked in one person's head or chat history.

### 4.3 How Skills Work in Practice

**The SKILL.md format:**

In tools like Claude, a skill is typically a Markdown file (`.md`) that contains structured instructions the AI reads before performing a task. This is why understanding Markdown matters (see Part 1).

A SKILL.md file typically includes:

- **Name and description:** What the skill does and when to use it.
- **Trigger conditions:** When should the AI activate this skill? (e.g., "Use this skill whenever the user asks to create a presentation.")
- **Step-by-step instructions:** The detailed procedure the AI should follow.
- **Best practices and constraints:** What to do and what to avoid.
- **Output format:** How the result should look.

**Example — a simplified Investment Screening Skill:**

```markdown
# Investment Screening Skill

## Description
Screen a company against investment inclusion criteria
and produce a standardized assessment.

## When to use
Use when asked to evaluate a company for portfolio inclusion
or investment eligibility.

## Instructions
1. Gather the company's financial data from available sources.
2. Evaluate against each of the core criteria:
   - Fundamentals: revenue growth, profit margins, debt-to-equity
   - Valuation: P/E ratio, P/B ratio, comparison to sector peers
   - Risk: volatility, liquidity, concentration exposure
3. Score each criterion on a scale of 1-10.
4. Flag any critical disqualifiers (e.g., regulatory sanctions,
   accounting irregularities, extreme leverage).
5. Provide an overall recommendation: Include / Exclude / Review.

## Output format
Return a structured assessment with:
- Company name and sector
- Score per criterion (1-10)
- Overall score (weighted average)
- Critical flags (if any)
- Recommendation with reasoning
```

This file lives in a repository. When the AI is asked to screen a company, it reads this skill and follows the instructions precisely — producing a consistent, high-quality output every time.

### 4.4 Skills as Building Blocks for Workflows

Skills are not just standalone tools. They are the building blocks that make AI workflows and agents possible.

Consider how skills connect to the concepts covered later in this guide:

- **A workflow** (Part 6) is a sequence of steps. Each step can be powered by a skill.
- **An agent** (Part 5) decides which skills to use and in what order.
- **Orchestration** (Part 7) coordinates multiple agents, each equipped with different skills.

**Analogy:** If an AI agent is an employee, skills are the training manuals and procedures that employee has been given. The more skills available, the more capable the agent becomes — but each skill is focused, tested, and reliable on its own.

### 4.5 Skills Across Platforms

The concept of reusable AI capabilities exists across different tools, though the implementation varies:

| Platform | Skill equivalent | How it works |
|---|---|---|
| **Claude** | Skills (SKILL.md files), Projects | Markdown instruction files loaded into context. Can include tool definitions and structured workflows. |
| **ChatGPT** | Custom GPTs | Preconfigured assistants with custom instructions, knowledge files, and tool access. Shared via link. |
| **Internal tools** | Prompt libraries, templates | Centralized collections of reusable prompts and configurations. |
| **Agent frameworks** | Tool definitions, runbooks | Structured instructions that agents follow when executing specific tasks. |

The underlying principle is the same across all platforms: capture what works, package it, and make it reusable.

### 4.6 Building Your Own Skills

You do not need to be a developer to create a skill. If you can describe a task clearly and define what a good output looks like, you can write a skill.

**Steps to create a skill:**

1. **Identify a repeatable task.** What do you do regularly that involves AI? (e.g., summarizing research reports, drafting client updates, screening companies)
2. **Write the prompt that works.** Iterate until you get consistently good results.
3. **Structure it.** Add a name, description, trigger conditions, step-by-step instructions, and output format.
4. **Save it as a Markdown file.** Store it in the shared GitHub repository so others can use and improve it.
5. **Test and refine.** Have others try the skill. Collect feedback. Improve the instructions.

The GitHub repository accompanying this guide is designed to be a growing collection of these skills. Every Portfolio Manager can contribute.

---

## Part 5: Tool Use & MCP

### 5.1 From Chat to Action — The Evolution

Early AI assistants could only read text and respond with text. That was useful, but limited. The breakthrough came when LLMs learned to use tools.

**The progression:**

1. **Chat only** (2022): Ask a question, get a text answer.
2. **Chat + retrieval** (2023): The model can search the web or internal documents before answering.
3. **Chat + tool use** (2024): The model can call APIs, run code, query databases, create files.
4. **Skills + agents** (2025–2026): The model can load reusable skills, plan multi-step tasks, use multiple tools, and execute workflows end-to-end.

### 5.2 What Is Tool Use?

Tool use means giving an LLM the ability to call external functions. Instead of just generating text, the model can:

- **Search the web** for current information
- **Query a database** to retrieve client data
- **Call an API** to get market prices, risk scores, or portfolio data
- **Create files** like spreadsheets, presentations, or PDFs
- **Send messages** via email or Slack
- **Execute code** to perform calculations or data analysis

**How it works (simplified):**

1. You give the model a list of available tools with descriptions.
2. The model reads your request and decides which tool(s) to use.
3. The model generates a structured "tool call" (in JSON format).
4. The system executes the tool call and returns the result to the model.
5. The model uses the result to compose its final response.

**Example flow:**

You ask: "What was the return of the Global Equity Fund in Q1 2026?"

1. Model decides to use the `portfolio_api` tool.
2. Model generates: `{"tool": "portfolio_api", "params": {"fund": "Global Equity", "period": "Q1 2026", "metric": "return"}}`
3. System calls the API and returns: `{"return": "4.7%", "benchmark": "3.2%"}`
4. Model responds: "The Global Equity Fund returned 4.7% in Q1 2026, outperforming its benchmark by 1.5 percentage points."

### 5.3 What Is MCP (Model Context Protocol)?

MCP is an open standard — created by Anthropic — that allows AI models to connect to external tools and data sources in a standardized way.

**Think of it like USB for AI.** Before USB, every device had a different connector. MCP is the universal connector that lets any AI model talk to any tool.

**Why does MCP matter?**

- **Standardization:** Instead of building custom integrations for every tool, you build one MCP connector and any compatible AI model can use it.
- **Interoperability:** A single MCP server (e.g., for Salesforce) can be used by Claude, ChatGPT, or any other compatible model.
- **Growing ecosystem:** Major platforms (Google Drive, Slack, Salesforce, GitHub, Jira, and many more) already have MCP connectors.

**In practice, MCP means:**

If an organization builds an MCP connector to its portfolio management system, any AI tool that supports MCP can immediately access that data — without rebuilding the integration from scratch for each tool.

---

## Part 6: AI Agents

### 6.1 What Is an AI Agent?

An AI agent is an LLM that can autonomously plan, reason, and execute multi-step tasks using tools. An agent's capabilities depend on what **skills** it has been given (Part 4) and what **tools** it can access (Part 5).

**The difference between a chatbot and an agent:**

| Chatbot | Agent |
|---|---|
| You ask, it answers | You assign a goal, it figures out how to achieve it |
| One turn at a time | Plans and executes multiple steps |
| No memory of actions | Tracks its progress and adapts |
| Uses no external tools | Uses tools and skills (APIs, databases, web, files) |
| You drive the conversation | The agent drives toward the goal |

**Analogy:**

A chatbot is like a very knowledgeable colleague who answers your questions. An agent is like a skilled analyst who you can delegate a full task to: "Research these 10 companies' financials, compare them against our inclusion criteria, and prepare a summary table with recommendations." The agent will figure out which skills and tools to use, in what order, and deliver the result.

### 6.2 The Agent Loop

Every agent follows a fundamental cycle:

```
┌─────────────────────────────────────┐
│                                     │
│   1. PERCEIVE                       │
│      Read input / observe state     │
│              │                      │
│              ▼                      │
│   2. REASON                         │
│      Analyze what needs to happen   │
│              │                      │
│              ▼                      │
│   3. PLAN                           │
│      Decide which tools to use      │
│              │                      │
│              ▼                      │
│   4. ACT                            │
│      Execute tool calls             │
│              │                      │
│              ▼                      │
│   5. EVALUATE                       │
│      Check if the goal is met       │
│              │                      │
│         ┌────┴──────┐               │
│         │           │               │
│       Done     Not done            │
│         │           │               │
│      Return    Loop back           │
│      result    to step 1           │
│                                     │
└─────────────────────────────────────┘
```

**This loop is what makes agents powerful.** They do not just respond once — they keep working until the task is done or they realize they need human input.

### 6.3 Agent Capabilities at Different Levels

Not all agents are equally autonomous. Here is a spectrum:

| Level | Name | Description | Example |
|---|---|---|---|
| L0 | **Chat** | Pure conversation, no tools | "What is a Sharpe ratio?" |
| L1 | **Tool-assisted chat** | Uses tools when asked, single step | "Look up the current P/E ratio for Nestlé" |
| L2 | **Simple agent** | Plans 2–5 steps, uses multiple tools | "Compare risk metrics of our top 10 holdings and flag any above threshold" |
| L3 | **Complex agent** | Multi-step reasoning, error handling, adapts plan | "Review our entire portfolio, identify concentration risks, cross-reference with recent news, and draft a risk report" |
| L4 | **Multi-agent system** | Multiple specialized agents collaborating | "Research agent finds data → Analysis agent evaluates → Writing agent drafts report → Review agent checks quality" |

**Where most investment teams are today:**

Most current AI usage in the industry is at L0–L1. The opportunity is to move toward L2–L3 for specific, well-defined workflows. L4 is an aspirational target for high-value, complex processes.

---

## Part 7: Workflows vs. Agents

### 7.1 What Is an AI Workflow?

A workflow is a predefined sequence of steps where an LLM is used at specific points. The flow is designed by humans. The AI executes within guardrails.

**Characteristics:**

- **Deterministic:** Same input → same path (though LLM outputs may vary slightly).
- **Human-designed:** A person defines the steps, conditions, and branching logic.
- **Predictable:** You know exactly what will happen at each step.
- **Easier to debug:** When something goes wrong, you know which step failed.

**Example — Automated Investment Screening Workflow:**

```
Step 1: Receive list of potential investments
         ↓
Step 2: For each company, call financial data API
         ↓
Step 3: LLM analyzes data against inclusion criteria
         ↓
Step 4: If score > threshold → "Approved"
        If score < threshold → "Rejected"
        If borderline → flag for human review
         ↓
Step 5: Generate summary report
         ↓
Step 6: Send report to portfolio manager
```

### 7.2 What Is an Agentic Workflow?

An agentic workflow gives the AI more autonomy within a structured framework. The agent decides how to accomplish each step, but the overall process is guided.

**Characteristics:**

- **Semi-autonomous:** The agent has freedom within boundaries.
- **Adaptive:** The agent can handle unexpected situations (missing data, errors, edge cases).
- **Goal-oriented:** You define the goal, the agent figures out the path.
- **Requires guardrails:** You set limits on what the agent can and cannot do.

### 7.3 When to Use Which?

| Scenario | Recommended approach | Why |
|---|---|---|
| Repeatable, well-defined process | **Workflow** | Predictable, auditable, lower risk |
| Process with many edge cases | **Agentic workflow** | Agent can handle exceptions flexibly |
| One-off complex research task | **Agent** | Too varied to predefine steps |
| High-stakes, regulated process | **Workflow + human checkpoints** | Compliance requires auditability |
| Exploratory analysis | **Agent** | Unknown path, needs flexibility |

**General rule of thumb:**

Start with workflows. Add agent capabilities only where the rigidity of a workflow creates real problems. In financial services, auditability and predictability are features, not bugs.

---

## Part 8: Orchestration — Multi-Agent Systems

### 8.1 What Is Orchestration?

Orchestration is the coordination of multiple AI agents (or AI steps) working together to accomplish a complex task. Think of it as a conductor leading an orchestra — each instrument (agent) has a role, and the conductor ensures they play together harmoniously.

Each agent in an orchestrated system is typically equipped with a specific set of **skills** (Part 4) and **tools** (Part 5). The orchestration layer decides which agent handles which part of the task, passes data between them, and ensures the final output meets quality standards.

### 8.2 Common Orchestration Patterns

**1. Sequential (Pipeline)**

Agents work one after another. The output of one is the input of the next.

```
Agent A → Agent B → Agent C → Final Output
(Research)  (Analyze)  (Write)
```

**Use case:** Research a topic → Analyze findings → Write a report.

**2. Parallel (Fan-Out / Fan-In)**

Multiple agents work simultaneously on different parts of a task, and their results are combined.

```
           ┌→ Agent A (Fundamentals) ───┐
Task ──────┼→ Agent B (Valuation)     ──┼──→ Combine → Final Output
           └→ Agent C (News/Sentiment)──┘
```

**Use case:** Analyze a company from multiple angles simultaneously.

**3. Router**

A single agent (the router) decides which specialized agent should handle each request.

```
                    ┌→ Agent A (Research queries)
Incoming request → Router ──┼→ Agent B (Portfolio queries)
                    └→ Agent C (Compliance queries)
```

**Use case:** An internal assistant that routes questions to the right expert agent.

**4. Evaluator-Optimizer (Feedback Loop)**

One agent generates output, another evaluates it, and sends feedback for improvement.

```
Generator Agent ←──→ Evaluator Agent
    (draft)              (review)
         ↓ (when approved)
     Final Output
```

**Use case:** Draft client communications with automatic quality review.

**5. Hierarchical (Supervisor)**

A supervisor agent manages and delegates to worker agents.

```
         Supervisor Agent
        ┌────┼────────┼─────┐
        │    │        │     │
     Agent Agent   Agent Agent
       A     B       C     D
```

**Use case:** Complex project execution where sub-tasks need coordination.

### 8.3 Human-in-the-Loop

In financial services, fully autonomous agents are rarely appropriate. The most practical pattern is **human-in-the-loop (HITL)**, where agents do the heavy lifting but humans approve key decisions.

**Where to place human checkpoints:**

- Before any client-facing communication is sent
- Before any trade or investment decision is executed
- When the agent encounters high-uncertainty situations
- At regulatory or compliance decision points
- When the agent's confidence is below a defined threshold

**The goal is not to replace human judgment. It is to amplify it.** Agents handle the research, data gathering, and first-draft analysis. Humans review, validate, and make the final call.

---

## Part 9: Practical Considerations for Portfolio Managers

### 9.1 Scoping AI-Powered Features

When evaluating whether to add AI to a process or investment workflow, ask:

1. **Is the task repetitive and well-defined?** → Start with a workflow.
2. **Does it require judgment across varied situations?** → Consider an agent.
3. **What is the cost of an error?** → High cost = more guardrails, more human oversight.
4. **Where does the data come from?** → Define what APIs/tools the agent needs.
5. **Who reviews the output?** → Always define the human checkpoint.
6. **How do we measure success?** → Define metrics before building.

### 9.2 Key Risks to Watch

- **Hallucination:** AI can generate plausible but incorrect information. Always verify factual claims, especially in financial contexts.
- **Cost:** API calls cost money. Complex agent workflows with many tool calls can become expensive. Design with cost awareness.
- **Latency:** Agent loops take time. A 5-step agent workflow might take 30–60 seconds. Set user expectations.
- **Reliability:** Agents can fail or loop infinitely. Always design timeout and fallback mechanisms.
- **Data privacy:** Be intentional about what data flows through external AI services. Understand what is processed locally vs. in the cloud.
- **Regulatory compliance:** In financial services, every AI-assisted decision may need an audit trail.

### 9.3 Your Role as a Portfolio Manager

You do not need to build agents. You need to:

- **Identify opportunities** where AI can save time or improve quality.
- **Define the requirements** clearly — what should the agent do, what tools does it need, what are the guardrails?
- **Evaluate feasibility** — is this an L1 task or an L4 task? Start simple.
- **Design the human-in-the-loop experience** — where do humans interact?
- **Measure impact** — did the AI actually save time / improve quality / reduce errors?

---

## Glossary

| Term | Definition |
|---|---|
| **LLM** | Large Language Model — the AI engine behind tools like ChatGPT and Claude |
| **Prompt** | The instruction or input you give to an AI model |
| **Token** | A unit of text (roughly ¾ of a word). Models process and charge by tokens |
| **Context window** | The maximum amount of text a model can consider at once |
| **Hallucination** | When an AI generates incorrect information that sounds confident |
| **API** | Application Programming Interface — how software systems communicate |
| **JSON** | A structured data format used for API communication |
| **Markdown** | A simple text formatting syntax used in documentation and AI tools |
| **MCP** | Model Context Protocol — a universal standard for connecting AI to tools |
| **Skill** | A packaged, reusable set of AI instructions for a specific task — from a saved prompt to a full capability with tools and validation |
| **SKILL.md** | A Markdown file containing structured instructions that guide an AI model's behavior for a specific task |
| **Agent** | An AI that can plan, reason, use skills and tools, and work autonomously toward a goal |
| **Workflow** | A predefined sequence of steps, some powered by AI |
| **Orchestration** | Coordinating multiple agents or AI steps to accomplish complex tasks |
| **HITL** | Human-in-the-Loop — humans reviewing/approving AI outputs at key points |
| **Few-shot** | Providing examples in a prompt to guide the model's behavior |
| **Chain-of-thought** | Asking the model to reason step by step |
| **RAG** | Retrieval-Augmented Generation — giving the model access to external knowledge |
| **System prompt** | A persistent instruction that defines the model's behavior for a session |
| **Tool use** | The ability of an LLM to call external functions (APIs, databases, etc.) |
| **Fine-tuning** | Training a model on custom data to specialize its behavior |
| **Embedding** | A numerical representation of text used for search and similarity |
| **GitHub** | A platform for hosting, versioning, and collaborating on code and documentation |
| **Repository (repo)** | A project folder on GitHub containing code, docs, and history |
| **Pull Request (PR)** | A proposal to merge changes, with review and discussion |

---

## Next Steps

1. **Explore the GitHub repository** — Browse existing skills, prompt templates, and documentation.
2. **Try structured prompting** — Use the techniques from Part 3 on your next AI task.
3. **Create your first skill** — Follow the steps in Part 4.6 to package a repeatable task as a reusable skill.
4. **Identify one workflow** — Think of a repetitive task in your area that could benefit from AI.
5. **Contribute** — Add your skills and improvements to the shared repository so others benefit too.

---

*This is a living document. It will grow as we develop new tools, skills, and best practices. Contributions are welcome via the GitHub repository.*
