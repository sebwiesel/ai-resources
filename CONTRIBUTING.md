# Contributing

This repository is intended to be useful in a professional investment context. Contributions should therefore optimize for clarity, repeatability, and reviewability.

## General Standards

- Keep content practical and easy to scan.
- Use Markdown for documentation and template assets.
- Avoid client identifiers, credentials, internal-only links, and proprietary source material.
- Explain assumptions, limitations, and intended audience where relevant.
- Prefer focused pull requests over broad mixed changes.

## What You Can Contribute

- Improvements to the core guide in `docs/`
- Curated external references in `docs/resources.md`
- Reusable prompt templates in `prompts/`
- Reviewed skills in `skills/`
- Sanitized worked examples in `examples/`
- Presentation materials in `presentation/`

## Review Bar by Content Type

### Documentation

Documentation should improve comprehension, remove ambiguity, or add clearly useful reference material.

### Prompt Templates

Prompt templates should include:

- A clear use case and target audience
- Required inputs or context
- Expected output format
- Any important constraints, review notes, or risk flags

### Skills

Skills are review-gated because they may be reused in higher-stakes workflows. A proposed skill should include:

- Clear business purpose and scope
- Defined inputs and expected outputs
- Tool or data dependencies
- Validation or review steps
- Known limitations and failure modes
- Ownership or point of contact where relevant

### Examples

Examples should be sanitized, reproducible, and useful for teaching. If an example depends on fictional data, say so explicitly.

## Pull Request Guidance

- Describe what changed and why it matters.
- Call out any sections that may need domain review.
- If you add or modify prompts or skills, include a short usage example.
- If your change affects professional use or risk posture, note that explicitly in the PR description.
