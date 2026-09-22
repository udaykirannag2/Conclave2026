# Topic 1 — 30-Minute Slide Words (v2)

Content for a 13-slide deck matching [`outline-30min-v2.md`](outline-30min-v2.md). Words only — no layout, imagery, or design direction. Slides 5 and 6 follow the sparse-slide-plus-speaker-notes pattern from the source [Module 1 Slides design doc](https://claude.ai/design/p/772ae942-8d32-4921-ba76-3943adcdb6fb) (slides 25 and 16) — minimal on-screen text, full narration in speaker notes.

---

### Slide 1 — Title

**Tokenomics**
Making Sense of AI Spend Before It Makes Sense of You

Uday Nagulavancha · PitchXPO Conclave 2026 · September 22, 2026

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

### Slide 5 — Where Cloud FinOps Breaks for AI

*SUBTOPIC · WHERE FINOPS BREAKS*

**Where cloud FinOps breaks for AI**

- Tagging mismatch — infrastructure-first tools, application-first spend
- Spend fragmentation — across vendors
- No benchmarks — the category's too new
- Forecasting is guessing — the adoption curve is vertical

**Speaker notes:**
Cloud tagging is infrastructure-first: you tag an EC2 instance, it runs for hours, the bill shows exactly whose it is. AI is application-first — a request happens in 50 milliseconds and is gone before you can tag it. The fix is tagging at API-call time, inside your application code. Meanwhile, AI spend fragments across vendors: AWS Bedrock $2,000, OpenAI $1,500, Anthropic $800, Pinecone $300 — $4,600 total, but finance's AWS view shows only $2,000. In cloud, a t2.micro costs about $10 a month, a c5.large about $85 — public, known numbers you can benchmark against. With AI, nobody knows what a chatbot should cost per user — the industry is too new, there's no historical data. Cloud forecasting is straightforward: $100,000 a month, forecast $100,000 next month, usually right. AI forecasting is guessing: $0 last month, $5,000 this month, $50,000 next — the adoption curve is vertical. One FinOps leader said: we went from $10,000 to $100,000 in two months. Nobody predicted it.

---

### Slide 6 — Primary Drivers of LLM Cost

*SUBTOPIC 1.3 · PRIMARY DRIVERS OF LLM COST*

**Three things shape the bill**

**Cost = Request Shape × Usage Scale × Overhead**

**Speaker notes:**
A provider rate card tells you the price of a unit — your application design determines how many units you consume. The eight drivers we just walked through actually collapse into three things. Request shape: input tokens, output tokens, and context-window size — the shape and size of each individual transaction. Usage scale: model tier, request volume, and number of model calls — how many transactions you're running, and on which model. And overhead: retries, agent loops, and latency requirements that force costlier models. Here's the key relationship — overhead is not a separate cost bucket added on top. It's a multiplier on the first two. A retry doesn't add a flat fee, it reruns the exact same request shape and usage-scale work a second time. A latency requirement that forces a pricier model doesn't sit outside usage scale, it inflates it. So the real equation is cost equals request shape times usage scale, all multiplied by overhead — where overhead is a multiplier starting at 1.0 for zero waste, and climbing above that for every retry, loop, or forced upgrade. That's why cutting overhead has an outsized effect: it doesn't just remove a cost, it removes a multiplier on everything else.

---

### Slide 7 — The Framework

**Track → Trim → Tame**

Track your AI spend, trim the waste, tame the parts — like agents — that can spiral on their own.

---

### Slide 8 — Stage 1: Track (Visibility)

**See where every dollar of AI spend actually goes**

*Find it → Tag it → Show it*

- **Find it** — identify every AI implementation across the org and classify its use case. You can't tag what you haven't inventoried.
- **Tag it** — at the **API-call level**: team / app / cost-center / environment.
- **Show it** — showback dashboards, tailored per audience: exec dashboards for CFO/CIO, engineering dashboards for teams.

Showback drives optimization — you can't cut a cost you can't see.

*(The course's underlying model for this stage is the INFORM framework:*
*Ingestion → Normalization → Allocation → Showback — the same shape as Find/Tag/Show, one layer more granular.)*

---

### Slide 9 — Stage 2: Trim (Levers)

**Cut the bill without cutting capability**

**The big three, in impact order:**

- **Model choice** — right-size the model to the task.
- **Pricing model** — on-demand vs. committed capacity vs. batch. Run the breakeven: `commitment cost ÷ on-demand cost = breakeven utilization %`
- **Caching** — 90% discount on repeated context. Breakeven inside the second request.

**Combined: 80%+ savings.**

Watch for the trap: published price ≠ real cost. Egress, throttling, and regional variance hide another 20–40%.

---

### Slide 10 — Stage 3: Tame (the 21.5x story)

**Build the guardrails that detect and act**

**One support question. Eight API calls.**

A support agent answers one billing question — re-sending full context at every step.

- Single direct call: ~1,000 tokens
- Same question, agentic: **21,500 tokens**

**21.5x the cost.** Before retries push it past 50x — or an unbounded loop makes it a surprise on the monthly bill.

---

### Slide 11 — Detect and Act: Five Guardrails + the KPI Shift

**Detect it** — anomaly detection: usage anomalies, model anomalies, cost anomalies. This is governance's early-warning system, not a dashboard feed.

**Act on it** — five guardrails: **Max depth · Max tokens/task · Retry limit · Timeout · Explicit fallback**

The KPI that matters: **cost per task**, not cost per call — the unit that lets you compare human work, machine work, and hybrid work.

In healthcare and finance: guardrails aren't optional. You need to audit what an agent did and what it spent.

---

### Slide 12 — Try It Yourself

**[QR code]**

A token-cost calculator. Take it with you. Run your own numbers tonight.

---

### Slide 13 — Close

**One question for founders:**
Which stage are you actually in — Track, Trim, or Tame?

**One question for investors:**
Ask a startup that question before you ask for the pitch deck.

*(calculator link / contact — CTA)*
