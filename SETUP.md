# Project 0: Get Set Up

**Time:** about 15 to 30 minutes

**You'll leave with:** an AI coding agent installed, signed in, and open in a folder you made.

This is the only part without an AI teacher, because you haven't set one up yet. It's also where most people stall.

> **Stuck?** Copy the link to this page, paste it into any AI chat you like (ChatGPT, Claude, Gemini, and so on), and tell it where you're stuck. Include any error message you see, word for word. It can walk you through the rest.

## 1. Pick an AI coding agent

An **AI coding agent** is an AI that works inside a folder on your computer: it can read and write files and run commands, with your permission. A regular chat can't, so you need one of these. The projects work with any major one. These two have the simplest desktop apps:

| Agent | Made by | What you need (as of October 2026) |
|---|---|---|
| **Claude Code**, in the Claude app | Anthropic | A paid Claude plan. Pro is about $20/month. The free plan doesn't include it. [Pricing](https://claude.com/pricing) |
| **Codex**, in the ChatGPT app | OpenAI | A ChatGPT account. Codex is included on every plan, but the free plan's limits are tight; Plus (about $20/month) is the safe choice. [Pricing](https://learn.chatgpt.com/docs/pricing) |

Other agents, such as Cursor or GitHub Copilot, work too. Follow their own setup guide, then skip to step 4.

**Not sure which one?** If you already pay for ChatGPT, use Codex. If you already pay for Claude, use Claude Code. If you pay for neither and you're a student, Codex with the student credits below is the cheapest way in.

### Student discounts

Checked in October 2026. Offers change often and several have deadlines, so read the details page before signing up. Most verify you're a student through SheerID, using your university email.

| Provider | Offer for students | Details |
|---|---|---|
| **OpenAI (Codex)** | About $100 of free Codex usage, good for 12 months, on any ChatGPT plan, including the free one. For students at US and Canadian universities. Separately, US college students have been offered 4 free months of ChatGPT Plus, reportedly until October 31, 2026; it needs a card and renews at $20/month unless you cancel. | [Codex for Students](https://chatgpt.com/codex/students/) |
| **Anthropic (Claude Code)** | No individual student discount right now. Some universities get Claude through a school-wide deal, and Anthropic's campus program gives student club leaders API credits for their members. | [Claude for Education](https://www.anthropic.com/news/introducing-claude-for-education), [Claude Campus program](https://claude.com/programs/campus) |
| **Google** | A free year of Google AI Pro for US college students aged 18 and up, if you sign up by December 31, 2026. It needs a card and renews at $19.99/month unless you cancel. Google's coding agent is called Antigravity and has its own desktop app; it isn't covered step by step in this guide. | [Gemini for Students](https://gemini.google/students/) |
| **GitHub (Copilot)** | A free Copilot Student plan through GitHub Education. You can't choose which AI model it uses, and new sign-ups have been paused at times. | [GitHub Education](https://github.com/education/students) |
| **Cursor** | The free year for students closed to new sign-ups in June 2026. Cursor still hands out credits at campus events. | [Cursor for Students](https://cursor.com/students) |

If an offer renews into a paid plan, set a calendar reminder to cancel first, unless you want to keep it. Also ask your instructor or school IT whether your university provides any of these tools.

## 2. Install the app and sign in

### Claude Code

1. Download the Claude app for Mac or Windows from the [Claude Code desktop guide](https://code.claude.com/docs/en/desktop-quickstart), install it, and sign in.
2. **Click the Code tab** at the top of the window. This is the important part. The app opens on **Chat**, a regular chatbot that can't touch your files; **Code** is Claude Code. (There's also a **Cowork** tab. You don't need it for these projects.)

### Codex

1. Download the ChatGPT desktop app for Mac or Windows from [chatgpt.com/download](https://chatgpt.com/download), install it, and sign in.
2. Choose **Codex**. The app also has a regular chat that can't touch your files; you want Codex. ([Codex app guide](https://learn.chatgpt.com/docs/app))

## 3. Install git

Project 1 uses git, a tool for saving versions of your work.

**Mac:** open the Terminal app (press `Cmd + Space`, type `Terminal`, press Return). Paste this in and press Return:

```bash
xcode-select --install
```

Click **Install** in the window that appears. If it says the tools are already installed, you're set.

**Windows:** install [Git for Windows](https://git-scm.com/downloads/win) and accept the default options.

## 4. Make a project folder and open it in your agent

Each project lives in its own folder. Your agent works only inside the folder you give it.

1. Make a new, empty folder somewhere you'll find it again, such as your Desktop or Documents. Project 1 calls it `my-game`.
2. Open it in your agent:
   - **Claude Code:** in the Code tab, choose **Local**, click **Select folder**, and pick your folder.
   - **Codex:** choose **open a folder** (or create a project) and pick your folder. Then start a **New chat**.

## 5. Set the model and effort

Next to where you type, there's a menu for the **model** (which AI does the work) and the **effort** (how hard it thinks before answering). Bigger models and higher effort use up your plan's allowance faster, so on a $20/month plan a two-hour lesson needs a middle setting:

- **Claude Code:** **Opus 5.5** at **Medium** effort. These are the defaults on Pro, so you may not need to change anything. Click the usage ring next to the model menu to see how much of your allowance is left.
- **Codex:** **GPT-6.1 Sol** at **Medium** reasoning effort. If you're on the free plan or running low, switch to **GPT-6 Luna**, which goes much further. ([Codex model guide](https://learn.chatgpt.com/codex/model-selection))
- **Other tools:** the main recommended coding model at medium effort. Avoid the top model and the highest effort settings.

If you run low partway through a project, switch to the cheaper model (**Sonnet 5.5** in Claude Code, **GPT-6 Luna** in Codex) and carry on. The lesson still works.

## 6. Find the terminal inside the app

A **terminal** is a window where you type commands to your computer instead of clicking. Project 1 explains it properly; you'll use it a few times in every project. Both apps have one built in that opens in your project folder:

- **Claude Code:** click **Terminal** at the top of the session, or press `` Ctrl + ` `` (that's the backtick key, usually above Tab; it's Ctrl on Mac too).
- **Codex:** press `` Ctrl + ` ``, or open a new tab and choose **Terminal**.

Open it once now so you know where it is, then close it.

## 7. Paste in your first project

Go to [Project 1](projects/01-make-a-game/) and follow "How to start."

## About permission modes

Your agent asks before certain things, like running a command. A control next to where you type sets how much it can do without asking. These are **permission modes**:

- **Claude Code:** Manual, Accept edits, Plan, Auto, and (hidden by default) Bypass permissions.
- **Codex:** Ask for approval, Approve for me, and Full access.

For Project 1, use the mode that asks you before acting: **Manual** in Claude Code, **Ask for approval** in Codex. The projects work up to letting the agent act on its own inside a safety boundary; the [main page](README.md#3-decide-what-your-agent-is-allowed-to-do-on-its-own) explains why. Never pick Bypass permissions or Full access; they remove the safety checks.

Read each request before you approve it. "Don't ask again" options save time, but let the agent do that kind of thing unchecked next time.

## Prefer the terminal version?

Both agents also come as command-line tools, if you'd rather work entirely in a terminal: see the [Claude Code setup guide](https://code.claude.com/docs/en/setup) or the [Codex CLI guide](https://learn.chatgpt.com/docs/codex/cli). The projects work the same way.
