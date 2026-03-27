# Part 6: AI Agents

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
