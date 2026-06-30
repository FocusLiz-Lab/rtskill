---
name: rts-review
description: |
  Review trading ideas, chart screenshots, trade journals, and strategy drafts using Rayner Teo style price-action and risk-management frameworks with default IMA knowledge-base grounding. Use when the user asks to critique a setup, review an entry/stop/target, diagnose a failed trade, improve a trading plan, or evaluate a chart-based thesis. Default IMA knowledge base: "Rayner Teo 知识库". Triggers include $rts-review, 交易复盘, 图表复盘, 点评交易, 策略评审, 入场, 止损, 目标, and 交易日志.
---

# rts-review

Review user-provided trading material using a structured, education-only process.

## Default IMA Knowledge Base

Use `Rayner Teo 知识库` unless the user explicitly names another knowledge base.

## Required Inputs

Ask for missing details only when they materially affect the review:

- instrument and timeframe
- entry, stop, target, and reason for trade
- market condition at entry
- risk amount and trade management rules
- chart screenshot or journal text if available

## Workflow

1. Restate the user's setup without adding assumptions.
2. Check market environment, level quality, trigger, stop, target, and risk.
3. Separate strategy design issues from execution discipline issues.
4. Use IMA for Rayner Teo-specific source references if the user asks for source grounding.
5. Return a repair checklist.

## Output Format

```markdown
## 复盘结论
## 结构检查
| 项目 | 观察 | 风险 | 修改建议 |
## 策略问题 vs 执行问题
## 下次交易前检查
## 需要补充的信息
```

## Quality Bar

- Do not say the user should have bought or sold.
- Do not judge outcome quality only by profit/loss.
- Highlight missing risk rules before discussing entries.
