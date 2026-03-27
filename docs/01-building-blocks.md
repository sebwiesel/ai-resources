# Part 1: The Building Blocks

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
