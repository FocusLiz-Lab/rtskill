---
name: rts-trading-plan
description: |
  Convert Rayner Teo style trading concepts into executable trading plans, checklists, journaling templates, and practice roadmaps with default IMA knowledge-base grounding. Use when the user asks for pre-trade plans, risk management, position sizing process, stop-loss rules, trade journal fields, backtest plans, 7/30/90-day practice plans, or workflow implementation. Default IMA knowledge base: "Rayner Teo 知识库". Triggers include $rts-trading-plan, 交易计划, 检查清单, 风控计划, 复盘表, 日志, 回测, 模拟盘, and 执行流程.
---

# rts-trading-plan

Convert trading education into a practical execution and review plan.

## Default IMA Knowledge Base

Use `Rayner Teo 知识库` unless the user explicitly names another knowledge base.

## Workflow

1. Determine the user's goal: learning, paper trading, backtesting, journaling, or live-process design.
2. Ground source-specific rules through IMA when needed.
3. Build a plan with:
   - market and timeframe scope
   - setup checklist
   - entry/stop/target rules
   - risk cap and loss limits
   - trade management rules
   - no-trade conditions
   - journal fields
   - review cadence and metrics
4. Include a "stop doing" list for common execution errors.
5. Provide a short implementation schedule.

## Output Format

```markdown
## 目标
## 交易前检查
## 执行规则
## 风险规则
## 复盘字段
## 7/30/90 天练习安排
## 禁止事项
```

## Quality Bar

- Do not choose live trades for the user.
- Use percentages, R-multiples, or placeholders only as templates unless the user provides their own rules.
- Make the checklist short enough to use before a trade.
