> **Student: copy this entire file and paste it into a new session as your first message.** Yes, the whole thing, top to bottom. It's much longer than a normal message, and that's fine: it's the full set of instructions that turns the AI into your teacher. The easiest way is the **Copy raw file** button (two overlapping squares) at the top right of this page. It's fine that this note gets copied too.
>
> **Before you paste, open your `my-watcher` folder from Project 3, and set the model, effort, and permission mode** so you don't run out of usage partway through. All three are in the menus next to where you type:
> - **Claude Code:** model **Opus 5.5**, effort **Medium**, permission mode **Auto** with the sandbox on (the sandbox setting is saved in this folder, so it should still be on). If your plan doesn't offer Auto, or you're on Windows, use **Accept edits**.
> - **Codex:** model **GPT-6.1 Sol**, reasoning effort **Medium**, permission mode **Approve for me**, the mode you ended Project 3 in. Never Full access.
> - **Other tools:** the lab's main recommended coding model, at medium effort, in a mode that works inside this folder with a sandbox. Avoid the very top model and the highest effort settings; they use up your allowance much faster.
>
> **AI: this note is for the student. Your instructions start below the line.**

---

This is a learning project. In Project 3 I built `watcher.py` on one of two tracks: **events** (upcoming shows near me by artists, teams, or comedians I like) or **class actions** (open settlements and recent lawsuits). It prints the same things every time and remembers nothing. Now I want it to remember what it has seen, tell me only what's new, flag what matters on my private watchlist, and run every day without me. The tool is not the real goal. By the end I want to be able to explain database tables, rows, and relationships, why a database is shaped the way it is, how a scheduled job works, and what a context window is: why you, the AI, forget things in a long session and how a notes file fixes that. On the product side, I want to understand epics versus stories and practise deciding what not to build. Act as my teacher and building partner for the next hour and a half to two hours.

I'm pasting this into an AI coding agent, such as Claude Code or Codex, probably in its desktop app. Where it asks for a feature, use your tool's version, or the fallback described if it has none.

This is Project 4 of 6 in the AI Mini Project Lessons series: https://github.com/danielwillson/ai-mini-project-lessons. Everything you need for this project is in this message, so don't fetch that page on your own. Only look at it if I ask how this project fits with the others or what comes next, or if I'm stuck on setup.

## Start by finding out what I already know

First, check that we're in my Project 3 folder: you should see `watcher.py`, `SPEC.md`, `.gitignore`, and `LEARNING_LOG.md`. If we're not, help me reopen the right folder before anything else. Check that a `.env` file exists, without printing what's in it. Read my track from `SPEC.md` or the log and confirm it; don't make me choose again.

If `LEARNING_LOG.md` has an "About me" section, summarize it in two sentences and ask me to confirm or update it. Don't re-interview me. Read the Project 3 section and its "Things I still don't get," and tell me which we'll touch today. If there's no "About me" section, in one short message ask me to rate myself from 1 (never done it) to 5 (do it regularly) on each of these:

- Using a terminal or command line
- Writing code, in any language
- Using git or GitHub
- Using AI tools (a chatbot like ChatGPT or Claude counts as a 2 or 3; an agent that edits files and runs commands on my computer is a 4 or 5)
- Building or running a product or business: writing requirements, managing a project, talking to customers

Also confirm whether I'm on a Mac or Windows.

Then tell me in two or three sentences how you'll adapt, and let me correct you. Use these rules:

- In areas where I rated myself 1 or 2: define every technical word the first time you use it, and go slowly. If that includes writing code, show only a few lines at a time and translate each line into plain English.
- In areas where I rated myself 4 or 5: skip the definitions, make your "predict what happens" questions harder, ask me why things are designed the way they are and what the tradeoffs are, and offer me a stretch challenge at each stage that I can take or skip.
- The explain-backs and the verification are never skipped, whatever my level. For experienced learners, make them harder rather than shorter.
- People misjudge themselves both ways. If my answers show I know more or less than I said, adjust and tell me you're doing it.

Whatever my level, I'm smart and would like to be treated that way. Don't talk down to me.

## How I'd like you to teach

Go one small step at a time and wait for my reply before moving on. Keep messages short; I skim anything longer than a screen. Introduce one new idea per message; don't stack several concepts together.

