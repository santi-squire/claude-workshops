# Session 1 — Speaker Script (v3)
### Claude Code: Getting Started | 45 minutes | 40 slides

> **Pre-session**: 
> 1. Open the waiting room: `file:///Users/santianaya/code/claude-workshops/waiting-room.html` (AI dad jokes auto-rotating)
> 2. Play Hobbiton music in background: https://www.youtube.com/watch?v=HFlxEM6zZsc
> 3. When ready to start, switch to the main presentation

---

## SLIDE 1 — TITLE (0:00)
**[Music playing. Black slide. Let people settle in. Stop music when ready.]**

> "Welcome everyone. Let's get started. This is Session 1 of the Claude Code Workshop Series — Getting Started. And yes, that tagline is intentional: one tool to rule them all."

---

## SLIDE 2 — PRESENTERS (0:30)
**[Photos of Santi and Yurii]**

> "Quick intro — I'm Santi, and Yurii is leading the workshop series. I'm running today's session, and you'll see different presenters for each of the five workshops."

---

## SLIDE 3 — AI AS A SECOND LANGUAGE (1:00)
**[Pause here. Let the message land.]**

> "Before we dive in — this is the 'why.' Our goal at Squire is that everyone uses AI daily. Not just engineers. PMs, QA, design, recruiting — everyone. AI is becoming a second language. The people who learn it now will be the ones who move fastest."

> "Here's a real example: you used to lose 30 minutes searching Slack threads to find that one decision. Now you ask Claude and get the answer in 10 seconds. You can also paste screenshots, docs, anything — Claude understands images too."

> "After today, the goal is simple: before you ask a colleague, ask Claude first."

---

## SLIDE 4 — WHY CLAUDE CODE? (2:30)
**[Before/After comparison]**

> "Quick before and after. Left is what we used to do. Right is what Claude does now."

> "Why Claude Code specifically? It's number one on SWE-bench — that's the industry benchmark for coding AI. It reads your entire codebase, connects to Jira, Slack, and Figma, and works in terminal, Desktop App, and IDE. No other tool does all of that. And it's not just for engineers — PMs, QA, design, recruiters all use it."

---

## SLIDE 5 — WHAT CAN I DO WITH IT? (3:30)
**[6 role cards — fragments reveal one by one. Point to each.]**

> "Let me make this real. Engineering — 'add rate limiting to this endpoint.' Claude writes the code, tests, and opens a PR."

> "Product — 'review this Jira ticket and find gaps in the spec.' Claude reads the ticket and the code and finds what the spec missed."

> "QA — 'generate a test plan for the checkout flow.' Claude reads the implementation and produces structured test cases."

> "Design — 'what components does the settings page use?' Claude connects to your Figma and your codebase."

> "Recruiting — 'draft a job description for a senior backend engineer based on our tech stack.' Claude knows our stack from the codebase."

> "And for everyone — 'summarize the last 3 Slack threads about the outage.' Same tool. Different questions."

**[If someone raises their hand about Jira/Figma connection: "That's MCP — Session 2 with Artur covers exactly that."]**

---

## SLIDE 6 — WHAT WE'LL COVER (5:00)
**[Index slide. Quick.]**

> "Here's today's roadmap. Terminal basics, commands, the context window — which is arguably the most important concept — models, CLAUDE.md, and prompting. 40 minutes, and you'll leave knowing how to use this."

---

## SLIDE 7 — TWO WAYS TO USE CLAUDE (5:30)
**[Desktop App LEFT, Terminal RIGHT]**

> "Two interfaces, same Claude. The Desktop App on the left — visual, familiar, works like ChatGPT but way more powerful. The terminal on the right — full power, all features. Both are legitimate. Use whichever feels natural."

> "Today we'll mostly demo the terminal because it shows everything that's happening, but everything works in the Desktop App too."

---

## SLIDE 8 — DESKTOP APP: 3 MODES (6:30)
**[Three app mockups]**

> "If you use the Desktop App, it has three modes. Chat — just conversation, great for questions. Cowork — Claude works with your files and tools, creates documents, connects to Jira and Slack. And Code — which is literally the terminal Claude Code but inside the app."

---

## SLIDE 9 — SECTION: THE TERMINAL (7:30)
**[Black divider. Brief pause.]**

---

## SLIDE 10 — WHY THE TERMINAL (7:35)
**[Terminal mockup]**

> "The terminal is just a text conversation with your computer. You type, it responds. With Claude Code, you don't even need to know commands — you just describe what you want in English."

> "If you can write a Slack message, you can use the terminal. It's that simple."

