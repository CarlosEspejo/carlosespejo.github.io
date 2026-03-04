---
layout: post
title: "Building a Rich Life Skill for Claude"
tags: claude ai personal-finance ramit-sethi
---

Most people know they should be investing. They just don't know where to start — and generic advice ("spend less, save more") doesn't help. I built a Claude skill to fix that: a Rich Life guide grounded in Ramit Sethi's *I Will Teach You To Be Rich* philosophy that gives you a concrete plan, not platitudes.

## What is a Claude Skill?

Skills are structured prompts that give Claude a specific persona, framework, and operating procedure for a domain. Instead of starting every conversation from scratch, a skill primes Claude with deep context so it can act like a specialist from the first message.

## Try It Yourself

The skill file is [open source on GitHub](https://github.com/CarlosEspejo/knowledge-work-plugins/blob/main/plugins/rich-life/skills/rich-life/SKILL.md). This works with any Claude account, including the free tier at [claude.ai](https://claude.ai).

1. Open the [raw SKILL.md file](https://raw.githubusercontent.com/CarlosEspejo/knowledge-work-plugins/refs/heads/main/plugins/rich-life/skills/rich-life/SKILL.md) on GitHub
2. Select all and copy the contents
3. Start a new conversation at [claude.ai](https://claude.ai)
4. Paste the skill content as your first message and send it

Claude will acknowledge the framework and immediately adopt the Rich Life persona. Then just describe your situation — something like:

> *"I make $5k/month, have $8k in credit card debt, and no investments yet. Where do I start?"*

It'll diagnose your situation, map out a Conscious Spending Plan, and give you a prioritized list of next steps — not a wall of disclaimers.

## Why Ramit Sethi's Framework?

Most personal finance advice is either too generic or too anxiety-inducing. Ramit's approach is different. It focuses on:

- **Big wins over small cuts** — Negotiating a raise or eliminating high-interest debt moves the needle far more than skipping lattes
- **Conscious spending** — You don't have to cut everything, just spend intentionally on what you actually value
- **Automation** — Build systems so good financial behavior happens without relying on willpower

This translates really well into an AI assistant context. The skill doesn't lecture; it helps you build a plan.

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

You describe your situation — income, debt, savings, what's stressing you out — and the skill takes it from there. It asks clarifying questions to fill in the gaps, then maps your numbers onto the Conscious Spending Plan and tells you exactly where to focus first.

If you're drowning in credit card debt, it won't tell you to max your Roth IRA. If you're leaving employer match on the table, that's the first thing it flags. The advice is sequenced to your actual situation, not a one-size-fits-all checklist.

The tone is direct and warm, not preachy. The goal is specific, actionable advice — not a disclaimer farm. The skill is open source — pull requests welcome.
