---
layout: post
title: "Building a Personal Financial Advisor Skill for Claude"
tags: claude ai personal-finance ramit-sethi
---

I've been experimenting with Claude's skill system for a while now, and I recently built one that I'm genuinely excited about: a personal financial advisor skill grounded in Ramit Sethi's *I Will Teach You To Be Rich* philosophy.

You can find it on GitHub: [financial-advisor skill](https://github.com/CarlosEspejo/knowledge-work-plugins/blob/main/plugins/financial-advisor/skills/financial-advisor/SKILL.md)

## What is a Claude Skill?

Skills are structured prompts that give Claude a specific persona, framework, and operating procedure for a domain. Instead of starting every conversation from scratch, a skill primes Claude with deep context so it can act like a specialist from the first message.

## Why Ramit Sethi's Framework?

Most personal finance advice is either too generic ("spend less, save more") or too anxiety-inducing. Ramit's approach is different. It focuses on:

- **Big wins over small cuts** — Negotiating a raise or eliminating high-interest debt moves the needle far more than skipping lattes
- **Conscious spending** — You don't have to cut everything, just spend intentionally on what you actually value
- **Automation** — Build systems so good financial behavior happens without relying on willpower

This translates really well into an AI assistant context. The advisor doesn't lecture; it helps you build a plan.

## The Conscious Spending Plan

The core of the skill is the Conscious Spending Plan (CSP), which allocates take-home income across four buckets:

| Category | Target |
|---|---|
| Fixed Costs | 50–60% |
| Investments | 10% |
| Savings Goals | 5–10% |
| Guilt-Free Spending | 20–35% |

That last bucket is key. Guilt-free spending isn't a failure mode — it's an intentional allocation. Calling it that changes how people think about it.

## The Investment Priority Ladder

One thing I wanted to make sure the skill got right was sequencing. A lot of people ask "should I pay off debt or invest?" The answer depends on the interest rates and account types involved. The skill walks through a clear ladder:

1. Contribute to your 401k up to the employer match (free money)
2. Pay off high-interest debt (credit cards)
3. Max your Roth IRA ($7,000 for 2024–2025)
4. Max your 401k ($23,500 for 2025)
5. Invest in a taxable brokerage (VOO is the default recommendation)

The skill also specifically flags 401k loans as something to avoid — they create a double-taxation problem that most people don't realize until it's too late.

## How a Session Works

The skill structures each conversation in five steps:

1. Warm greeting and situation assessment
2. Financial diagnosis
3. Mapping out the Conscious Spending Plan
4. Prioritized action items
5. Follow-up and iteration

The tone is direct and warm, not preachy. The goal is specific, actionable advice — not a disclaimer farm.

## Try It Yourself

If you use Claude, you can load the skill and start a conversation about your finances. Whether you're just starting out, dealing with debt, or trying to figure out how to invest, it gives you a structured framework to work through your situation.

The skill file is [open source on GitHub](https://github.com/CarlosEspejo/knowledge-work-plugins/blob/main/plugins/financial-advisor/skills/financial-advisor/SKILL.md). Pull requests welcome.