---

## SLIDE 11 — MEET WARP (8:30)
**[Warp mockup + try-now box]**

> "If you're going to use the terminal, install Warp. It's a modern terminal — block-based output, searchable, feels like an IDE instead of the 1970s. It's free. Right now, open a browser tab and go to warp.dev, or if you have Homebrew, run `brew install warp`."

---

## SLIDE 12 — THE DESKTOP ALTERNATIVE (9:30)
**[Desktop app mockup with recruiter example]**

> "If the terminal feels unfamiliar — there's a Desktop App that works exactly the same way. Just download it and chat. You can paste Jira links, screenshots, documents."

> "For codebase questions, ask your engineering lead which repo to point Claude at. We're also thinking about setting up a central 'repo of repos' — one repo with READMEs linking to all services, so anyone can ask Claude about the whole org."

---

## SLIDE 13 — SECTION: INSTALLATION (10:30)
**[Black divider.]**

---

## SLIDE 14 — INSTALLING CLAUDE CODE (10:35)
**[Terminal + try-now box]**

> "One command: `npm install -g @anthropic-ai/claude-code`. Needs Node 18. If you use the Desktop App, skip this entirely — just download from claude.ai/download."

---

## SLIDE 15 — FIRST INTERACTION (11:30)
**[Side-by-side terminal + app]**

> "First thing that happens: Claude scans your project. It finds all the files, detects the tech stack, reads the CLAUDE.md. Then you just type naturally. 'Explain this project.' It already knows your codebase — you don't need to explain anything."

---

## SLIDE 16 — SECTION: COMMANDS (12:30)
**[Black divider.]**

---

## SLIDE 17 — DAILY ESSENTIALS (12:35)
**[Command list + /cost output]**

> "Commands you'll use every day. `/help` shows everything — there are 50+ commands. `/clear` resets conversation. `/model` switches models. `/effort` controls thinking depth. `/fast` toggles fast mode — same model, quicker responses."

> "Two interesting ones: `/diff` opens an interactive diff viewer showing what Claude changed on each turn. And `/desktop` — this one bridges the gap — you can start in the terminal and continue the same session in the Desktop App. All commands are linked to docs, click them later."

---

## SLIDE 18 — CONTEXT & MEMORY COMMANDS (13:30)
**[Command list + /compact output]**

> "`/compact` compresses your conversation. Look at this output: from 71% down to 19%. That's huge. `/context` shows a visual colored grid of what's using space. `/memory` saves your preferences across sessions."

> "Two new ones: `/resume` picks up any previous session — name it first with `/rename` so you can find it. Think of it like naming your browser tabs."

---

## SLIDE 19 — CONVERSATION CONTROL (14:30)
**[/btw + /branch terminal demo]**

> "Now the game-changers. `/btw` — quick side question without leaving your current task. Look at the demo: you're mid-refactor, ask a side question, get the answer, and you're right back where you were."

> "`/branch` — fork the conversation to try a different approach. `/rewind` — undo conversation AND code changes back to any checkpoint. `/plan` — make Claude plan before coding."

> "`/copy` grabs the last response to your clipboard — even lets you pick specific code blocks. `/export` saves the whole conversation as a file. These six commands will change how you work."

---

## SLIDE 20 — CLI FLAGS + BUNDLED SKILLS (15:30)
**[Two columns: flags left, skills right]**

> "Quick power moves. `-p` for one-shot questions without starting a conversation. `--continue` to resume where you left off. `/batch` is wild — it spawns parallel agents that each work independently and open their own PRs."

> "Power user tip: you can pipe things in. `cat error.log | claude -p 'what went wrong?'` — use Claude in scripts and CI. More on that in Session 5."

---

## SLIDE 21 — CHEAT SHEET (16:30)
**[Color-coded command rows — now 7 rows including FUN row]**

> "Everything on one slide. There are 50+ commands — these are the ones that matter most. Notice the FUN row at the bottom: `/buddy` gives you a companion, `/color` customizes your prompt, `/stickers` lets you order actual Claude stickers, and `/voice` turns on voice dictation."

> "Pull out your phones right now and screenshot this. I'll wait."

**[Actually wait 5 seconds.]**

> "Also — every command in the previous slides is linked to the official docs. Click them later for the full details."

---

## SLIDE 22 — SECTION: THE CONTEXT WINDOW (17:00)
**[Black divider. Slow down.]**

> **[Pause 3 seconds]** "This next section is the most important thing you'll learn today."

---