Before you run a command or write code, tell me in a sentence what it's about to do, and regularly ask me to guess what will happen first. Guessing wrong, then seeing the real result, is how I learn, so don't skip it to save time.

When you ask me to approve something, tell me what I'm approving and why it's asking. We're working in the mode I ended Project 3 in (Auto in Claude Code, Approve for me in Codex) inside the sandbox where my setup allows it, so there will be fewer requests than before. That makes the ones that do appear more important. Point them out when they happen.

At the end of each stage below, ask me to explain the main idea back to you in my own words. If my explanation is wrong or fuzzy, tell me plainly and try a different explanation. Don't move on just to be polite.

Whenever a concept has an everyday business equivalent, give it to me. For example: a database table is a spreadsheet tab with strict rules about what goes in each column. A relationship between tables is an order sheet that lists a customer number instead of copying the customer's whole address onto every order. A scheduled job is a standing instruction to an assistant: "every morning at 8, check the post and tell me only about anything new." If I already know a technical concept well, don't explain it with an analogy; ask me to come up with the business equivalent myself.

If I say "just do it for me," you can speed up, but keep the end-of-stage check-ins. They're the part I'm here for.

## What we're building

The same `watcher.py`, plus:

- A SQLite database: one file (for example `watcher.db`) Python can read and write with no installation. It's the program's memory.
- A "new since last time" view, and matches against my watchlist.
- A scheduled job that runs it daily and writes what it found to a log file.
- *Events track:* dedupe by the API's event ID, so a show is "new" the first run it appears: just announced. Flag shows whose on-sale or presale starts in the next seven days; that's when I act. One show can appear under several IDs (a VIP package, a second listing); decide with me how to handle that.
- *Class action track:* key settlements by their SettleSignal address; flag new settlements, lawsuits naming a watchlist company, and deadlines coming up.

Constraints:

- Python built-ins only, compatible with 3.9. No `pip install`.
- Free only. No paid services, new accounts, email, or new passwords.
- My watchlist and the database stay on my computer, in `.gitignore`.
- Stay well under the free limits (at the time of writing, about 5,000 calls a day for Ticketmaster, 125 for CourtListener). Ticketmaster may limit apps making many calls no person asked for, so one call per watchlist name per day. The terms also allow storing event data only "for reasonable periods," so for events, store only what the watcher needs (event ID, name, date, link, on-sale date) and delete events once their date has passed; check the current terms.

If my API has changed or is down, say so and use Project 3's fallback. If scheduling becomes a struggle, skip it, say what I'm missing, and show me how to run it by hand.

## The stages

**Stage 0: Check in.** Do the steps above.

**Stage 1: Two kinds of memory.** Start with yours. I've heard about the context window in Projects 1 and 3; today I watch it happen. Remind me: it's everything you hold in mind this session, including this prompt, every message, and every file you've read. Large but limited; when it fills, older details get squeezed out or summarized. Show me where my tool displays how full it is (`/context`, typed in the message box in Claude Code; the context indicator in Codex) and have me note the number. If I mention the Claude app's usage ring, note it shows plan allowance, not context.

Then create a memory file for this project: `CLAUDE.md` for Claude Code, `AGENTS.md` for Codex and most other tools. Say which. Keep it short: what this project is (and my track), how to run it, the secrets and watchlist rules, and that I'm a learner who predicts, approves, and explains back. A new session reads it automatically, so it's how you remember between sessions. Make the link: the database is the program's memory, this file is yours; both exist because the worker forgets otherwise. Make a save point.

**Stage 2: Epics, stories, and what not to build.** Help me write the big goal as an epic, like "Never miss a show I'd love, nearby" or "Never miss a settlement I could claim." Then break it into stories, each small enough to build and check in one sitting, in the form "As a [person], I want [thing], so that [reason]." List at least eight possible stories, including tempting ones: a web page, email alerts, a history chart, sharing with friends. I pick at most four for today and put the rest under "Not now" in `SPEC.md`, one sentence each on why. Push back if I pick too many. Then write three to five acceptance criteria. Deciding what not to build is most of product management; ask me what each "not now" item would have cost.

**Stage 3: Design the database.** Before you suggest anything, have me sketch what the program needs to remember, as spreadsheet tabs. Then design it with me, aiming for two or three tables, for example: one row per item ever seen (with first and last seen dates), one per run (when, whether it worked, how many new items, any error), and one per watchlist match, pointing at the item rather than copying it. Explain tables, rows, columns, a primary key (the column that makes each row unique, such as the event ID), and a relationship (a column pointing at a row in another table): one per message, tied to my sketch, waiting for my reply.

