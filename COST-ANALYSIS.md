# AI Coding Tool Cost Breakdown: Subscriptions vs API Pricing

**The real numbers nobody talks about.** Every AI coding tool you use is being subsidized. The subscription price you pay is a fraction of what it actually costs to run. Here's the breakdown.

---

## The Three Tools Compared

### Claude Code (Anthropic)

| Plan | Monthly Price | What You Get |
|------|-------------|--------------|
| Pro | $20/mo | Sonnet 4.6 + Opus 4.6, ~45 msgs/5hr window |
| Max 5x | $100/mo | 5x Pro limits (~225 msgs/5hr) |
| Max 20x | $200/mo | 20x Pro limits (~900 msgs/5hr) |

**What it actually costs at API rates:**

| Model | Input (per 1M tokens) | Output (per 1M tokens) |
|-------|----------------------|----------------------|
| Opus 4.6 | $5.00 | $25.00 |
| Sonnet 4.6 | $3.00 | $15.00 |
| Haiku 4.5 | $1.00 | $5.00 |

**The subsidy:** Anthropic says the average Claude Code developer uses ~$6/day in API-equivalent costs. That's ~$180/month. On the $20 Pro plan, you're getting a 9x discount. Heavy users on Max ($200/mo) can consume $3,650+/month in API-equivalent usage -- an 18x subsidy. One tracked user consumed 10 billion tokens over 8 months. API cost: ~$15,000. Subscription cost: ~$800. That's a 95% discount.

---

### Codex CLI (OpenAI)

| Plan | Monthly Price | What You Get |
|------|-------------|--------------|
| Plus | $20/mo | 30-150 Codex msgs/5hr, GPT-5.2 |
| Pro | $200/mo | 300-1,500 Codex msgs/5hr, o1 Pro mode |

**What it actually costs at API rates:**

| Model | Input (per 1M tokens) | Output (per 1M tokens) |
|-------|----------------------|----------------------|
| GPT-4.1 | $2.00 | $8.00 |
| o3 | $2.00 | $8.00 |
| o4-mini | $1.10 | $4.40 |
| codex-mini | $1.50 | $6.00 |

**The subsidy:** OpenAI's CEO Sam Altman publicly admitted they lose money on $200/month Pro subscribers. OpenAI spent $8.67 billion on inference in just 9 months of 2025. They project $14 billion in losses for 2026. Worth noting: OpenAI claims Codex is roughly 4x more token-efficient than Claude Code per task, meaning the same coding job costs ~$15 on Codex vs ~$155 on Claude Code at API rates.

---

### Gemini / Jules (Google)

| Plan | Monthly Price | What You Get |
|------|-------------|--------------|
| Free | $0 | Jules: 15 tasks/day, Gemini CLI, Flash models |
| AI Plus | $7.99/mo | Gemini 3 Pro, 30 prompts/day |
| AI Pro | $19.99/mo | Jules: 100 tasks/day, 1M context, $10 Cloud credits |
| AI Ultra | $249.99/mo | Jules: 300 tasks/day, Deep Think, $100 Cloud credits |

**What it actually costs at API rates:**

| Model | Input (per 1M tokens) | Output (per 1M tokens) |
|-------|----------------------|----------------------|
| Gemini 2.5 Pro | $1.25 | $10.00 |
| Gemini 2.5 Flash | $0.30 | $2.50 |
| Gemini 2.0 Flash | $0.15 | $0.60 |

**The subsidy:** Google's API prices are already the cheapest of the three. Gemini 2.5 Flash at $0.30/$2.50 is 10x cheaper than Claude Sonnet and 5x cheaper than GPT-4.1 for input tokens. Google can afford this because they cross-subsidize with $175B+ in annual ad revenue. They own the TPU infrastructure. For them, AI is a cost of keeping you in the Google ecosystem, not a standalone business that needs to be profitable.

---

## The Side-by-Side: What a Heavy Coding Day Actually Costs

**Scenario: 8-hour coding day, ~2M input tokens, ~500K output tokens (typical heavy session)**

| Tool | Subscription Cost | API-Equivalent Cost | You Save |
|------|------------------|--------------------|---------| 
| **Claude Code (Opus)** | $6.67/day ($200/mo) | $22.50/day | 70% |
| **Claude Code (Sonnet)** | $6.67/day ($200/mo) | $13.50/day | 51% |
| **Codex (GPT-4.1)** | $6.67/day ($200/mo) | $8.00/day | 17% |
| **Codex (o3)** | $6.67/day ($200/mo) | $8.00/day | 17% |
| **Gemini (2.5 Pro)** | $0.67/day ($19.99/mo) | $7.50/day | 91% |
| **Gemini (2.5 Flash)** | $0.67/day ($19.99/mo) | $1.85/day | 64% |

