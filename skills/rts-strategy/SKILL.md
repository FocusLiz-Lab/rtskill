---
name: rts-strategy
description: |
  Extract and structure Rayner Teo style trading strategies with default IMA knowledge-base grounding. Use when the user asks about price action, trend trading, support and resistance, breakout or false breakout, candlestick patterns, moving averages, indicators, entries, exits, stops, targets, invalidation, backtesting assumptions, or trading system design. Default IMA knowledge base: "RaynerTeo交易知识库 | 顺势而为". Triggers include $rts-strategy, 策略研究, 交易策略, 趋势交易, 突破交易, 支撑阻力, K线, 指标, and 交易系统.
---

## 手动更新路由

用户明确要求“更新 skill / 检查更新 / 同步最新原子库”时，先执行此路由。使用当前 SKILL.md 所在目录解析脚本绝对路径：

```text
python "{skillDir}/tools/update_skill.py"
```

只检查时加 `--check`。脚本从 GitHub main 的固定提交同步本仓库整套 skill 和原子资料，覆盖前备份，写入失败回滚；不需要 Git 或 GitHub 登录。根据脚本实际结果报告当前提交、更新状态与失败原因。普通业务问题不自动更新。更新后重新读取相关 SKILL.md。


# rts-strategy

Turn Rayner Teo material into a testable trading strategy structure.

## Default IMA Knowledge Base

Use `RaynerTeo交易知识库 | 顺势而为` unless the user explicitly names another knowledge base.

## Workflow

1. Define the strategy question: market, timeframe, style, and objective.
2. Retrieve relevant IMA materials before making source-specific claims.
3. Extract the method into a rule set:
   - market environment
   - setup conditions
   - entry trigger
   - stop placement
   - target or trailing logic
   - risk and position sizing assumptions
   - invalidation conditions
   - filters and anti-patterns
4. Identify what must be tested instead of assumed.
5. Convert the strategy into a checklist or backtest worksheet.

## Output Format

```markdown
## 策略问题
## 来源依据
## 策略结构
| 模块 | 规则 | 待验证点 |
## 风险边界
## 回测/模拟测试清单
## 下一步
```

## Quality Bar

- Treat all strategy output as education and research, not financial advice.
- Do not invent performance metrics.
- Do not collapse a general concept into a buy/sell signal.
- Explain where rules are inferred from sources versus explicitly retrieved.
