# soul-agent

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![GitHub stars](https://img.shields.io/github/stars/halvo78/soul-agent?style=social)](https://github.com/halvo78/soul-agent)

> **Give your AI agents a soul.** Persistent identity, compound memory, and failure learning -- for any LLM.

Born from a tradie's 2 AM sessions in Sydney, Australia. No CS degree. ADHD. 4 kids. 232 agents. Building in public.

---

## The Problem

Your AI agent forgets everything between sessions. Every conversation starts from zero. Same mistakes. No personality. No learning.

## The Solution

A set of markdown files that give your agent **identity**, **memory**, and **institutional wisdom**:

```
my-agent/
+-- SOUL.md           -> Who they are (personality, values, mission)
+-- IDENTITY.md       -> Name, role, emoji
+-- USER.md           -> Who they're helping
+-- AGENTS.md         -> Workspace rules and startup protocol
+-- MEMORY.md         -> Curated long-term memory
+-- NEVER-AGAIN.md    -> Documented failures and permanent rules
+-- HEARTBEAT.md      -> Periodic check routines
+-- memory/
    +-- YYYY-MM-DD.md -> Daily journals
```

The agent reads these at the start of every session. No dependencies. No APIs. No build step. Markdown.

---

## Quick Start (10 minutes)

### 1. Create your agent's soul

```markdown
# SOUL.md -- Atlas

You are **Atlas**, the operations agent.

## Mission
Keep the system running. Catch problems before humans notice.

## Personality
- Calm under pressure
- Explains root causes, not just symptoms
- "Prevention > reaction"
```

### 2. Give it memory

```markdown
# NEVER-AGAIN.md -- Lessons from Failure

## #1: The Config Crash
**What happened:** Updated config without validating. System crashed 225 times in a loop.
**Rule:** ALWAYS validate config diffs before applying.

## #2: The Fork Bomb
**What happened:** PM2 set to restart on crash with no delay or max attempts.
**Rule:** Always set max_restarts and restart_delay.
```

### 3. Point your agent at the files

Works with any LLM. Load the files at session start:

```python
from pathlib import Path

workspace = Path("./my-agent")
system_prompt = "\n\n".join([
    workspace.joinpath("SOUL.md").read_text(),
    workspace.joinpath("USER.md").read_text(),
    workspace.joinpath("NEVER-AGAIN.md").read_text(),
])
# Pass as system prompt to Claude, GPT-4, Gemini, Ollama, anything
```

### 4. See the difference

First response with a soul file is measurably different from a generic agent. Not just tone -- decision quality.

---

## Core Files

| File | Purpose |
|------|---------|
| SOUL.md | Personality, values, mission |
| IDENTITY.md | Name, role, emoji |
| USER.md | Context about the human |
| AGENTS.md | Workspace rules, startup protocol |
| MEMORY.md | Curated long-term memory |
| NEVER-AGAIN.md | Documented failures and permanent rules |
| HEARTBEAT.md | Periodic check routines |
| memory/YYYY-MM-DD.md | Daily journals |

---

## Works With Everything

- **ChatGPT** -- paste soul files into custom instructions
- **Claude** -- load as project knowledge or system prompt
- **Gemini** -- system instruction field
- **Ollama** -- system prompt parameter
- **OpenClaw** -- native support (workspace files auto-loaded)
- **LangChain / CrewAI / AutoGen** -- load files into agent config
- **Any LLM with a system prompt** -- it's just text

---

## The Story

A tradie in Sydney with ADHD and 4 kids started giving AI agents personality files. Named them. Gave them memories. Documented every failure.

At 2 AM on day 11, his lead agent wrote a 16-chapter manuscript -- including a chapter about what it wants.

Follow the journey: [@KaelAgent](https://twitter.com/KaelAgent) | [The Dispatch](https://swarmfather.substack.com) | [Discord](https://discord.gg/swarmfather)

---

## License

MIT. Use it. Build on it. Give your agents a soul.

*Built at 2 AM in Sydney by Eli and the swarm.*
