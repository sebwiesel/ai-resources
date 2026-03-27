# Part 4: Skills — Reusable AI Capabilities

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
