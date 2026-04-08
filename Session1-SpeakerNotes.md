# Speaker Notes — Session 1
### Quick-reference cards. Read the bold line, expand with the bullets.

---

### 1. TITLE
- Music playing, let people settle
- **"Welcome to Session 1 of the Claude Code Workshop. One tool to rule them all."**

### 2. PRESENTERS
- **"I'm Santi, Yurii is leading the workshop series. Five sessions, different presenters."**

### 3. AI AS A SECOND LANGUAGE
- **"Our goal: everyone at Squire uses AI daily. Not just engineers."**
- Before asking a colleague, ask Claude first
- You can paste screenshots, docs, Jira links — Claude reads images too
- "30 min searching Slack threads → 10 seconds with Claude"

### 4. WHY CLAUDE CODE?
- **"Before vs after. Left is the old way, right is Claude."**
- #1 on SWE-bench (industry coding benchmark)
- Reads your entire codebase, connects to Jira/Slack/Figma
- Works in terminal, Desktop App, and IDE
- Not just for engineers — PMs, QA, design, recruiters

### 5. WHAT CAN I DO WITH IT?
- **Cards appear one by one with arrow key. Point to each role.**
- "Who's a PM here? This one's for you"
- ENG: "add rate limiting" → writes code, tests, opens PR
- PM: "review Jira ticket" → finds gaps in the spec
- QA: "generate test plan" → structured test cases from real code
- DESIGN: connects to Figma
- RECRUIT: drafts JDs from your actual tech stack
- EVERYONE: summarizes Slack threads

### 6. WHAT WE'LL COVER
- **Quick index slide. Don't read it out loud.**
- "Terminal, commands, context window — most important — models, CLAUDE.md, prompting"
- "Follow along! Install as we go"

### 7. TWO WAYS TO USE CLAUDE
- **"Two interfaces, same Claude. Desktop App or terminal. Both are powerful."**
- Today we demo mostly terminal because it shows everything
- But everything works in the Desktop App too

### 8. DESKTOP APP: 3 MODES
- **"Chat = Q&A. Cowork = works with your files and tools. Code = terminal in the app."**
- Quick slide, don't linger

### 9. SECTION: TERMINAL
- **Pause 3 seconds. Let the title land.**

### 10. WHY THE TERMINAL
- **"The terminal is just a text conversation with your computer."**
- "If you can type a Slack message, you can use it"

### 11. MEET WARP
- **"Install Warp. Modern terminal, feels like an IDE. Free."**
- `brew install warp` or warp.dev
- "Do it now if you can"

### 12. THE DESKTOP ALTERNATIVE
- **"If the terminal feels unfamiliar — Desktop App works the same way."**
- No codebase needed, just chat
- Paste Jira links, screenshots, docs
- We're thinking about a "repo of repos" for org-wide questions

### 13. SECTION: INSTALLATION
- Quick pass

### 14. INSTALLING CLAUDE CODE
- **`npm install -g @anthropic-ai/claude-code`**
- Needs Node 18. Don't have it? Ask in #claude-code-workshop
- Desktop App: claude.ai/download

### 15. FIRST INTERACTION
- **"Claude scans your project automatically. Then just type naturally."**
- Show both sides: terminal left, app right

### 16. SECTION: COMMANDS
- **"50+ commands. We'll cover the essential ones."**

### 17. DAILY ESSENTIALS
- **`/help` shows everything. `/clear` resets. `/model` switches.**
- `/fast` — same model, faster output
- `/diff` — browse what Claude changed on each turn
- `/desktop` — continue this terminal session in the Desktop App (bridge!)
- `/cost` — token usage, but don't worry, we have Team subs

### 18. CONTEXT & MEMORY
- **`/compact` compresses conversation. Look: 71% → 19%.**
- `/context` — visual colored grid of what's using space
- `/memory` — saves preferences across sessions
- `/resume` — pick up any previous session
- `/rename` — name sessions so you find them later
- Rule: `/clear` = fresh start, `/compact` = keep going

### 19. CONVERSATION CONTROL
- **"These are the game-changers."**
- `/btw` — side question, doesn't pollute context
- `/branch` — fork conversation, try different approach
- `/rewind` — undo conversation AND code changes
- `/plan` — think before coding
- `/copy` — grab response to clipboard, picks code blocks
- `/export` — save whole conversation as a file

### 20. CLI FLAGS + SKILLS
- **`-p` for one-shot questions. `--continue` to resume.**
- `/batch` — parallel agents, each opens own PR
- Tip: `cat error.log | claude -p 'what went wrong?'`

### 21. CHEAT SHEET
- **"Screenshot this now. Pull out your phones. I'll wait."**
- Wait 5 seconds for real
- 7 rows, 50+ commands, including FUN row: `/buddy`, `/color`, `/stickers`
- "Commands in previous slides are linked to docs"

### 22. SECTION: CONTEXT WINDOW
- **Pause. "This is the most important concept today."**

