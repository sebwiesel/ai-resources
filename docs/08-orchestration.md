# Part 8: Orchestration — Multi-Agent Systems

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
