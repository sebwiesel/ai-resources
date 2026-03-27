# Part 9: Practical Considerations for Portfolio Managers

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