## SLIDE 23 — CONTEXT WINDOW EXPLAINED (17:15)
**[Desk analogy + sizes]**

> "Think of it like a desk. Everything Claude works with has to fit on this desk — your conversation, files, system instructions. When the desk fills up, Claude starts forgetting."

> "Sonnet and Haiku have 200K tokens — roughly a 500-page book. Opus has 1 million. Sounds huge, but the system prompt and CLAUDE.md already eat 10-15% before you type anything."

> "For non-engineers: think of it as conversation length. Longer chat means Claude is more likely to forget earlier parts."

---

## SLIDE 24 — CONTEXT STRATEGIES (18:30)
**[DO / DON'T columns + warning]**

> "Practical rules. `/clear` between unrelated tasks. `/compact` proactively at about 70%."

> **[Point to the red warning]** "And this is critical: if Claude auto-compacts — that means it hit 95% and quality is already bad. **Start a new conversation instead.** Auto-compact is an emergency brake, not a feature."

> "Real case at Squire — look at these screenshots. We had 4 memory files eating 7.7k tokens — 3.8% of our context loaded before we even typed anything. We merged them into one lean CLAUDE.md and dropped to 4.6k — 2.3%. That's a 40% reduction. And look at the free space: jumped from 143k to 157k. Fourteen thousand more tokens for actual work, every single session."

**[Point to the before/after screenshots on the slide]**

---

## SLIDE 25 — DATA & PRIVACY (20:00)
**[Do/Don't terminal mockup]**

> "Important one. We use Claude Team — that means your prompts and code are NOT used to train models. Conversations are isolated per user."

> "But — still never paste API keys, customer PII, passwords, or financial data. Code, specs, docs, Jira tickets, error logs, screenshots — all fine."

---

## SLIDE 26 — SECTION: MODELS & PLANS (21:00)
**[Black divider.]**

---

## SLIDE 27 — AVAILABLE MODELS (21:05)
**[Three model cards — fragments reveal one by one]**

> "Three models. Haiku — fast and cheap, for quick questions. Sonnet — your default, great balance. And Opus — the big brain, 1 million token context, but expensive."

> "We have Team subs — switch freely with `/model`. No cost concerns."

---

## SLIDE 28 — OPUS + IDEAL WORKFLOW (22:00)
**[Opus explanation + 3-step vertical flow]**

> "What makes Opus special? It thinks before answering. It has 'extended thinking' — like a senior engineer who pauses, considers tradeoffs, then gives a well-reasoned answer."

> "The catch: Opus 4.6 eats significantly more tokens than previous versions. That thinking costs extra. So here's the ideal workflow:"

> "Step 1: Haiku — quick recon, understand the codebase. Step 2: Opus — create a comprehensive plan. Step 3: Sonnet — fast implementation following the plan."

> "Haiku explores. Opus plans. Sonnet builds."

---

## SLIDE 29 — PLAN MODE (23:30)
**[/plan terminal example]**

> "This is the single biggest productivity tip I can give you. `/plan` tells Claude to think through the approach without writing any code."

> "Watch: switch to Opus, run `/plan`, describe the task. Opus comes back with a phased plan. You review it. Approve it. Switch to Sonnet. 'Implement it.'"

> "**Never let Claude jump straight to code on something complex.** Plan first, code second."

---

## SLIDE 30 — MEMORY & PERSISTENCE (25:00)
**[Three layers + terminals]**

> "Three layers of remembering. Context — temporary, dies when you clear. Memory — personal preferences across sessions. CLAUDE.md — shared team rules."

> "`--continue` picks up where you left off. Went to lunch? Resume."

---

## SLIDE 31 — SECTION: CLAUDE.MD (26:00)
**[Black divider.]**

---

## SLIDE 32 — WHAT IS CLAUDE.MD (26:05)
**[VS Code mockup + good vs bad examples]**

> "CLAUDE.md is a markdown file at the root of your repo. Claude reads it every session. It's your team's constitution — coding style, architecture patterns, what to never do."

> "Be specific. 'Validate inputs' is useless. 'Use Zod schemas for all API input validation' — now Claude knows exactly what to do. And keep it lean — every line costs tokens every session."

> "Use `/init` to scaffold one for an existing project."

---

## SLIDE 33 — SECTION: PROMPTING (27:30)
**[Black divider.]**

---

## SLIDE 34 — EFFECTIVE PROMPTING (27:35)
**[Bad vs good + role examples]**

> "The formula: What + Where + Constraints + Expected Behavior. Look at the difference: 'fix the bug' versus 'the /api/users endpoint returns 500 when email has a plus sign — fix validation in userController.ts.'"

> "And this works for everyone. Engineering, PM, QA, recruiting — same formula, different questions."

---

## SLIDE 35 — LIVE DEMO (28:30)
**[Pulsing LIVE badge. 5 minutes.]**

> "Let's see it for real."

**[Switch to terminal. Have squire-platform repo ready.]**

Demo script:
1. `cd ~/squire-platform && claude` — show it scanning files, detecting stack
2. `"explain the checkout service and how it connects to payments"` — real question about real code
3. `/context` — show the grid (point out: "see? system prompt, memory, free space")
4. `/compact` — compress and show the before/after token count
5. `/model opus` → `/plan "add a retry mechanism for failed Stripe payments"` — realistic task, show Opus thinking
6. `/diff` — show the interactive diff viewer
7. `/buddy` — fun ending, show Waffletch appear
8. `/cost` — show what that session cost

> "Note: in real use, Claude would implement the plan too. I'm skipping that to save time. But you saw the thinking process."

> "Any questions about what you just saw?"

---

## SLIDE 36 — PITFALLS + HOMEWORK (34:00)
**[Safety checklist + homework merged into one section]**

> "Safety rules: always read the diff. Commit before big changes. If confused, `/clear` and restart."

> "Homework — and I mean right now. Open your laptop. Install Claude Code AND download the Desktop App. Try both. Run `/init`, explore commands, ask Claude about a Jira ticket or a file. And run `/buddy` — screenshot it and post in #claude-code-workshop."

> "Don't leave this room without having sent at least one message to Claude."

---

## SLIDE 37 — WORKSHOP SERIES (36:00)
**[5 sessions with presenters]**

> "Here's what's coming. Today was Session 1 — me. Session 2 is Artur on Skills and MCP — connecting Claude to Jira, Slack, Figma — that one is for everyone. Session 3 is Jonathan on subagents and hooks — engineering deep-dive. Session 4 is Nico on spec-driven development — also engineering-focused. And Session 5 ties it all together with CI/CD and a full end-to-end demo."

---

## SLIDE 38 — KEY TAKEAWAYS (37:30)
**[6 takeaways — fragments reveal one by one]**

> "Six things to remember:"
> 1. "Claude reads your codebase — just type naturally."
> 2. "Context is your most valuable resource. New chat beats auto-compact."
> 3. "Haiku explores, Opus plans, Sonnet builds."
> 4. "Plan first, code second."
> 5. "CLAUDE.md is your team's playbook."
> 6. "Always review the output."

> "Questions?"

**[Q&A until 43:00]**

---

## SLIDE 39 — BONUS: MEET YOUR BUDDY (43:00)
**[Fun slide. Only if time allows.]**

> "One last thing — just for fun. Claude Code has a companion feature. Type `/buddy` and a little character appears next to your input. Mine is Waffletch — a mushroom with opinions."

**[Show your Waffletch screenshot]**

> "Everyone gets a different buddy with a unique name and personality. Try `/buddy` and screenshot yours — post it in #claude-code-workshop!"

---

## SLIDE 40 — THANK YOU (44:00)
**[Closing slide]**

> "That's it. Now go use it. Questions, ideas, screenshots — post everything in #claude-code-workshop on Slack. See you at Session 2 with Artur!"

---

## EMERGENCY SHORTCUTS
If running long (>38 min at slide 35), skip:
- **Context Strategies details** — just say "clear between tasks, compact at 70%"
- **Memory & Persistence** — mention verbally during CLAUDE.md
- **Buddy** — skip entirely, mention in Slack after

If running short, expand:
- **Live demo** — let audience request things to ask Claude
- **Q&A** — open early, get discussion going

---

## NOTES FROM ROLE REVIEWERS

### For PM/Recruiter moments:
- On the roles slide, **look around the room** and ask "who's a PM here? QA? Recruiter?"
- When showing Desktop App: "This is the one most of you will use day one"
- If someone asks about Jira/Figma connection: "That's Session 2 with Artur — it's already set up"
- Context window: say "think of it as conversation length" for non-devs

### For Engineers:
- On /batch: emphasize isolated worktrees = real parallelism
- On cheat sheet: "there are 50+ commands, these are the ones you'll use most"
- On Plan Mode: "this is the workflow that separates good from great Claude users"
- Mention `cat error.log | claude -p` for the power users

### Watch for glazed eyes:
- Commands Deep Dive (slides 17-21) is where non-devs may zone out
- Speed up through these, slow down on Context Window and Models
- The live demo brings everyone back — make it count
