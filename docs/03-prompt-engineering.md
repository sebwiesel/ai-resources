# Part 3: Prompt Engineering

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
