# Serenity Research Kit

Personal stock-research skill kit built from:

- `muxuuu/serenity-skill`
- `haskaomni/serenity-skill`

This kit keeps the original strengths separate instead of merging all logic into one large skill.

## Scope

The bottleneck framework is strongest for small and mid-cap companies in physical supply chains where scarcity, qualification cycles, customer urgency, and market neglect can create asymmetric upside. It is less decisive for mega-cap compounders, broad software platforms, banks, consumer brands, or companies whose value is driven mainly by macro, regulation, network effects, or capital allocation.

The valuation modules are broader. `serenity-equity-memo`, `serenity-growth-valuation`, `serenity-tam-peg`, and `serenity-dma-health` can still be used on large caps, software, platforms, cyclicals, and non-bottleneck companies. In those cases, use the kit as a general valuation and thesis-testing workflow, not as proof that the company is a Serenity-style bottleneck.

## Skills

| Skill | Role |
| --- | --- |
| `serenity-stock-research` | Router for full single-stock research. Use this as the default entry point. |
| `serenity-bottleneck-research` | Supply-chain bottleneck analysis, value-chain mapping, evidence grading, red flags. Based on `muxuuu/serenity-skill`. |
| `serenity-equity-memo` | Buy-side stock memo with financials, valuation scenarios, catalysts, risks, and monitoring dashboard. |
| `serenity-growth-valuation` | Bayesian intrinsic-growth valuation: intrinsic 3-5Y growth vs market-implied growth. |
| `serenity-tam-peg` | Growth-stock valuation using TAM runway and business quality adjustments. |
| `serenity-dma-health` | Valuation/trend health using fundamentals, moving averages, divergence, and revisions. |
| `serenity-alpha` | Translate news or supply-chain clues into testable alpha hypotheses. |

## Recommended Use

For a normal ticker request:

```text
Use $serenity-stock-research to analyze [ticker].
Start with the supply-chain bottleneck thesis, then run valuation and bull/base/bear checks.
Focus on evidence strength, current valuation, catalysts, risks, and falsification conditions.
```

For a pure supply-chain question:

```text
Use $serenity-bottleneck-research to judge whether [company] is a real bottleneck.
```

For valuation only:

```text
Use $serenity-equity-memo and $serenity-growth-valuation to value [ticker].
```

## Install

Copy the skill folders into your Codex skills directory:

```text
skills/* -> ~/.codex/skills/
```

Restart Codex if newly copied skills do not appear immediately.
