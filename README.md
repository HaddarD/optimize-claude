# optimize-claude

***Interactive reference guide to Claude model selection, token usage, context windows, and compression — built to help Claude users work more efficiently and compress less often.***

## 🔗 Live version

👉 **[View the interactive guide](https://haddard.github.io/optimize-claude/)**

---

## What it covers

Four interactive tabs plus permanent reference sections:

### 💰 Token Cost
Estimated token usage across **Sonnet 4.6, Opus 4.6, Opus 4.7, Opus 4.8, and Fable 5** at every effort level (Low → Medium → High → xHigh → Max), with a **Thinking ON/OFF toggle** that updates all bars in real time. Fixed scale so toggling thinking correctly grows bars rather than rescaling them. Fable 5 shows N/A when thinking is set to OFF — it has no off switch.

### 📊 Benchmarks
Six benchmark categories you can flip between:
- **Everyday Coding** (SWE-bench Verified)
- **Hard Coding** (SWE-bench Pro)
- **Science & PhD Reasoning** (GPQA Diamond)
- **Computer Use** (OSWorld)
- **Terminal** (Terminal-Bench)
- **Creative & Emotional Writing** (Chatbot Arena ELO)

Includes a starred cost-per-solve note on Fable 5: despite costing 2× per token, it's cheaper per successfully solved task at frontier-hard difficulty than Opus 4.8 — because Opus fails more often and retries cost more.

### ❓ What Limits You?
Explains the relationship between token cost and context window — they use the same pool of tokens, not two separate systems. Covers:
- What actually fills your context window (messages, responses, accumulated thinking tokens on current models, tool definitions)
- What doesn't change your window ceiling (billing weights, model choice within same surface)
- Context window sizes by model and surface (chat vs Claude Code, Pro vs Max)
- Which problem is actually yours: usage limit, compression, or both — with targeted fixes for each

### 🎯 Decision Guide
Task-type → model + effort + thinking mapping covering companion conversation, memoir/book writing, interview/storytelling, easy bugs, stuck loops, multi-file coding, architecture, research, frontier tasks, and Fable 5's specific use case.

Includes escalation ladder and the "jump vs grind" decision framework.

---

## Permanent reference sections (always visible)

- **Context window table** — Pro vs Max, chat vs Claude Code, every model
- **What to use & when** — plan-specific recommendations (Pro and Max) with warnings
- **Claude Code vs Chat** — real differences side by side
- **Usage credits warning** — what they actually cost, what happens without them, the billing gate bug workaround
- **Haiku 4.5 note** — why it's excluded from the calculator and who it's actually for (API volume users, not monthly subscribers)

---

## Key findings

- Switching from Opus to Sonnet does **not** reduce compression speed — it reduces usage budget burn. To compress less, you need a larger context window or shorter messages.
- Thinking tokens **do accumulate** in the context window on Sonnet 4.6+, Opus 4.5+, and Fable 5 — turning thinking OFF genuinely helps both usage and compression.
- Opus 4.7/4.8 use 20–35% more tokens than Opus 4.6 for identical text due to a new tokenizer — same price, higher effective cost.
- Fable 5 has thinking permanently ON with no toggle, costs ~4.23× Sonnet base per token minimum, and requires usage credits on all plans.
- On Max plan, Claude Code with Opus 4.6 gives you a 1M context window included — double chat's 500K — without usage credits.

---

## Built with

Claude Sonnet 4.6 across multiple research sessions. Data compiled from Anthropic's official documentation, published benchmarks, Chatbot Arena, and independent third-party analysis. Token cost numbers are estimates — Anthropic does not publish official effort-level multipliers.

## License

Free to share, remix, and adapt. Attribution appreciated.
