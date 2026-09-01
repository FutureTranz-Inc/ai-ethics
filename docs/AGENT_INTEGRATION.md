# Agent Integration Guide

**Credits:** [FutureTranz-Inc](https://github.com/FutureTranz-Inc) | [victorjquinones](https://github.com/victorjquinones)

This is the single entry point for LLM agent starter files in this repository. Copy the file that matches the tool you are configuring, then follow [AGENTS.md](../AGENTS.md) for repository-specific rules.

## Common Principles

Every starter file follows the same rules:

1. Read [AGENTS.md](../AGENTS.md) first.
2. Copy the matching starter into your project root or agent configuration directory.
3. Customize project-specific rules without weakening human authorship requirements.
4. Do not add AI co-author lines, "Generated with" footers, or tool credit in commits, pull requests, or documentation. See [AI_ATTRIBUTION_POLICY.md](../AI_ATTRIBUTION_POLICY.md).

AI tools are assistants. Humans remain the authors.

## Starter Files

| Tool | Vendor | Starter file |
| --- | --- | --- |
| Claude | Anthropic | [CLAUDE.md](../CLAUDE.md) |
| Gemini | Google | [GEMINI.md](../GEMINI.md) |
| GPT | OpenAI | [GPT.md](../GPT.md) |
| Copilot | GitHub | [COPILOT.md](../COPILOT.md) |
| Cursor | Cursor | [CURSOR.md](../CURSOR.md) |
| Grok | xAI | [GROK.md](../GROK.md) |

## How to Add Another Agent

1. Add a root starter file that matches the existing starters in structure and tone.
2. Link it from this guide and from the Agent Starter Files section in [README.md](../README.md).
3. If the tool can emit authorship footers, add its name to the prohibited patterns in `src/ai_ethics_enforcer.py`, `scripts/ci-check-attribution.sh`, `scripts/clean-ai-attribution-history.sh`, and [AI_ATTRIBUTION_POLICY.md](../AI_ATTRIBUTION_POLICY.md).
