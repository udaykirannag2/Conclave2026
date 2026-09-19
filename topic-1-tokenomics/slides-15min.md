# Topic 1 — 15-Minute Slide Words

Content for a 12-slide deck, one slide per beat in [`outline-15min.md`](outline-15min.md). This is the words only — no layout, imagery, or design direction; build the visual deck from this whenever you're ready.

---

### Slide 1 — Title

**Tokenomics**
The New Unit Economics Every AI Founder and Investor Needs to Understand

*(speaker name / PitchXPO Conclave 2026)*

---

### Slide 2 — Cold Open

**You're paying for something you can't see.**

Every AI feature carries a real, variable cost behind every single interaction.

Most people building AI products couldn't tell you what one query costs. Or one task. Or one tenant.

---

### Slide 3 — The Margin Problem

**Microsoft lost $20 per user per month — and that's normal now.**

- Classic SaaS gross margin: **80–90%**
- AI-native gross margin: **50–60%**
- Same metric. Same investors. Half the margin.

*Source: Bessemer Venture Partners, "The AI Pricing and Monetization Playbook"*

The gap isn't overhead. It's compute.

---

### Slide 4 — The Cost Asymmetry (one line)

Claude reads your question in parallel. It writes its answer one token at a time.

**Output costs 3–5x more than input, per token.**

That's the only "what is a token" this talk needs.

---

### Slide 5 — The Core Insight

**The math that lied to everyone: why 10x users became 30x cost.**

- AI cost is **linear** in tokens. It never compounds on its own.
- Tokens-per-user is not fixed — it drifts:
  - Longer context as conversations age
  - Wider retrieval as your RAG index grows
  - Agent loops calling the model 5–10x per user action

**10x user growth × unmodeled 3x token drift = 30x cost growth.**
Your pricing was built for the 10x world.

---

### Slide 6 — The Framework

**Inform → Optimize → Operate**

The three-stage arc you're taking home.

---

### Slide 7 — Stage 1: Inform

**You can't manage what you can't see.**

| Stage | Cost attributable to task/tenant/feature |
|---|---|
| Crawl | < 10% |
| Walk | 60–80% |
| Run | > 95%, real-time, anomalies caught same-day |

Which rung are you actually on?

---

### Slide 8 — Stage 2: Optimize

**Where the real money is.**

- **Caching** — repeat context, ~90% off on a hit
- **Batching** — 30–40% of workloads qualify, 50% off
- **Commitment math** — one formula before you buy reserved capacity:

`commitment cost ÷ on-demand cost = breakeven utilization %`

Can't hit that utilization? The discount is a loss.

---

### Slide 9 — Stage 3: Operate (the story)

**The agent that cost 21x more than it should have.**

An 8-step agent loop, re-sending full context at every step:

**21.5x** the cost of a single call — before unguardrailed retries make it worse.

---

### Slide 10 — Stage 3: Operate (the controls + proof)

**Five guardrails that stop it:**
Max depth · Max tokens/task · Retry limits · Timeouts · Explicit fallback

**Proof it works:**
- Itemized per-reel cost breakdown, shipped multi-agent video pipeline
- $10M/year client engagement: loop caps + kill-switch made **20–25% savings stick**

---

### Slide 11 — Try It Yourself

**[QR code]**

A token-cost calculator. Take it with you. Run your own numbers tonight.

---

### Slide 12 — Close

**One question for founders:**
Which stage are you actually in — Inform, Optimize, or Operate?

**One question for investors:**
Ask a startup that question before you ask for the pitch deck.

*(calculator link / contact — CTA)*
