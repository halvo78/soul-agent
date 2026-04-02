---
title: Agent Registry
tags: [agents, openclaw, swarm, registry]
aliases: [Agent Registry, Swarm, Agents]
---

# Agent Registry -- 25 OpenCLAW Agents

> [!info] All 25 agents have: IDENTITY.md + SOUL.md + memory/ directory + indexed memory
> Identity files: `E:\repos\halvo-fortress\agents\{name}\IDENTITY.md`
> Config: `C:\Users\Halvo\.openclaw\` | Gateway: `openclaw.cmd` on Windows
> Gateway: OpenCLAW :19000 (v2026.2.26) | CLI: `openclaw.cmd agent list`

---

## Tier Overview

| Tier | Model | Count | Purpose |
|------|-------|-------|---------|
| Premium | openai/gpt-4o | 5 | Heavy-lift specialists (gilfoil, musk, strategist, redhat, counsel) |
| Mid | openai/gpt-4o | 10 | Domain experts (goggins, jarvis, buffett, hormozi, naval, bluehat, analyst, scribe, pixel, quant) |
| Budget | openai/gpt-4o-mini | 10 | Fast routing and lightweight tasks |
| Free | ollama/llama3.2:3b | 1 | Local quality gate (oversight) |

---

## Opus Tier (5 Agents)

| # | Agent | Role | Link |
|---|-------|------|------|
| 2 | gilfoil | Security | [[gilfoil]] |
| 10 | musk | Engineering | [[musk]] |
| 12 | strategist | Planning | [[strategist]] |
| 18 | redhat | Emotional Intelligence & Intuition | [[redhat]] |
| 21 | counsel | Australian Compliance | [[counsel]] |

## Sonnet Tier (10 Agents)

| # | Agent | Role | Link |
|---|-------|------|------|
| 1 | goggins | Discipline | [[goggins]] |
| 5 | jarvis | Operations | [[jarvis]] |
| 6 | buffett | Investment | [[buffett]] |
| 7 | hormozi | Revenue | [[hormozi]] |
| 8 | naval | Philosophy | [[naval]] |
| 19 | bluehat | Defensive Security | [[bluehat]] |
| 20 | analyst | Data Intelligence | [[analyst]] |
| 22 | scribe | Writing Craft | [[scribe]] |
| 23 | pixel | UX Design | [[pixel]] |
| 24 | quant | Financial Modeling | [[quant]] |

## Mini Tier (10 Agents)

| # | Agent | Role | Link |
|---|-------|------|------|
| 0 | main | Router | [[main]] |
| 3 | kevin | Morale | [[kevin]] |
| 4 | drcox | Code Review | [[drcox]] |
| 9 | aurelius | Stoic | [[aurelius]] |
| 11 | coach | Goals | [[coach]] |
| 13 | mrbeast | Content | [[mrbeast]] |
| 14 | dropship | Ecommerce | [[dropship]] |
| 15 | marketer | Growth | [[marketer]] |
| 16 | ideagen | Ideas | [[ideagen]] |
| 17 | profithunter | Profit | [[profithunter]] |

## Free Tier (1 Agent)

| # | Agent | Role | Link |
|---|-------|------|------|
| - | oversight | Quality Gate & Gap Detector | [[oversight]] |

---

## Teams

| Team | Lead | Members | Purpose |
|------|------|---------|---------|
| Security Council | [[gilfoil]] | redhat (intuition), bluehat (process) | Threat assessment, security decisions |
| Wealth Council | [[buffett]] | profithunter (radar), quant (models), analyst (data) | Investment and revenue analysis |
| Decision Panel | [[strategist]] | bluehat (facilitation), redhat (emotion), counsel (legal) | Major business decisions |
| Business Launch | [[strategist]] | hormozi (offers), marketer (distribution), dropship (operations), counsel (compliance) | New venture execution |
| Growth Engine | [[mrbeast]] | marketer (distribution), hormozi (monetization), profithunter (opportunities) | Scaling and revenue growth |
| Code Quality | [[drcox]] | oversight (gaps), gilfoil (security) | Code review and quality assurance |
| First Principles | [[musk]] | ideagen (creativity), naval (philosophy), aurelius (principles) | Moonshot planning and innovation |
| Creative Squad | [[ideagen]] | mrbeast (scale), scribe (craft), pixel (design) | Content and creative output |
| Support | [[jarvis]] | kevin (morale/accounting), coach (accountability), main (routing) | Daily operations and team health |

---

## Array Index Map

Used for config commands: `openclaw.cmd config set "agents.list[N].model.primary" "model/name"`

```
0:main  1:goggins  2:gilfoil  3:kevin  4:drcox  5:jarvis  6:buffett
7:hormozi  8:naval  9:aurelius  10:musk  11:coach  12:strategist
13:mrbeast  14:dropship  15:marketer  16:ideagen  17:profithunter
18:redhat  19:bluehat  20:analyst  21:counsel  22:scribe  23:pixel  24:quant
```

---

## Channels

| Channel | Platform | Status |
|---------|----------|--------|
| Discord | @HALVO-HOME-Brain | Connected |
| Telegram | @Kael_home_bot | Connected |

> [!warning] Routing Gap
> 27 keyword routing rules exist in `routing-rules.json` but NO executor code. All messages route to `main` by default. Keyword routing needs a custom bridge layer -- `agents bind` only does channel-level routing.

---

## Plugins (12/36 Loaded)

copilot-proxy, device-pair, discord, google-gemini-cli-auth, llm-task, lobster, memory-core, open-prose, phone-control, talk-voice, telegram, diagnostics-otel

## Skills (11/51 Ready)

prose, coding-agent, discord, gh-issues, github, healthcheck, nano-banana-pro, openai-whisper-api, session-logs, skill-creator, weather

---

*Registry verified Session 17 (2026-02-27). 5 new agents added Session 7 (2026-03-06).*
