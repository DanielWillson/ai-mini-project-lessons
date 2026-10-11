# AI Mini Project Lessons

**The AI does the building. You learn to run the show.**

A short series of prompts that turn an AI coding agent, such as Claude Code or Codex, into a patient teacher. You make something real, and the AI teaches you how it works as you go. No coding experience needed.

---

## What this is

AI tools can now build working software from a plain-English request. That means almost anyone can make things, not that they'll be good at it. The people who get the most out of these tools understand what's happening underneath, can tell whether the result is right, and know how to turn an idea into something people use.

Each project here is a single prompt you paste into an **AI coding agent**: an AI tool that can read files, run commands, and build things on your computer. Claude Code and OpenAI's Codex are examples; the prompts work in any of them. It sets up a small, real project and makes the AI your teacher as well as your builder. It goes one step at a time, asks you to guess before it runs anything, stops so you can explain ideas in your own words, and breaks something on purpose so you learn to read an error. Every technical idea is paired with a business one.

The goal isn't to make you an engineer. It's to make you someone who can direct AI with judgment, check its work, and turn an idea into something real.

## Who it's for

Anyone curious about how software and the companies that make it work. It was written for university entrepreneurship students, but doesn't assume you're a student, a coder, or a "tech person."

**Already know some of this?** Good. Every project starts with a few quick questions about your experience with the terminal, code, git, AI tools, and running projects. The AI skips what you know, asks harder questions, and offers stretch challenges.

## How it works

1. **Set up once.** Follow [Project 0: Get Set Up](SETUP.md) to install an AI coding agent's desktop app. This is the only part without an AI guide; if you get stuck, the page explains how to get help from any AI chat.
2. **Make or open the folder** the project names. Some projects start fresh; others continue in the previous project's folder.
3. **Paste the prompt** into your AI agent.
4. **Answer a few questions** so the AI knows where you're starting from.
5. **Build, guess, explain, verify.** The AI leads you through it in stages.

Each project takes about 90 minutes to 2 hours and leaves you with a `LEARNING_LOG.md` written in your own words. The next project reads it, so you don't start from scratch.

## The projects

| # | Project | You'll learn | Status |
|---|---|---|---|
| 0 | [Get set up](SETUP.md) | Installing an AI coding agent, opening a terminal | Ready |
| 1 | [Make a game](projects/01-make-a-game/) | Terminal, files, if statements, loops, git and commits, acceptance criteria, delegating to subagents, adversarial review | Ready |
| 2 | [Put it online](projects/02-put-it-online/) | Your computer vs. the cloud, deploying, domains, GitHub, turning user feedback into a plan | Ready |
| 3 | [Build a watcher, part 1](projects/03-build-a-watcher-1/) (concerts or class actions) | APIs, JSON, API keys, keeping secrets safe, reading docs, turning on the sandbox | Ready |
| 4 | [Build a watcher, part 2](projects/04-build-a-watcher-2/) | Databases, "what's new" alerts, scheduled jobs, context windows and AI memory, running a team of AI agents | Ready |
| 5 | [Grocery cart over MCP](projects/05-grocery-cart-mcp/) | A real Instacart cart for your week of meals. How agents connect to tools (MCP), signing in with OAuth, permissions, prompt injection, when a human must approve | Ready |
| 6 | [Sell something before you build it](projects/06-sell-before-you-build/) | Landing pages, pricing, marketing, sales, unit economics | Ready |

Do them in order. Each one builds on the last.

## Three ideas that run through everything

### 1. Check the work. Then have someone else check it.

Whoever built something is the worst person to check it, because they check what they *meant* to build. AI has the same problem: ask an agent "did that work?" and it will usually say yes.

So in every project, **you** verify the result against **acceptance criteria** you wrote before building started. The AI is told not to declare the work finished. Then a second AI agent, one that didn't see the build, gets the explicit job of finding what's wrong. This is called **adversarial verification**. Some of its findings will be real and some won't, so you check those too.

Businesses do this all the time: auditors are separate from accountants, testers are separate from developers, and big payments need a second signature.

### 2. Be the manager, not just the worker.

An AI agent has a limited working memory, called its **context window**. If one agent does every task itself, its memory fills with details and it loses the big picture, like a manager who does all the work personally.

The better pattern is **orchestration**: one agent stays in charge, writes clear briefs, hands the building to **subagents** (often faster, cheaper models), and checks what comes back. You'll see this from Project 1 onward, and learn when it's worth it and when it's faster to just do the job yourself.

Writing a good brief for a subagent is the same skill as writing a good ticket for a human team, or a good prompt.

### 3. Decide what your agent is allowed to do on its own.

AI agents have **permission modes**, ranging from "ask me before every action" to "go ahead on your own." You'll start in a mode where the agent asks before running anything, so you learn to read what it wants to do and why.

The goal is to graduate to letting the agent work on its own inside a **sandbox**: a boundary enforced by your computer itself that limits which files and websites the agent can reach. That sounds riskier, but it's arguably safer. People who approve every request by hand stop reading by the fiftieth and just click yes. A sandbox doesn't get tired, and it limits the damage if the agent errs or is tricked by something it reads.

It's like a new employee. In their first week, their manager reviews every expense. Later, they get a company card with a spending limit, and the limit is what makes it safe to stop checking every receipt.

## Questions people ask

**Will using AI like this make me dumber?**
It can, if you let it do your thinking. These projects are built the other way around. You predict before anything runs, you explain ideas back in your own words, you read errors yourself, and you're the one who decides whether the work is done. The AI is told to keep those check-ins even if you ask it to skip them.

**Why all the jargon?**
You'll learn the words real teams use: commit, repo, deploy, acceptance criteria, user story, backlog, MVP, API, unit economics. Each one starts in plain English, then gets its real name. Most of these aren't AI words at all. Product managers, engineers, designers, and testers have used them for decades, in tickets, meetings, and job postings. Knowing them makes you useful on a team from your first day, and they're also the clearest way to tell an AI what you want.

**Do I need to know how to code?**
No. You'll read some code and change a little by hand, but the point is understanding, not syntax.

**What does it cost?**
The projects use free tools wherever possible. The AI agent is the one real cost: most need a paid plan, usually about $20 a month, though some have free tiers or student offers. See [the setup guide](SETUP.md) for options.

**What if I break something?**
You will, on purpose, in every project. Each project stays inside its own folder, and from Project 1 on you'll use git commits (save points) so you can always go back. Early on, your agent asks permission before running commands or changing files; read those requests before saying yes. Later it works inside a sandbox your computer enforces.

**Mac or Windows?**
Either. The AI asks which you're using and adjusts its instructions.

**Which AI tool do I need?**
Any major AI coding agent that works in a folder on your computer and can run commands: Claude Code, Codex, Cursor, and similar tools, used through their desktop apps. A regular chatbot website won't work: it can't create files or run anything on your machine. Some lessons use subagents; if your tool can't start one, the prompt has you open a second session instead.

## Recommended listening and reading

Optional, but worth your time if you want to go deeper.

### Articles

*Coming soon.*

### Videos

*Coming soon.*

### Podcasts

*Coming soon.*

## Who made this

Daniel Willson and Andy Page, as the take-home for their guest lecture on building with AI in UVA entrepreneurship courses.

Feedback is welcome. If something confused you, broke, or took far longer than it should have, please [open an issue](../../issues).
