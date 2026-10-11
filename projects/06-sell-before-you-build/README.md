# Project 6: Sell Something Before You Build It

**Time:** about 90 minutes to 2 hours, plus whatever outreach you choose to do afterwards

**You need:** your AI coding agent ([see the setup guide](../../SETUP.md)), your `LEARNING_LOG.md` from Project 5, the hosting account you used in Project 2, and an idea (a rough one is fine). During the session you'll make a free Stripe account yourself. You shouldn't need a credit card, and no real money moves unless you later decide it should.

**You'll leave with:** a live one-page site for your own idea that takes a refundable deposit (tested with fake money), a plan for who sees it first and what result counts as a yes, and a working understanding of positioning, calls to action, pricing, unit economics, and outreach.

## What happens

This is the last project, and the AI steps back. You lead; it coaches. You'll:

1. Hear how a course sold $7,000 of seats before it existed, then choose an idea starting from what you already have.
2. Confirm your own permission mode and defend the choice.
3. Write down what "done" means twice: for the page, and for the test itself, including how many deposits count as a yes, before anyone sees it.
4. Work out a price and a back-of-envelope version of whether it's worth doing.
5. Set up a deposit button in Stripe's sandbox, where payments are pretend.
6. Write the build brief yourself, decide who builds it, and deploy it.
7. Find a problem the AI plants in your live site.
8. Check the page yourself, then have a skeptical "customer" agent tell you why they wouldn't pay, and decide which objections matter.
9. Plan your first 20 people, and decide whether to go live with real money.
10. Look back across all six projects in your learning log.

The page doesn't need to be pretty. The question this project keeps asking: does anyone want this, and how will you know?

## How to start

1. Make a new, empty folder somewhere on your computer. Name it after your idea, or `my-idea` if you don't have one yet.
2. Copy your `LEARNING_LOG.md` from your Project 5 folder into the new folder. (The AI asks for it if you forget.)
3. Open the new folder in your AI agent's app. In the Claude app, make sure you're on the **Code** tab, not Chat. (The [setup guide](../../SETUP.md) shows how.)
4. Check the settings next to where you type:
   - **Permission mode:** start in the mode you ended Project 5 in: **Auto** in Claude Code or **Approve for me** in Codex, with the sandbox on. The final choice is yours; be ready to explain why it fits a project that deploys a site and touches a payment account. Never pick Bypass permissions or Full access.
   - **Model and effort:** **Opus 5.5** at **Medium** effort in Claude Code; **GPT-6.1 Sol** at **Medium** in Codex.
5. Start a **new session** (a fresh conversation in your agent). Open [PROMPT.md](PROMPT.md), click the **Copy raw file** button (the two overlapping squares near the top right of the file), and paste it in as your first message.

**Yes, paste the whole file.** It's much longer than anything you'd normally type into an AI, on purpose: it's the full set of instructions that turns the AI into your teacher. Don't trim it.

**About what goes public.** A free GitHub Pages site needs a public repository. Before the first push, the AI lists every file that would be published and asks what to keep private (your hourly rate, learning log, outreach list).

**About money.** You create the Stripe account and type any details yourself; the AI never does. Everything in the session uses Stripe's sandbox and its published test card numbers. Going live with real deposits is your decision, made after the session, and needs your own identity and bank details. If you'd rather not handle money at all, the AI will set up an email signup instead.

## When you're done

That's the series. Keep your folders and your `LEARNING_LOG.md`. Then send your page to the people on your list, and hold yourself to the number you wrote down before you sent it.
