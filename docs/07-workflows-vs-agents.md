# Part 7: Workflows vs. Agents

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
