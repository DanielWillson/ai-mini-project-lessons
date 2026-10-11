# Project 2: Put It Online

**Time:** about 90 minutes to 2 hours, plus waiting for your players to reply. You can split it into two sittings.

**You need:** your `my-game` folder from [Project 1](../01-make-a-game/), an email address for a free GitHub account, and five people you can send a link to. A phone helps for testing. No credit card.

**You'll leave with:** your game live on the internet at a link anyone can open, real feedback from real players, one improvement built from that feedback, and a working understanding of local versus cloud, servers, URLs and domains, deploying to production, GitHub, user stories, backlogs and kanban boards (the same tools product teams use in Jira or Linear), writing a prompt for an AI agent, and checking the live version rather than your own copy.

## What happens

The AI starts by reading your Project 1 learning log, so it doesn't interview you again. Then you'll:

1. Learn what "local" and "the cloud" mean, and what a server, URL, and domain are.
2. Make a GitHub account (you do this yourself) and put your project on it.
3. Deploy: turn on hosting and get a real link to your game.
4. Break it on purpose: get your upload rejected and work out why.
5. Send the link to five people and ask them good questions. If nobody's around, you pause here and come back when they've replied.
6. Turn their feedback into user stories and put them on a simple board.
7. Write the prompt yourself for a subagent (a separate AI agent) to build one of those stories.
8. Check the change on the live site, then have a reviewer agent check it too.
9. Write down what you learned, in your own words.

Everything in your project becomes public on GitHub, including your learning log. The AI will show you exactly what's about to be shared and ask first.

## How to start

1. Find your `my-game` folder from Project 1. Don't make a new one: this project uses the game, `SPEC.md`, commit history, and `LEARNING_LOG.md` already in it.
2. Open that folder in your AI agent's app. In the Claude app, make sure you're on the **Code** tab, not Chat. (The [setup guide](../../SETUP.md) shows how.)
3. Check the settings next to where you type:
   - **Permission mode:** one step up from Project 1. Use the mode that changes files in your folder without asking but still asks before running commands. That's **Accept edits** in Claude Code. In Codex, stay on **Ask for approval**, which already works this way. The AI explains what changed.
   - **Model and effort:** **Opus 5.5** at **Medium** effort in Claude Code; **GPT-6.1 Sol** at **Medium** in Codex.
4. Start a **new session** (a fresh conversation in your agent). Open [PROMPT.md](PROMPT.md), click the **Copy raw file** button (the two overlapping squares near the top right of the file), and paste it in as your first message.

**Yes, paste the whole file.** It's long on purpose: it's the full set of instructions that turns the AI into your teacher. Don't trim it.

**Coming back after waiting for feedback?** Open the same folder, start a new session, and paste the whole file again. The AI finds the `NEXT_STEPS.md` note it left and carries on from there.

## When you're done

Keep your `my-game` folder and GitHub account. You'll use GitHub again, and your `LEARNING_LOG.md` helps the next project pick up where this one left off.
