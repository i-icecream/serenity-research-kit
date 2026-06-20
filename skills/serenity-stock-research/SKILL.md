---
name: serenity-stock-research
description: Personal Serenity stock research router. Use when the user asks to analyze a single ticker/company, compare listed companies, build a buy-side stock memo, judge whether a company is a supply-chain bottleneck, estimate valuation upside/downside, run bull/base/bear scenarios, translate news into alpha, or combine muxuuu-style bottleneck research with haskaomni-style valuation checks. Routes work across serenity-bottleneck-research, serenity-equity-memo, serenity-growth-valuation, serenity-tam-peg, serenity-dma-health, and serenity-alpha.
---

# Serenity Stock Research

This is the personal entry point for stock research built from two source families:

- `serenity-bottleneck-research`: muxuuu-style supply-chain bottleneck research.
- `serenity-equity-memo`, `serenity-growth-valuation`, `serenity-tam-peg`, `serenity-dma-health`, and `serenity-alpha`: haskaomni-style memo, valuation, trend-health, and news-to-alpha checks.

Keep the responsibilities separate. Do not blend every module into every answer.

## Default Flow

For a single ticker or listed company, run the work in this order:

1. Use `serenity-bottleneck-research` first when the thesis involves AI infrastructure, semiconductors, photonics, memory, power, robotics, hardware, materials, manufacturing, supply chains, or any claim that the company is a bottleneck.
2. Use `serenity-equity-memo` when the user wants a complete stock analysis, buy-side memo, investment committee note, bull/base/bear scenarios, catalysts, risks, or source-backed financial analysis.
3. Use `serenity-growth-valuation` when the key question is whether intrinsic 3-5 year growth is above or below market-implied growth.
4. Use `serenity-tam-peg` when the company is a growth stock and valuation depends on TAM runway, quality, earnings growth, or whether the multiple is justified.
5. Use `serenity-dma-health` only when current price trend, entry health, moving averages, revision confirmation, or overheated/undervalued technical setup matters.
6. Use `serenity-alpha` when the starting input is news, a product launch, procurement signal, customer clue, supply-chain change, or earnings-call clue.

## Output Contract

Start with the judgment, then show the path:

```text
结论 -> 卡点判断 -> 证据强度 -> 估值判断 -> 催化剂 -> 证伪条件 -> 下一步核验
```

When data is current or time-sensitive, verify live filings, prices, market cap, earnings releases, guidance, and news before making claims. If current data cannot be verified, label the answer as an initial framework pass and list the exact facts that need checking.

## Module Boundaries

- Bottleneck analysis answers: what layer, why scarce, who depends on it, evidence quality, red flags, and what would prove the thesis wrong.
- Equity memo answers: business quality, financial statements, value drivers, valuation scenarios, catalysts, risks, and monitoring dashboard.
- Growth valuation answers: intrinsic growth probability, market-implied growth, FOMO/multiple expansion, and price-growth divergence.
- TAM-PEG answers: whether growth duration, TAM, and quality justify the current forward multiple.
- DMA health answers: whether the current price trend is supported or stretched relative to fundamentals and revisions.
- Alpha answers: whether news has already translated into observable demand and which small/pure company could show financial-statement elasticity.

## Preferred Final Shape

For normal stock requests, keep the final answer concise and decision-useful:

1. One-line conclusion.
2. `卡点/产业链位置`.
3. `估值与市场隐含预期`.
4. `未来 3-6 个月催化剂`.
5. `最大风险与证伪条件`.
6. `下一步需要核验的数据`.

Avoid direct buy/sell commands. Use research-priority and condition-based language.
