# Topic 1 — Title & Abstract

## Title

**Tokenomics: The New Unit Economics Every AI Founder and Investor Needs to Understand**

## Abstract

Every AI feature now carries a real, variable cost behind every single user interaction — and the math behind that cost is stranger than most people building AI products realize. AI spend is linear in tokens, never exponential, yet bills routinely blow up 30x when usage only grows 10x — because what actually drifts is tokens-per-user, not the pricing curve itself. That gap is also a margin problem: Bessemer's research shows AI-native companies running 50-60% gross margins versus 80-90% for classic SaaS, on the same measure.

This talk introduces Tokenomics — the discipline of knowing what a query, a task, or a tenant actually costs before you ever set a customer price — through a practical three-stage framework: Inform (see the spend), Optimize (cut it — caching, batching, and the commitment math that actually pays off), and Operate (govern it, through a real story of an AI agent that cost 21x more than it should have, and the five guardrails that prevent it). Along the way: why Salesforce launched Agentforce on flat $2-per-conversation pricing and had to add two more ways to pay within months, after customers couldn't predict their bills — and how Workday and ServiceNow landed on the same hybrid shape independently.

Attendees leave with a live, interactive token-cost calculator to try themselves, a pricing checklist for founders, and — for investors — a new diligence question: ask what a startup's tokenomics and guardrails look like before you ask what they charge.

## Sourcing note

- SaaS gross margin (80-90%) vs. AI-native gross margin (50-60%): Bessemer Venture Partners, "The AI Pricing and Monetization Playbook" — same metric (gross margin) on both sides.
- Median SaaS gross margin cross-check: Benchmarkit 2025 data, 342 companies, median 80% software gross margin, top quartile 86%+.
- Salesforce pricing evolution: publicly documented — $2/conversation (Fall 2024) → Flex Credits added (May 2025) → still offers all three pricing models today (per-conversation, Flex Credits, per-seat). Driven by customer confusion over the definition of "conversation" and bill unpredictability, not a disclosed internal cost/margin problem at Salesforce.
- Microsoft GitHub Copilot early losses (~$20/user/month): cited in Bessemer's playbook as the canonical example of inference cost exceeding subscription price.
