---
title: "Perplexity Computer: My Honest Review After Building 7 Real Projects"
date: 2026-04-09
draft: false
description: "I built my own AI system with 103 skills — then Perplexity Computer did it in one prompt. Honest review with real builds, real costs, and a framework for when to use what."
tags: ["perplexity", "ai-tools", "perplexity-computer", "ai-agents", "review"]
categories: ["AI"]
author: "NetworkChuck"
youtube_id: "G3jvn7n-68Y"
---

{{< youtube "G3jvn7n-68Y" >}}

## What You'll Learn

- What Perplexity Computer actually is and how it works under the hood
- How 19 frontier AI models get orchestrated automatically for each task
- What Firecracker micro VMs are and why they matter
- How to build self-improving apps with scheduled cron jobs
- The real credit costs — no sugarcoating
- When to use Perplexity Computer vs Claude Code vs building your own system

---

## Prerequisites

- A Perplexity Max subscription ($200/month) — required for Computer access
- A browser or the Perplexity mobile app
- Ideas. That's literally it. No terminal, no IDE, no local setup.

---

## The Confession: I Didn't Want to Like This

Look, I have to be honest with you. I've spent months building my own AI system. I'm talking about [Morpheus](https://youtu.be/MsQACpcuTkU) — my Personal AI Infrastructure inside Claude Code with 103 skills. I've got OpenClaw running AI employees. I use multiple models — Gemini, Codex, GPT — for different tasks. Image generation, video editing, research agents... I built all of it.

And then Perplexity drops Perplexity Computer. $200 a month. 19 AI models. Runs in the cloud while you sleep.

And it kind of does all of this... frustratingly well. Like, I didn't have to build a single tool to make it work. Which I don't like.

But here's what got me: I gave it to my wife Abbey — a heavy ChatGPT user, zero coding experience — and she started building things. She said, "Man, Perplexity is smart." And she meant it.

So let me walk you through everything I built, what it actually costs, and when you should (and shouldn't) use this thing.

---

## What Is Perplexity Computer?

Think of it this way: Perplexity's regular search is like raising your hand in class for a quick answer. Computer is like hiring a professor on a 40-hour-a-week retainer to deliver an entire body of work.

You don't ask it to perform tasks — you describe the outcome and it makes it happen.

Here's how it works under the hood:

### Step 1: The Orchestrator

When you submit a prompt, it goes to a meta router. This router picks an orchestrator model — usually Claude Opus 4.6 for heavy thinking. The orchestrator reads your prompt and figures out:

- What's your intent?
- Is this a one-shot task or a recurring/scheduled thing?
- How big is this project?
- What subtasks need to happen, and which can run in parallel?

It loads up relevant skills (website building, research assistant, code execution) and has access to 400+ OAuth connectors — Slack, Gmail, GitHub, Notion, Snowflake, Salesforce — with read AND write access.

### Step 2: Multi-Model Routing

This is where it gets interesting. For each subtask, the orchestrator picks the best model:

- **Claude Opus 4.6** — reasoning, orchestration, complex task decomposition
- **Gemini 3.1 Pro** — deep research, spawning its own sub-agents
- **GPT-5.2 / 5.4** — long-context recall, writing
- **Grok** — speed-sensitive lightweight tasks
- **Nano Banana Pro** — image generation
- **Veo 3.1** — video generation
- Plus 13 more specialized models

It's model agnostic. Not locked to any one company. Best model for the job gets the job.

### Step 3: Firecracker Micro VMs

Each subtask gets its own isolated compute environment. These are called Firecracker micro VMs — the same technology AWS uses for Lambda.

- **2 vCPU, 8GB RAM** per sandbox
- **Boot time: under 125 milliseconds**
- Pre-installed: Python, Node.js, ffmpeg, standard Unix tools
- Persistent filesystem via FUSE
- No direct internet access — all external calls go through a secure egress proxy

Sub-agents share a workspace filesystem. One agent writes a file, another reads it. That's how they coordinate.

### Step 4: It Keeps Working When You Leave

Close your browser. Close your laptop. Ride the metro. Tasks run in the cloud — not on your device, not in your browser session. Come back to results.

### Step 5: Memory Across Tasks

Computer uses a vector database for semantic recall. "Remember the arcade we built? Now add a new game" — it knows what you're talking about. Each chat is a new task context, but memory carries knowledge between tasks.

---

## Building a Blockbuster POS System — Live

I used to work at Blockbuster. Yes, I'm old. And one thing I miss was the POS (point of sale) system we used to rent videos. It was command line — my first experience with command line, actually.

So I asked Perplexity Computer to rebuild it. One prompt. No follow-ups.

<!-- Screenshot: Perplexity Computer prompt for Blockbuster POS system -->

The orchestrator loaded up skills, created a research plan, and launched Firecracker VMs. It found the actual Blockbuster CSR handbook online. It hit some roadblocks trying to access Reddit (Whoa there, partner), but figured it out.

About 14 minutes later — a fully working Blockbuster POS simulation. I could download the HTML or click to launch it as a shareable website.

<!-- Screenshot: Finished Blockbuster POS system running in browser -->

Fun fact: I went to the last Blockbuster in Oregon. They still use that same system. It runs off floppy drives.

---

## Self-Improving Apps That Run While You Sleep

Here's where it gets wild. I told Computer: "Every hour, improve one thing about this simulation. Make it better, make it more realistic."

And it just... did it. You can set up cron jobs and scheduled tasks. I've done this on a bunch of the things I built.

You could also do:
- "Check my email every five minutes"
- "Check the news every day and alert me if something crazy is going on"
- "Send me a Slack message when you're done"

All stuff I can do with what I've built. But Computer just did it. No tooling required. No messing around. No tweaking.

---

## Building a Gaming Website for My Kids

I hate when my kids play those dumb gaming websites. There's one game where it's just a big ball of poop. So new rule: you can only play games that I make or you make.

Now, this isn't my first time trying to build a gaming arcade for my kids. First attempt failed. Second attempt took me weeks — started with Gemini, moved to Codex, moved back to Claude. It looked okay, but it took forever.

With Computer? One prompt. It asked a few clarifying questions, then went to town.

<!-- Screenshot: Keith Arcade running with multiple games -->

Result: A full-stack retro arcade with sound effects, multiple original games (Pug Dash, Neon Racer, Exit 8), user accounts, leaderboards, and an admin panel. I even had it publish to a VPS — just gave it my login and it handled the deployment.

Then I set it to self-improve every hour (bumped to every four hours because my credit card was melting).

The games are live if you want to play — link in the description.

---

## Why My Ideas Started Pouring Out

After building several projects, I had to sit down and think about something. Why didn't I have all these ideas bubbling out of me with my other tools?

The answer hit me: **I spent all of my idea energy on creating those tools.** Sharpening my axe. With Perplexity Computer, there was no axe to sharpen. It was already there. All that was left was to be the idea person.

So my ideas started flowing. Konbini Quest (a Japanese convenience store RPG), a viral Content Radar, a gamified IT news site, an IT Job Market dashboard... 7 builds in one week.

That's the builder's trap. You love building the tools so much you never stop to use them.

---

## I Found a Cult in Japan

We're in Kyoto, Japan. Walking down the street. We pass this deli called the Yellow Deli. Great food, locations all over the world.

I got curious about how it started. Did a simple search in Perplexity and... dude, it's a cult. The Twelve Tribes.

But the regular search couldn't tell me anything about the Kyoto location. How it got started, who runs it — all dark.

So I pulled up Perplexity Computer on my phone, sitting in that deli, and asked it to investigate. I wanted a corkboard-style investigation dashboard.

<!-- Screenshot: Yellow Deli Files investigation dashboard -->

It deployed multiple research agents. And it found things about the Kyoto branch that I couldn't find with regular Perplexity — where their commune is, how it got there from Australia, the people who started it.

1,700 credits. Twenty minutes. That's what separates Computer from regular search tools — multi-agent research that goes deeper than any single-pass search can.

---

## How Much Does Perplexity Computer Actually Cost?

Time to get real. Perplexity gave me credits for this sponsorship. I didn't pay for everything I showed you. But let me show you what it actually cost.

- **Base plan:** $200/month gives you 10,000 credits
- **My usage:** Plan credits (10K) + 35K bonus from Perplexity + 37.5K I paid for = ~82,500 total credits
- **Keith Arcade alone** was 8,650 credits — almost your entire base monthly allotment
- **Yellow Deli research:** 1,700 credits
- **Konbini Quest:** Multiple thousand credits with the hourly self-improvement cron

You'll burn through 10K credits fast if you're having fun. That's the reality.

Perplexity is paying API prices for these models — Opus 4.6, Gemini, all of them. They're a middleman. They do amazing orchestration, but the pricing reflects it.

I hope they figure out how to get the price down. Because the product is genuinely good.

---

## Everything Else I Built

Quick showcase of the other projects:

- **Konbini Quest** — A Pokemon-style Japanese learning RPG for convenience stores. It auto-improves itself hourly.
- **IT Quest Daily** — Gamified IT news where every story becomes a playable battle. No two days are the same.
- **IT Job Market Pulse** — A dashboard tracking job market trends. Actually useful.
- **Komei Kitchen** — My daughter Millie built this. A rice cooking game that looks like Roblox. She couldn't stop using Computer.

Most of these are live — links in the description.

---

## My Honest Verdict

The thing I was most surprised about wasn't the software itself. It's that it revealed my problem: I need to stop playing with the AI tools and start using them.

**Perplexity Computer wins when:**
- You want zero-setup, no-terminal building
- Research-heavy multi-model tasks (Yellow Deli proved this)
- Fire-and-forget persistence (apps that keep running)
- Mobile-first building (same interface on phone and desktop)
- Non-technical users (my wife and kids proved this)

**Claude Code / your own system wins when:**
- Deep coding with live iteration
- Full local control and filesystem access
- Single-session focused work
- Cost efficiency at scale

**The honest answer:** I'm going to keep using both. I'll keep building Morpheus because I love it. But when I want to just make something — no tweaking, no configuring, just ideas to reality — I'm reaching for Computer. And I didn't think I'd say that.

If you're spending more time perfecting your tools than actually using them, Perplexity Computer might be the thing that sets you free.

---

## Resources & Links

- [Perplexity Computer](https://ntck.co/perplexity) — Try it yourself
- [Keith Arcade](https://keitharcade.networkchuck.video) — Play the games I built for my kids
- [Konbini Quest](https://konbiniquest.networkchuck.video) — Japanese convenience store RPG
- [Yellow Deli Files](https://yellowdelifiles.networkchuck.video) — The cult investigation dashboard
- [Blockbuster POS Simulator](https://blockbuster.networkchuck.video) — Recreated Blockbuster point-of-sale system
- [Perplexity Computer Launch Blog](https://www.perplexity.ai/hub/blog/computer)
- [NetworkChuck Academy](https://ntck.co/NCAcademy) — Learn networking, security, and more

---

## People Mentioned

- **Daniel Miessler** — AI/Security Researcher, creator of PAI (Personal AI Infrastructure) | [X/Twitter](https://x.com/DanielMiessler) | [YouTube](https://youtube.com/@DanielMiessler)

---

*This post is a companion guide to [the YouTube video](https://youtube.com/watch?v=G3jvn7n-68Y). Watch it for the full walkthrough with demos.*