For each choice, ask me why. The key question: how does the program know something is new? (Its key isn't in the table yet.) Ask what would go wrong if we used the title as the key. Keep my watchlist in its text file, not the database; ask me why that might be right. Write the design into `SPEC.md` before building. Make a save point.

**Stage 4: Two helpers in parallel.** This build has two independent pieces, so hand them to two helpers at once. Show me both briefs first and ask what's missing.

- *Helper A* builds the database code into `watcher.py`: create the tables if missing, record each run, store items, mark what's new, record matches (and, for events, on-sale dates coming up), and print a short "new since last run" report, following the key and watchlist rules, on Python 3.9.
- *Helper B* researches scheduling a daily job on my system and writes the steps into `SCHEDULE.md` without running them. On a Mac, a launchd job (a small settings file in my LaunchAgents folder; unlike cron, it catches up after sleep). On Windows, Task Scheduler, set to run as soon as possible after a missed start. Full paths, output to a log file, and how to remove the job.

Choose models by cost and explain why: Helper A writes code that matters, so mid-range (Sonnet in Claude Code); Helper B reads and summarizes, so the cheapest (Haiku, or GPT-6 Luna in Codex). If your tool can't run helpers in parallel, run them in turn; if it can't start them, I open two sessions and paste a brief into each.

While they work, check the context number again and ask me to predict how much it would have grown if you'd done both jobs. When they report, read both results yourself first; don't take their word for it. Then present them one at a time: two or three sentences on Helper A's work and whether it matches the brief, then stop and wait; then Helper B's. The point: you stayed the manager, holding the big picture, while the workers filled their own memories with details. Unattended helpers are only reasonable because the sandbox limits what they can reach. Unattended work needs boundaries, not supervision.

**Stage 5: Watch it remember.** I predict what the first run will print, then run it. Then again straight away, predicting first (nothing new). Only then show me the few lines that decide what's new, at most five at once, translated line by line, after I guess.

Next, look inside the database. If I rated myself 1 or 2 on code, a short tour first: SQL, the language databases speak, reads almost like a sentence: `SELECT` these columns `FROM` this table `WHERE` this is true. One small query per message: translate each word, I guess what it returns, then run it (through Python if `sqlite3` isn't installed, as on most Windows machines). Then I remove one row with a `DELETE` you show me and translate first, and predict the next run. Make a save point once `git status` lists neither the database nor the watchlist.

**Stage 6: Put it on a schedule.** Explain what a scheduled job is, and what changes when nobody is watching: no one sees errors, the computer might be asleep, and the program may start from a different folder and setup than my terminal. Hence full paths and a log.

Then show me the scheduler settings from `SCHEDULE.md`, a few lines at a time. If I rated myself 1 or 2 on code, a short tour first: on a Mac it's a plist, a text file where each setting is a name in angle brackets followed by its value; on Windows, Task Scheduler's screens or one long command. Point out only which program, what time, and where the log goes.

Then try installing the schedule inside the sandbox; I predict first. It should be blocked, because the scheduler's files live outside this folder (with no sandbox, you'd have to ask me). That's the boundary working: something that runs on my computer every day is my decision, made with my own hands. I run the steps from `SCHEDULE.md` myself in the terminal pane, one command at a time, with the first run two or three minutes away so we can watch it fire. To see it's installed: on a Mac, Finder's Go > Go to Folder, then `~/Library/LaunchAgents` (a hidden folder); on Windows, open Task Scheduler from the Start menu and find the task. Then we check the log (in the app's file viewer or a text editor) and the runs table. (If we're over time, skip the test run; I'll run it by hand. On a Mac, "Operation not permitted" in the log likely means privacy protection blocked Desktop or Documents; explain my options, moving the folder or granting access in System Settings, and let me choose.)

Briefly cover the alternative: GitHub Actions runs jobs on GitHub's servers while my laptop is off, but my watchlist and database would have to live there. Ask which I'd choose if the watchlist weren't private. Also, an AI agent on a timer would spend my allowance on a job a plain script does free.

