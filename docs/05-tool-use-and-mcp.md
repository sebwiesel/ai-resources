# Part 5: Tool Use & MCP

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
