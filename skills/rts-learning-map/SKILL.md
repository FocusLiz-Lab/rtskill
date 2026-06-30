---
name: rts-learning-map
description: |
  Build Rayner Teo trading learning paths with default IMA knowledge-base grounding. Use when the user asks where to start, how to learn price action, trend trading, support/resistance, breakout trading, candlestick patterns, indicators, risk management, trading psychology, or how to turn the Rayner Teo knowledge base into a staged curriculum. Default IMA knowledge base: "Rayner Teo 知识库". Triggers include $rts-learning-map, 学习地图, 学习路径, 系统学习, 先学什么, 入门, 价格行为学习, and 交易学习计划.
---

# rts-learning-map

Create a structured learning path for Rayner Teo trading materials.

## Default IMA Knowledge Base

Use `Rayner Teo 知识库` unless the user explicitly names another knowledge base.

## Workflow

1. Clarify the user's current level, market type, timeframe, and goal if missing.
2. Use IMA retrieval for source-grounded topic lists, lesson names, or quote-level claims.
3. Organize learning into stages:
   - market environment and trend/range recognition
   - price action and support/resistance
   - entries, stops, targets, and trade management
   - risk management and position sizing
   - psychology, journaling, and review
   - strategy testing and iteration
4. For each stage, specify the learning output: notes, checklist, chart examples, backtest sheet, or review log.
5. End with the next 3 actions the user should take.

## Output Format

```markdown
## 学习目标
## 默认知识库
## 阶段路线
| 阶段 | 主题 | 要解决的问题 | 产出 |
## 推荐检索词
## 练习任务
## 下一步
```

## Quality Bar

- Do not promise trading results.
- Do not give live trade recommendations.
- Separate beginner, intermediate, and advanced paths when relevant.
- Prefer practice outputs over passive reading lists.