**At power-user levels (~5M input, ~2M output tokens/day):**

| Tool | Subscription Cost | API-Equivalent Cost | You Save |
|------|------------------|--------------------|---------| 
| **Claude Code (Opus)** | $6.67/day | $75.00/day | 91% |
| **Claude Code (Sonnet)** | $6.67/day | $45.00/day | 85% |
| **Codex (GPT-4.1)** | $6.67/day | $26.00/day | 74% |
| **Gemini (2.5 Pro)** | $0.67/day | $26.25/day | 97% |

---

## Where Perplexity Computer Fits

Perplexity Computer costs $200/month with 10,000 credits included. Here's the thing nobody tells you: Perplexity is a middleman. They're paying API prices to Anthropic, OpenAI, and Google for every model they use.

When Computer orchestrates a task using Claude Opus for reasoning, Gemini for research, and GPT-5.2 for writing -- Perplexity pays each provider's API rates. They're eating those costs and giving you a flat monthly price.

**My actual usage:** ~82,500 credits total (10K plan + 35K bonus + 37.5K purchased). A simple task costs ~30-60 credits. A complex build can burn 5,000-20,000+ credits. One user reported a single 40-minute task eating 15,000 credits -- 150% of the entire monthly allocation.

**The catch:** There's no published per-credit cost, no way to estimate cost before running a task, and failed runs still drain credits. You find out what it cost after it's done.

---

## The Big Picture: Why Is Everything So Cheap?

Every AI company is subsidizing you right now. Here's why:

| Company | 2026 Revenue | 2026 Projected Loss | Break-Even Target |
|---------|-------------|--------------------|--------------------|
| OpenAI | ~$12.7B | ~$14B | 2030 |
| Anthropic | ~$30B | Investing $19B in training+infra | 2027 |
| Google | $350B+ (Alphabet) | AI costs absorbed | Already profitable |

**This is the Amazon Web Services playbook.** Price below cost to capture the market. Once everyone depends on your tools and switching costs are high, raise prices. Amazon did this from 2006-2012 and it worked.

Signs it's already happening:
- Anthropic added weekly usage caps and extra-usage billing at API rates
- Cursor replaced unlimited requests with credit-based pricing
- OpenAI launched the $200/mo Pro tier to shift heavy users up
- Google removed Pro models from the free API tier in April 2026

**The honest truth:** The $20-$200/month you pay today is artificially low. These companies are burning billions to get you hooked. Enjoy the ride, but know the prices will go up.

---

## Quick Reference: API Prices Across All Providers

| Model | Input/1M | Output/1M | Cache Discount | Batch Discount |
|-------|---------|----------|----------------|----------------|
| **Anthropic** | | | 90% on reads | 50% off |
| Opus 4.6 | $5.00 | $25.00 | $0.50 cached | $2.50/$12.50 |
| Sonnet 4.6 | $3.00 | $15.00 | $0.30 cached | $1.50/$7.50 |
| Haiku 4.5 | $1.00 | $5.00 | $0.10 cached | $0.50/$2.50 |
| **OpenAI** | | | 75% on reads | 50% off |
| GPT-4.1 | $2.00 | $8.00 | $0.50 cached | $1.00/$4.00 |
| o3 | $2.00 | $8.00 | $0.50 cached | $1.00/$4.00 |
| o4-mini | $1.10 | $4.40 | $0.275 cached | $0.55/$2.20 |
| **Google** | | | 90% on reads | 50% off |
| Gemini 2.5 Pro | $1.25 | $10.00 | $0.13 cached | $0.625/$5.00 |
| Gemini 2.5 Flash | $0.30 | $2.50 | $0.03 cached | $0.15/$1.25 |
| Gemini 2.0 Flash | $0.15 | $0.60 | -- | $0.075/$0.30 |

---

*All prices current as of April 2026. Prices change frequently -- check provider pricing pages for the latest.*

*Sources: Anthropic API docs, OpenAI API pricing page, Google AI Developer docs, The Register, Forbes, Martin Alderson's analysis, multiple third-party pricing aggregators.*
