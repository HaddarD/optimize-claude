# optimize-claude

***Interactive reference guide to Claude model selection, token usage, context windows, and compression — built to help Claude users work more efficiently and compress less often.***

## 🔗 Live version

👉 **[View the interactive guide](https://haddard.github.io/optimize-claude/)**

---

## What it covers

Four interactive tabs plus permanent reference sections:

### 💰 Token Cost
Estimated token usage across **Sonnet 4.6, Sonnet 5, Opus 4.6, Opus 4.7, Opus 4.8, and Fable 5** at every effort level (Low → Medium → High → xHigh → Max), with a **Thinking ON/OFF toggle** that updates all bars in real time. Fixed scale so toggling thinking correctly grows bars rather than rescaling them. Fable 5 shows N/A when thinking is set to OFF — it has no off switch.

### 📊 Benchmarks
Six benchmark categories you can flip between:
- **Everyday Coding** (SWE-bench Verified)
- **Hard Coding** (SWE-bench Pro)
- **Science & PhD Reasoning** (GPQA Diamond)
- **Computer Use** (OSWorld)
- **Terminal** (Terminal-Bench) — Sonnet 5 beats Opus 4.8 here
- **Creative & Emotional Writing** (Chatbot Arena ELO)

Includes a starred cost-per-solve note on Fable 5: despite costing 2× per token, it's cheaper per successfully solved task at frontier-hard difficulty than Opus 4.8.

### ❓ What Limits You?
Explains the relationship between token cost and context window — they use the same pool of tokens, not two separate systems. Covers:
- What actually fills your context window (messages, responses, accumulated thinking tokens on current models, tool definitions)
- Context window sizes by model and surface (chat vs Claude Code, Pro vs Max)
- Which problem is actually yours: usage limit, compression, or both — with targeted fixes for each

### 🎯 Decision Guide
Task-type → model + effort + thinking mapping covering companion conversation, memoir/book writing, interview/storytelling, easy bugs, stuck loops, multi-file coding, architecture, research, frontier tasks, and Fable 5's specific use case. Includes escalation ladder and the "jump vs grind" decision framework.

---

## Permanent reference sections (always visible)

- **Context window table** — Pro vs Max, chat vs Claude Code, every model including Sonnet 5
- **What to use & when** — plan-specific recommendations (Pro and Max) updated for Sonnet 5
- **Claude Code vs Chat** — real differences side by side
- **Usage credits warning** — what they actually cost, what happens without them
- **Haiku 4.5 note** — why it's excluded and who it's actually for (API volume users, not monthly subscribers)

---

## Key findings

- **Sonnet 5 (Jun 30, 2026):** New default for all plans. 1M context window in regular chat — no Claude Code required. Beats Opus 4.6 on coding and Opus 4.8 on Terminal-Bench. Same standard pricing as Sonnet 4.6 but ~17.5% more tokens from new tokenizer. Net result: ~70% more turns before compression vs Sonnet 4.6 despite tokenizer overhead.
- Switching from Opus to Sonnet does **not** reduce compression speed in isolation — it's the same tokens for both context and usage. To compress less, you need a larger context window or shorter messages. Sonnet 5's 1M chat window is the biggest single lever.
- Thinking tokens **do accumulate** in the context window on Sonnet 4.6+, Opus 4.5+, and Fable 5 — turning thinking OFF genuinely helps both usage and compression.
- Opus 4.7/4.8 use 20–35% more tokens than Opus 4.6 for identical text due to a new tokenizer — same price, higher effective cost.
- Fable 5 has thinking permanently ON with no toggle, costs ~4.23× Sonnet base per token minimum. **Redeployed July 1, 2026** after a June 12–30 suspension due to a US export control directive — now included at no extra cost for up to 50% of weekly usage limit through July 7, 2026, then usage-credits-only after that.
- On Max plan, Claude Code with Opus 4.6 gives you a 1M context window — but Sonnet 5 now matches this in regular chat.

---

## Built with

Claude Sonnet 4.6 across multiple research sessions. Data compiled from Anthropic's official documentation, published benchmarks, Chatbot Arena, and independent third-party analysis. Token cost numbers are estimates — Anthropic does not publish official effort-level multipliers. Some Sonnet 5 benchmark scores marked (~) are estimated from Anthropic's "close to Opus 4.8" framing; confirmed scores cited where available.

## License

Free to share, remix, and adapt. Attribution appreciated.
