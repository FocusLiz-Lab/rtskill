---
name: rts
description: |
  Rayner Teo 交易学习 Skill 工具箱主入口。用于价格行为、趋势交易、支撑阻力、突破交易、假突破、K线形态、均线、交易指标、风险管理、交易心理、交易系统、交易计划、交易复盘、学习路径、内容选题和 IMA 资料检索。默认使用 IMA 知识库「RaynerTeo交易知识库 | 顺势而为」，并可在 IMA 不可用时读取本地原子库。触发词包括 $rts、/rts、Rayner Teo、TradingwithRayner、价格行为、趋势交易、支撑阻力、突破交易、假突破、K线、风控、交易心理、交易计划、复盘和学习地图。
---

# rts Rayner Teo 交易学习工具箱

这是 Rayner Teo 交易学习工具箱的主入口。先判断用户意图，再路由到最相关的 workflow skill；如果上下文足够，直接在同一回答中完成对应工作流。

## 默认 IMA 知识库

所有 workflow skills 默认读取：

```text
RaynerTeo交易知识库 | 顺势而为
```

用户不需要每次输入这个知识库名称。如果用户明确指定其他 IMA 知识库，则优先使用用户指定的知识库。

## 必要依赖

所有需要资料依据的 workflow 都使用 `ima-skill` 做检索：

- `ima-skill/SKILL.md`
- `ima-skill/knowledge-base/SKILL.md`

不要臆造 IMA API。不要向用户暴露 IMA 内部 ID。

如果没有安装 `ima-skill` 或凭证缺失，先提示用户安装并配置 IMA：

```text
请安装 ima 技能
下载地址：https://app-dl.ima.qq.com/skills/ima-skills-1.1.7.zip
API Key 获取：https://ima.qq.com/agent-interface
```

## 路由表

| User intent | Route to | Use when |
|---|---|---|
| Learning path, topic order, where to start | `$rts-learning-map` | User asks how to study Rayner Teo, what to learn first, or how to navigate the knowledge base. |
| Strategy extraction, trading system research | `$rts-strategy` | User wants to organize price action, trend, breakout, indicators, support/resistance, entries, exits, and invalidation rules. |
| Trading plan, checklist, execution process | `$rts-trading-plan` | User wants a pre-trade checklist, risk plan, journaling template, backtest plan, or 7/30/90-day practice plan. |
| Trade/chart/idea review | `$rts-review` | User asks to review a trade journal, trading idea, chart screenshot, entry/stop/target plan, or strategy draft. |
| Psychology and discipline diagnosis | `$rts-psychology` | User mentions overtrading, fear, greed, revenge trading, early exits, moving stops, drawdowns, or execution problems. |
| Content ideas, scripts, notes, course outline | `$rts-content` | User wants to turn the knowledge base into articles, short videos, threads, lesson notes, or a curriculum. |
| Explicit IMA search/read/cite/troubleshooting | `$rts-ima` | User specifically asks to search, read, cite IMA, or debug IMA retrieval. |

## Clarify Once

If the user is vague, ask one question:

```text
你现在最想处理哪一块：学习地图、策略研究、交易计划、复盘评审、交易心理、内容创作，还是从 IMA 资料里找原文？
```

After the answer, route immediately.

## Finance Boundary

- Treat Rayner Teo material as trading education, not investment advice.
- Do not recommend buying, selling, shorting, leverage, position size, or specific instruments as a personalized decision.
- Do not promise profit, win rate, return, drawdown, or risk-free execution.
- For live market questions, provide a decision framework and risk checklist rather than a trade call.
- Do not invent quotes, episode titles, book passages, chart examples, dates, results, backtests, or performance metrics.

## Handoff Format

```text
这个问题交给 $skill-name。
原因：{one sentence}
需要输入：{what the user should provide next, if anything}
```

## Quality Bar

- Default to IMA-grounded workflow skills for substantive source claims.
- Separate "source says", "inference", and "practical next step".
- Prefer rule-based checklists over vague trading advice.
- State assumptions about market, timeframe, instrument, and risk before suggesting a process.
- Do not imitate Rayner Teo's persona.
