# Topic 1 — 30-Minute Run of Show

Framework the audience takes home: **Inform → Optimize → Operate**, one concrete story anchoring each stage.

| Time | Headline | Content |
|---|---|---|
| 0:00–2:00 | *"You're Paying for Something You Can't See"* | Cold open — the token as an invisible billing unit. |
| 2:00–5:00 | *"Microsoft Lost $20 Per User Per Month — And That's Normal Now"* | The margin problem: 80-90% gross margin for classic SaaS vs. 50-60% for AI-native, same measure — the gap is compute, not overhead. |
| 5:00–7:00 | *"Claude's Answer Costs More Than Your Question"* | One line on what a token is, straight into the input/output cost asymmetry (parallel reading vs. sequential generation) — 3-5x cost gap. |
| 7:00–11:00 | *"The Math That Lied to Everyone: Why 10x Users Became 30x Cost"* | The core insight — AI cost is linear in tokens (never exponential), but tokens-per-user drifts for reasons nobody forecasts (longer context, wider retrieval, agent loops). Strongest "lean in" moment of the talk. |
| 11:00–13:00 | *"The Framework You're Taking Home: Inform, Optimize, Operate"* | Names the three-stage arc explicitly — this is the takeaway, not just a story. |
| 13:00–16:00 | *"Stage 1 — Inform: You Can't Manage What You Can't See"* | Allocation/tagging coverage, cost-per-task/tenant, anomaly detection + time-to-detect. Crawl (<10% attributable) → Walk (60-80%) → Run (>95%) as a self-diagnostic. |
| 16:00–20:00 | *"Stage 2 — Optimize: Where the Real Money Is"* | Cache hit rate (90% off hits), batch-eligible workload % (30-40% typically qualifies, 50% off), the commitment breakeven formula (`commitment cost ÷ on-demand cost = breakeven utilization %`). |
| 20:00–25:00 | *"Stage 3 — Operate: The Agent That Cost 21x More Than It Should Have"* | Single-focus Operate story: an 8-step agent loop that re-sends context at every step can cost 21.5x a single call; unguardrailed retries push further. Five real controls: max depth, max tokens/task, retry limits, timeouts, explicit fallback. Personal proof: real itemized per-reel cost breakdown from a shipped multi-agent video pipeline, and a $10M/year client engagement where loop caps + a kill-switch made 20-25% savings stick instead of drifting back. |
| 25:00–27:00 | *"Try It Yourself"* | Live QR-code demo — audience plays with a token-cost calculator on their phones. |
| 27:00–30:00 | *"One Question for Founders, One Question for Investors"* | Close: founders — "which stage are you actually in?"; investors — "ask a startup that question before you ask for the pitch deck." CTA. |

## Notes

- Deliberately drops a full "what is a token" 101 explanation (barcode/definitional metaphors) — audience is founders/investors/some learners, not first-time AI users. One line of grounding, then straight to the insight.
- Operate stage is guardrails-only, single focus. Forecast-variance content and a Salesforce-pricing-predictability aside were both considered and cut from this segment to keep one clean story per stage — Salesforce's pricing story instead lives in the title/abstract's sourcing note and segment 2 if a passing mention is wanted live.
