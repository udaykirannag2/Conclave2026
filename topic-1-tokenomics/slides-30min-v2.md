# Topic 1 — 30-Minute Slide Words (v2)

Content for a ~17-slide deck matching [`outline-30min-v2.md`](outline-30min-v2.md). Words only — no layout, imagery, or design direction.

---

### Slide 1 — Title

**Tokenomics**
The New Unit Economics Every AI Founder and Investor Needs to Understand

*(speaker name / PitchXPO Conclave 2026)*

---

### Slide 2 — Cold Open, prompt 1

**Drop it in the chat:**
How many of you are building or managing an AI application right now?

---

### Slide 3 — Cold Open, prompt 2

**The real question:**
How many of you know exactly what it costs to run that application?

---

### Slide 4 — Cold Open, landing

That drop-off is normal.

Most organizations are struggling to know what their AI spend actually is — and even harder, what value it's delivering back to the business.

That gap has a name getting a lot of attention right now: **Tokenomics.**

A framework — a practice — for making sense of your AI spend, and figuring out the value it's providing your business.

---

### Slide 5 — Section: Where FinOps Breaks for AI

**Why this is hard — not just under-invested.**

Four challenges in token spend management.

---

### Slide 6 — Challenge 1: Tagging Mismatch

**Cloud tagging is infrastructure-first. AI is application-first.**

- Tag an EC2 instance → it runs for hours → the bill shows exactly whose it is.
- An AI request happens in 50 milliseconds and is gone before you can tag it.

**The fix:** tag at API-call time, inside the application code.

---

### Slide 7 — Challenge 2: Spend Fragmentation

**Your AI bill is bigger than your cloud bill shows.**

| Vendor | Spend |
|---|---|
| AWS Bedrock | $2,000 |
| OpenAI | $1,500 |
| Anthropic | $800 |
| Pinecone | $300 |
| **Real total** | **$4,600** |

Finance's AWS-only view: **$2,000.**
Over half the spend is invisible to whoever's supposed to be watching it.

---

### Slide 8 — Challenge 3: No Benchmarks

**Cloud has known prices. AI doesn't — yet.**

- A t2.micro: ~$10/month. A c5.large: ~$85/month. Public, known, benchmarkable.
- Nobody knows what a chatbot *should* cost per user. The category's too new. No historical data.

---

### Slide 9 — Challenge 4: Forecasting Is Guessing

**Cloud forecasting: straightforward. AI forecasting: a guess.**

- Cloud: spend $100K this month → forecast $100K next month → usually right.
- AI: $0 last month → $5K this month → $50K next. The adoption curve is vertical.

*"We went from $10,000 to $100,000 in two months. Nobody predicted it."*
— a FinOps leader

---

### Slide 10 — Section: Primary Drivers of LLM Cost

**Three things shape the bill.**

**Cost = Request Shape × Usage Scale × Overhead**

---

### Slide 11 — The Three Drivers

- **Request Shape** — input tokens, output tokens, context-window size. The size of one transaction.
- **Usage Scale** — model tier, request volume, number of model calls. How many transactions, on which model.
- **Overhead** — retries, agent loops, latency requirements forcing costlier models.

---

### Slide 12 — Overhead Is a Multiplier, Not a Line Item

Overhead isn't added on top. It **multiplies** the first two.

A retry doesn't add a flat fee — it reruns the exact same request shape and usage-scale work again.

Overhead starts at **1.0** for zero waste. It climbs with every retry, loop, or forced upgrade.

**Cutting overhead doesn't just remove a cost — it removes a multiplier on everything else.**

---

### Slide 13 — The Framework

**Inform → Optimize → Operate**

The three-stage arc you're taking home.

---

### Slide 14 — Stage 1: Inform (Visibility)

**The INFORM framework:**
Ingestion → Normalization → Allocation → Showback

- Tag at the **API-call level** — team / app / cost-center / environment.
- **Anomaly detection:** usage anomalies, model anomalies, cost anomalies.
- **Showback dashboards:** different metrics for CFO, team lead, engineer.

Showback drives optimization — you can't cut a cost you can't see.

---

### Slide 15 — Stage 2: Optimize (Levers)

**The big three, in impact order:**

- **Model choice** — right-size the model to the task.
- **Pricing model** — on-demand vs. committed capacity vs. batch. Run the breakeven: `commitment cost ÷ on-demand cost = breakeven utilization %`
- **Caching** — 90% discount on repeated context. Breakeven inside the second request.

**Combined: 80%+ savings.**

Watch for the trap: published price ≠ real cost. Egress, throttling, and regional variance hide another 20–40%.

---

### Slide 16 — Stage 3: Operate (the 21.5x story)

**One support question. Eight API calls.**

A support agent answers one billing question — re-sending full context at every step.

- Single direct call: ~1,000 tokens
- Same question, agentic: **21,500 tokens**

**21.5x the cost.** Before retries push it past 50x — or an unbounded loop makes it a surprise on the monthly bill.

---

### Slide 17 — Five Guardrails + the KPI Shift

**Max depth · Max tokens/task · Retry limit · Timeout · Explicit fallback**

The KPI that matters: **cost per task**, not cost per call — the unit that lets you compare human work, machine work, and hybrid work.

In healthcare and finance: guardrails aren't optional. You need to audit what an agent did and what it spent.

---

### Slide 18 — Try It Yourself

**[QR code]**

A token-cost calculator. Take it with you. Run your own numbers tonight.

---

### Slide 19 — Close

**One question for founders:**
Which stage are you actually in — Inform, Optimize, or Operate?

**One question for investors:**
Ask a startup that question before you ask for the pitch deck.

*(calculator link / contact — CTA)*
