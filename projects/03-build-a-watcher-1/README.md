# Project 3: Build a Watcher, Part 1

**Time:** about 90 minutes to 2 hours

**You need:** an AI coding agent such as Claude Code or Codex ([setup guide](../../SETUP.md)), your `LEARNING_LOG.md` from Project 2 (it's still in your `my-game` folder), and an email address for a free API account, which you'll make yourself during the lesson. On Windows, you may also need to install Python; the AI walks you through it.

**You'll leave with:** a small program that watches a public data source for things you care about, and a working understanding of APIs, requests and responses, status codes, JSON, API keys, keeping secrets out of git, reading documentation, and scoping a first version, plus the names teams use for them.

## Pick what to watch

At the start, you choose one of two versions. Both teach exactly the same things.

- **Events watcher (suggested if you're unsure).** You list artists, teams, or comedians you like, plus your home area (say, Charlottesville, Richmond, or DC) and how far you'd travel. The watcher finds their upcoming shows nearby and shows when tickets go on sale, including presales, so you hear about them early. It uses the [Ticketmaster Discovery API](https://developer.ticketmaster.com/) (free key).
- **Class action watcher.** You list companies you buy from. The watcher finds class action settlements you might be able to claim, and new lawsuits against those companies. It uses [SettleSignal](https://settlesignal.com/)'s public settlement list (no key needed) and [CourtListener](https://www.courtlistener.com/)'s court records API, run by the nonprofit Free Law Project (free key).

If a source is unavailable, the AI uses a named backup.

## What happens

The AI starts by reading your learning log so it can pick up where Project 2 left off. Then you'll:

1. Choose your track and write your private watchlist.
2. Look at a real API response in your own web browser and learn to read it.
3. Send a subagent (a second AI agent the main one starts) to read a long set of documentation, then check what its summary left out.
4. Cut your idea down to a first version (an MVP, minimum viable product) and write its acceptance criteria: what "done" means.
5. Set up your git repo so your secrets can't end up in a commit.
6. Turn on the sandbox, see what it blocks, and move to auto mode.
7. Get your own API key and paste it into a hidden settings file yourself. The AI walks you through it, step by step for Mac or Windows.
8. Build the watcher, run it yourself, then read its Python one small piece at a time. Then break it on purpose with a wrong key.
9. Check it yourself, then have a reviewer agent hunt for any way your key could leak.
10. Write down what you learned, in your own words.

## How to start

1. Make a new, empty folder next to your `my-game` folder. Name it `my-watcher`.
2. Copy `LEARNING_LOG.md` from your `my-game` folder into the new folder.
3. Open the new folder in your AI agent's app. In the Claude app, make sure you're on the **Code** tab, not Chat. (The [setup guide](../../SETUP.md) shows how.)
4. Check the settings next to where you type:
   - **Permission mode:** **Accept edits** in Claude Code, **Ask for approval** in Codex. The lesson changes this partway through, to **Auto** in Claude Code and **Approve for me** in Codex.
   - **Model and effort:** **Opus 5.5** at **Medium** effort in Claude Code; **GPT-6.1 Sol** at **Medium** in Codex.
5. Start a **new session**. Open [PROMPT.md](PROMPT.md), click the **Copy raw file** button (the two overlapping squares near the top right of the file), and paste it in as your first message.

**Yes, paste the whole file.** It's a few pages long, and that's on purpose. It's the full set of instructions that turns the AI into your teacher. Don't trim it or summarize it.

**One rule to know before you start:** you create your API account and copy your key yourself. The AI should never type a password or your key for you. If it offers to, say no.

## When you're done

Keep your `my-watcher` folder, including your `.env` file. Project 4 continues in the same folder: the watcher gets a memory and a daily schedule.