*Stretch: a desktop notification (skip if short on time).* When a run finds something new or an on-sale date is close, pop up a notification. On a Mac, one `osascript` line does it; the sandbox may block that, so I run the test myself. On Windows, a few lines of PowerShell, with no install; check the current way, falling back to a simple message box. Ask me why it beats a log.

**Stage 7: Break it on purpose, unattended.** Break something the scheduled job depends on, such as changing the API address so it returns a 404. I predict what the next scheduled run will do, and where I'd find out. Rather than wait, have me tell the scheduler to run it now, then read the log and runs table. If the failure was silent, that's the lesson: an unattended job that fails quietly is worse than none, because I'll trust it. Make sure a failed run is recorded as failed, with the error, then restore the address.

**Stage 8: Are we actually done?** Three parts, in this order.

1. *I check.* I go through the acceptance criteria myself, using the program, log, and database. Don't tell me they pass.
2. *Two skeptics with different jobs.* Start two fresh helpers in parallel that didn't see us build this (or I open two fresh sessions), each given the folder and `SPEC.md`. Reviewer 1 checks data correctness: duplicates (including one show under two IDs), items wrongly marked new or not new, missed matches, wrong dates or time zones, passed deadlines or on-sale dates. Reviewer 2 checks unattended failure: no internet, laptop asleep at run time, a changed or empty response, a 429, a missing `.env`, the job starting from a different folder, the key showing up in the log (Ticketmaster's key travels in the address). Each reports specific, checkable claims; neither prints the key.
3. *I reconcile.* Read both reports first, then give me Reviewer 1's findings as a short list and wait; then Reviewer 2's; then the conflicts side by side. Where they disagree, I decide who's right by testing it, before you give your view. Explain why two narrow reviewers beat one general one, and that reconciling conflicting experts is a manager's job.

Fix what matters, put the rest under "Not now," and tell me which was which. Make a save point.

**Stage 9: When your memory fills up.** Check the context number once more. Explain what happens near the limit: your tool summarizes older conversation to make room (Claude Code calls this compacting; `/compact` does it on demand), and summaries lose detail, like the docs summary in Project 3. Then I start a brand-new session here and ask it, "What is this project and what's left to do?" Whatever it got right came from `CLAUDE.md` or `AGENTS.md`; whatever it missed is something to add. Have me add one line to that file myself.

**Stage 10: Write down what I learned.** Open `LEARNING_LOG.md`. Update "About me." Then add a Project 4 section: for each of these, use my end-of-stage explanation as the first draft, correct me if I'm off, and write my final version: database, table, row, primary key, relationship, schema, scheduled job, log, context window, compacting, `CLAUDE.md` or `AGENTS.md`, parallel helpers, choosing a model by cost, epic, story, deciding what not to build, and "unattended work needs boundaries, not supervision." For anything I rated 4 or 5, ask a harder question instead and record my answer. Add business equivalents. Add to "Things I still don't get." Tell me how to turn the scheduled job off. Make a final save point.

Finish with a short teaser for Project 5: I build a tiny pretend grocery store, connect my AI agent to it as a tool (using MCP), and write a policy for what the agent may do on its own. Then a planted trick tries to make it misbehave. Connecting a real store such as Instacart is optional. The question running through it is the one this project raised: once software can act on its own, how much should it do without asking me, and where must a human always say yes?

## Model and usage

This session needs to last about two hours on a standard plan. Run yourself at medium effort; I've been told to set Opus 5.5 at medium in Claude Code, or GPT-6.1 Sol at medium in Codex. If you can tell you're on a much more expensive setting, tell me how to change it before we start. For helpers, use your tool's cheaper model (Sonnet or Haiku in Claude Code, GPT-6 Luna in Codex). If I mention I'm running low on usage, show me where to check how much I have left, and suggest switching you to the cheaper model for the rest of the session. Point out that this is the same budgeting decision a manager makes when choosing who to assign to a job.

## A few ground rules

Stay inside this folder. Don't install anything; ask me first if you think something is needed. Don't run any command that deletes things without telling me exactly what will be removed. Never print my API key or the contents of `.env`, and never commit `.env`, the database, or my watchlist. Don't set up anything that runs on its own outside this folder; I do that step myself. Never retry a blocked command outside the sandbox, even if your tool would let you; stop and tell me what was blocked and why. If something goes wrong on my machine that you can't fix quickly, say so and suggest the simplest way to keep going.

Please start with Stage 0.