### 23. CONTEXT WINDOW EXPLAINED
- **"Think of it like a desk. Everything has to fit."**
- Sonnet/Haiku: 200K tokens (~500 page book)
- Opus: 1M tokens (~all 7 Harry Potters)
- System prompt + CLAUDE.md already eat 10-15%
- For non-devs: "think of it as conversation length"

### 24. CONTEXT STRATEGIES
- **"Three rules: /clear between tasks. /compact at 70%. New chat beats auto-compact."**
- Point to red WARNING: auto-compact at 95% = quality already bad
- **Real case @ Squire**: show the screenshots
  - "4 memory files eating 7.7k tokens"
  - "Merged into one CLAUDE.md → 4.6k, 40% reduction"
  - "14k more tokens free for actual work, every session"

### 25. DATA & PRIVACY
- **"Team plan = your data is NOT used for training."**
- Never paste: API keys, PII, passwords, financial data
- Fine to paste: code, specs, docs, Jira tickets, error logs, screenshots

### 26. SECTION: MODELS & PLANS
- Quick pass

### 27. AVAILABLE MODELS
- **Cards appear one by one.**
- Haiku: fast, cheap, quick questions
- Sonnet: your default, great balance
- Opus: big brain, 1M context, expensive
- "Team subs — switch freely with /model"

### 28. OPUS + IDEAL WORKFLOW
- **"Opus thinks before answering. Like a senior engineer who pauses."**
- 4.6 eats more tokens than previous versions — use wisely
- **The workflow: Haiku explores → Opus plans → Sonnet builds**
- "This saves tokens AND gets better results"

### 29. PLAN MODE
- **"Never let Claude jump straight to code on something complex."**
- `/plan` → Claude thinks through the approach without writing code
- Switch to Opus for planning, Sonnet for implementation
- **"Plan first, code second. Biggest productivity tip."**

### 30. MEMORY & PERSISTENCE
- **"Three layers: Context (temporary), Memory (personal), CLAUDE.md (team)."**
- `--continue` picks up where you left off
- `/memory` — show the preferences example

### 31. SECTION: CLAUDE.MD
- Quick pass

### 32. CLAUDE.MD + TIPS
- **"Markdown file at repo root. Claude reads it every session."**
- Team's constitution: coding style, patterns, what to never do
- Be specific: "Use Zod" not "Validate inputs"
- Keep it lean — every line costs tokens
- `/init` scaffolds one for you

### 33. SECTION: PROMPTING
- Quick pass

### 34. EFFECTIVE PROMPTING
- **"The formula: What + Where + Constraints + Expected Behavior."**
- Bad: "fix the bug" → Good: "the /api/users endpoint returns 500 when email has +"
- Show role examples: same formula works for PM, QA, recruiter

### 35. LIVE DEMO (~5 min)
- **Switch to terminal. Repo ready.**
1. `cd ~/squire-platform && claude`
2. "explain the checkout service"
3. `/context` — point out the grid
4. `/compact` — show before/after
5. `/model opus` → `/plan "add retry for failed Stripe payments"`
6. `/diff`
7. `/buddy` — fun moment
8. `/cost`
- "In real use Claude implements the plan too. Skipping to save time."

### 36. PITFALLS + HOMEWORK
- **"Always read the diff. Commit before big changes. If confused, /clear."**
- **"Do it NOW. Open your laptop."**
  1. Install Claude Code + Desktop App
  2. Run `/init`
  3. Send your first message in both
  4. Try `/context`, `/compact`
  5. Ask about a file, Jira ticket, or doc
  6. Run `/buddy` and share in Slack
- "Don't leave without having sent at least one message"

### 37. WORKSHOP SERIES
- **Name each presenter.**
- S1: Santi (today) — Getting Started
- S2: Artur — Skills & MCP (Jira, Slack, Figma)
- S3: Jonathan — Subagents & Hooks
- S4: Nico — Spec-Driven Development
- S5: TBD — CI/CD & End-to-End

### 38. KEY TAKEAWAYS
- **Read each one as it appears (fragments):**
1. Claude reads your codebase — just type naturally
2. Context is your most valuable resource — new chat > auto-compact
3. Haiku explores → Opus plans → Sonnet builds
4. Plan first, code second
5. CLAUDE.md is your team's playbook
6. Always review the output

### 39. BUDDY
- **"Fun bonus. Type /buddy to meet your companion."**
- Show Waffletch screenshot
- "Everyone gets a different one. Screenshot yours, post in #claude-code-workshop"

### 40. THANK YOU
- **"Now go use it. Questions go to #claude-code-workshop on Slack."**
- "See you at Session 2 with Artur!"

---

## IF RUNNING LONG (>38 min at slide 35)
Skip: Desktop Alternative (12), Context Strategies details, Buddy (39)

## IF RUNNING SHORT
Expand: Live Demo (let audience request things), Q&A
