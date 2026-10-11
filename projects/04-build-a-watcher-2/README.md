# Project 4: Build a Watcher, Part 2

**Time:** about 90 minutes to 2 hours

**You need:** an AI coding agent such as Claude Code or Codex ([setup guide](../../SETUP.md)), and your `my-watcher` folder from Project 3, with its `.env` file and `LEARNING_LOG.md`. No new accounts. You keep the track you chose in Project 3 (events or class actions).

**You'll leave with:** a watcher that remembers what it has seen, tells you only what's new (a show just announced near you, or a new settlement), flags what matters on your private watchlist (such as tickets going on sale this week), and runs every day on its own. Plus a working understanding of databases, scheduled jobs, context windows and AI memory, running several AI agents at once (subagents), epics versus stories, and deciding what not to build.

## What happens

The AI reads your learning log and checks your Project 3 folder. Then you'll:

1. See how much the AI can hold in mind at once, and give it a memory file.
2. Turn a big goal into small stories, and choose what not to build.
3. Design a small database before anything gets built.
4. Watch two agents build and research at the same time, on models picked by cost.
5. Run the watcher twice and see it remember.
6. Put it on a daily schedule, a step you do with your own hands. If there's time, add a free desktop notification.
7. Break it on purpose while nobody is watching, and find out where the error went.
8. Check it yourself, then have two reviewers with different jobs look for problems, and settle their disagreements.
9. Start a fresh AI session and see what it remembers.
10. Write down what you learned.

Your watchlist and the database stay on your computer. They're never committed to git.

## How to start

1. Open your `my-watcher` folder from Project 3 in your AI agent's app. In the Claude app, make sure you're on the **Code** tab, not Chat.
2. Check the settings next to where you type:
   - **Permission mode:** the one you ended Project 3 in: **Auto** in Claude Code if your plan offers it, with the sandbox still on from Project 3 (type `/sandbox` to check). If not, **Accept edits**. On Windows with Claude Code, use **Accept edits**. In Codex, use **Approve for me**.
   - **Model and effort:** **Opus 5.5** at **Medium** effort in Claude Code; **GPT-6.1 Sol** at **Medium** in Codex.
3. Start a **new session**. Open [PROMPT.md](PROMPT.md), click the **Copy raw file** button (the two overlapping squares near the top right of the file), and paste it in as your first message.

**Yes, paste the whole file.** It's a few pages long, and that's on purpose. Don't trim it or summarize it.

## When you're done

The watcher will keep running once a day. The AI shows you how to turn it off at the end, if you'd rather it didn't. Keep your `LEARNING_LOG.md`; Project 5 starts from it.
