# Part 2: AI Chat — The Foundation

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
